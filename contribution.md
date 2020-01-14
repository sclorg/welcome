# Contribution to Container Images

This document describes rules and best practices for contributing to http://github.com/sclorg/.


## Pull Requests

All changes done in the images go through pull request (PR) and require review from another maintainer before merging. A reasonably small change that is extra-obvious and cannot cause any issue can be merged/committed without a review (typically typos in documentation).


## Dockerfile Guidelines

The images under sclorg organization generally follow [Container Best Practices](http://docs.projectatomic.io/container-best-practices/). Read through them before submitting a PR.

As for names and labels, [guidelines available here](https://github.com/projectatomic/ContainerApplicationGenericLabels/) are followed.

### OpenShift

Ideally all the images available under sclorg should be working fine in OpenShift environment. For more about what is required from developer, read the [Guidelines for writing Dockerfiles for OpenShift](https://docs.openshift.com/enterprise/3.0/creating_images/guidelines.html).



## Repositories 

### Naming

Git repositories follow the pattern `<name>-container` where the `<name>` is the name of the main component available in the container, lowercase, one word. Some packages include also `s2i-` prefix, but since it does not mean other container are not s2i enabled, this is not required.

### Directory structure

Every repository contains directories with particular major versions. For example MySQL repository includes directories 5.5, 5.6, and 5.7.

### Active versions

Actively maintained versions should be kept as close to each other as possible -- both, source-code wise and feature-wise. It means maintainers should try to keep the list of use cases supported in the different versions same, if possible.

Also the source code changes between particular versions should be kept as small as possible, ideally the source-code should be the same across the versions, except small differences in Dockerfiles (version specification).

### EOL versions

When some version or even whole package retires (gets EOL), the sources are kept in the repository, but one cannot expect any changes. It is always on decision of the maintainer, whether the PR will cover the older versions, but no review should be expected.

### Adding a new version

When we add a new version to the existing repository, we want to ideally keep the git history in the newest version, so the recommended way of adding a new version directory is this (suppose we add version 2.0 and the previous latest one is 1.9):

    $> git mv 1.9 2.0
    $> git commit
    $> cp -r 2.0 1.9
    $> git add 1.9
    $> git commit
    
This way the git history will be lost in 1.9, but will be kept in 2.0. At this point the content of 2.0 is the same as 1.9, so the next step is to do all necessary changes in 2.0 directory.

When adding the changes for a new version please modify each of the Dockerfiles even if the image cannot be built yet.  You can add `.exclude-$OS` files for images that should not be built via the build scripts.

E.g. If the building failed for CentOS, Fedora, and RHEL-7 then add these files into the relevant version like `2.0/.exclude-centos7`, `2.0/.exclude-fedora`, `2.0/.exclude-rhel7`.
These files mean that the new version will not be built accidentally.

As soon as the packages are available for given distribution, then delete corresponding `.exclude` file.

## Distributions

There are currently Dockerfiles for RHEL 7, CentOS 7 and Fedora. Not every image


## Packages installing in Dockerfile

All packages installed in the Dockerfile must come from the official repositories and are installed using conventional ways -- YUM or DNF. Only scripts that live in this repositories can be added into the images on top of the RPM data.

For Fedora images, we aim to use the modules from [Modularity effort](https://docs.pagure.org/modularity/).

For CentOS, we take packages from [SCLo SIG](http://wiki.centos.org/SpecialInterestGroup/SCLo), so the images use actually RPM packaged as [Software Collections](http://softwarecollections.org).

For RHEL, we install packages either from RHEL 7 base or from Red Hat [Software Collections](https://access.redhat.com/documentation/en/red-hat-software-collections/).


## Testing

The images in this organization include test-suites, that test the images in basic use cases. Every pull-request is then tested by running this test-suite. The tests run in ci.centos.org:

 * https://ci.centos.org/view/SCLo-images/

Every PR that deliver new feature or fixes a severe bug should include particular test-case.
