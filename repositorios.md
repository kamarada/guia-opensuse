---
layout: default
title: 11. Repositórios de software - adicionando e gerenciando repositórios de pacotes
permalink: repositorios
---

# 11. Repositórios de software

As mentioned in the previous chapter, the package manager installs software by fetching packages from software repositories, therefore the software available for easy installation via the package manager depends on the configured repositories.

A software repository is a collection of RPM packages (the openSUSE packaging format) and metadata for the available packages. Usually repositories are on online servers, but it can also be on a CD/DVD or on other media.

## 11.1 Managing Repositories

Respositories can be added, removed and configured via YaST, in the module called Software Repositories.

{% include screenshot.html image="yast-repos" %}

### 11.1.1 Adding Repositories

The official repositories are pre-configured, but many unofficial repositories exist and can be added too.

{% capture add_repositories_with_care %}
Add repositories with care.

- Unofficial repositories might include experimental packages
- Not all repositories are mutually compatible
- The risk level of a repository can change over time
- Too many repositories makes the package manager slower
{% endcapture %}
{% include note.html note=add_repositories_with_care %}

The easiest and safest way to add repositories is using the list of online community repositories in YaST. This provides you with a selection of popular and quite safe repositories to choose from:

<div class="path">YaST => Software => Software Repositories => Click on "Add" => Select "Community Repositories" and click "Next"</div>

Note that the _openSUSE BuildService_ is a service for the community to build and share packages. _openSUSE BuildService repositories are unofficial and unsupported_. Use at your own risk.

### 11.1.2 Recommended Repositories

You should always have the four _official_ repositories (which are configured out of the box).

- **Main Repository (OSS)**
- **Main Repository (NON-OSS)**
- **Main Update Repository**
- **Main Update Repository (NON-OSS)**

Additionally I recommend adding the following _unofficial_ repositories from the Community Repositories list, for having a good balance of software supply and stability for most users.

- **Packman Repository**

{% capture still_missing_a_package %}
Still missing a package? You can search for packages/repositories on the openSUSE BuildService here:

<http://software.opensuse.org/>
{% endcapture %}
{% include tip.html tip=still_missing_a_package %}

### 11.1.3 Vendor Change Updates

Updating installed packages from one repository to versions from a different repository with a different _vendor_, is a little bit complicated. Read about it here:

<http://en.opensuse.org/SDB:Vendor_change_update>

## 11.2 Repository Management in the Terminal

If you wish, you can manage your repositories via a terminal too.

Add a repository with auto-refresh enabled _zypper addrepo -f [URL] [Alias]_. Example:

<div class="clroot">zypper addrepo -f http://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Leap_15.5/ packman</div>

Disable a repository _zypper modifyrepo -d [URL|Alias]_. Example:

<div class="clroot">zypper modifyrepo -d Packman</div>

Remove a repository _zypper removerepo [URL|Alias]_. Example:

<div class="clroot">zypper removerepo http://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Leap_15.5/
</div>

List configured repositories, showing  details (priorities, URL, etc.):

<div class="cl">zypper repos -d</div>

See _man zypper_ for more.

<div class="cl">man zypper</div>

Or for help on indvidual commands use for example:

<div class="cl">zypper addrepo --help</div>
