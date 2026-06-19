
# Windows Help Desk Troubleshooting

A collection of common Windows IT Help Desk troubleshooting scenarios documented using a structured support methodology. This project demonstrates practical troubleshooting skills, root cause analysis, and resolution steps used in real-world IT support environments.

---

## Project Objective

The goal of this project is to showcase fundamental IT Help Desk skills by documenting common user issues, troubleshooting procedures, root causes, and resolutions.

---

# Scenario 1: Wi-Fi Connected but No Internet

## Issue

A user reports that the computer is connected to Wi-Fi but cannot access the internet.

### Initial Checks

* Confirmed Wi-Fi connection status
* Asked whether other devices were affected
* Verified network availability

### Troubleshooting Steps

1. Opened Command Prompt.
2. Ran:

```cmd
ipconfig
```

3. Checked for an APIPA address (`169.254.x.x`).
4. Verified DNS server configuration.
5. Restarted the network adapter.
6. Reconnected to the wireless network.

### Root Cause

Incorrect DNS configuration prevented domain name resolution.

### Resolution

Configured the adapter to obtain DNS settings automatically and reconnected to the network.

### What I Learned

This issue highlighted the importance of DNS in network connectivity and reinforced a structured troubleshooting approach.
---

# Scenario 2: Computer Running Very Slowly

## Issue

A user reports that the computer is performing slowly during normal operation.

### Initial Checks

* Asked when the issue started
* Determined whether the issue occurred at startup or during specific tasks
* Checked for recent software installations

### Troubleshooting Steps

1. Opened Task Manager.
2. Reviewed CPU, Memory, and Disk utilization.
3. Examined startup applications.
4. Disabled unnecessary startup programs.
5. Verified available disk space.
6. Restarted the computer.

### Root Cause

Excessive startup applications were consuming system resources.

### Resolution

Disabled non-essential startup programs, reducing resource usage and improving performance.

### What I Learned

This scenario reinforced the importance of checking system resources and startup processes when troubleshooting performance issues

---

# Scenario 3: Printer Not Printing / Printer Missing

## Issue

A user reports that the printer is not printing or does not appear in the list of available printers.

### Initial Checks

* Confirmed the printer was powered on
* Verified cable and network connections
* Determined whether other users were affected

### Troubleshooting Steps

1. Opened **Devices and Printers**.
2. Checked printer status.
3. Restarted the **Print Spooler** service.
4. Verified printer driver installation.
5. Removed and re-added the printer.
6. Tested printing functionality.

### Root Cause

The Print Spooler service had stopped running.

### Resolution

Restarted the Print Spooler service and verified successful printing.

### What I Learned

This scenario demonstrated the importance of checking Windows services when troubleshooting printer-related issues.

---

# Tools Used

* Windows 10 / Windows 11
* Command Prompt (CMD)
* Task Manager
* Network Adapter Settings
* Services Console (`services.msc`)
* Devices and Printers

---

# Key Takeaways

Through these troubleshooting exercises, I strengthened my understanding of:

* Network troubleshooting fundamentals
* DNS and IP addressing concepts
* Windows performance optimization
* Printer and driver management
* Service management in Windows
* IT Help Desk documentation practices

---



**Rohan Pinto**

