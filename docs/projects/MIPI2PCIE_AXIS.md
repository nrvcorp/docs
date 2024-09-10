#Zynq UltraScale+ MPSoC - ZCU106 MIPI2PCIE_AXIS Example Design
This technical article provides you an overview of the ZCU106 MIPI2PCIE_AXIS Example design.

**Table of Contents**

1. [Document History](#document-history)
2. [Introduction](#introduction)
3. [Download and Installation](#download-and-installation)
4. [Steps to Operate DVS Camera](#steps-to-operate-dvs-camera)

----


###Document History
| Date            | Version | Author      | Description of Revisions                       |
|-----------------|---------|-------------|------------------------------------------------|
| August 31, 2024 | 1.0     | Soosung Kim | First MIPI2PCIE_AXIS Example Design of ZCU106  |

###Introduction
ZCU106 Evaluation Platform <br>
<img src="https://github.com/nrvcorp/docs/blob/gh-pages/assets/projects/MIPI2PCIE_AXIS/imgs/zcu106.png?raw=true" alt="board_setup" width="" />

The ZCU106 MIPI2PCIE_AXIS Example Design uses the following IPs along with the Zynq UltraScale+ Processing System for demonstrating Video Streaming using mipi_rx_subsystem block made by our company.

1. Zynq UltraScale+ MPSoC Processing System (Xilinx IP)
2. MIPI D-PHY (Xilinx IP)
3. mipi_rx_subsystem (NRV IP)
4. DMA/Bridge Subsystem for PCI Express (Xilinx IP)
5. AXI IIC (Xilinx IP)
6. AXI GPIO (Xilinx IP)

###Download and Installation
1. Install __Vivado 2021.2__, __Vitis 2021.2__ from [Vivado Design suite](https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/vivado-design-tools/archive.html).
2. Download __host code__ from our GitHub page ([https://github.com/nrvcorp/mipi_controller_new](https://github.com/nrvcorp/mipi_controller_new)).

Here are some reference materials you might find useful: <br>
- _View our DVS-MIPI Register Setfile from [here](https://nrvcorp.github.io/docs/register/DVS_MIPI/)._ <br>
- _View our DVS-FMC Board Pinmap from [here](https://nrvcorp.github.io/docs/datasheet/DVS_FMC/)._ <br>
- _View AER Packet Format from [here](https://github.com/nrvcorp/docs/blob/gh-pages/assets/datasheet/dvs_datasheet/aer_packet_format.pdf?raw=true)._


###Steps to Operate DVS Camera
1) The distributed SD Card will contain a boot image (BOOT.BIN)

<img src="https://github.com/nrvcorp/docs/blob/gh-pages/assets/projects/MIPI2PCIE_AXIS/imgs/boot_image.png?raw=true" alt="boot_image" width="" />

2) Power off the host PC and ZCU106, then insert the SD card. <br>
3) Set the boot mode switch SW6 to ON-OFF-OFF-OFF to SD boot mode as shown in the following figure. <br>
<img src="https://github.com/nrvcorp/docs/blob/gh-pages/assets/projects/MIPI2PCIE_AXIS/imgs/boot_mode.png?raw=true" alt="boot_mode" width="320" />

4) Connect the DVS Camera into HPC0 port. <br>
5) Turn on the host PC and ZCU106 board. <br>
6) Once the host PC is fully powered on, press the SW19 GPIO pin on the ZCU106 board. <br>
7) Run host code on the PC.


Below figure shows the complete board setup. <br>
<img src="https://github.com/nrvcorp/docs/blob/gh-pages/assets/projects/MIPI2PCIE_AXIS/imgs/board_setup.png?raw=true" alt="board_setup" width="320" />

The video will appear as follows: <br>
<video width="320" height="240" controls loop="" muted="" autoplay="">
    <source src="https://github.com/nrvcorp/docs/raw/gh-pages/assets/projects/MIPI2PCIE_AXIS/video/dvs_Streaming.mp4">
</video>
<br>
