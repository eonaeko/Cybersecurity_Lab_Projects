# Android Forensics Analysis and Reporting 

**Objective:** To analyse a provided Android forensic image and compile a formal digital investigation report 
**Tasks:**
- Conduct forensic analysis of the Android image:
**Extract and document:**
- SMS messages, call logs, contact lists
- Application usage history
- Files, images, browser history, crypto wallets, deleted content
- Generate a comprehensive Forensics Investigation Report including:
- Methodology and tools used
- Screenshots and findings
- Conclusion and professional recommendations


| **Tools used**  | **Description** |
| -------------------| --------------------- |
| 7-Zip             | This tool was used to decompress and extract the Android image used to carry out investigations and prepare it for analysis | 
| Autopsy           | This tool is a powerful open source application used in digital forensics and was utilized to conduct investigations on  the Android image to extract evidence |
| VirtualBox        |  It was used to create an isolated environment for the evaluation of the Android Image |
| Windows 10 VM     |  This is the isolated Virtual environment for the lab used for investigation and analysis |

## METHODLOGY 
This is the detailed step followed to  ensure proper evidence analysis 
- **Virtual Environment Setup**:  The virtual environment was set up on VirtualBox, leveraging the Windows 10 operating system, after which Autopsy was installed to cover digital activity.
- **Integrity Check for Android Image:** The Android image was hashed and compared to verify that the image was correctly handled and no changes were made.
- **Case Initialisation in Autopsy:** The case was launched and initialized on Autopsy by documenting the case name, case number, and the  Examiner was enabled for the structured storage of all analysis, artefacts, and logs generated during the case investigation
- **Android Image Setup:** The Android image was extracted using 7-Zip and then properly imported as a case study file on Autopsy, and it was ensured that it was properly imported to ensure proper  configuration and to preserve the integrity of the findings of the investigation
- **Forensic Examination:** The case was systematically investigated to reveal various findings that were adopted as evidence for the allegation of a scam

### Overview of analysis
1. File System Overview
- File system: Logical file
2. User Data Recovered
- Contacts: 7 contacts found
- SMS/MMS: 28 text messages recovered
-  Call Logs: 14 unique call entries
3. Web Artefacts
- Web cookies found: 207
-  Web History: 12
-  Web search: 4
4. Media Metadata (EXIF)
-  9 key images found
-  Camera app used: Android default
-   No videos found
5. Deleted Files: Nil

## Evidences and Findings 
Several pieces of evidence and findings were gathered and documented to prove that a particular suspect was guilty of an alleged financial crime. I have highlighted these findings here as follows 

### Incriminating Messages obtained from the message on the Android Phone 
<img width="1357" height="653" alt="EVIDENCE 1 message initiate " src="https://github.com/user-attachments/assets/20615af0-e8b5-4941-956b-688a50097591" />
<img width="1364" height="638" alt="EVIDENCE 2 sam reply" src="https://github.com/user-attachments/assets/84ed3c20-06ab-4662-abc0-feedc34113bb" />
<img width="1364" height="638" alt="EVIDENCE 2 sam reply" src="https://github.com/user-attachments/assets/c55e9b1d-15de-486c-afa9-4db01e228c88" />
<img width="1366" height="659" alt="EVIDENCE 3 fake website to scam" src="https://github.com/user-attachments/assets/ab0eba09-45a4-49e6-a21c-366656f551a6" />
<img width="1366" height="629" alt="EVIDENCE 4 message to foreign number" src="https://github.com/user-attachments/assets/4752a598-a70d-4385-aee2-e863a5fbd23f" />
<img width="1364" height="648" alt="EVIDENCE 5 Foreign number reply to SAM" src="https://github.com/user-attachments/assets/e9b2725f-7950-4393-b907-4f929f73cf9b" />


### Incriminating  Web Services traffic and Searches
<img width="1091" height="447" alt="EVIDENCE 6 Web History " src="https://github.com/user-attachments/assets/df7a2c5a-2498-4f56-8555-a2cf1ef8a310" />
<img width="539" height="132" alt="EVIDENCE 7 Web Search" src="https://github.com/user-attachments/assets/2338942b-2c56-4dac-8756-5e630ed7afef" />
<img width="823" height="458" alt="EVIDENCE 9 frequent call to foreign number" src="https://github.com/user-attachments/assets/a9a2131a-e36e-46ea-b817-14a3229b482e" />

### Incriminating Pictures
<img width="1353" height="650" alt="EVIDENCE 10 potential scam picture 1 " src="https://github.com/user-attachments/assets/2d50f9ad-205c-4d5b-8832-a60d909080d5" />
<img width="1361" height="640" alt="EVIDENCE 10 potential scam picture 2" src="https://github.com/user-attachments/assets/de4f39c1-3d3e-4a91-8396-3a8ed7319c27" />
<img width="1363" height="649" alt="EVIDENCE 11 lifestyle" src="https://github.com/user-attachments/assets/a1d8e912-e64e-44ee-90ac-2c7b9c42c0cf" />

### Incriminating Applications Installed 
<img width="434" height="216" alt="Installed Program evidence" src="https://github.com/user-attachments/assets/ccd7336b-5b24-4602-80c2-d4a1e7e5ee98" />

###  All Message Evidences
<img width="1001" height="458" alt="1753348977357" src="https://github.com/user-attachments/assets/d1214303-ea3f-4a98-9f88-ba89a2cda754" />
<img width="998" height="536" alt="1753348961006" src="https://github.com/user-attachments/assets/90da1da1-bb12-43d1-8f28-0626f5d8dfd5" />


## SUMMARY 
This lab was carried out to show the best ethnics by carefully doing a forensic examination of the Android Image and significantly recovering incriminating digital evidence that can be legally admissible in a court of law,  as it ensured integrity and reliable findings 
Following a thorough forensic examination of the extracted Android device image, we successfully recovered significant digital evidence that is both incriminating and suspicious.

 [View Full Report Here](https://drive.google.com/drive/folders/1_elAsBZ7zahLFZ6mzkah2WCuKSsFFgi0)
### Lessons Learnt 

This lab allowed me to explore the use of the tool ***"Autopsy"*** and act as a digital forensic investigator,  understanding the principles of **Chain of Custody**, **Evidence Integrity and Preservation**, **Data Recovery**, and **Forensic Analysis**, and develop the apt skill of **Report Writing**, **Evidence Management** 









