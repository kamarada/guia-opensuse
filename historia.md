---
layout: default
title: "Apêndice D: História - o que é software livre e de código aberto e qual é a história do openSUSE"
permalink: historia
---

# Apêndice D: História

The purpose of this chapter is to give readers some insight into and background knowledge of the history and eco system of GNU/Linux and free/open source software in general.

## D.1 Source Code vs. Binary Machine Code

Computer software is written in various different programming languages. This _source code_ can be written and understood by anyone with the proper training:

    #include <iostream.h>

    main()
    {
        cout << "Hello World!";
        return 0;
    }

The human-readable source code is then compiled into _binary machine code_ that computers can run:

    01001000 01100101 01101100 01101100 01101111 00100000 01010111 01101111 01110010 01101100 01100100 00100001 00100000

Without access to the source code and permission to modify it, neither you as an individual, nor your community at large, can study how the software works and what it does - let alone change it and improve it - you are completely dependent on the whims of the company/person which does have the source code.

## D.2 Richard Stallman, GNU and Free Software

In 1984 and 1985 respectively, system programmer Richard M. Stallman (RMS), who was increasingly frustrated by the technical and social restrictions proprietary software imposed on him, founded the [GNU](http://www.gnu.org/) project (GNU's Not Unix) with the aim to create a free Unix like operating system, and the [Free Software Foundation (FSF)](http://www.fsf.org) a foundation to promote free software.

<table style="text-align: left; width: 100%;" border="0" cellpadding="2" cellspacing="2">
	<tbody>
	<tr>
		<td style="width: 50%;"><div style="text-align: center;"><img style="width: 200px; height: 220px;" alt="rms" src="images/pics/rms.jpg" /></div></td>
	</tr>
      	<tr>
		<td class="image-caption">Richard M. Stallman</td>
	</tr>
</tbody>
</table>

Free software doesn't mean free of charge, free software can be commercial. It refers to free as in freedom, specifically defined by the following four fundamental freedoms:

- (0) The freedom to run the program, for any purpose.
- (1) The freedom to study how the program works, and change it to make it do what you wish.
- (2) The freedom to redistribute copies so you can help your neighbor.
- (3) The freedom to improve the program, and release your improvements (and modified versions in general) to the public, so that the whole community benefits.

The freedoms 1 and 3 require access to the source code of the program.

{% include tip.html tip="If you want to know more about free software, consider downloading this [video of Richard M. Stallman speaking](http://audio-video.gnu.org/video/20090122_richard_stallman.ogv) (550 MB, Ogg Theora format)" %}

### D.2.1 GNU GPL, Copyleft and Other Free Software Licenses

Any software licence that secures the above mentioned four fundamental freedoms, is considered a free software licence. Dozens and dozens of different free software licenses exist. Free software licences work by building on existing copyright laws to provide users with a lot more freedom and rights than you'd normally have.

The most widely used free software licence by far, is the GNU General Public License (GPL). One of the characteristics of the GNU GPL is that it applies a principle known as _copyleft_. This means that while you're allowed to modify and redistribute GPL'ed software - these derivative works **must** be distributed under similar terms - thus ensuring that GPL'ed programs will always remain free software. Non-copyleft licenses are also called _permissive_ licenses, these types of free software licenses allow redistributing the software under different, incompatible licenses - even proprietary ones.

## D.3 Linux and Linus Torvalds

By the late 1980s the GNU project had created an [almost complete free Unix operating system](http://directory.fsf.org/GNU/), but the kernel was causing problems.

In 1991, independentantly of the GNU project, then 22-year old Finnish university student Linus Torvalds decided to write a Unix kernel that he could use at home. Later that year he announced the first release on a newsgroup, using these now immortal words: _"...I'm doing a (free) operating system (just a hobby, won't be big and professional like gnu)..."_.

<table style="text-align: left; width: 100%;" border="0" cellpadding="2" cellspacing="2">
	<tbody>
	<tr>
		<td style="width: 50%;"><div style="text-align: center;"><img style="width: 200px; height: 207px;" alt="linus" src="images/pics/linus.jpg" /></div></td>
	</tr>
      	<tr>
		<td class="image-caption">Linus Torvalds</td>
	</tr>
</tbody>
</table>

The kernel was named Linux and soon it was licenced under the GNU GPL, and people started combining it with the GNU tools. A fully functional, free Unix-like operating system consisting of GNU plus Linux was reality!

Today Linus Torvalds lives in the U.S. and continues to lead development of the Linux kernel - but he's no longer alone, today over a thousand developers contribute code to the kernel every year - some of which are volunteers contributing in their spare time, while others are employed by large corporations, such as IBM, Intel, Novell and Red Hat.

## D.4 Open Source

The term [open source](http://opensource.org/) was created in 1998, by a group of people who wanted to distance themselves somewhat from the ideological rhetoric of the free software movement for the purpose of making free software more appealing to commercial interests.

The software licences recognised by the Free Software Foundation and the Open Source Initiative are almost all the same, therefore there's very little difference between open source and free software in practice - the differences are almost exclusively on a philosophical and rhetorical level. To bridge the gap between the two camps the term "FOSS" (Free and Open Source Software) is often used.

## D.5 The History of openSUSE

SUSE was founded on September 2, 1992 in Germany, under the name Gesellschaft f&uuml;r Software- und Systementwicklung mbH (S.u.S.E. GmbH), meaning: "Software and System Development, Inc.". The first GNU/Linux distribution (S.u.S.E. Linux 1.0) was released in 1994 - making SUSE one of the oldest existing GNU/Linux distributions. Originally it was merely a German version of an American distribution called Slackware, but later SUSE has become one of the leading distributions. In 2003 SUSE was acquired by Novell.

In 2005 the openSUSE project was started with the goal of opening up development and involve the community more.

In 2010 Novell was acquired by Attachmate. The deal was finalized in April 2011, and one of the first actions of Attachmate was to split SUSE into a separate business unit independant of Novell, and move SUSE headquarters back to Nuremberg, Germany. In 2014 Micro Focus merged with Attachmate, but this did not affect SUSE nor the openSUSE Project. In 2019 Micro Focus sold SUSE to Swedish private equity firm EQT Partners, again this had little or no direct effect on the openSUSE project.

In 2014 the development branch openSUSE Factory was stabilized enough to become a usable rolling relese distribution, called openSUSE Tumbleweed. openSUSE Tumbleweed forms the base for SUSE Linux Enterprise Server and Desktop (SLES and SLED). This again lead to changes in the stable openSUSE releases and the creation of openSUSE Leap in 2015, which uses SUSE Linux Enterprise for the core system, and has a form of long term support with major yearly service packs and major releases only happening every 3-4 years.

<table style="text-align: left; width: 100%;" border="0" cellpadding="2" cellspacing="2">
<tbody>
	<tr>
		<td style="width: 25%;"><div style="text-align: center;"><img style="border: 0px solid ; width: 148px; height: 140px;" alt="gnu" src="images/pics/gnu-head.jpg" /></div></td>

		<td style="width: 25%;"><div style="text-align: center;"><img style="width: 128px; height: 128px;" alt="tux" src="images/pics/linux.png" /></div></td>

		<td style="width: 25%"><div style="text-align: center;"><img style="width: 120px; height: 141px;" alt="konqui" src="images/pics/konqui.png" /></div></td>

		<td style="width: 25%"><div style="text-align: center;"><img style="width: 150px; height: 150px;" alt="geeko" src="images/pics/opensuse.jpg" /></div></td>
	</tr>
      	<tr>
		<td class="image-caption">The GNU project mascot</td>
		<td class="image-caption">The official mascot of Linux - the penguin Tux</td>
		<td class="image-caption">The KDE mascot - the dragon Konqui</td>
		<td class="image-caption">The SUSE mascot - the chameleon named Geeko</td>
	</tr>
</tbody>
</table>

## D.6 The GNU/Linux Ecosystem

### D.6.1 Distributions

When the Linux kernel and the GNU tools and other free software components from "upstream" are bundled together to form a complete contemporary operating system, it's called a  GNU/Linux _distribution_. Many distributions exist targetting different types of users and use cases - enterprises, home users, servers, desktops, multimedia centers etc. Some are commercial, others are fully based on the efforts of community volunteers. Besides bundling the software, distributors usually also integrate it, brand it, patch it, provide additional tools developed in-house and so forth. The existence of multiple distributions is only possible because the software components are free software of course.

<table style="text-align: left; width: 100%;" border="0" cellpadding="2" cellspacing="2">
	<tbody>
	<tr>
	<td style="width: 50%;"><center><a href="images/pics/ecosystem.png" rel="thumbnail"><img src="images/pics/ecosystemb.png" alt="ecosystem" class="pic" /></a></center></td>			
	</tr>
      	<tr>
	<td class="image-caption">This figure shows the ecosystem of upstream projects, distributors and end users.</td>
	</tr>
</tbody>
</table>

### D.6.2 Who Develops Free Software and Why?

Many developers are employed by large companies such as IBM, Novell, Red Hat, Google, Mozilla Foundation, KDAB, Intel, AMD, Canonical, Oracle etc. These companies usually have a business model of selling services around free software or selling hardware with free software installed on it. By using free software companies can share the development costs with others.

Also many people are paid to develop free software in other ways, via university work, government sponsorships, donations, students can be paid via the [Google Summer of Code](http://code.google.com/soc) project, etc.

However there are also many, many people working on free software in their spare time for nothing. They can have many different motivations.

- They may need a feature or suffer a bug ("scratch your own itch").
- It builds their skills and network and creates job opportunities.
- Programming is fun and challenging.
- There's a lot of recognition and respect to be gained.
- You can work on projects of you own choosing, unlike at your day-job.
- They may think software freedom in itself is important enough to work for.
- They'll take part in an exciting worldwide community.
- Etc.

### D.6.3 Who is Using GNU/Linux?

Many people still perceive GNU/Linux as a small hobbyist operating system - and the marketshare on standard desktop PCs is quite small of course. Nevertheless a marketshare of about one percent, still adds up to millions and millions of people worldwide. No truly reliable measure of the marketshare or total number of users is possible, for something which is usually freely redistributable.

However GNU/Linux is very widespread in other areas. A very large share of web servers and other servers run GNU/Linux. Facebook, Google and Yahoo build their entire infrastructures on GNU/Linux. GNU/Linux has been used everywhere from Antarctica to NASA using it in outer space. GNU/Linux is the preferred operating system for most of the world's [super computers](https://www.top500.org/stats/). And GNU/Linux is used [embedded in devices](http://linuxdevices.com/) where people often don't even know it's there, such as mobile phones, TVs, e-book-readers, PDAs, routers, hard disk recorders, NAS devices, and more.
