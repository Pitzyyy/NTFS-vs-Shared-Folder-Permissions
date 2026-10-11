# File Sharing: NTFS vs Shared Folder Permissions+

## Description

A practical lab walkthrough demonstrating how to configure network file sharing, Share Permissions, and NTFS Security Permissions on Windows Server 2022. This activity illustrates the principle of combining Share and NTFS permissions to implement precise access controls based on specific organizational user roles and scenarios.

## Environment Used

- Windows Server 2022 (Domain Controller)
- Windows 10 Enterprise (Domain-Joined Client Workstation)
- VMware Workstation

## Lab walk-through

### Activity 1: Granting Read-Only Access to a Marketing Intern
### Scenario

A Marketing Intern needs access to the Marketing Team’s shared folder ("Marketing") to view content but should not modify or delete files.  

##

<p align="center">
Navigate to Local Disk (C:) on the file server and create the target shared directory named "Marketing"
  <img src="./assets/images/1.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Open folder Properties, navigate to the Sharing tab, and click "Advanced Sharing" to enable network sharing for the Marketing folder.
  <img src="./assets/images/2.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Configure Share Permissions by granting the #Marketing_Staff group Full Control / Change / Read access at the network share level.
  <img src="./assets/images/3.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Configure NTFS Security Permissions under the Security tab by granting the #Marketing_Intern <br> group Read & execute, List folder contents, and Read permissions while ensuring Write permission is unchecked.
  <img src="./assets/images/4.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

##

### Activity 2: Restricting Access to HR Department Share
### Scenario

The HR Department needs a secure folder "HRGroup" that only HR staff can access. Other employees should not see or access the folder at all.
##

<p align="center">
Access folder Properties for HRGroup and open the Sharing tab to initiate network sharing options.
  <img src="./assets/images/5.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Open Share Permissions and inspect default permissions assigned to the Everyone group.
  <img src="./assets/images/6.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
emove the Everyone group and explicitly grant Full Control, Change, and Read share permissions exclusively to the #HR_Staff security group
  <img src="./assets/images/7.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
: Configure NTFS Security Permissions under the Security tab to ensure the #HR_Staff group is <br> granted Read & execute, List folder contents, and Read access on the file system level.
  <img src="./assets/images/8.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

##

### Activity 3: Restricting Access to HR Department Share
### Scenario

The HR Department needs a secure folder "HRGroup" that only HR staff can access. Other employees should not see or access the folder at all.
##

<p align="center">
Access folder Properties for HRGroup and open the Sharing tab to initiate network sharing options.
  <img src="./assets/images/5.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Open Share Permissions and inspect default permissions assigned to the Everyone group.
  <img src="./assets/images/6.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
emove the Everyone group and explicitly grant Full Control, Change, and Read share permissions exclusively to the #HR_Staff security group
  <img src="./assets/images/7.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
: Configure NTFS Security Permissions under the Security tab to ensure the #HR_Staff group is <br> granted Read & execute, List folder contents, and Read access on the file system level.
  <img src="./assets/images/8.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>










