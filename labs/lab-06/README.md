        # LAB-06 – Process & Log Investigation (Blue Team)

        **Objective:** Investigate services, logins, and system events.  
        **LPIC-1 alignment:** System maintenance

        ## Pre-flight
        - Snapshot: `LAB06-START`
        - Start terminal log (recommended):
          - `script -a ~/cyse270/logs/lab-06.log`

        ## Steps + Evidence
        ### Step 01
- Task: List processes: ps aux | head
- Screenshot filename: `lab-06_step-01_<shortdesc>.png`
- Prompt: Screenshot: ps output sample.

### Step 02
- Task: Find top CPU: top (q to quit)
- Screenshot filename: `lab-06_step-02_<shortdesc>.png`
- Prompt: Screenshot: top screen showing CPU/mem and top processes.

### Step 03
- Task: Listening ports: ss -tulpn
- Screenshot filename: `lab-06_step-03_<shortdesc>.png`
- Prompt: Screenshot: ss output with at least one LISTEN line.

### Step 04
- Task: Auth log tail: sudo tail -n 50 /var/log/auth.log (Ubuntu)
- Screenshot filename: `lab-06_step-04_<shortdesc>.png`
- Prompt: Screenshot: auth log lines.

### Step 05
- Task: Journal tail: sudo journalctl -n 50
- Screenshot filename: `lab-06_step-05_<shortdesc>.png`
- Prompt: Screenshot: journal lines.

### Step 06
- Task: Filter ssh: sudo journalctl -u ssh -n 50 (or sshd)
- Screenshot filename: `lab-06_step-06_<shortdesc>.png`
- Prompt: Screenshot: filtered output.

### Step 07
- Task: Create a failed login (wrong password once) and re-check logs.
- Screenshot filename: `lab-06_step-07_<shortdesc>.png`
- Prompt: Screenshot: log line showing failed authentication.

### Step 08
- Task: Write 5 bullets: what/when/from where/how fixed (in your notes).
- Screenshot filename: `lab-06_step-08_<shortdesc>.png`
- Prompt: Screenshot: your notes file (reflection.md) showing the 5 bullets.


        ## Verification checklist
        - [ ] I completed all steps
        - [ ] Screenshots stored in `evidence/screenshots/`
        - [ ] Commands recorded in `evidence/commands.log`
        - [ ] Reflection completed in `evidence/reflection.md`

        ## Mastery rep
        - [ ] Repeat lab from memory and update reflection with what improved.
