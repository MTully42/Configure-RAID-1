# Configure-RAID-1

The purpose of this repository is to show a walkthrough  of the CompTIA Security+ 701  lab Configure RAID 1

<h2>**WALKTHROUGH**</h2>

DISCLAIMER: THIS LAB PROJECT USED THE ACI LEARNING PLATFORM: ALL LABS WERE CREATED BY ACI [ITPRO] 

Task1: Configuring RAID 1 and Creating 2 unformatted Virtual Hard Disks
Summary: In this task we will walk through RAID 1 configuration by creating and initializing 2 VHD’s on a Win11 VM.
Step 1. Click on the start icon on the bottom center of the screen and type the following in the search bar. [create and format hard disk partitions]
 
Ref 1. Creating a search for VHD partitions
Step 2.
Select Create and format hard disk partitions from the search and click open. (See highlight of previous image)
Step 3.
In Disk Management select the Action menu and choose Create VHD from the dropdown menu
 
Ref2.  Action tab and VHD creation
Step4. 
In the Create and Attach Virtual Hard disk window, select Browse next to the Location field.
 
Ref3. Creating a VHD
Step 5
In the Browse Virtual Disk files window, navigate to This PC > Local Disk (C:).
 
Ref4 Navigating to Local disk
Step 6
In the Browse Virtual Disk files window, select New Folder, name it VHDs, Press enter and create the new folder VHDs
 
Ref6 Creating VHD folder on (C:)
Step 8. 
+In the Browse Virtual Disk files window, double-click on the VHDs folder.
Type the following in the File name section: VHD1 and click SAVE.
Step 9.
In the Create and Attach Virtual Hard Disk window, select GB from the dropdown menu and enter the following in the Virtual hard disk size field:
 
Ref7. Creating virtual HD size
Step 10. 
Click OK
Step 11.
Back in Disk Management click the Action Tab and follow the previous steps to create VHD2. Two uninitialized disks should be in the disk manager.
 
Ref8. Uninitilized disks shown.

Task 2 - Configure RAID 1 across the Unallocated Disks
Windows has the capability of creating software-based RAID configurations without the need for a hardware RAID controller. In this task, you will configure RAID 1 across the two VHDs that were created in Task 1.
Step 1
Click the Start charm and type the following: manage storage spaces
 
Ref9 accessing manage storage spaces
Step 2
In the Storage Spaces window, click the Create a new pool and storage space link. 
 
Ref10 Creating a storage pool
In the Create a storage space window, type the following in the Name field: RAID 1 VOL. Also, In the Create a storage space window, type the following into the Size (maximum) field: 8.74 and click Create storage space at the bottom.
 
Ref11   Creating a storage space
 
A NOTE FROM  ACI LEARNING: 
Note: In the Disk Management window, observe that Disks 2 and 3 are no longer listed, but a new Disk 4 (RAID 1 VOL) is present. This is the mirrored drive that was created. In Windows, Disks 2 and 3 are mirrored and represented by Disk 4. When data is moved to Disk 4, it is replicated to Disks 2 and 3.
FINAL STEPS:
In File Explorer, navigate to ACIHDD (D:).
In File Explorer, right-click on the Module_1_Folder and select Copy.
In File Explorer, navigate to RAID VOL 1 (E:).
In File Explorer, right-click on the screen and select Paste.
The Module_1_Folder has been replicated to the RAID 1 VOL. This is in preparation for the next exercise, establishing FIM on this folder. The copying of the folder is not required for FIM configuration. It is done in this case to link together Exercise 1 and Exercise 2 by using the RAID 1 VOL that was created for this exercise.
 
Ref12 Module Folder 1 moved from  ACIHDD (D:) to RAID 1 VOL (E:)

