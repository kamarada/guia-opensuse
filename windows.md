---
layout: default
title: 12. MS Windows Interoperability - Using openSUSE With Windows Network, Documents and Running MS Windows
permalink: /windows
---

# 12. MS Windows Interoperability

The PC world is dominated by Microsoft, and they're not exactly known for making interoperability easy. Despite this, it's possible to interoperate fairly seamlessly in most cases. This chapter addresses the most common issues.

## 12.1 Office Documents

LibreOffice defaults to the Open Document Format (*.odt, *.ods, *.odp, etc.) which is an open standard. This format is partially supported by Microsoft Office >= 2007 Service Pack 2. Or you can suggest to your MS Windows and Mac OSX using contacts to install LibreOffice, as it's freely available for those platforms too.

LibreOffice can also read and write the Microsoft Office formats (*.doc, *.xls,*.ppt, *.docx, *.xlsx, *.pptx etc.) quite well - as well as a wide range of other formats.

<div class="tip">
<table>
<tbody>
<tr>
<td><img src="images/pics/tip.png" alt="tip" /></td>
<td>If you come across Microsoft documents that LibreOffice doesn't render well, consider trying if you have better luck with the Calligra suite.</td>
</tr>
</tbody>
</table>
</div>

## 12.2 Windows Network

For sharing resources on a local network with MS Windows machines the Samba service is used.

### 12.2.1 Accessing Shares

No configuration is needed to access files shared by others. Simply:

<div class="path">Launch the Dolphin file manager => Click the location bar or press Ctrl+L for an editable location bar => Enter 'smb://[ip-address]'</div>

{% include screenshot.html image="smb-dolph" %}

If you don't know the IP-address of the share you want to access, you can <i>browse</i> the local network by simply entering <i>smb:/</i> in the Dolphin location bar. However, this will only work if you configure or (temporarily) disable the firewall first. More instructions coming soon...

### 12.2.2 Sharing Your Files

To share <i>your</i> files with MS Windows users, Mac OSX users or other GNU/Linux users on the local network you must configure the Samba Server (make sure the packages <i>yast2-samba-server</i> and <i>samba</i> are installed). You only need to perform the first three steps the first time you want share a folder.

<b>1) </b> Open the YaST Samba Server module.

<div class="path">YaST =&gt; Network Services  =&gt; Samba Server</div>

{% include screenshot.html image="samba-server" %}

<b>2) </b> In the tab <i>Start-Up</i> select whether to autostart the Samba service during boot and whether to open the firewall ports required.

<b>3) </b> Go to the <i>Shares</i> tab, check the options <i>Allow Users to Share Their Directories</i> and <i>Allow Guest Access</i>. In the <i>Identity</i> tab you can configure your workgroup and share name.

<b>4) </b> Add shares by clicking the "Add" button and specifying the directories you want to share.

## 12.3 Running MS Windows Applications

High quality, native GNU/Linux applications exist for almost any purpose, but it's possible that you're dependent on a MS Windows-only application for some job. These are your options in such a case.

<div class="note">
<table>
<tbody>
<tr>
<td><img src="images/pics/obs.png" alt="obs" /></td>
<td>You should only run non-native applications as a last resort. Apps work better in their native environment.</td>
</tr>
</tbody>
</table>
</div>

### 12.3.1 Wine

Wine (Wine Is Not an Emulator) is an application that enables you to run many MS Windows applications, you can install wine with YaST or zypper.

Wine is a command line application, the syntax is:

<div class="cl">wine /path/to/setup.exe</div>

<div class="tip">
<table>
<tbody>
<tr>
<td><img src="images/pics/tip.png" alt="tip" /></td>
<td>The package <a href="http://sourceforge.net/projects/q4wine/" target="_blank">q4wine</a> provides a graphical interface for some features of Wine.</td>
</tr>
</tbody>
</table>
</div>

The Wine project keeps a database for sharing experiences of running applications, see:

<a href="http://appdb.winehq.org/appbrowse.php" target="_blank">http://appdb.winehq.org/appbrowse.php</a>

### 12.3.2 CrossOver

CrossOver is not gratis. It's specialised in running a select few of the major MS Windows applications - mostly office related.

<a href="https://www.codeweavers.com/products/cxlinux/" target="_blank">https://www.codeweavers.com/products/cxlinux/</a>

### 12.3.3 Dual Boot

As mentioned in the <i>Installation</i> chapter, it's relatively simple to run GNU/Linux and MS Windows on the same computer. If you only need a few applications that you rarely use, maybe it's worth it to reboot into MS Windows now and then, when you need to use these particular apps.

### 12.3.4 Virtualisation

It's possible to run MS Windows on top of GNU/Linux inside a <i>virtual machine</i>, using software such as VirtualBox, KVM, Xen or VMware. This is somewhat advanced, and requires some computer power.