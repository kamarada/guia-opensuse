---
layout: default
title: 10. Instalando software - instale programas com o gerenciador de pacotes
permalink: instalando-software
---

# 10. Instalando software

Software installation is generally incredibly easy on openSUSE. There's a package manager, which lets you install and remove packages very easily - it's comparable to the app stores found on many modern smart phones.

## 10.1 Using the package manager

Simply open YaST Software Management.

{% include video.html video="installpackage114" screenshot="sw-single" size="1.0 MB" %}

Now search for the package you want, select it for installation and click Accept. The package manager will then fetch the RPM package from your configured software repositories - and install it including any dependencies. After installation is complete the application should appear in the launch menu (unless it's a command line program).

{% include tip.html tip="The availability of software packages in the package manager depends on the configured _software repositories_. Read about software repositories in the next chapter." %}

### 10.1.1 Using 1-click Installation

When browsing openSUSE related websites, you're likely to come across buttons such as this one:

{% include pic.html src="oneclick.png" %}

1-click installation (also referred to as "Direct Install") simply automates the process of adding one or more software repositories to the package manager and installing one or more RPM packages. Therefore 1-click installation _should be used with the same care_ as manually adding unofficial repositories (see the next chapter for more on software repositories).

## 10.2 Other Installation Methods

Most users will find everything they need and more in the package manager - especially if a few additional software repositories are added (see next chapter). But not all software is packaged and provided via repositories, and non-free software usually can't be legally redistributed via the package manager because of license restrictions.

In these cases you'll need to go to the developer/vendor website and download and install the software manually - but **always** look for an openSUSE package in repositories first - and make sure you only download and install software from trusted sources.

### 10.2.1 RPM file

With a bit of luck the developer/vendor website will have an RPM file for openSUSE. To install a single, downloaded RPM file:

<div class="path">Open the Dolphin file manager =&gt; Navigate to the RPM file =&gt; Right Click it => Open With... => Install/Remove Software</div>

{% include note.html note="Only install RPM files that are built specifically for (your version of) openSUSE." %}

### 10.2.2 Tarball

If the website doesn't have an RPM for openSUSE, it will most likely have a so-called _tarball_. Tarballs (*.tar.gz, *.tar.bz2) are simply compressed archives similar to ZIP and RAR files. To uncompress a tarball:

<div class="path">Open the Dolphin file manager =&gt; Navigate to the tarball =&gt; Right click =&gt; Extract Archive</div>

The tarball might contain binaries that just need to be run, or it might contain source code which needs to be compiled to run on your system - this can be very complicated, and requires you to first install various developer tools. There's no one standard way to install tarball content, but instructions should always be included in the tarball in files called INSTALL, README or similar - or you should be able to find installation instructions on the website where you downloaded the tarball.

## 10.3 Package Management in the Terminal

If you wish, you can install and remove packages via a terminal too.

To search for a package run _zypper search [search term]_. Example:

<div class="cl">zypper search thunder</div>

To install a package run _zypper install [package name]_. Example:

<div class="clroot">zypper install MozillaThunderbird</div>

To remove a package run _zypper remove [package name]_. Example:

<div class="clroot">zypper remove PackageKit</div>

See _man zypper_ for more.

<div class="cl">man zypper</div>

Or for help on indvidual commands use for example:

<div class="cl">zypper install --help</div>

### 10.3.1 Using 1-click in the Terminal

You can actually use 1-click installation in the terminal too, the syntax is _OCICLI [URL]_, Example:

<div class="clroot">OCICLI http://opensuse-community.org/nvidia.ymp</div>

### 10.3.2 Manually downloaded RPM file

To install a manually downloaded RPM file, run:

<div class="clroot">zypper install /path/to/manually/downloaded.rpm</div>

### 10.3.3 RPM Queries

You can get a lot of useful information about installed packages from the RPM database very easily.

Check which version is installed. Example:

<div class="cl">rpm -q MozillaFirefox</div>

List the files which are installed by a package, and where. Example:

<div class="cl">rpm -ql amarok</div>

Find out which package a certain file belongs to. Example:

<div class="cl">rpm -qf /usr/bin/firefox</div>

Get various information about a package, including changelog. Example:

<div class="cl">rpm -qi --changelog MozillaFirefox</div>
