        # LAB-10 – Automation & Cron (Proof of Execution)

        **Objective:** Schedule tasks, verify execution, clean up responsibly.  
        **LPIC-1 alignment:** Job scheduling

        ## Pre-flight
        - Snapshot: `LAB10-START`
        - Start terminal log (recommended):
          - `script -a ~/cyse270/logs/lab-10.log`

        ## Steps + Evidence
        ### Step 01
- Task: Create script: echo 'date >> ~/cyse270/logs/cronproof.txt' > ~/cyse270/scripts/cronproof.sh
- Screenshot filename: `lab-10_step-01_<shortdesc>.png`
- Prompt: Screenshot: cat cronproof.sh output.

### Step 02
- Task: Add shebang + exec bit: sed -i '1i #!/bin/bash' ~/cyse270/scripts/cronproof.sh ; chmod +x ~/cyse270/scripts/cronproof.sh
- Screenshot filename: `lab-10_step-02_<shortdesc>.png`
- Prompt: Screenshot: head -n 2 showing shebang + command.

### Step 03
- Task: Edit cron: crontab -e ; add '* * * * * ~/cyse270/scripts/cronproof.sh'
- Screenshot filename: `lab-10_step-03_<shortdesc>.png`
- Prompt: Screenshot: crontab -l showing the entry.

### Step 04
- Task: Wait 2–3 minutes then tail log: tail -n 5 ~/cyse270/logs/cronproof.txt
- Screenshot filename: `lab-10_step-04_<shortdesc>.png`
- Prompt: Screenshot: timestamps proving execution.

### Step 05
- Task: Remove the cron job and confirm crontab -l is clean.
- Screenshot filename: `lab-10_step-05_<shortdesc>.png`
- Prompt: Screenshot: crontab -l showing removed entry.


        ## Verification checklist
        - [ ] I completed all steps
        - [ ] Screenshots stored in `evidence/screenshots/`
        - [ ] Commands recorded in `evidence/commands.log`
        - [ ] Reflection completed in `evidence/reflection.md`

        ## Mastery rep
        - [ ] Repeat lab from memory and update reflection with what improved.
