        # LAB-07 – Networking Without Training Wheels

        **Objective:** Diagnose network issues with Linux tools.  
        **LPIC-1 alignment:** Networking fundamentals

        ## Pre-flight
        - Snapshot: `LAB07-START`
        - Start terminal log (recommended):
          - `script -a ~/cyse270/logs/lab-07.log`

        ## Steps + Evidence
        ### Step 01
- Task: Interfaces: ip link
- Screenshot filename: `lab-07_step-01_<shortdesc>.png`
- Prompt: Screenshot: ip link output.

### Step 02
- Task: IPs: ip a
- Screenshot filename: `lab-07_step-02_<shortdesc>.png`
- Prompt: Screenshot: inet address shown.

### Step 03
- Task: Routes: ip route
- Screenshot filename: `lab-07_step-03_<shortdesc>.png`
- Prompt: Screenshot: default route line.

### Step 04
- Task: DNS config: cat /etc/resolv.conf
- Screenshot filename: `lab-07_step-04_<shortdesc>.png`
- Prompt: Screenshot: nameserver entries.

### Step 05
- Task: Ping gateway: ping -c 3 $(ip route | awk '/default/ {print $3}')
- Screenshot filename: `lab-07_step-05_<shortdesc>.png`
- Prompt: Screenshot: ping results.

### Step 06
- Task: Ping public IP: ping -c 3 1.1.1.1
- Screenshot filename: `lab-07_step-06_<shortdesc>.png`
- Prompt: Screenshot: ping results.

### Step 07
- Task: Ping domain: ping -c 3 google.com
- Screenshot filename: `lab-07_step-07_<shortdesc>.png`
- Prompt: Screenshot: ping results (DNS success).

### Step 08
- Task: Traceroute: traceroute 1.1.1.1 (install if needed)
- Screenshot filename: `lab-07_step-08_<shortdesc>.png`
- Prompt: Screenshot: traceroute first hops.

### Step 09
- Task: HTTP header test: curl -I https://example.com
- Screenshot filename: `lab-07_step-09_<shortdesc>.png`
- Prompt: Screenshot: HTTP headers displayed.


        ## Verification checklist
        - [ ] I completed all steps
        - [ ] Screenshots stored in `evidence/screenshots/`
        - [ ] Commands recorded in `evidence/commands.log`
        - [ ] Reflection completed in `evidence/reflection.md`

        ## Mastery rep
        - [ ] Repeat lab from memory and update reflection with what improved.
