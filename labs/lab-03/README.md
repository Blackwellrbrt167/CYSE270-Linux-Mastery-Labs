        # LAB-03 – User & Group Control (Least Privilege)

        **Objective:** Create role-based users and enforce least privilege.  
        **LPIC-1 alignment:** User administration

        ## Pre-flight
        - Snapshot: `LAB03-START`
        - Start terminal log (recommended):
          - `script -a ~/cyse270/logs/lab-03.log`

        ## Steps + Evidence
        ### Step 01
- Task: Create groups: sudo groupadd analysts ; sudo groupadd services
- Screenshot filename: `lab-03_step-01_<shortdesc>.png`
- Prompt: Screenshot: getent group analysts/services output.

### Step 02
- Task: Create users: sudo useradd -m -s /bin/bash alice ; sudo useradd -m -s /bin/bash bob
- Screenshot filename: `lab-03_step-02_<shortdesc>.png`
- Prompt: Screenshot: tail -n 2 /etc/passwd showing alice and bob lines.

### Step 03
- Task: Set passwords: sudo passwd alice ; sudo passwd bob
- Screenshot filename: `lab-03_step-03_<shortdesc>.png`
- Prompt: Screenshot: terminal showing 'password updated successfully' for each.

### Step 04
- Task: Assign groups: sudo usermod -aG analysts alice ; sudo usermod -aG services bob
- Screenshot filename: `lab-03_step-04_<shortdesc>.png`
- Prompt: Screenshot: id alice and id bob outputs.

### Step 05
- Task: Create shared folder: sudo mkdir -p /srv/shared
- Screenshot filename: `lab-03_step-05_<shortdesc>.png`
- Prompt: Screenshot: ls -ld /srv/shared output.

### Step 06
- Task: Set ownership + setgid perms: sudo chown root:analysts /srv/shared ; sudo chmod 2770 /srv/shared
- Screenshot filename: `lab-03_step-06_<shortdesc>.png`
- Prompt: Screenshot: ls -ld /srv/shared showing permissions (drwxrws---).

### Step 07
- Task: Test alice write: sudo -u alice touch /srv/shared/alice.txt
- Screenshot filename: `lab-03_step-07_<shortdesc>.png`
- Prompt: Screenshot: ls -l /srv/shared showing alice.txt and group ownership.

### Step 08
- Task: Lock bob: sudo usermod -L bob ; test: su - bob (should fail)
- Screenshot filename: `lab-03_step-08_<shortdesc>.png`
- Prompt: Screenshot: failed login message.

### Step 09
- Task: Unlock bob: sudo usermod -U bob
- Screenshot filename: `lab-03_step-09_<shortdesc>.png`
- Prompt: Screenshot: successful su - bob login prompt.


        ## Verification checklist
        - [ ] I completed all steps
        - [ ] Screenshots stored in `evidence/screenshots/`
        - [ ] Commands recorded in `evidence/commands.log`
        - [ ] Reflection completed in `evidence/reflection.md`

        ## Mastery rep
        - [ ] Repeat lab from memory and update reflection with what improved.
