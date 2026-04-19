
Modbus Scanner + ECY Point Populator

> ⚠️ **IMPORTANT: COMMUNITY TOOL – NOT AN OFFICIAL DISTECH CONTROLS PRODUCT**
>
> This application is a special project developed by members of the Distech Controls Advanced Support Team and is **NOT a sanctioned, endorsed, or official product release** by Distech Controls Inc.  
> Please read **[DISCLAIMER.txt](DISCLAIMER.txt)** carefully before using this tool.

**Advanced Modbus discovery, diagnostics, and automated ECY point population utility**

[![Platform](https://img.shields.io/badge/platform-Windows-lightgrey)]()
[![PowerShell](https://img.shields.io/badge/PowerShell-5.1%2B%20%7C%207.0%2B-blue)]()
[![Modbus](https://img.shields.io/badge/protocol-Modbus%20TCP%20%7C%20RTU-green)]()
[![Community Tool](https://img.shields.io/badge/status-community%20tool-orange)]()



## ⚠️ Important Notice

**THIS IS A COMMUNITY TOOL – READ BEFORE USE**

This application is:
- ✅ **Freely available** for use by qualified professionals  
- ✅ **Built using** open Modbus standards (TCP and RTU-over-TCP) and publicly documented ECY APIs  
- ✅ **Supported at discretion** by Advanced Support for authorized partners  
- ❌ **NOT an official Distech Controls product**  
- ❌ **NOT covered** by Distech Controls warranties or standard support agreements  
- ❌ **NOT subject** to formal QA, certification, or release processes  

📋 **[READ THE FULL DISCLAIMER](DISCLAIMER.txt)** — contains important legal, warranty, and liability information.

**By using this tool, you acknowledge and accept these terms.**



## 🎯 What Is This Tool?

**Modbus Scanner + ECY Point Populator** is a **power-user utility** designed to simplify and accelerate:

- Modbus device discovery and diagnostics
- Live register and coil inspection
- Data type decoding and testing
- Writing coils and registers (FC05 / FC06)
- Rapid creation and population of ECY Modbus device definitions and points
- CSV-based import/export of register maps

It bridges the gap between **Modbus field testing** and **ECY controller integration**, reducing manual setup time and commissioning errors.

**Built for:**  
System integrators, commissioning engineers, and advanced technical support personnel

**Developed by:**  
Distech Controls Advanced Support Team (community project)



## ✨ Key Features

### 🔍 **Modbus Scanning & Discovery**

- Modbus **TCP** and **RTU-over-TCP tunnel** support
- Supports FC01, FC02, FC03, and FC04
- Batch scanning with configurable start address and quantity
- Parallel polling with adjustable intervals
- Built-in network diagnostics (Ping + TCP port test)
- Automatic quantity caps per Modbus specification



### 📊 **Live Register & Bit Inspection**

- Live polling with change tracking (`**` marker on value change)
- Automatic Modbus address formatting:
  - Coils (0xxxx)
  - Discrete Inputs (1xxxx)
  - Input Registers (3xxxx)
  - Holding Registers (4xxxx)
- Context menu tools:
  - Copy value
  - Copy address
  - Remove row
  - Decode bits / values



### 🧮 **Data Type Decoding**

Instant interpretation of raw register data as:
- BIT / BOOL
- UINT16 / INT16
- UINT32 / INT32
- FLOAT32
- HEX / Binary

Data type changes trigger automatic re-reads when connected.



### ✍️ **Write Operations (Use With Care)**

- **FC05** – Write Single Coil
- **FC06** – Write Single Register
- Input validation and logging
- Supports decimal and hex input (`0x1234`)
- Real-time confirmation via Modbus response

⚠️ *Writes affect live devices – ensure you understand the impact before use.*



### 🧩 **Manual & CSV Register Mapping**

- Add manual rows for non-scanned registers
- Import register maps from CSV
- Export current register view to CSV
- Preserve names, data types, and values
- Ideal for documenting vendor Modbus maps



### 🔌 **ECY Device & Point Population**

- Build ECY Modbus **Device definitions** from scan results
- Push discovered registers as points via ECY REST API
- Credential-based authentication
- Preview JSON payloads before POST
- Designed to reduce repetitive ECY configuration work

*(Point POST logic mirrors original Advanced Support internal tooling)*



### 🪛 **Frame Injector (Advanced / Experimental)**

- Craft and send raw Modbus frames
- Inspect raw request and response bytes
- Intended for protocol testing and troubleshooting
- **Recommended for advanced users only**



### 🖥️ **Rich UI & Diagnostics**

- Collapsible sections for cleaner workflows
- Expandable debug log panel:
  - Raw bytes
  - MBAP headers
  - TCP diagnostics
- Color-coded connection and status indicators
- Live statistics:
  - Poll count
  - Error count
  - Last scan time



## 📥 Installation & Requirements

### **System Requirements**

- Windows 10 / 11
- PowerShell:
  - 5.1+ (Windows built-in)
  - 7.x supported
- Network access to Modbus devices
- Network access to ECY REST APIs (for posting)

**No additional dependencies required.**



### **Running the Tool**

1. Launch `Modbus Scanner+ECY point populator 2.0.0.exe`
2. Configure connection:
   - Modbus TCP **or**
   - RTU-over-TCP tunnel
3. Connect to target device
4. Scan registers or coils
5. Decode, name, test, and optionally write values
6. Populate ECY device and points as needed



## 🎮 Typical Workflow

1. **Connect to Modbus device**
2. **Scan relevant address range**
3. **Identify and name registers**
4. **Adjust data types**
5. **Verify live values**
6. *(Optional)* Write test values
7. **Export CSV or**
8. **POST device & points into ECY**



## 🧠 Intended Users

This tool is designed for users who understand:
- Modbus addressing schemes
- Register vs coil semantics
- Risks of writing live data
- ECY controller configuration concepts

**Not recommended for untrained users or production experimentation without testing.**



## 🐛 Stability & Risk Notes

- Tool has been tested internally, but:
  - ❌ No formal QA coverage
  - ❌ No certification testing
- Writing coils/registers can:
  - Trigger equipment actions
  - Affect building operation
- Always validate in a **lab or maintenance window** first



## 📜 Legal & Licensing

- **Community project**
- **No warranty**
- **Use at your own risk**

See:
- 📄 **[DISCLAIMER.txt](DISCLAIMER.txt)** – legal status, warranty, liability
- 📄 **THIRD-PARTY-NOTICES.txt** – external components (if applicable)



## 🤝 Support & Feedback

Support is provided **at discretion only**, primarily for:
- Distech Controls System Integrators
- Authorized Distributors
- OEM / Partner organizations

There are:
- ❌ No SLAs
- ❌ No guaranteed response times
- ❌ No obligation for future development



## 📊 Project Information

- **Application:** Modbus Scanner + ECY Point Populator
- **Version:** 2.0.0
- **Platform:** Windows
- **Status:** Community Tool
- **Maintained by:** Distech Controls Advanced Support Team



**Built with ⚡ by the Distech Controls Advanced Support Team**

*Please review [DISCLAIMER.txt](DISCLAIMER.txt) before use.*



