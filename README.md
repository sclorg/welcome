Welcome to the SCL.org Space
============================
This is basically an overview around the sclorg organization, aka what all one can find here.

Why SCL.org? Since all the repositories, under this organization are somehow connected to the Software Collections concept. Software Collections give you the power to build, install, and use multiple versions of software on the same system, without affecting system-wide installed packages.

And since we have had set of new web development tools available as RPMs, tested and available in the directory on [softwarecollections.org](https://www.softwarecollections.org/en/), it is a good idea to re-use those tested packages and make container images from them, that are working fine in OpenShift.

Repositories Overview
---------------------

* [Container contribution guidelines](contribution.md): Learn about what principles to follow when contributing to the sclorg organization, especially containers repositories
* [Container images overview based on the Software Collections](images.md): Dockerfiles, other relevant sources and tests for the images
* [scl-utils](https://github.com/sclorg/scl-utils): Upstream project for the scl-utils package that is available in RHEL, CentOS and Fedora and that allows to build the RPM packages into alternative directory.
* [spec2scl](https://github.com/sclorg/spec2scl): Tool written in Python that helps migrating RPM spec files into SCL-enabled variant, which means adding some macros, scriptlets, etc.
* [softwarecollections.org](https://github.com/sclorg/softwarecollections): Sources for [softwarecollections.org](http://softwarecollections.org/) website, a django application that serves as a directory of available Software Collections.
* [centpkg for SCLo](https://github.com/sclorg/centpkg-sclo): Small wrapper that helps [SCLo SIG](http://wiki.centos.org/SpecialInterestGroup/SCLo) maintainers build SCL packages in [CBS](http://cbs.centos.org/).
* [centos-release package](https://github.com/sclorg/centos-release-scl): Small RPM package with YUM repository that provides upstream Software Collections built in [CBS](http://cbs.centos.org/) by community (not those that are part of RHSCL).
* [SCLo CI Tests](https://github.com/sclorg/sclo-ci-tests): Tests that are run in [CentOS CI](http://ci.centos.org) to verify the RPM packages were (re)build fine in [CBS](http://cbs.centos.org/).
* [RPM List Builder](https://github.com/sclorg/rpm-list-builder): Tool that should help rebuilding SRPMs in [CBS](http://cbs.centos.org/), that were previously made available in different repository (for example RHSCL, but not only this one).
* [RHSCL Container CI](https://github.com/sclorg/rhscl-container-ci): Scripts that help testing containers on RHEL platform.


Where to Learn More About Containers
====================================
There is a lot of articles around Docker and containers generally, these are just few that seemed to provide basic introduction:

 * https://developer.fedoraproject.org/tools/docker/about.html
 * https://fedoramagazine.org/quick-containers-with-fedora-dockerfiles/
 * https://www.liquidweb.com/kb/how-to-list-and-attach-to-docker-containers/
 * https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux_atomic_host/7/html/overview_of_containers_in_red_hat_systems/introduction_to_linux_containers


How to write a Dockerfile
-------------------------
Reproducible builds are created via Dockerfiles, learn more about Dockerfile basics in the following articles:

 * https://docs.docker.com/engine/reference/builder/
 * https://developers.redhat.com/blog/2016/02/24/10-things-to-avoid-in-docker-containers/
 * http://docs.projectatomic.io/container-best-practices/


Orchestrating Containers and PaaS
---------------------------------
Kubernetes (aka k8s) has become de-facto standard in the orchestrating containers (which means running them in scale, configuring as cattle, not pets). OpenShift is then PaaS built on top of Kubernetes, that offers whole application lifecycle management, i.e. rapidly build and deploy Docker-formatted containers and manage them on a robust, scalable platform. Learn more about those two technologies at:

 * https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/#kubernetes-is
 * https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux_atomic_host/7/html-single/getting_started_with_kubernetes/
 * https://www.openshift.com/index.html
 * https://access.redhat.com/documentation/en/openshift-container-platform/

Source-to-image
---------------
Many packages under this organization uses the source-to-image (s2i) concept, a toolkit and workflow for building reproducible Docker images from source code. Learn more about this at:

 * https://github.com/openshift/source-to-image


