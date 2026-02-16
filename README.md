# Install Oracle VirtualBox and Rocky Linux on Windows

This tutorial explains how to **download and install the latest Oracle VirtualBox on Windows** and then **install the latest Rocky Linux** inside it.

---

## Prerequisites

- Windows 10 / Windows 11
- At least **8 GB RAM**
- Internet connection
- Hardware virtualization enabled in BIOS

---

## Part 1: Download & Install Oracle VirtualBox (Latest)

### Step 1: Download Oracle VirtualBox (Windows)

Official website (always provides latest version):

🔗 https://www.virtualbox.org/wiki/Downloads

Download:
- **Windows hosts** → `VirtualBox-x.x.x-Win.exe`

---

### Step 2: Install Oracle VirtualBox

1. Double-click the downloaded `.exe` file
2. Click **Next**
3. Keep default settings
4. Accept the network interface warning
5. Click **Install**
6. Allow permissions when prompted
7. Click **Finish**

✅ VirtualBox installation completed

---


## Part 2: Download Rocky Linux (Latest)

### Rocky Linux Official Download Page

🔗 https://rockylinux.org/download

Choose **Architecture**:
- `x86_64` (for most systems)

---

## Rocky Linux ISO Variants Explained

| ISO Type | Description | Use Case |
|--------|-------------|---------|
| **Minimal ISO** | Small image, core OS only | ✅ Best for servers & learning |
| **Boot ISO** | Downloads packages during install | Requires internet |
| **DVD ISO** | Full offline installer | No internet needed |

### Recommended for Beginners
✅ **Minimal ISO**

---


## Part 3: Create Rocky Linux VM in VirtualBox

### Step 1: Create New VM

1. Open **VirtualBox**
2. Click **Machine** -> **New**

**Virtual machine name and operating system**
- VM Name: `RockyLinux`
- VM Folder: `D:\VirtualMachines`
- OS: `Linux`
- OS Distribution: `Red Hat`
- OS Version: `Red Hat (64-bit)`

**Specify vitual hardware**
- Base Memory: **2048 MB** (minimum RAM)
- CPU: **1 cores** (or more if available)

**Specify vitual hard disk**
- Create a new Virtual Hard Disk:
  - Hard Disk File Location and Size:
    - **E:\VirtualMachines\RockyLinux\RockyLinux.vdi**
    - **20 GB**

3. Click **Finish**
---


## Part 4: Attach Rocky Linux ISO

1. Select VM → **Settings**
2. Go to **Storage**
3. Remove **Empty.iso** under **Controller IDE**
4. Right click **Controller IDE**, click **Optical Drive**
5. Add Rocky Linux ISO
6. Select Rocky Linux ISO, click **Choose**
7. Click **OK**

---

## Part 5: Install Rocky Linux

### Step 1: Start Installer

1. Select VM → **Start**
2. Choose **Test this Media & install Rocky Linux XX.X**
3. Press **Enter**
4. wait for installation

---

### Step 2: Installation Settings

- Language: English
- Keyboard: English (India)
- Installation Destination: Auto
- Network: Enable Ethernet
- Time & Date: Asia/Kolkata timezone
- Root Account: Disabled
- User Creation: Create user (Add administrative priviliges to this user account)
- Click on **Begin Installation**

---

## Part 6: Change Network to Host Network (Bridged Adapter)

To allow the Rocky Linux VM to get an IP address from the same network as your host machine:

1. Select the VM → **Settings**
2. Go to **Network**
3. Set **Attached to** → **Bridged Adapter**
4. Select your active 
network adapter (Ethernet or Wi-Fi)
5. Click **OK**

---

## Part 7: First Login

Login using:
- The user you created during installation  
🎉 **Rocky Linux installation completed successfully.**

**Get the Linux IP Address**
Run this command inside the Rocky Linux VM:
```bash
ip a
```

---

### Connect to Rocky Linux Using Command Prompt or PowerShell
You can connect to the Linux machine remotely using **SSH**.

```bash
ssh <username>@<Linux-IP>
```

Example:
```bash
ssh utsav@192.168.1.50
```

## References

- Oracle VirtualBox: https://www.virtualbox.org/
- Rocky Linux: https://rockylinux.org/

---

**End of Guide**
