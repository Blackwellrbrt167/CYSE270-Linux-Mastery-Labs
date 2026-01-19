        # LAB-04 – Permission Warfare (Predict, Break, Fix)

        **Objective:** Predict access outcomes and fix permission issues fast.  
        **LPIC-1 alignment:** Permissions & ownership

        ## Pre-flight
        - Snapshot: `LAB04-START`
        - Start terminal log (recommended):
          - `script -a ~/cyse270/logs/lab-04.log`

        ## Steps + Evidence
        ### Step 01
- Task: Create folders: sudo mkdir -p /lab4/public /lab4/private
- Screenshot filename: `lab-04_step-01_<shortdesc>.png`
- Prompt: Screenshot: ls -ld /lab4/* output.

### Step 02
- Task: Public open: sudo chmod 777 /lab4/public
- Screenshot filename: `lab-04_step-02_<shortdesc>.png`
- Prompt: Screenshot: ls -ld /lab4/public showing 777.

### Step 03
- Task: Private locked: sudo chown root:root /lab4/private ; sudo chmod 700 /lab4/private
- Screenshot filename: `lab-04_step-03_<shortdesc>.png`
- Prompt: Screenshot: ls -ld /lab4/private showing 700.

### Step 04
- Task: Test public write as normal user: touch /lab4/public/test.txt
- Screenshot filename: `lab-04_step-04_<shortdesc>.png`
- Prompt: Screenshot: ls -l /lab4/public showing test.txt.

### Step 05
- Task: Test private access: ls /lab4/private (should fail)
- Screenshot filename: `lab-04_step-05_<shortdesc>.png`
- Prompt: Screenshot: permission denied output.

### Step 06
- Task: Fix for analysts: sudo chown root:analysts /lab4/private ; sudo chmod 770 /lab4/private
- Screenshot filename: `lab-04_step-06_<shortdesc>.png`
- Prompt: Screenshot: ls -ld /lab4/private showing group analysts and 770.

### Step 07
- Task: Verify alice: sudo -u alice ls /lab4/private
- Screenshot filename: `lab-04_step-07_<shortdesc>.png`
- Prompt: Screenshot: successful listing (even if empty).

### Step 08
- Task: Optional ACL: sudo apt -y install acl ; sudo setfacl -m u:bob:rx /lab4/private
- Screenshot filename: `lab-04_step-08_<shortdesc>.png`
- Prompt: Screenshot: getfacl /lab4/private output showing bob entry.


        ## Verification checklist
        - [ ] I completed all steps
        - [ ] Screenshots stored in `evidence/screenshots/`
        - [ ] Commands recorded in `evidence/commands.log`
        - [ ] Reflection completed in `evidence/reflection.md`

        ## Mastery rep
        - [ ] Repeat lab from memory and update reflection with what improved.
