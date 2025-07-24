# Android Forensics Analysis and Reporting 

**Objective:** To analyse a provided Android forensic image and compile a formal digital investigation report 

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
- **Forensic Examination:** The case was systematically investigated to reveal various findings that were adopted as evidence for the allegation of scam

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
