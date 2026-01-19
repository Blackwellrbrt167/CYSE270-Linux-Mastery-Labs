        # LAB-11 – Incident Simulation Capstone

        **Objective:** Integrate permissions, logs, networking, and firewall in one incident.  
        **LPIC-1 alignment:** Integrated administration

        ## Pre-flight
        - Snapshot: `LAB11-START`
        - Start terminal log (recommended):
          - `script -a ~/cyse270/logs/lab-11.log`

        ## Steps + Evidence
        ### Step 01
- Task: Setup issue: sudo mkdir -p /srv/incident ; sudo chmod 000 /srv/incident
- Screenshot filename: `lab-11_step-01_<shortdesc>.png`
- Prompt: Screenshot: ls -ld /srv/incident showing 000 perms.

### Step 02
- Task: Generate failed login once (wrong password once) then stop.
- Screenshot filename: `lab-11_step-02_<shortdesc>.png`
- Prompt: Screenshot: auth log line showing failed attempt.

### Step 03
- Task: Enable firewall with SSH allowed only (UFW).
- Screenshot filename: `lab-11_step-03_<shortdesc>.png`
- Prompt: Screenshot: ufw status numbered showing only SSH allowed.

### Step 04
- Task: Investigate: test access to /srv/incident; record error.
- Screenshot filename: `lab-11_step-04_<shortdesc>.png`
- Prompt: Screenshot: permission denied output.

### Step 05
- Task: Check ports: ss -tulpn
- Screenshot filename: `lab-11_step-05_<shortdesc>.png`
- Prompt: Screenshot: ss output showing ssh listening.

### Step 06
- Task: Fix: sudo chown root:analysts /srv/incident ; sudo chmod 770 /srv/incident
- Screenshot filename: `lab-11_step-06_<shortdesc>.png`
- Prompt: Screenshot: ls -ld showing fixed ownership/perms.

### Step 07
- Task: Verify analyst access (alice): sudo -u alice ls /srv/incident
- Screenshot filename: `lab-11_step-07_<shortdesc>.png`
- Prompt: Screenshot: successful listing.

### Step 08
- Task: Write 5-bullet incident note in reflection.md.
- Screenshot filename: `lab-11_step-08_<shortdesc>.png`
- Prompt: Screenshot: reflection.md showing 5 bullets (what/when/where/fix/prevent).

### Step 09
- Task: Cleanup: revert snapshot OR remove /srv/incident (your choice).
- Screenshot filename: `lab-11_step-09_<shortdesc>.png`
- Prompt: Screenshot: snapshot revert confirmation OR cleanup evidence.


        ## Verification checklist
        - [ ] I completed all steps
        - [ ] Screenshots stored in `evidence/screenshots/`
        - [ ] Commands recorded in `evidence/commands.log`
        - [ ] Reflection completed in `evidence/reflection.md`

        ## Mastery rep
        - [ ] Repeat lab from memory and update reflection with what improved.
