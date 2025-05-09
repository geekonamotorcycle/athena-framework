# Dell PowerEdge x20-Series Hardware Baseline Template

> For use with Dell PowerEdge T320/R620/R720-class servers. Fill using iDRAC, OS tools, or physical inspection.  
> Do not reboot or open chassis unless approved. Use iDRAC web UI, virtual console, REST, or supported OS commands.  

---

## 📌 Server Identity and Role

- **Hostname:**  
- **Client Name:**  
- **Site / Location:**  
- **Chassis Model:**  
- **Service Tag:** *(iDRAC: Dashboard or System > Overview > Hardware)*  
- **Asset Tag (if applicable):**  
- **Deployment Role (e.g., hypervisor, NAS, domain controller):**  
- **Deployment Date:**  
- **Last Inventory Date:**  

---

## 🔧 Firmware and Core System Versions

- **BIOS Version / Date:** *(iDRAC: Server > BIOS)*  
- **iDRAC Version:** *(iDRAC: Overview > Firmware > iDRAC Settings)*  
- **Lifecycle Controller Version:** *(iDRAC: Overview > Firmware)*  
- **Boot Mode (BIOS/UEFI):** *(iDRAC: Server > BIOS Summary)*  
- **Operating System / Hypervisor:**  
- **Kernel / Build Version:** *(OS: `uname -a`, `systeminfo`, etc.)*  

---

## 🧠 CPU and Memory

- **CPU Model(s):** *(iDRAC: Server > Processor Info)*  
- **CPU Count / Cores / Threads:**  
- **RAM Installed (Total):** *(iDRAC: Memory > Summary)*  
- **RAM Slot Count (Used/Total):** *(iDRAC: Memory > Slot Details)*  
- **ECC Supported:**  
- **Max RAM Supported:**  
- **RAM Slot Map:**  
  - A1: __ GB – Manufacturer – Type – Speed  
  - A2: __ GB – Manufacturer – Type – Speed  
  - (extend as needed)  

---

## 🖧 Network Interfaces

- **NIC Overview:** *(iDRAC: Network > NIC Inventory)*  
  - Adapter Model(s):  
  - Number of Ports:  
  - PCI Slot (if applicable):  
  - iDRAC Shared NIC Enabled: Yes / No  

- **MAC to Physical Label Mapping:**  
  - Use [nic-labeler](https://github.com/geekonamotorcycle/xcp-ng-nic-labeler) on any Linux system with `lshw`, `dmidecode`, `ethtool`  
  - Works on XCP-ng, Ubuntu, RHEL, Proxmox, and most Linux servers  
  - Store `nic-labels.json` in inventory folder for reference

  - Example Mapping:  
    - eth0: MAC `xx:xx:xx:xx:xx:xx` – Label: `iDRAC Shared / LOM1`  
    - eth1: MAC `xx:xx:xx:xx:xx:xx` – Label: `10GbE SFP+ Port 1`  
    - eth2: MAC `xx:xx:xx:xx:xx:xx` – Label: `10GbE SFP+ Port 2`  

---

## 💾 Storage and RAID Configuration

- **Controller Model:** *(iDRAC: Storage > Controllers)*  
- **Slot (Integrated/PCIe):**  
- **Firmware Version:**  
- **Mode (RAID/JBOD/IT):**  
- **Battery/Cache Module Present:** Yes / No  

- **Virtual Disk Layout:** *(iDRAC: Storage > Virtual Disks)*  
  - VD 0 – 512GB – RAID 1 – Purpose: OS Boot  
  - VD 1 – 8TB – RAID 5 – Purpose: VM Storage  

- **Physical Disk Map:** *(iDRAC: Storage > Physical Disks)*  
  - Bay 0: 512GB SAS – SN: XXXXX – VD 0 – Status: Online  
  - Bay 1: 512GB SAS – SN: XXXXX – VD 0 – Status: Online  
  - Bay 2: 2TB SAS – SN: XXXXX – VD 1 – Status: Online  
  - (extend as needed)

---

## 🧩 PCIe and Expansion Slot Map

- **Slot Map:** *(iDRAC: System > PCIe Devices)*  
  - Slot 1: Dell PERC H310 – Purpose: HBA passthrough for TrueNAS  
  - Slot 2: Intel X520-DA2 – Purpose: 10GbE NAS + VM trunk  
  - Slot 3: Quadro K2200 – Purpose: Docker GPU workloads  
  - Slot 4: Empty  
  - Slot 5: Coral USB TPU – Purpose: Frigate NVR acceleration  

---

## 🔌 Power Supply and Fans

- **Power Supply Count / Wattage:** *(iDRAC: Power > PSU Details)*  
- **Redundancy Mode:** *(iDRAC: Power > Redundancy)*  
- **Fan Count / Placement:** *(iDRAC: System > Fans)*  
- **Fan Speed Snapshot:**  
  - Fan 1: __%  
  - Fan 2: __%  
  - Fan 3: __%  
  - (extend as needed)

---

## 🌡️ Thermal and Power Metrics

- **Thermal Sensors:** *(iDRAC: Thermal > Temperature Sensors)*  
  - CPU Temp: __ °C  
  - Inlet Temp: __ °C  
  - System Temp: __ °C  

- **Power Usage (from iDRAC):** *(iDRAC: Power > Consumption History)*  
  - Idle: __ W  
  - Peak: __ W  
  - BTU/hr Estimate: __  

- **Thermal Profile Notes:**  
  - Max Safe Load Temp: __ °C  
  - Current Operation: Normal / Elevated / Critical  
  - Cooling Adequacy: Yes / No  

---

## 🗂️ Additional Notes and Observations

- **Connected USB Devices:**  
  - Coral TPU – Used for Frigate detection VM  
  - USB Drive – Diagnostic Bootloader  

- **Console Access Method(s):**  
  - iDRAC Virtual Console / Serial Console / VGA  

- **Special BIOS Settings:**  
  - VT-d: Enabled  
  - Boot Mode: UEFI  

- **Backup Integration:**  
  - XOA for VM backup  
  - NAS target via 10Gb link  

---

## ✅ Engineer Signoff

- **Engineer Name:**  
- **Date Completed:**  
- **Validation Methods Used:** iDRAC / OS CLI / Physical  
- **Signature or Initials:**  

---

## 📘 Change Log

| Date       | Engineer   | Summary of Change                   | Section(s) Modified        |
|------------|------------|-------------------------------------|----------------------------|
| YYYY-MM-DD | j.smith    | Initial inventory completed         | All                        |
| YYYY-MM-DD | t.lee      | Updated disk layout after upgrade   | Storage                    |
| YYYY-MM-DD | j.smith    | Added power readings from iDRAC     | Power, Thermals            |

---
