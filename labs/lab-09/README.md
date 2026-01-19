        # LAB-09 – Bash Scripting (Healthcheck)

        **Objective:** Write scripts to automate admin checks (from scratch).  
        **LPIC-1 alignment:** Shell scripting

        ## Pre-flight
        - Snapshot: `LAB09-START`
        - Start terminal log (recommended):
          - `script -a ~/cyse270/logs/lab-09.log`

        ## Steps + Evidence
        ### Step 01
- Task: Create folder: mkdir -p ~/cyse270/scripts ~/cyse270/logs
- Screenshot filename: `lab-09_step-01_<shortdesc>.png`
- Prompt: Screenshot: ls -ld showing scripts/logs folders exist.

### Step 02
- Task: Create file: vim ~/cyse270/scripts/healthcheck.sh (type your script)
- Screenshot filename: `lab-09_step-02_<shortdesc>.png`
- Prompt: Screenshot: vim view showing your script contents.

### Step 03
- Task: Make executable: chmod +x ~/cyse270/scripts/healthcheck.sh
- Screenshot filename: `lab-09_step-03_<shortdesc>.png`
- Prompt: Screenshot: ls -l showing executable bit.

### Step 04
- Task: Run + capture: ~/cyse270/scripts/healthcheck.sh | tee ~/cyse270/logs/lab9-healthcheck.txt
- Screenshot filename: `lab-09_step-04_<shortdesc>.png`
- Prompt: Screenshot: output + tee confirmation.

### Step 05
- Task: Add an if-check (disk >80%) and prove it triggers (optional).
- Screenshot filename: `lab-09_step-05_<shortdesc>.png`
- Prompt: Screenshot: script output showing warning OR note explaining your test.


        ## Verification checklist
        - [ ] I completed all steps
        - [ ] Screenshots stored in `evidence/screenshots/`
        - [ ] Commands recorded in `evidence/commands.log`
        - [ ] Reflection completed in `evidence/reflection.md`

        ## Mastery rep
        - [ ] Repeat lab from memory and update reflection with what improved.
