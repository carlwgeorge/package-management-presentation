# CLI Tools

* RPM
    * rpm - basic command for interacting with installed RPMs or RPM files
    * yum/dnf - front end for rpm, handles repositories
    * yum-utils - collection of several related tools
    * repoquery - part of yum-utils, query repositories

* DEB
    * dpkg - basic command for interacting with installed DEBs or DEB files
    * apt - front end for dpkg, handles repositories
    * aptitude - ncurses and CLI front end for apt
    * synaptic - graphically front end for apt
    * https://www.debian.org/doc/manuals/debian-faq/ch-pkgtools.en.html

# Tasks

## Install Package

* RPM
    * rpm -i $pkg
    * yum localinstall $pkg
    * yum install $pkg
* DEB
    * dpkg $pkg
    * apt-get install $pkg

## Update Package

rpm -u
yum update

## Uninstall Package

rpm -e
yum erase

## Basic Package Query

rpm -q $pkg

## Show Package Information

rpm -qi $pkg
yum info $pkg


## List All Installed Packages

rpm -qa

## What Package Owns File

rpm -qf

rpm ‐qc packagename
package config files

rpm ‐ql packagename
all files from package

yum check‐updates
list available updates

yum provides $thing
lists all packages that provide $thing.  could be a file, a package name, or a capability

yum clean all
clears all yum caches

# Package signing

RPMs are signed with GPG keys
Repositories usually place their keys in /etc/pki/rpm‐gpg.
Yum will bug you to accept a key if you haven't already imported it into the RPM keyring.

rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7

