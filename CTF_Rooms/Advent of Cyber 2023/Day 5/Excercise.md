## Scenario
The backup tapes are corrupted. They can only be restored using a special program, which can only run in MS-DOS. Explore AntarctiCrafts’ legacy systems and restore the files!

## Requirements
- Start the Machine
- Connect with TryHackMe’s VPN or Start the Attackbox
- After the Machine starts, Connect with the Remote Machine
- If you are on Windows, use Remote Desktop Connection else use rdpclient

## Day 5 — Tasks Answers

### 1. How large (in bytes) is the AC2023.BAK file?
- Open the Dos Application
- Type Dir and you’ll able to see the Size of the File
  
`Ans: 12,704`


### 2. What is the name of the backup program?

- Navigate to /TOOLS/BACKUP/and Type EDIT README.TXT
- Read the File and you’ll able to see the Backup program name

`Ans: BackupMaster3000`

### 3. What should the correct bytes be in the backup’s file signature to restore the backup properly?

`Ans: 41 43`

### 4. What is the flag after restoring the backup successfully?

- Type EDIT AC2023.BAK
- Change the X X to 41 43, Click Alt+F and Click save
- Now, Type C:\TOOLS\BACKUP\BUMASTER.EXE AC2023.BAK

`Ans: THM{0LD_5CH00L_C00L_d00D}`
