<img width="315" alt="image" src="https://github.com/user-attachments/assets/8fef679c-03d9-485e-b902-5f1f4b8b77a5" />
<img width="311" alt="image" src="https://github.com/user-attachments/assets/b875a7f3-b339-4728-bcd5-667202d9ed67" />
<img width="311" alt="image" src="https://github.com/user-attachments/assets/71ea5a9f-6ac4-41cd-8db2-a22a97ed574d" />



qualcomm_efs_nv_tool is the first tool that can directly open the EFS folder and read/write NV items on commercial mobile devices. Previously, accessing the EFS folder required Qualcomm's official tool QPST, while reading and writing NV items required Qualcomm's official tool QXDM. Usable versions of QPST can be found online, but they require enabling USB diag mode and depend on Windows systems. QXDM has even stricter requirements, needing a Qualcomm official license, and similarly depends on USB diag mode and Windows systems.

The working principle of qualcomm_efs_nv_tool is to obtain data from Qualcomm's diag device, which is also the principle behind several existing tools for capturing cellular network logs, such as qcsuper, mobileinsight, and scat.

For Qualcomm chips before Snapdragon 888, including Snapdragon 765, they generally run on Linux kernel 4.19 or earlier versions (subject to further verification). Starting from Snapdragon 888, they run on Linux kernel 5.4.61 or later versions (8gen1 uses 5.12). This has led to the disappearance of the /dev/diag device on Snapdragon 888 and later chips, which is why many tools, including qcsuper, mobileinsight, and scat, cannot run on Snapdragon 888 and later chips. Our tool solves this problem and currently runs on Snapdragon 888 devices (OnePlus 9) and Snapdragon 765 devices (Xiaomi 10 Youth Edition and Google Pixel 5), all running Android 11. We will gradually add compatibility for more devices and Android versions.

The source code will also be fully published in this repository.
