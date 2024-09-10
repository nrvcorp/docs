# Zynq UltraScale+ MPSoC - ZCU106 CIS_DVS streaming Example Design

This technical article provides you an overview of the CIS camera and DVS camera streaming Example design.

**Table of Contents**

1. [Document History](#document-history)
2. [Introduction](#introduction)
3. [Download and Installation](#download-and-installation)

## 1. Document History

| Date               | Version | Author       | Description of Revisions                       |
|--------------------|---------|--------------|------------------------------------------------|
| September 10, 2024 | 3.3     | Mincheol Cha | First CIS_DVS Example Design of ZCU106         |

---

## 2. Introduction

**[ZCU106 Evaluation Platform]** <br>
<img src="https://github.com/nrvcorp/docs/blob/gh-pages/assets/projects/MIPI2PCIE_AXIS/imgs/zcu106.png?raw=true" alt="board_setup" width="" />

The **ZCU106 CIS_DVS streaming Example Design** uses the following IPs along with the Zynq UltraScale+ Processing System for demonstrating Video Streaming using mipi_rx_subsystem block made by our company.

1. Zynq UltraScale+ MPSoC Processing System (Xilinx IP)
2. MIPI D-PHY (Xilinx IP)
3. mipi_rx_subsystem (NRV IP)
4. DMA/Bridge Subsystem for PCI Express (Xilinx IP)
5. AXI IIC (Xilinx IP)
6. AXI GPIO (Xilinx IP)
7. Sensor Demosaic (Xilinx IP)
8. Gamma LUT (Xilinx IP)
9. Video Processing Subsystem (Xilinx IP)

**[LI-IMX274MIPI-FMC]** <br>
<img src="https://leopardimaging.com/wp-content/uploads/2023/04/IMX274MIPI-FMC.jpg?raw=true" alt="board_setup" width="30%" /> <br>

The **ZCU106 CIS_DVS streaming Example Design** uses **LI-IMX274MIPI-FMC** for the CIS camera.
[Cis Camera Vendor Link](https://leopardimaging.com/product/platform-partners/amd/li-imx274mipi-fmc/)

---

## 3. Download and Installation

The project consists of the following

- Vivado Project ([Download Link](https://github.com/nrvcorp/docs/blob/gh-pages/assets/projects/CIS_DVS/cis_dvs_project.zip?raw=true))
- Firmware code ([Download Link]())
- Host code ([Download Link]())

<br>

### How to Install

1. Install **Vivado 2021.2**, **Vitis 2021.2** from [Vivado Design suite](https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/vivado-design-tools/archive.html).
2. Download cis_dvs_project.zip file and unzip <br />
([Download the project](https://github.com/nrvcorp/docs/blob/gh-pages/assets/projects/CIS_DVS/cis_dvs_project.zip?raw=true))
3. Open **Vivado 2021.2** and run the provided TCL script (Click `Tools` → `Run Tcl Script` → Select `<current_dir>/CIS_DVS.tcl`)
4. The project will open in `<current_dir>/vivado_project` folder
5. Generate Bitstream
6. Generate XSA file (Click `File` → `Export` → `Export Hardware...` →  select `include bitstream` → write xsa_file_name) <br />
([Download generated XSA file](https://github.com/nrvcorp/docs/blob/gh-pages/assets/projects/CIS_DVS/xsa/CIS_DVS_wrapper_v3_3.xsa?raw=true))
7. Open **Vitis 2021.2** and create Application Project (Click `File` → `New` → `Application Project` → `Create a new platform from hardware (XSA)`)
8. Select the generated XSA file and write Application Project Name
9. Select `Empty Application(C)` → `Finish` and the application with the platform will be created.
10. Copy the provided firmware code to `project_name_system/project_name/src` <br />
([Download firmware code](https://github.com/nrvcorp/docs/blob/gh-pages/assets/projects/CIS_DVS/xsa/CIS_DVS_wrapper_v3_3.xsa?raw=true))
11. Download and install XDMA driver from Xilinx

Here are some reference materials you might find useful: <br>

- _View our DVS-MIPI Register Setfile from [here](https://nrvcorp.github.io/docs/register/DVS_MIPI/)._ <br>
- _View our DVS-FMC Board Pinmap from [here](https://nrvcorp.github.io/docs/datasheet/DVS_FMC/)._ <br>
- _View AER Packet Format from [here](https://github.com/nrvcorp/docs/blob/gh-pages/assets/datasheet/dvs_datasheet/aer_packet_format.pdf?raw=true)._

## 4. Steps to Operate Both Cameras
