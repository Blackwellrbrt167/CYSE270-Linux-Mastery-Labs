        # LAB-02 – vi Under Pressure (Config Editing)

        **Objective:** Edit and recover safely using vi/vim, including over SSH.  
        **LPIC-1 alignment:** Text processing

        ## Pre-flight
        - Snapshot: `LAB02-START`
        - Start terminal log (recommended):
          - `script -a ~/cyse270/logs/lab-02.log`

        ## Steps + Evidence
        ### Step 01
- Task: Create a practice copy: cp /etc/hosts ~/cyse270/lab2-hosts.backup
- Screenshot filename: `lab-02_step-01_<shortdesc>.png`
- Prompt: Screenshot: ls -l showing backup file created.

### Step 02
- Task: Open with vim: vim ~/cyse270/lab2-hosts.backup
- Screenshot filename: `lab-02_step-02_<shortdesc>.png`
- Prompt: Screenshot: vim screen showing file open (top lines visible).

### Step 03
- Task: Search 'localhost' using /localhost then Enter.
- Screenshot filename: `lab-02_step-03_<shortdesc>.png`
- Prompt: Screenshot: vim showing highlighted match.

### Step 04
- Task: Insert comment at top: # CYSE270 LAB2 (use i, then Esc).
- Screenshot filename: `lab-02_step-04_<shortdesc>.png`
- Prompt: Screenshot: top of file showing comment line.

### Step 05
- Task: Save/quit :wq
- Screenshot filename: `lab-02_step-05_<shortdesc>.png`
- Prompt: Screenshot: terminal back at prompt after saving.

### Step 06
- Task: Global replace: :%s/localhost/LOCALHOST/g then :wq
- Screenshot filename: `lab-02_step-06_<shortdesc>.png`
- Prompt: Screenshot: grep output confirming LOCALHOST appears in file.

### Step 07
- Task: Recovery drill: make changes then :q! to discard.
- Screenshot filename: `lab-02_step-07_<shortdesc>.png`
- Prompt: Screenshot: terminal showing file unchanged (compare with cat).

### Step 08
- Task: Remote drill: SSH into VM and edit same file via vim over SSH.
- Screenshot filename: `lab-02_step-08_<shortdesc>.png`
- Prompt: Screenshot: host terminal showing SSH session + vim open.


        ## Verification checklist
        - [ ] I completed all steps
        - [ ] Screenshots stored in `evidence/screenshots/`
        - [ ] Commands recorded in `evidence/commands.log`
        - [ ] Reflection completed in `evidence/reflection.md`

        ## Mastery rep
        - [ ] Repeat lab from memory and update reflection with what improved.
