# Welcome to the Software Collections Organization

This document offers a comprehensive introduction to the Software Collections Organization (SCLOrg), highlighting the repositories under our umbrella and providing examples of their practical applications, along with links to relevant external resources.

The primary focus of SCLOrg revolves around the Software Collections concept. Software Collections offer a streamlined approach to building, installing, and utilizing multiple software versions on a single system, without disrupting pre-existing system-wide package installation.

In light of recent developments, we have introduced a series of RPMs web development tools. To maximize the utility of these verified packages, we encourage the creation of container images compatible with OpenShift.

## Repository Overview

- [Container Contribution Guidelines](contribution.md): Learn about what principles to follow when contributing to the SCLOrg, particularly in relation to container repositories.
- [Container Images Overview Based on Software Collections](images.md): Access Dockerfiles, relevant sources, and tests for container images.

- [scl-utils](https://github.com/sclorg/scl-utils): The upstream project for the scl-utils package available in RHEL, CentOS, and Fedora, enabling the building of RPM packages in an alternative directory.
- [spec2scl](https://github.com/sclorg/spec2scl): A Python-based tool that facilitates the migration of RPM spec files into SCL-enabled variants by adding macros, scriptlets, and more.
- [SCLOrg](https://github.com/sclorg/softwarecollections): Source code for the [SCLOrg](http://softwarecollections.org/) website, a Django application that serves as a directory for available Software Collections Organization.
- [centpkg for SCLo](https://github.com/sclorg/centpkg-sclo): A compact wrapper that assists [SCLo SIG](http://wiki.centos.org/SpecialInterestGroup/SCLo) maintainers in building SCL packages in [CBS](http://cbs.centos.org/).
- [centos-release package](https://github.com/sclorg/centos-release-scl): A minimal RPM package with a YUM repository, offering upstream Software Collections built in [CBS](http://cbs.centos.org/) by the community (excluding those in RHSCL).
- [SCLo CI Tests](https://github.com/sclorg/sclo-ci-tests): Tests executed in [CentOS CI](http://ci.centos.org) to verify the successful (re)building of RPM packages in [CBS](http://cbs.centos.org/).
- [RPM List Builder](https://github.com/sclorg/rpm-list-builder): A tool designed to facilitate the rebuilding of SRPMs in [CBS](http://cbs.centos.org/) that were previously available in different repositories (e.g., RHSCL and others).
- [RHSCL Container CI](https://github.com/sclorg/rhscl-container-ci): Scripts for testing containers on the RHEL platform.

## Orchestrating Containers and PaaS

Kubernetes (commonly referred to as k8s) has emerged as the de-facto standard for orchestrating containers, enabling the large-scale management and configuration of containers as cattle rather than pets. OpenShift is a Platform-as-a-Service (PaaS) built on top of Kubernetes, providing comprehensive application lifecycle management. This includes the ability to quickly build and deploy Docker-formatted containers while managing them on a robust, scalable platform. To learn more about these two technologies, explore the following resources:

- https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/#kubernetes-is
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux_atomic_host/7/html-single/getting_started_with_kubernetes/
- https://www.openshift.com/index.html
- https://access.redhat.com/documentation/en/openshift-container-platform/

## Source-to-image

Numerous packages within this organization utilize the source-to-image (s2i) concept, a toolkit and workflow designed for building reproducible Docker images directly from source code. To learn more about source-to-image, you can visit:

- https://github.com/openshift/source-to-image
