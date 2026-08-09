
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



---

## 📑 Table of Contents

* [Overview](#-overview)
* [Scenarios](#-scenarios)
* [Resources](#-resources)
* [Common Tools Used](#-common-tools-used)
* [Best Practices](#-best-practices)

---

# 🌐 Overview

This repository documents real-world IT support scenarios and how to resolve them step by step. Each scenario reflects common helpdesk tickets encountered in entry-level IT support, desktop support, and system administration roles.

The purpose of this lab is to:

- Build troubleshooting methodology
- Practice documenting technical issues
- Learn Windows administration basics
- Improve customer support communication
- Gain familiarity with common enterprise tools
- Simulate real-world helpdesk environments

---

# 🧩 Scenarios

---

## 1. 🔒 User Account Locked Out

**Problem:** A user cannot log in and receives an "Account is locked out" message.

### Steps to Resolve
1. Open **Active Directory Users and Computers (ADUC)**
2. Search for the user's account
3. Right-click the account > **Properties** > **Account** tab
4. Check the **Unlock account** checkbox
5. Click **Apply** > **OK**
6. Ask the user to try logging in again
7. If it continues:
   - Check **Event Viewer** > Windows Logs > Security
   - Investigate failed login attempts
   - Verify saved credentials on mapped drives or mobile devices

---

## 2. 🔑 Password Reset Request

**Problem:** A user forgot their password and cannot log in.

### Steps to Resolve
1. Verify the user's identity
2. Open **ADUC**
3. Locate the user account
4. Right-click > **Reset Password**
5. Enter a temporary password
6. Enable **User must change password at next logon**
7. Communicate the password securely
8. Confirm successful login

---

## 3. 🌐 No Internet Connection

**Problem:** A workstation has no internet access.

### Steps to Resolve
1. Verify whether other devices are affected
2. Open **Command Prompt**
3. Run:

```bash
ipconfig
ping 8.8.8.8
ping google.com
```

4. If no valid IP:

```bash
ipconfig /release
ipconfig /renew
```

5. Restart the network adapter
6. Reboot the router if needed
7. Escalate to networking team if unresolved

---

## 4. 🖨️ Printer Not Working

**Problem:** Print jobs are stuck or printer is unavailable.

### Steps to Resolve
1. Verify power and cable/network connection
2. Open printer queue
3. Cancel stuck jobs
4. Restart **Print Spooler**
5. Print test page
6. Remove/re-add printer
7. Reinstall drivers if necessary

---

## 5. 💻 Computer Running Slow

**Problem:** User reports system slowness.

### Steps to Resolve
1. Open **Task Manager**
2. Check CPU, RAM, and disk usage
3. End unnecessary tasks
4. Disable startup applications
5. Run malware scan
6. Free disk space
7. Run Disk Cleanup
8. Reboot system
9. Check hardware age/specifications

---

## 6. 📶 Unable to Connect to Wi-Fi

**Problem:** Laptop cannot connect to wireless network.

### Steps to Resolve
1. Verify Wi-Fi is enabled
2. Forget and reconnect to network
3. Run:

```bash
netsh wlan show interfaces
ipconfig /flushdns
```

4. Update Wi-Fi drivers
5. Run Windows Network Troubleshooter
6. Restart wireless adapter

---

## 7. 📧 Outlook Not Receiving Emails

**Problem:** Outlook inbox is not updating.

### Steps to Resolve
1. Verify internet connectivity
2. Check Junk/Spam folders
3. Disable **Work Offline**
4. Verify mailbox quota
5. Re-add Outlook profile
6. Check Microsoft 365 service status
7. Escalate to email administrator if needed

---

## 8. 🖥️ Blue Screen of Death (BSOD)

**Problem:** Computer crashes unexpectedly.

### Steps to Resolve
1. Record BSOD error code
2. Review **Event Viewer**
3. Open **Reliability Monitor**
4. Run:

```bash
sfc /scannow
chkdsk /f /r
```

5. Update drivers
6. Roll back recent software changes
7. Run memory diagnostics
8. Escalate hardware failures

---

## 9. 🔌 Computer Won't Turn On

**Problem:** Computer does not power on.

### Steps to Resolve
1. Verify power cable and outlet
2. Test another outlet
3. Check power supply switch
4. Perform hard reset
5. Test charger/battery
6. Escalate for hardware diagnostics

---

## 10. 🗂️ User Cannot Access Shared Drive

**Problem:** Access denied to network share.

### Steps to Resolve
1. Verify domain login
2. Confirm mapped drive exists
3. Re-map network drive
4. Check security group membership
5. Verify NTFS/share permissions
6. Ask user to sign out/sign back in

---

## 11. 🎤 Microphone Not Working

**Problem:** User cannot be heard during Teams/Zoom calls.

### Steps to Resolve
1. Verify microphone is connected
2. Check mute button/headset controls
3. Open **Sound Settings**
4. Confirm correct input device selected
5. Test microphone levels
6. Allow microphone permissions
7. Update audio drivers
8. Test in another application

---

## 12. 🔊 No Sound From Speakers

**Problem:** User cannot hear audio.

### Steps to Resolve
1. Check volume and mute settings
2. Verify correct playback device
3. Disconnect/reconnect headset
4. Restart Windows Audio service
5. Update sound drivers
6. Test audio using another application

---

## 13. 🖥️ Second Monitor Not Detected

**Problem:** External monitor is not working.

### Steps to Resolve
1. Check HDMI/DisplayPort cable
2. Verify monitor power
3. Press:

```bash
Windows + P
```

4. Select **Extend**
5. Open Display Settings > Detect Displays
6. Update graphics drivers
7. Test different cable or port

---

## 14. 🔄 Windows Update Failed

**Problem:** Windows updates will not install.

### Steps to Resolve
1. Restart the computer
2. Run Windows Update Troubleshooter
3. Clear SoftwareDistribution cache
4. Run:

```bash
sfc /scannow
DISM /Online /Cleanup-Image /RestoreHealth
```

5. Retry updates
6. Install updates manually if necessary

---

## 15. 🧱 Application Keeps Crashing

**Problem:** Specific software closes unexpectedly.

### Steps to Resolve
1. Restart application
2. Reboot computer
3. Check for updates
4. Reinstall application
5. Review Event Viewer logs
6. Test with another user profile
7. Verify system requirements

---

## 16. 🔐 VPN Connection Issues

**Problem:** User cannot connect to VPN remotely.

### Steps to Resolve
1. Verify internet connectivity
2. Confirm VPN credentials
3. Restart VPN client
4. Verify MFA approval
5. Reinstall VPN software if necessary
6. Test alternate network
7. Escalate to networking/security team

---

## 17. 🧹 Disk Space Full

**Problem:** User receives low disk space warnings.

### Steps to Resolve
1. Run Disk Cleanup
2. Empty Recycle Bin
3. Remove temporary files
4. Uninstall unused applications
5. Move files to cloud/network storage
6. Check for unusually large folders

---

## 18. 🖱️ Keyboard or Mouse Not Working

**Problem:** Peripheral device is unresponsive.

### Steps to Resolve
1. Disconnect/reconnect device
2. Replace batteries (wireless)
3. Try different USB port
4. Restart computer
5. Update drivers
6. Test device on another computer

---

## 19. 🧑‍💻 Remote Desktop (RDP) Not Working

**Problem:** User cannot remote into workstation/server.

### Steps to Resolve
1. Verify target machine is online
2. Confirm Remote Desktop is enabled
3. Verify firewall allows RDP
4. Confirm correct hostname/IP
5. Test network connectivity:

```bash
ping hostname
```

6. Verify user permissions
7. Restart Remote Desktop Services if needed

---

## 20. ☁️ OneDrive Not Syncing

**Problem:** Files are not syncing to cloud storage.

### Steps to Resolve
1. Verify internet connection
2. Restart OneDrive client
3. Check storage quota
4. Sign out/sign back in
5. Verify file path length limitations
6. Reinstall OneDrive if necessary

---

## 21. 🛑 High CPU Usage

**Problem:** System CPU remains near 100%.

### Steps to Resolve
1. Open Task Manager
2. Identify high CPU process
3. End unnecessary tasks
4. Disable startup applications
5. Scan for malware
6. Update problematic applications/drivers

---

## 22. 🗃️ File Permissions Issue

**Problem:** User cannot edit or save files.

### Steps to Resolve
1. Verify NTFS permissions
2. Confirm file ownership
3. Check if file is open elsewhere
4. Verify read-only settings
5. Test access with another account

---

## 23. 📱 MFA / Authenticator Problems

**Problem:** User cannot complete MFA authentication.

### Steps to Resolve
1. Verify phone date/time settings
2. Ensure user has internet/mobile signal
3. Resync authenticator app
4. Remove/re-add MFA method
5. Provide temporary bypass if policy allows

---

## 24. 🧪 Software Installation Failed

**Problem:** Application installation will not complete.

### Steps to Resolve
1. Verify admin permissions
2. Check available disk space
3. Disable antivirus temporarily (if approved)
4. Download fresh installer
5. Run installer as administrator
6. Review installation logs

---

## 25. 🌍 DNS Resolution Problems

**Problem:** User can ping IP addresses but not websites.

### Steps to Resolve
1. Run:

```bash
nslookup google.com
ipconfig /flushdns
```

2. Change DNS server temporarily:
   - 8.8.8.8
   - 1.1.1.1
3. Restart network adapter
4. Verify DNS server availability

---

## 26. 🔄 PC Stuck Restarting

**Problem:** Computer enters reboot loop.

### Steps to Resolve
1. Boot into Safe Mode
2. Remove recent updates/drivers
3. Run Startup Repair
4. Run:

```bash
sfc /scannow
```

5. Restore system using System Restore
6. Escalate for OS reinstallation if needed

---

## 27. 📂 Missing Network Drive

**Problem:** Mapped drive disappeared after reboot.

### Steps to Resolve
1. Verify network connectivity
2. Re-map drive manually
3. Enable:
   - **Reconnect at sign-in**
4. Verify login scripts/GPOs
5. Check server availability

---

## 28. 🔥 Laptop Overheating

**Problem:** Laptop becomes extremely hot or shuts down.

### Steps to Resolve
1. Check for blocked vents
2. Clean dust buildup
3. Verify fans are spinning
4. Close intensive applications
5. Update BIOS/drivers
6. Escalate for hardware cleaning or fan replacement

---

## 29. 🪫 Battery Not Charging

**Problem:** Laptop battery remains at low percentage.

### Steps to Resolve
1. Verify charger connection
2. Test different outlet
3. Check battery health in BIOS
4. Update power drivers
5. Test alternate charger
6. Replace battery if degraded

---

## 30. 📡 Ethernet Connection Not Working

**Problem:** Wired connection has no network access.

### Steps to Resolve
1. Verify Ethernet cable connection
2. Test another cable
3. Check switch/router port lights
4. Disable/re-enable network adapter
5. Renew IP address
6. Update NIC drivers

---
