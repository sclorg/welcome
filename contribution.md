# Contributing to Container Images

This document outlines the guidelines and best practices for contributing to the container images within the [SCLOrg](http://github.com/sclorg/) on GitHub.

## Pull Requests

All modifications to the repositories and images must be submitted via a Pull Request (PR) and undergo review by another maintainer before merging. Exceptionally, small and obvious changes that pose no risk (such as fixing typos in documentation) may be merged or committed without review.

## Dockerfile Guidelines

The images under SCLOrg generally follow [Container Best Practices](http://docs.projectatomic.io/container-best-practices/). Please read through them before submitting a PR.

As for names and labels, [guidelines available here](https://github.com/projectatomic/ContainerApplicationGenericLabels/) are followed.

### OpenShift

Ideally, all the images available under sclorg should work fine in the OpenShift environment. For more about what is required from developers, read the [Guidelines for writing Dockerfiles for OpenShift](https://docs.openshift.com/enterprise/3.0/creating_images/guidelines.html).

## Repositories

### Submodule

All our repositories are using [Common Build Helpers](https://github.com/sclorg/container-common-scripts). All standard test files and other shared scripts are stored in this repository. To test your changes or generate documentation from shared files, please use the scripts found here.
It is recommended to download this repository via `git submodule update --init`. This command will include the `common/common.mk` makefile where all commands are available.

### Naming

Git repositories follow the pattern `<name>-container` where the `<name>` is the name of the main component available in the container, lowercase, one word. Some packages also include the `s2i-` prefix, but since it does not mean other containers are not s2i enabled, this is not required.

### Directory structure

Every repository contains directories with particular major versions. For example, MySQL repository includes directories 5.5, 5.6, and 5.7.


### Labels

Every repository has its own labels which help categorize and prioritize issues and pull requests, making it easier for contributors to understand the status and purpose of each item. However, we also have a few global labels used across all repositories.

Here's a brief explanation of the common labels:

1. **bug**: Indicates an issue that describes a defect or problem in the software.
2. **duplicate**: Marks an issue or pull request that has already been reported or submitted and is identical or very similar to an existing one.
3. **enhancement**: Signifies a request for a new feature or improvement to an existing feature.
4. **help wanted**: Suggests that the issue or pull request needs assistance from other contributors or maintainers.
5. **invalid**: Highlights an issue or pull request that is deemed inappropriate, incorrect, or not relevant to the project.
6. **question**: Denotes an item that is primarily seeking clarification or further information.
7. **ready for review**: Indication that an issue or pull request has been completed and is now awaiting review from team members or maintainers. You can find all items with this label using this [query](https://github.com/search?q=org%3Asclorg+label%3A%22ready+for+review%22+state%3Aopen&type=Issues).
8. **wontfix**: Implies that the maintainers or contributors have decided not to address the issue or implement the requested change.

### Active versions

Actively maintained versions should be kept as close to each other as possible -- both source-code-wise and feature-wise. It means maintainers should try to keep the list of use cases supported in the different versions the same, if possible.

Also, the source code changes between particular versions should be kept as small as possible. Ideally, the source code should be the same across the versions, except for slight differences in Dockerfiles (version specification).

### EOL versions

When a specific version or an entire package reaches its end-of-life (EOL), the source files will be retained in the repository, but no further updates should be expected. It is up to the maintainer's discretion whether a PR will cover older versions; however, no review should be anticipated for such cases.

### Adding a New Version of an Image

Adding a new version of an image to an existing repository involves three main steps. First, update the testing configuration files to include the new `$VERSION` and `$OS` combination. Next, make necessary changes to the new version directory while retaining the git history for the latest version. Lastly, modify the build configuration file and create a repository to make the new images available on [quay.io](quay.io). Detailed instructions for each step can be found below.

#### 1) Enable Testing

Initially, the corresponding `$VERSION` and `$OS` combination must be added to the testing configuration files. The `.github/workflows/container-tests.yml` file contains the configuration for container testing, while the `.github/workflows/openshift-tests.yml` file includes the configuration for testing containers in OpenShift 4.

Testing must be enabled in a separate Pull Request, which should be merged before the Pull Request containing the actual version addition is tested.

#### 2) Add Sources

When adding a new version to an existing repository, it is preferable to maintain the git history for the latest version. The recommended approach to add a new version directory is as follows (assuming we are adding version 2.0 and the previous latest version is 1.9):

```
$> git mv 1.9 2.0
$> git commit
$> cp -r 2.0 1.9
$> git add 1.9
$> git commit
```

This method will result in the loss of git history for 1.9 but will retain it for 2.0. At this stage, the contents of 2.0 are identical to 1.9, so the next step is to apply all necessary changes to the 2.0 directory.

When introducing changes for a new version, ensure that all Dockerfiles are modified, even if the image cannot be built yet. For images that cannot be built using the build scripts, add `.exclude-$OS` files.

For example, if building fails for CentOS, Fedora, and RHEL-7, add these files to the relevant version like `2.0/.exclude-centos7`, `2.0/.exclude-fedora`, and `2.0/.exclude-rhel7`. These files ensure that the new version will not be built accidentally.

Once the image can be built using testing or production RPMs, delete the corresponding `.exclude-$OS` files.

#### 3) Enable Publishing

To make the images available on [quay.io](quay.io), update the `.github/workflows/build-and-push.yml` configuration file with the appropriate `$OS` and `$VERSION`.

Published images can be found at the following locations:

- Fedora images: https://quay.io/organization/fedora
- CentOS7 images: https://quay.io/organization/centos7
- CentOS Stream 8 and CentOS Stream 9 images: https://quay.io/organization/sclorg

To create a repository for the relevant organizations, contact phracek@redhat.com, pkubat@redhat.com, hhorak@redhat.com, or zmiklank@redhat.com. In the created repositories, add a robot account, which is necessary for publishing images.

In the case of Fedora, request the addition of a robot account by contacting cverna@redhat.com, but consult the SCLORG team first.

## Typical Contribution Session

You should be informed about each repository package's requirements, as they can slightly differ. Usually, these packages are needed:

- [distgen](https://github.com/devexp-db/distgen/) - is used for generating image source files,
- [go-md2ma](https://github.com/cpuguy83/go-md2man) - is used for generating documentation from README.md

1. Fork the repository
2. Run `git submodule update --init` to download the `common` submodule with `common/common.mk` makefile. We use this submodule for common tests and functions across all our repositories.
3. Implement a new feature or bug fix\*
4. Consider running CI tests, as described in the Testing section (and in each repository)
5. Commit the files and generated files in two separated commits with a conventional commit message for each.
6. Open a Pull Request for review!

\*Look at specific repository contribution rules. A small amount of repositories have a distgen-enabled `/src` folder, and you will need to regenerate files with the `common.mk` makefile.

## Distributions

Currently, there are Dockerfiles available for RHEL 7, RHEL 8, RHEL 9, CentOS 7, CentOS Stream 8, CentOS Stream 9, and Fedora distributions. However, not every image version is available for each distribution.

## Packages installing in Dockerfile

When installing packages in the Dockerfile, it is important to ensure that all packages come from official repositories and are installed using conventional methods such as YUM or DNF. Only scripts that are available in these repositories should be added to the images on top of the RPM data.

For Fedora images, we aim to use the modules from [Modularity effort](https://docs.pagure.org/modularity/).

For CentOS, we take packages from [SCLo SIG](http://wiki.centos.org/SpecialInterestGroup/SCLo). As a result, the images use RPM packages from the [Software Collections](http://softwarecollections.org).

For RHEL, we install packages from RHEL 7 base or Red Hat [Software Collections](https://access.redhat.com/documentation/en/red-hat-software-collections/).

## Testing

This organization's images include test suites, which test the images in basic use cases.
The tests are being run on [Testing Farm](https://docs.testing-farm.io/general/0.1/index.html). Testing is done before the change is merged into the master branch (main branch). Therefore the place for triggering tests on demand is in a Pull Request.

### Triggering tests

Tests can be triggered by writing a comment containing a specific string into the Pull Request:

- `[test-all]` - triggers container and OpenShift tests
- `[test]` - triggers container tests
- `[test-openshift]` - triggers OpenShift tests

**_Only maintainers and owners of the SCLOrg can trigger the tests._**

**_The person triggering the tests has to check that no malicious code is in the Pull Request._**

Every PR that delivers a new feature or fixes a severe bug should include a particular test case.
