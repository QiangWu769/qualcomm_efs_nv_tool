# Qualcomm EFS NV Tool

## Overview
**qualcomm_efs_nv_tool** is the first tool that can directly open the EFS folder and read/write NV items on commercial mobile devices. 

Previously, accessing the EFS folder required Qualcomm's official tool QPST, while reading and writing NV items required Qualcomm's official tool QXDM. Usable versions of QPST can be found online, but they require enabling USB diag mode and depend on Windows systems. QXDM has even stricter requirements, needing a Qualcomm official license, and similarly depends on USB diag mode and Windows systems.

## Working Principle
The working principle of qualcomm_efs_nv_tool is to obtain data from Qualcomm's diag device, which is also the principle behind several existing tools for capturing cellular network logs, such as qcsuper, mobileinsight, and scat.

## Compatibility
For Qualcomm chips before Snapdragon 888, including Snapdragon 765, they generally run on Linux kernel 4.19 or earlier versions (subject to further verification). Starting from Snapdragon 888, they run on Linux kernel 5.4.61 or later versions (8gen1 uses 5.12). 

This has led to the disappearance of the `/dev/diag` device on Snapdragon 888 and later chips, which is why many tools, including qcsuper, mobileinsight, and scat, cannot run on Snapdragon 888 and later chips. 

**Our tool solves this problem** and currently runs on:
- Snapdragon 888 devices (OnePlus 9)
- Snapdragon 765 devices (Xiaomi 10 Youth Edition)

All tested devices are running Android 11. We will gradually add compatibility for more devices and Android versions.

## Source Code
The source code will also be fully published in this repository.

<img width="315" alt="image" src="https://github.com/user-attachments/assets/6af01797-8569-49fc-af13-78ac74e10fd9" />
<img width="305" alt="image" src="https://github.com/user-attachments/assets/254f96cb-31db-43c5-a57c-ee6a73f0e4f7" />
<img width="317" alt="image" src="https://github.com/user-attachments/assets/28af78c2-c73e-40f1-bd18-f74f90a15336" />


