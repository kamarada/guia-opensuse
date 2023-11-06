---
layout: default
title: 9. Administrator Settings (YaST) - Introduction to the YaST Setup Tool
permalink: /yast
---

# 9. Administrator Settings (YaST)

YaST (Yet another Setup Tool) is the central tool for system administration. You find YaST in the launch menu in the System category.

{% include screenshot.html image="yast-controlcenter" %}

<b>Default YaST modules</b>

In YaST you can perform almost any system task, with powerful graphical modules, e.g.:
<ul>
<li>Install and remove software (see next chapter)</li>
<li>Set up your printer</li>
<li>Configure the firewall</li>
<li>Enable and disable system services</li>
<li>Configure network sharing (samba)</li>
<li>Format and partition your drives</li>
<li>Enable NTP daemon</li>
<li>And much, much more...</li>
</ul>

<b>Additional YaST modules</b>

A lot more YaST modules are available than the ones included in the default installation (read about installing packages in the next chapter). Some notable modules not installed by default are:

<ul>
<li>Apache web server (package: yast2-http-server)</li>
<li>SSH daemon (package: yast2-sshd)</li>
<li>FTP server (package: yast2-ftp-server)</li>
<li>NFS server (package: yast2-nfs-server)</li>
<li>And many more...</li>
</ul>

<div class="tip">
<table>
<tbody>
<tr>
<td><img src="images/pics/tip.png" alt="tip" /></td>
<td>You don't have to use YaST if you don't want to. You can achieve the same things and more using command line tools and manually editing configuration files.</td>
</tr>
</tbody>
</table>
</div>

## 9.1 YaST in the Terminal

The YaST modules can also be used in a terminal (ncurses mode) - this is very useful for servers with no graphical environment running, for remote access via SSH, or in case your graphical environment fails.

Simply run <i>yast</i> as root in a terminal.

<div class="clroot">yast</div>

{% include screenshot.html image="yast-ncurses" %}

Navigate using arrow keys, Enter and Alt+[highlighted letters] (e.g. Alt+Q to quit).