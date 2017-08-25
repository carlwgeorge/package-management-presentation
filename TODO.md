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

## install package

* RPM
    * rpm -i $pkg
    * yum localinstall $pkg
    * yum install $pkg
* DEB
    * dpkg $pkg
    * apt-get install $pkg

## update package

* rpm -u
* yum update

## uninstall package

* rpm -e
* yum erase

## basic package query

* rpm -q $pkg

## show package information

* rpm -qi $pkg
* yum info $pkg


## list all installed packages

* rpm -qa

## what package owns file

* rpm -qf

## show package config files 

* rpm ‐qc packagename

# show all files from package

* rpm ‐ql packagename

# list available updates

* yum check‐updates

# lists all packages that provide $thing.  could be a file, a package name, or a capability

* yum provides $thing

# clears all yum caches (except for disabled/removed repos)

* yum clean all

# package signing

* RPMs are signed with GPG keys
* Repositories usually place their keys in /etc/pki/rpm‐gpg.
* Yum will bug you to accept a key if you haven't already imported it into the RPM keyring.

# package signing keys

* rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7


# version strings

* NEVRA - name, epoch, version, release, arch
* semantic

# shared libraires versus bundled libraries
