# Install Oracle VirtualBox and Rocky Linux on Windows

This tutorial explains how to **download and install the latest Oracle VirtualBox on Windows** and then **install the latest Rocky Linux** inside it.

---

## Prerequisites

- Windows 10 / Windows 11 (64-bit)
- At least **8 GB RAM** (4 GB minimum)
- Internet connection
- Hardware virtualization enabled in BIOS (Intel VT-x / AMD-V)

---

## Part 1: Download & Install Oracle VirtualBox (Latest)

### Step 1: Download Oracle VirtualBox (Windows)

Official website (always provides latest version):

🔗 https://www.virtualbox.org/wiki/Downloads

Download:
- **Windows hosts** → `VirtualBox-x.x.x-Win.exe`

(Optional but recommended)
- **Oracle VM VirtualBox Extension Pack**
  - Must match the same VirtualBox version

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

### Step 3: Install Extension Pack (Recommended)

1. Double-click the downloaded Extension Pack
2. Click **Install**
3. Accept the license

This enables:
- USB 2.0 / 3.0
- Better device support
- RDP features

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

## Direct Download Links (Latest Rocky Linux)

> These links always point to the newest stable release.

### Minimal ISO
🔗 https://download.rockylinux.org/pub/rocky/9/isos/x86_64/Rocky-9-Minimal-x86_64.iso

### Boot ISO
🔗 https://download.rockylinux.org/pub/rocky/9/isos/x86_64/Rocky-9-Boot-x86_64.iso

### DVD ISO
🔗 https://download.rockylinux.org/pub/rocky/9/isos/x86_64/Rocky-9-DVD-x86_64.iso

---

## Part 3: Create Rocky Linux VM in VirtualBox

### Step 1: Create New VM

1. Open **VirtualBox**
2. Click **New**

**VM Details**
- Name: `RockyLinux`
- Type: `Linux`
- Version: `Red Hat (64-bit)`

Click **Next**

---

### Step 2: Memory & CPU

- RAM: **4096 MB** (minimum 2048 MB)
- CPU: **2 cores** (or more if available)

---

### Step 3: Virtual Hard Disk

- Disk Type: **VDI**
- Allocation: **Dynamically allocated**
- Size: **40 GB**

Click **Create**

---

## Part 4: Attach Rocky Linux ISO

1. Select VM → **Settings**
2. Go to **Storage**
3. Under **Controller IDE**, click **Empty**
4. Click disk icon → **Choose a disk file**
5. Select Rocky Linux ISO
6. Click **OK**

---

## Part 5: Install Rocky Linux

### Step 1: Start Installer

1. Select VM → **Start**
2. Choose **Install Rocky Linux**
3. Press **Enter**

---

### Step 2: Installation Settings

- Language: English
- Keyboard: English (US)
- Network: Enable Ethernet
- Installation Destination: Auto
- Software Selection:
  - **Minimal Install**

---

### Step 3: Set Root Password

1. Click **Root Password**
2. Set a strong password
3. Click **Done**

(Optional) Create a normal user.

---

### Step 4: Begin Installation

Click **Begin Installation**

Wait for completion.

---

### Step 5: Reboot

1. Click **Reboot System**
2. Remove ISO if prompted

---

## Part 6: First Login

Login using:
- `root` user  
or  
- The user you created

🎉 Rocky Linux installation completed successfully.

---

## What to Do Next

- Install **Guest Additions**
- Configure **Network & SSH**
- Setup **Docker / Jenkins / Ansible**
- Use as **Server or Dev Environment**

---

## References

- Oracle VirtualBox: https://www.virtualbox.org/
- Rocky Linux: https://rockylinux.org/

---

**End of Guide**
