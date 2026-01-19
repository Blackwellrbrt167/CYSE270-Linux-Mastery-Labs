        # LAB-01 – Command Line Muscle Memory

        **Objective:** Build CLI speed: navigation, search, pipes, redirection.  
        **LPIC-1 alignment:** GNU & Unix commands

        ## Pre-flight
        - Snapshot: `LAB01-START`
        - Start terminal log (recommended):
          - `script -a ~/cyse270/logs/lab-01.log`

        ## Steps + Evidence
        ### Step 01
- Task: Create sandbox: mkdir -p ~/cyse270/lab1/{in,out,tmp}
- Screenshot filename: `lab-01_step-01_<shortdesc>.png`
- Prompt: Screenshot: terminal showing directory tree created (use: tree ~/cyse270/lab1).

### Step 02
- Task: Create file: printf 'alpha\nbeta\ngamma\n' > ~/cyse270/lab1/in/words.txt
- Screenshot filename: `lab-01_step-02_<shortdesc>.png`
- Prompt: Screenshot: cat words.txt output.

### Step 03
- Task: Copy: cp .../words.txt .../words-copy.txt
- Screenshot filename: `lab-01_step-03_<shortdesc>.png`
- Prompt: Screenshot: ls -l showing both files.

### Step 04
- Task: Search: grep -n 'beta' .../words.txt
- Screenshot filename: `lab-01_step-04_<shortdesc>.png`
- Prompt: Screenshot: grep output with line number.

### Step 05
- Task: Count: wc -l .../words.txt
- Screenshot filename: `lab-01_step-05_<shortdesc>.png`
- Prompt: Screenshot: wc output.

### Step 06
- Task: Pipe + tee: cat words.txt | tr a-z A-Z | tee .../WORDS_UPPER.txt
- Screenshot filename: `lab-01_step-06_<shortdesc>.png`
- Prompt: Screenshot: command run + resulting output.

### Step 07
- Task: Recursive search: grep -R 'GAMMA' ~/cyse270/lab1
- Screenshot filename: `lab-01_step-07_<shortdesc>.png`
- Prompt: Screenshot: grep -R results pointing to WORDS_UPPER.txt.

### Step 08
- Task: Archive: tar -czf .../lab1.tgz -C ~/cyse270/lab1 .
- Screenshot filename: `lab-01_step-08_<shortdesc>.png`
- Prompt: Screenshot: ls -lh showing lab1.tgz size.

### Step 09
- Task: List archive: tar -tzf .../lab1.tgz | head
- Screenshot filename: `lab-01_step-09_<shortdesc>.png`
- Prompt: Screenshot: tar list output.

### Step 10
- Task: Cleanup tmp: rm -rf ~/cyse270/lab1/tmp/*
- Screenshot filename: `lab-01_step-10_<shortdesc>.png`
- Prompt: Screenshot: ls of tmp folder showing it's empty.


        ## Verification checklist
        - [ ] I completed all steps
        - [ ] Screenshots stored in `evidence/screenshots/`
        - [ ] Commands recorded in `evidence/commands.log`
        - [ ] Reflection completed in `evidence/reflection.md`

        ## Mastery rep
        - [ ] Repeat lab from memory and update reflection with what improved.
