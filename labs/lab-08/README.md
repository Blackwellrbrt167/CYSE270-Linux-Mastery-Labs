        # LAB-08 – Firewall Hardening (UFW)

        **Objective:** Apply default-deny firewall and recover safely.  
        **LPIC-1 alignment:** Security administration

        ## Pre-flight
        - Snapshot: `LAB08-START`
        - Start terminal log (recommended):
          - `script -a ~/cyse270/logs/lab-08.log`

        ## Steps + Evidence
        ### Step 01
- Task: Install: sudo apt -y install ufw
- Screenshot filename: `lab-08_step-01_<shortdesc>.png`
- Prompt: Screenshot: ufw install output.

### Step 02
- Task: Status: sudo ufw status verbose
- Screenshot filename: `lab-08_step-02_<shortdesc>.png`
- Prompt: Screenshot: status verbose output.

### Step 03
- Task: Defaults: sudo ufw default deny incoming ; sudo ufw default allow outgoing
- Screenshot filename: `lab-08_step-03_<shortdesc>.png`
- Prompt: Screenshot: terminal confirming rule set.

### Step 04
- Task: Allow SSH: sudo ufw allow 22/tcp
- Screenshot filename: `lab-08_step-04_<shortdesc>.png`
- Prompt: Screenshot: rule added output.

### Step 05
- Task: Enable: sudo ufw enable
- Screenshot filename: `lab-08_step-05_<shortdesc>.png`
- Prompt: Screenshot: ufw enabled message.

### Step 06
- Task: Verify numbered: sudo ufw status numbered
- Screenshot filename: `lab-08_step-06_<shortdesc>.png`
- Prompt: Screenshot: numbered rules list.

### Step 07
- Task: Test SSH still works from host.
- Screenshot filename: `lab-08_step-07_<shortdesc>.png`
- Prompt: Screenshot: host terminal showing active SSH session after firewall enabled.

### Step 08
- Task: Recovery: sudo ufw disable then sudo ufw enable
- Screenshot filename: `lab-08_step-08_<shortdesc>.png`
- Prompt: Screenshot: disable/enable outputs.


        ## Verification checklist
        - [ ] I completed all steps
        - [ ] Screenshots stored in `evidence/screenshots/`
        - [ ] Commands recorded in `evidence/commands.log`
        - [ ] Reflection completed in `evidence/reflection.md`

        ## Mastery rep
        - [ ] Repeat lab from memory and update reflection with what improved.
