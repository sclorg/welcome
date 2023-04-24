# Container Images Overview

The following is a list of container images maintained in this organization. Most of the Dockerfiles are based on the [Software Collection](https://www.softwarecollections.org/en/docs/) packages from [Red Hat Software Collections](https://access.redhat.com/documentation/en/red-hat-software-collections/) or from packages delivered on CentOS by [SCLo SIG](http://wiki.centos.org/SpecialInterestGroup/SCLo).

## PHP
| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| 5.6 – deprecated † | [rhscl/php-56-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/php-56-rhel7) | [centos/php-56-centos7](https://hub.docker.com/r/centos/php-56-centos7/) |
| 7.0 – deprecated † | [rhscl/php-70-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/php-70-rhel7) | [centos/php-70-centos7](https://hub.docker.com/r/centos/php-70-centos7/) |
| 7.1 – deprecated † | [centos/php-71-centos7](https://hub.docker.com/r/centos/php-71-centos7/) |
| 7.2 – deprecated † | [rhscl/php-72-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/php-72-rhel7) | [centos/php-72-centos7](https://hub.docker.com/r/centos/php-72-centos7/) |
| [7.3](https://github.com/sclorg/s2i-php-container/tree/master/7.3) | [rhscl/php-73-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/php-73-rhel7) | [centos/php-73-centos7](https://hub.docker.com/r/centos/php-73-centos7/) |
| [7.4](https://github.com/sclorg/s2i-php-container/tree/master/7.4) | [rhscl/php-74-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/php-74-rhel7) | [centos/php-74-centos7](https://hub.docker.com/r/centos/php-74-centos7/) |
| [8.0](https://github.com/sclorg/s2i-php-container/tree/master/8.0) | [rhscl/php-80-rhel9](https://access.redhat.com/containers/#/registry.redhat.io/rhel9/php-80) |
| [8.1](https://github.com/sclorg/s2i-php-container/tree/master/8.1) | [rhscl/php-81-rhel9](https://access.redhat.com/containers/#/registry.redhat.io/rhel9/php-81)|


## Python

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| [2.7](https://github.com/sclorg/s2i-python-container/tree/master/2.7) | [rhscl/python-27-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/python-27-rhel7) | [centos/python-27-centos7](https://hub.docker.com/r/centos/python-27-centos7/) |
| 3.4 – deprecated † | [rhscl/python-34-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/python-34-rhel7) | [centos/python-34-centos7](https://hub.docker.com/r/centos/python-34-centos7/) |
| 3.5 – deprecated † | [rhscl/python-35-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/python-35-rhel7) | [centos/python-35-centos7](https://hub.docker.com/r/centos/python-35-centos7/) |
| [3.6](https://github.com/sclorg/s2i-python-container/tree/master/3.6) | [rhscl/python-36-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/python-36-rhel7) | [centos/python-36-centos7](https://hub.docker.com/r/centos/python-36-centos7/) |
| [3.8](https://github.com/sclorg/s2i-python-container/tree/master/3.8) | [rhscl/python-38-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/python-38-rhel7) | [centos/python-38-centos7](https://hub.docker.com/r/centos/python-38-centos7/) |
| [3.9](https://github.com/sclorg/s2i-python-container/tree/master/3.9) | [rhel9/python-39](https://access.redhat.com/containers/#/registry.redhat.io/rhel9/python-39) | |
| [3.9-minimal](https://github.com/sclorg/s2i-python-container/tree/master/3.9-minimal) | | |
| [3.10](https://github.com/sclorg/s2i-python-container/tree/master/3.10) | | |
| [3.11](https://github.com/sclorg/s2i-python-container/tree/master/3.11) | | |

## Perl

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| [5.16](https://github.com/sclorg/s2i-perl-container/tree/master/5.16) | | |
| [5.20](https://github.com/sclorg/s2i-perl-container/tree/master/5.20) | [rhscl/perl-520-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/perl-520-rhel7) | [centos/perl-520-centos7](https://hub.docker.com/r/centos/perl-520-centos7/) |
| [5.24](https://github.com/sclorg/s2i-perl-container/tree/master/5.24) | [rhscl/perl-524-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/perl-524-rhel7) | [centos/perl-524-centos7](https://hub.docker.com/r/centos/perl-524-centos7/) |
| [5.26-mod_fcgid](https://github.com/sclorg/s2i-perl-container/tree/master/5.26-mod_fcgid) | | |
| [5.26](https://github.com/sclorg/s2i-perl-container/tree/master/5.26) | [rhscl/perl-526-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/perl-526-rhel7) | [centos/perl-526-centos7](https://hub.docker.com/r/centos/perl-526-centos7/) |
| [5.30-mod_fcgid](https://github.com/sclorg/s2i-perl-container/tree/master/5.26) | | |
| [5.30](https://github.com/sclorg/s2i-perl-container/tree/master/5.30) | [rhscl/perl-530-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/perl-524-rhel7) | |
| [5.32](https://github.com/sclorg/s2i-perl-container/tree/master/5.32) | | |
| [5.34](https://github.com/sclorg/s2i-perl-container/tree/master/5.34) | | |
| [5.36](https://github.com/sclorg/s2i-perl-container/tree/master/5.36) | | |

## Ruby

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| 2.2 – deprecated †  | [rhscl/ruby-22-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/ruby-22-rhel7) | [centos/ruby-22-centos7](https://hub.docker.com/r/centos/ruby-22-centos7/) |
| 2.3 – deprecated †  | [rhscl/ruby-23-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/ruby-23-rhel7) | [centos/ruby-23-centos7](https://hub.docker.com/r/centos/ruby-23-centos7/) |
| 2.4 – deprecated †  | [rhscl/ruby-24-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/ruby-24-rhel7) | [centos/ruby-24-centos7](https://hub.docker.com/r/centos/ruby-24-centos7/) |
| [2.5](https://github.com/sclorg/s2i-ruby-container/tree/master/2.5) | [rhscl/ruby-25-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/ruby-25-rhel7) | [centos/ruby-25-centos7](https://hub.docker.com/r/centos/ruby-25-centos7/) |
| [2.7](https://github.com/sclorg/s2i-ruby-container/tree/master/2.7) | [rhel8/ruby-27](https://access.redhat.com/containers/#/registry.redhat.io/rhel8/ruby-27) | [centos/ruby-27-centos7](https://hub.docker.com/r/centos/ruby-27-centos7/) |
| [3.0](https://github.com/sclorg/s2i-ruby-container/tree/master/3.0) | [rhel9/ruby-30](https://access.redhat.com/containers/#/registry.redhat.io/rhel9/ruby-30) | |
| [3.1](https://github.com/sclorg/s2i-ruby-container/tree/master/3.1) | [rhel9/ruby-31](https://access.redhat.com/containers/#/registry.redhat.io/rhel9/ruby-30) | |

## Varnish

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| 4 – deprecated † | [rhscl/varnish-4-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/varnish-4-rhel7) | [centos/varnish-4-centos7](https://hub.docker.com/r/centos/varnish-4-centos7/) |
| [6](https://github.com/sclorg/varnish-container/tree/master/6) | [rhel8/varnish-6](https://access.redhat.com/containers/#/registry.redhat.io/rhel8/varnish-6) | [centos/varnish-4-centos7](https://hub.docker.com/r/centos/varnish-6-centos7/) |
| [7](https://github.com/sclorg/varnish-container/tree/master/7) | | |

## Nginx

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| 1.8 – deprecated † | [rhscl/nginx-18-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/nginx-18-rhel7) | [centos/nginx-18-centos7](https://hub.docker.com/r/centos/nginx-18-centos7/) |
| 1.10 – deprecated † | [rhscl/nginx-110-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/nginx-110-rhel7) | [centos/nginx-110-centos7](https://hub.docker.com/r/centos/nginx-110-centos7/) |
| 1.12 – deprecated † | [rhscl/nginx-112-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/nginx-112-rhel7) | [centos/nginx-112-centos7](https://hub.docker.com/r/centos/nginx-112-centos7/) |
| 1.14 – deprecated † | [rhscl/nginx-114-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/nginx-114-rhel7) | [centos/nginx-114-centos7](https://hub.docker.com/r/centos/nginx-114-centos7/) |
| [1.18](https://github.com/sclorg/nginx-container/tree/master/1.18) – deprecated † | | |
| [1.20](https://github.com/sclorg/nginx-container/tree/master/1.20) | [rhel8/nginx-20](https://access.redhat.com/containers/#/registry.redhat.io/rhel8/nginx-120) | |
| [1.22-micro](https://github.com/sclorg/nginx-container/tree/master/1.22-micro) | | |
| [1.22](https://github.com/sclorg/nginx-container/tree/master/1.22) | | |

## Node.JS

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| 4 – deprecated † | [rhscl/nodejs-4-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/nodejs-4-rhel7) | [centos/nodejs-4-centos7](https://hub.docker.com/r/centos/nodejs-4-centos7/) |
| 6 – deprecated †| [rhscl/nodejs-6-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/nodejs-6-rhel7) | [centos/nodejs-6-centos7](https://hub.docker.com/r/centos/nodejs-6-centos7/) |
| 8 – deprecated † | [rhscl/nodejs-8-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/nodejs-8-rhel7) | [centos/nodejs-8-centos7](https://hub.docker.com/r/centos/nodejs-8-centos7/) |
| 10 – deprecated † | [rhscl/nodejs-10-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/nodejs-10-rhel7) | [centos/nodejs-10-centos7](https://hub.docker.com/r/centos/nodejs-10-centos7/) |
| [14-minimal](https://github.com/sclorg/s2i-nodejs-container/tree/master/14-minimal) | [rhel9/nodejs-14-minimal](https://access.redhat.com/containers/#/registry.redhat.io/rhel9/nodejs-14-minimal) | |
| [14](https://github.com/sclorg/s2i-nodejs-container/tree/master/14) | [rhel9/nodejs-14](https://access.redhat.com/containers/#/registry.redhat.io/rhel9/nodejs-14) | |
| [16-minimal](https://github.com/sclorg/s2i-nodejs-container/tree/master/16-minimal) | [rhel9/nodejs-16-minimal](https://access.redhat.com/containers/#/registry.redhat.io/rhel9/nodejs-18-minimal) | |
| [16](https://github.com/sclorg/s2i-nodejs-container/tree/master/16) | [rhel9/nodejs-16](https://access.redhat.com/containers/#/registry.redhat.io/rhel9/nodejs-16) | |
| [18-minimal](https://github.com/sclorg/s2i-nodejs-container/tree/master/18-minimal) | [rhel9/nodejs-18-minimal](https://access.redhat.com/containers/#/registry.redhat.io/rhel9/nodejs-18-minimal) | |
| [18](https://github.com/sclorg/s2i-nodejs-container/tree/master/18) | [rhel9/nodejs-18](https://access.redhat.com/containers/#/registry.redhat.io/rhel9/nodejs-18) | |


## Apache httpd

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| [2.4-micro](https://github.com/sclorg/httpd-container/tree/master/2.4-micro) | | |
| [2.4](https://github.com/sclorg/httpd-container/tree/master/2.4) | [rhscl/httpd-24-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/httpd-24-rhel7) | [centos/httpd-24-centos7](https://hub.docker.com/r/centos/httpd-24-centos7/) |

## s2i base

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| [s2i](https://github.com/sclorg/s2i-base-container.git) | [rhscl/s2i-base-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/s2i-base-rhel7) | [centos/s2i-base-centos7](https://hub.docker.com/r/centos/s2i-base-centos7/) |

## Redis

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| [3.2](https://github.com/sclorg/redis-container/tree/master/3.2) | [rhscl/redis-32-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/redis-32-rhel7) | [centos/redis-32-centos7](https://hub.docker.com/r/centos/redis-32-centos7/) |
| [5](https://github.com/sclorg/redis-container/tree/master/5) | [rhscl/redis-5-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/redis-5-rhel7) |  |
| [6](https://github.com/sclorg/redis-container/tree/master/6) | [rhscl/redis-6-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/redis-6-rhel7) |  |


## MySQL

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| [5.5](https://github.com/sclorg/mysql-container/tree/master/5.5)  – deprecated †|  |  |
| [5.6](https://github.com/sclorg/mysql-container/tree/master/5.6) | [rhscl/mysql-56-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/mysql-56-rhel7) | [centos/mysql-56-centos7](https://hub.docker.com/r/centos/mysql-56-centos7/) |
| [5.7](https://github.com/sclorg/mysql-container/tree/master/5.7) | [rhscl/mysql-57-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/mysql-57-rhel7) | [centos/mysql-57-centos7](https://hub.docker.com/r/centos/mysql-57-centos7/) |
| [8.0](https://github.com/sclorg/mysql-container/tree/master/8.0) | [rhscl/mysql-80-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/mysql-80-rhel7) | [centos/mysql-80-centos7](https://hub.docker.com/r/centos/mysql-80-centos7/) |

## MariaDB

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| [10.0](https://github.com/sclorg/mariadb-container/tree/master/10.0) | [rhscl/mariadb-100-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/mariadb-100-rhel7) | [centos/mariadb-100-centos7](https://hub.docker.com/r/centos/mariadb-100-centos7/) |
| [10.1](https://github.com/sclorg/mariadb-container/tree/master/10.1) | [rhscl/mariadb-101-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/mariadb-101-rhel7) | [centos/mariadb-101-centos7](https://hub.docker.com/r/centos/mariadb-101-centos7/) |
| [10.2](https://github.com/sclorg/mariadb-container/tree/master/10.2) | [rhscl/mariadb-102-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/mariadb-102-rhel7) | [centos/mariadb-102-centos7](https://hub.docker.com/r/centos/mariadb-102-centos7/) |
| [10.3](https://github.com/sclorg/mariadb-container/tree/master/10.3) | [rhscl/mariadb-103-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/mariadb-103-rhel7) |  |
| [10.5](https://github.com/sclorg/mariadb-container/tree/master/10.5) | [rhscl/mariadb-105-rhel7](https://access.redhat.com/containers/#/registry.redhat.io/rhel9/mariadb-105) |  |

## PostgreSQL

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| 9.6 – deprecated † | [rhscl/postgresql-96-rhel7](https://access.redhat.com/containers/?tab=overview#/registry.access.redhat.com/rhscl/postgresql-96-rhel7) | [centos/postgresql-96-centos7](https://hub.docker.com/r/centos/postgresql-96-centos7/) |
| [10](https://github.com/sclorg/postgresql-container/tree/master/10) | [rhscl/postgresql-10-rhel7](https://access.redhat.com/containers/?tab=overview#/registry.access.redhat.com/rhscl/postgresql-10-rhel7) | [centos/postgresql-10-centos7](https://hub.docker.com/r/centos/postgresql-10-centos7/) |
| [12](https://github.com/sclorg/postgresql-container/tree/master/12) | [rhscl/postgresql-12-rhel7](https://access.redhat.com/containers/?tab=overview#/registry.access.redhat.com/rhscl/postgresql-12-rhel7) | [centos/postgresql-12-centos7](https://hub.docker.com/r/centos/postgresql-12-centos7/) |
| [13](https://github.com/sclorg/postgresql-container/tree/master/13) | [rhscl/postgresql-13-rhel7](https://access.redhat.com/containers/?tab=overview#/registry.access.redhat.com/rhscl/postgresql-13-rhel7) | [centos/postgresql-13-centos7](https://hub.docker.com/r/centos/postgresql-13-centos7/) |
| [14](https://github.com/sclorg/postgresql-container/tree/master/14) |  |  |
| [15](https://github.com/sclorg/postgresql-container/tree/master/15) |  |  |

## Ruby on Rails

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| [4.1](https://github.com/sclorg/ror-container/tree/master/4.1) | [rhscl/ror-41-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/ror-41-rhel7) | [centos/ror-41-centos7](https://hub.docker.com/r/centos/ror-41-centos7/) |
| [4.2](https://github.com/sclorg/ror-container/tree/master/4.2) | [rhscl/ror-42-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/ror-42-rhel7) | [centos/ror-42-centos7](https://hub.docker.com/r/centos/ror-42-centos7/) |
| [5.0](https://github.com/sclorg/ror-container/tree/master/5.0) | [rhscl/ror-50-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/ror-50-rhel7) | [centos/ror-50-centos7](https://hub.docker.com/r/centos/ror-50-centos7/) |


## Apache HTTP Server
| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| [2.4](https://github.com/sclorg/httpd-container/tree/master/2.4)| [centos7/httpd-24-centos7](https://quay.io/repository/centos7/httpd-24-centos7) | |
| [2.4-micro](https://github.com/sclorg/httpd-container/tree/master/2.4-micro) | | |

## Deprecated images

Deprecated images are container images that are no longer actively maintained or updated by our team. This means that these images may become outdated, potentially containing security vulnerabilities or lacking new features and improvements. It is strongly recommended to avoid using deprecated images in your projects and to migrate to newer, supported images whenever possible. Please check the documentation or repository for alternative images and migration guidelines.

### Developer Toolset

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| [4-toolchain](https://github.com/sclorg/devtoolset-container/tree/master/4-toolchain) | [rhscl/devtoolset-4-toolchain-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/devtoolset-4-toolchain-rhel7) | [centos/devtoolset-4-toolchain-centos7](https://hub.docker.com/r/centos/devtoolset-4-toolchain-centos7/) |
| [4-perftools](https://github.com/sclorg/devtoolset-container/tree/master/4-perftools) | [rhscl/devtoolset-4-perftools-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/devtoolset-4-perftools-rhel7) | [centos/devtoolset-4-perftools-centos7](https://hub.docker.com/r/centos/devtoolset-4-perftools-centos7/) |
| [6-toolchain](https://github.com/sclorg/devtoolset-container/tree/master/6-toolchain) | [rhscl/devtoolset-6-toolchain-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/devtoolset-6-toolchain-rhel7) | [centos/devtoolset-6-toolchain-centos7](https://hub.docker.com/r/centos/devtoolset-6-toolchain-centos7/) |
| [6-perftools](https://github.com/sclorg/devtoolset-container/tree/master/6-perftools) | [rhscl/devtoolset-6-perftools-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/devtoolset-6-perftools-rhel7) | [centos/devtoolset-6-perftools-centos7](https://hub.docker.com/r/centos/devtoolset-6-perftools-centos7/) |

### Thermostat

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| [16-agent](https://github.com/sclorg/thermostat-container/tree/master/16-agent) | [rhscl/thermostat-16-agent-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/thermostat-16-agent-rhel7) | [centos/thermostat-16-agent-centos7](https://hub.docker.com/r/centos/thermostat-16-agent-centos7/) |
| [16-storage](https://github.com/sclorg/thermostat-container/tree/master/16-storage) | [rhscl/thermostat-16-storage-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/thermostat-16-storage-rhel7) | [centos/thermostat-16-storage-centos7](https://hub.docker.com/r/centos/thermostat-16-storage-centos7/) |

### MongoDB

| **version**  | **Red Hat Catalog** | **Docker Hub** |
| ------------ | ------------------- | -------------- |
| [2.6](https://github.com/sclorg/mongodb-container/tree/master/2.6) | [rhscl/mongodb-26-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/mongodb-26-rhel7) | [centos/mongodb-26-centos7](https://hub.docker.com/r/centos/mongodb-26-centos7/) |
| [3.2](https://github.com/sclorg/mongodb-container/tree/master/3.2) | [rhscl/mongodb-32-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/mongodb-32-rhel7) | [centos/mongodb-32-centos7](https://hub.docker.com/r/centos/mongodb-32-centos7/) |
| [3.4](https://github.com/sclorg/mongodb-container/tree/master/3.4) | [rhscl/mongodb-34-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/mongodb-34-rhel7) | [centos/mongodb-34-centos7](https://hub.docker.com/r/centos/mongodb-34-centos7/) |
| [3.6](https://github.com/sclorg/mongodb-container/tree/master/3.6) | [rhscl/mongodb-36-rhel7](https://access.redhat.com/containers/#/registry.access.redhat.com/rhscl/mongodb-36-rhel7) | [centos/mongodb-36-centos7](https://hub.docker.com/r/centos/mongodb-36-centos7/) |

