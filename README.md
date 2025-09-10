# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details
<img width="1920" height="1080" alt="Screenshot 2025-08-29 091734" src="https://github.com/user-attachments/assets/1479d651-c440-4470-8c40-ca62e7a2f17b" />
<img width="1920" height="1080" alt="Screenshot 2025-09-04 120250" src="https://github.com/user-attachments/assets/46d32875-6dda-4b7d-b894-a44bf028aefa" />
<img width="1920" height="1080" alt="Screenshot 2025-09-04 120618" src="https://github.com/user-attachments/assets/7b2ebc72-be69-4d49-a469-eb450094100c" />


<img width="1920" height="1080" alt="Screenshot 2025-08-29 092438" src="https://github.com/user-attachments/assets/2bba11ed-c7bc-4b9b-b9d6-14ffca4aba26" />
<img width="1920" height="1080" alt="Screenshot 2025-09-04 120720" src="https://github.com/user-attachments/assets/cbdfcbc9-2b96-42a5-a870-74f6817f3518" />

<img width="1920" height="1080" alt="Screenshot 2025-08-29 093320" src="https://github.com/user-attachments/assets/fcc88f87-c6ef-496f-9bc1-9987a1b45f81" />
<img width="919" height="670" alt="Screenshot 2025-08-29 093522" src="https://github.com/user-attachments/assets/56b6e4da-4208-4258-b92a-b4ff711d7ad0" />

<img width="1920" height="1080" alt="Screenshot 2025-08-29 093652" src="https://github.com/user-attachments/assets/3ff6928c-e08f-428f-a499-741e0ecd1d77" />
<img width="1920" height="1080" alt="Screenshot 2025-08-29 093712" src="https://github.com/user-attachments/assets/898b3375-c4a8-4fd3-aa8b-071e85ba9d8b" />
<img width="1920" height="1080" alt="Screenshot 2025-08-29 093722" src="https://github.com/user-attachments/assets/c9eca91d-8ee4-441f-b3e7-84ecf4173fb7" />











## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
