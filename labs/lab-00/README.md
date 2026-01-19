        # LAB-00 – Environment Control (VM + SSH + Snapshots)

        **Objective:** Own your environment: two Linux VMs, stable identity, and remote access.  
        **LPIC-1 alignment:** System architecture / installation basics

        ## Pre-flight
        - Snapshot: `LAB00-START`
        - Start terminal log (recommended):
          - `script -a ~/cyse270/logs/lab-00.log`

        ## Steps + Evidence
        ### Step 01
- Task: Boot Ubuntu Server VM. Log in.
- Screenshot filename: `lab-00_step-01_<shortdesc>.png`
- Prompt: Screenshot: VM console showing successful login prompt (username + hostname visible).

### Step 02
- Task: Set hostname: sudo hostnamectl set-hostname ubuntu-cyse270
- Screenshot filename: `lab-00_step-02_<shortdesc>.png`
- Prompt: Screenshot: command + output of hostnamectl showing new hostname.

### Step 03
- Task: Update packages: sudo apt update && sudo apt -y upgrade
- Screenshot filename: `lab-00_step-03_<shortdesc>.png`
- Prompt: Screenshot: terminal showing successful upgrade completion (no errors).

### Step 04
- Task: Install SSH: sudo apt -y install openssh-server
- Screenshot filename: `lab-00_step-04_<shortdesc>.png`
- Prompt: Screenshot: install output showing openssh-server installed.

### Step 05
- Task: Verify SSH: sudo systemctl status ssh
- Screenshot filename: `lab-00_step-05_<shortdesc>.png`
- Prompt: Screenshot: status output showing 'active (running)'.

### Step 06
- Task: Find IP: ip a
- Screenshot filename: `lab-00_step-06_<shortdesc>.png`
- Prompt: Screenshot: interface output with inet address highlighted.

### Step 07
- Task: From host PC: ssh youruser@IP_ADDRESS (accept key, login)
- Screenshot filename: `lab-00_step-07_<shortdesc>.png`
- Prompt: Screenshot: host terminal showing successful SSH login banner.

### Step 08
- Task: Repeat hostname + updates on Kali (optional SSH if needed).
- Screenshot filename: `lab-00_step-08_<shortdesc>.png`
- Prompt: Screenshot: Kali terminal showing hostname + successful update.

### Step 09
- Task: Take snapshot LAB0-DONE for both VMs.
- Screenshot filename: `lab-00_step-09_<shortdesc>.png`
- Prompt: Screenshot: VirtualBox/VMware snapshot list showing LAB0-DONE.


        ## Verification checklist
        - [ ] I completed all steps
        - [ ] Screenshots stored in `evidence/screenshots/`
        - [ ] Commands recorded in `evidence/commands.log`
        - [ ] Reflection completed in `evidence/reflection.md`

        ## Mastery rep
        - [ ] Repeat lab from memory and update reflection with what improved.
