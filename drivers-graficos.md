---
layout: default
title: 14. Drivers gráficos - instale os drivers das placas de vídeo 3D NVIDIA ou ATI/AMD no openSUSE
permalink: drivers-graficos
---

# 14. Drivers gráficos

Note that there's no need to install the below non-free video drivers, if the free drivers used by default work for your needs.

<!-- nvidia KMPs start -->

## 14.1 Nvidia

This section describes two different ways of installing the proprietary Nvidia graphics driver, either using 1-click installation or using the terminal.

### 14.1.2 Install the Nvidia Driver in the Terminal

You can install the Nvidia driver in the terminal. **By using this method you don't need to know your graphics card model or series**.

First add the repository:

<div class="clroot">zypper addrepo -f https://download.nvidia.com/opensuse/leap/15.5 nvidia</div>

The following command should automatically install the correct driver for your card:

<div class="clroot">zypper install-new-recommends --repo https://download.nvidia.com/opensuse/leap/15.5</div>

When installation is done reboot the computer.

<!-- nvidia KMP end -->
<!-- ati KMP start -->

## 14.2 ATI/AMD

The free software drivers included by default should work very well for most. For some newer cards you may need a proprietary driver, see:

<https://en.opensuse.org/SDB:AMDGPU-PRO>

<!-- ati KMP end -->

## 14.3 Intel

The 3D drivers for Intel graphics cards are free software, and can therefore be included in openSUSE out of the box. No additional installation or configuration is needed.
