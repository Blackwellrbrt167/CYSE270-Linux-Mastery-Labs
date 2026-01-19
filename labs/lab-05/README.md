        # LAB-05 – Filesystems & Mounts (Loop Device)

        **Objective:** Create storage, format it, mount it, persist it.  
        **LPIC-1 alignment:** Storage management

        ## Pre-flight
        - Snapshot: `LAB05-START`
        - Start terminal log (recommended):
          - `script -a ~/cyse270/logs/lab-05.log`

        ## Steps + Evidence
        ### Step 01
- Task: Create disk file: dd if=/dev/zero of=~/cyse270/lab5.disk bs=1M count=200
- Screenshot filename: `lab-05_step-01_<shortdesc>.png`
- Prompt: Screenshot: dd output summary.

### Step 02
- Task: Attach loop: sudo losetup -fP ~/cyse270/lab5.disk
- Screenshot filename: `lab-05_step-02_<shortdesc>.png`
- Prompt: Screenshot: sudo losetup -a | grep lab5.disk output with /dev/loopX.

### Step 03
- Task: Format: sudo mkfs.ext4 /dev/loopX
- Screenshot filename: `lab-05_step-03_<shortdesc>.png`
- Prompt: Screenshot: mkfs.ext4 completion output.

### Step 04
- Task: Mount point: sudo mkdir -p /mnt/lab5
- Screenshot filename: `lab-05_step-04_<shortdesc>.png`
- Prompt: Screenshot: ls -ld /mnt/lab5 output.

### Step 05
- Task: Mount: sudo mount /dev/loopX /mnt/lab5
- Screenshot filename: `lab-05_step-05_<shortdesc>.png`
- Prompt: Screenshot: mount | grep /mnt/lab5 output.

### Step 06
- Task: Test write: sudo touch /mnt/lab5/hello.txt ; ls -l /mnt/lab5
- Screenshot filename: `lab-05_step-06_<shortdesc>.png`
- Prompt: Screenshot: listing showing hello.txt.

### Step 07
- Task: Get UUID: sudo blkid /dev/loopX
- Screenshot filename: `lab-05_step-07_<shortdesc>.png`
- Prompt: Screenshot: blkid output with UUID.

### Step 08
- Task: Backup + edit fstab: sudo cp /etc/fstab /etc/fstab.bak ; sudo vim /etc/fstab (add UUID line)
- Screenshot filename: `lab-05_step-08_<shortdesc>.png`
- Prompt: Screenshot: /etc/fstab snippet showing your added line (be careful).

### Step 09
- Task: Test: sudo umount /mnt/lab5 ; sudo mount -a ; mount | grep lab5
- Screenshot filename: `lab-05_step-09_<shortdesc>.png`
- Prompt: Screenshot: mount -a success + mount output confirming mounted.


        ## Verification checklist
        - [ ] I completed all steps
        - [ ] Screenshots stored in `evidence/screenshots/`
        - [ ] Commands recorded in `evidence/commands.log`
        - [ ] Reflection completed in `evidence/reflection.md`

        ## Mastery rep
        - [ ] Repeat lab from memory and update reflection with what improved.
