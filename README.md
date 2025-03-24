# DCC-SCE-files-apply-and-verify

create a new folder with your DCC SCE files
![image](https://github.com/user-attachments/assets/2a355b2c-37ee-4218-a669-4ad33c90d3ed)
- to apply them one by one in the desired install order - SCE files should start with   00_...., 01_..., 02..., etc


After usage of the PowerShell PS1 and PSMs 
![image](https://github.com/user-attachments/assets/c0f5e949-aa95-46be-a317-020e286dfa7c)


It should look like this'
![image](https://github.com/user-attachments/assets/0f0f001b-4403-46b5-9dab-d6a2a73d3450)


A logfile will be written, which will list all steps
like this    - BLUE:  the exported "Vendor Log Information"
![image](https://github.com/user-attachments/assets/d471a7b4-6b58-4253-9846-d112a52b3d9a)


Process workflow

Step 1   - Start SCE Exe  ( Extract-only ), detect if Payload or Config, Get-CCTK.EXE, Query ABIState and ABIProvState
Step 1a   - Start SCE Exe  ( Extract-only )
Step 1b   - query ExtractFolder for ABI_Payload.xml
Step 1c   - Get file filepath to CCTK.EXE ( part of SCE, available after extract)
Step 1d   - use CCTK to query current ABIState- and ABIProvState- values

Step 2a   - Start SCE Exe  ( Apply )  
Step 2b   - verify result

if an error gets detected then the script terminates immedeately
