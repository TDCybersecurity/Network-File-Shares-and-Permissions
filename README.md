<h1><strong>Network File Sharing and Permissions</strong></h1>

<h2>1 Go to portal.azure.com and confirm that DC-B and Client-B are running.</h2>

![FS 1a](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/940ec209-23e5-4f95-b88b-fa74dda329cb)



<h2>2 Access DC-B\> make a RDC\> signing in as Joe\_Admin\> from mydomain.com to access Server Manager Dashboard.</h2>

![FS 2a](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/0298658b-de37-4d3e-8923-7b60a55102e0)![FS2b](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/d36abd05-25a9-4273-87d4-b15789e469f1)
![FS2c](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/2dd735a1-92ea-40c2-b292-13157bab2385)


<h2>3 RDC into Client-B as a random employee Bacek.Moju from the \_ EMPLOYEES group on mydomain.com.</h2>

![](RackMultipart20240524-1-trpzuw_html_49a7627d6e1b4c66.png) ![](RackMultipart20240524-1-trpzuw_html_213060efe5b2f52f.png)

<h2>4 On DB-B go to File Explorer\> C: Drive\> and create 3 new folders: read-access, write-access, and no-access.</h2>

![FS4a](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/d4dde5c4-5849-41bd-bbc7-280a916b8877)![FS4b](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/ba07d58d-192d-47d8-a7f6-bfd394d8bbec)


<h2>5 Set the following (Share Folder) permissions for the Domain Users Group.</h2>

| **FOLDER**| **GROUP**| **PERMISSIONS**|
| --- | --- | --- |
| read-access | **Domain Users**| **Read**|
| write-access | **Domain Users**| **Read/Write**|
| no-access | **Domain Admins**| **Read/Write**|
| accounting |


a right click on **read-access**\> Properties \> Sharing \> Share \> type in **domain users**\> Share \> Permission \> **read**\> Share \> Done

b right click on **write-access**\>Properties \> Sharing \> Share \> type in **domain users**\> Share \> Permission \> **read/write**\> Share \> Done

c right click on **no-access**\> Properties \> Sharing \> Share \> type in **domain admins**\> Share \> Permission \> **read/write**\>Share\> Done

read-access\>Properties\>Sharing\>Share\>domain users\>read-access\> read\>Share\>Done

![FS5a](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/846112ec-effb-4b39-a446-150198b2f4ef)![FS 5b](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/350348ad-c394-47ec-8ae9-587bf739cc3f)
![FS 5gg](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/3270514a-81b9-4304-ae1f-cde389f62a15)![FS 5ff](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/64f1bd7c-08a7-4b0a-a95f-b6d8394e140b)

![FS 5e](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/9c5d6d3d-3218-4290-af13-2aad58b701cd)![FS 5d](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/4714726b-f846-4f8b-bc90-ef2b11690e41)

![FS 5c](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/5a9d5cd8-fb3d-4210-a599-1d6f763cb4a6)



<h2>6 Go to Client-B and navigate to the root folder by going to Start, run,[\\DC-B](////DC-B).</h2>

Go to File Explorer Search bar and enter [\\dc-b](////dc-b) and enter \> and the folders appear.

Observe the three folders that you created: read-access, write-access, and no-access

a **read-access**\> double click to open \> you **can read** it \> you **can not write** in it

b **write-access**\> double click to open \> you **can read** it \> and you **can write** in it \> see test folder

c **no access**\> double click to open \> **Network Error Windows cannot access**[**\\dc-b\no-access**](////dc-b/no-access)

In Client-B\>Start\>Run\>\\DC-B\> 
Observe the three access foldes you created
![FS 6a](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/f412233a-f64a-423d-ba57-eafd1f554a28)![FS 6b](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/9872ac4c-1602-40a9-975d-88dba9ccfe03)

New\>Text\> This is read only, you cannot write.
![FS 6c](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/79375cb9-91d1-4449-8d6e-117a4eccb63d)![FS 6d](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/84ea38eb-acd7-406d-b54a-b9bd989b22d2)

Write access\>You have write access and can write text, observe "test" document.
![FS 6e](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/54f3b6be-2d6c-4293-b75a-3b4c6d96d585)![FS 6f](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/6bb328f6-9320-454d-ad68-48933f7dbcdb)

No access\> Generates a Network Error\> You have no access.
![FS 7h](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/00c24851-17d5-4419-b5db-eb09954745ba)

![FS 6g](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/9ce1ddc8-3451-4a5e-90c4-6025cf08ecbf)


<h2>7 Go to Active Directory DC-B and create a Security Group called ACCOUNTANTS.</h2>

- Go to Server Manager Dashboard \> Tools \> ADUC \> make a new Organizational Unit called \_SECURITY GROUPS.
- Go to mydomain.com \> Refresh \>
- Go to Security Groups \> New \> Group \> Accountants \> OK
- Go to Domain Controller **File Explorer**\> **C: Drive**\> Accounting Folder\> Properties \>Sharing\>Share\> **ACCOUNTANTS** Add
- Go to Client-B \> [\\DC-B](////DC-B) \> see the folders \> double click on accounting \> No access
- Go back to ADUC and make **Bacek.Moju** a member of the Security Groups of Accounts.
- Go to Security Groups \> Accountants \> Members \> Add\> Bacek.Moju\> Add\>Apply\>OK\>
- Go back to Client-B VM in the portal\> Refresh\> Go to folder and try to access accounting with bacek.moju
- Go to DC-B\> File Explorer \> accounting folder\>Properties\>Sharing\>Share

Have Client-B log out\> Log back in\> Access the accounting folder\>

Go to Server Manager Dashboard \> Tools \> ADUC \> make a new Organizational Unit.
![FS 7a](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/872351e8-1446-473e-9cd6-1cd669ab8b62)

Name the new Organizational Unit _SECURITY GROUPS and click OK
![fs 7b](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/49fe21e3-8ee0-4272-88fc-65f55e7cc492)

In ADUC Refresh the _SECURITY GROUPOS Organization Unit 
![FS 7c](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/70560522-af86-4a17-b7cf-0652d23a9068)

Go to Security Groups and create a new Group called ACCOUNTANTS with a Global Group Scope and Group type as Security
![FS 7e](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/4d3f1e6d-2df6-4db6-a5f6-b8aad3f4cbdc)

Go to File Explorer in the Domain Controller on the C:Drive and locate the ACCOUNTANTS Security Group
![FS 7f](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/6a14a7b8-dcfd-4d5f-bf8d-3803eb591ec9)

On Client-B enter DC-B\\ and locate the Accounting Folder and  double click.
![fs 7g](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/61d92d42-2544-407d-b95b-c15f8281a7ba)

Observe NO ACCESS Network Error Windows cannot access \\dc-b accounting.
![FS 7h](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/00c24851-17d5-4419-b5db-eb09954745ba)

Go to DC-B ADUC and make Bacek.Moju a member of the Security Groups > Accounts
![FS 7d](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/0f2b1538-d439-4589-8465-662f358029a5)


![FS 7i](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/ea2d02d2-c833-4adb-8dd1-b73937043784)

Enter Bacek.Moju as the object name to select.
![FS 7j](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/91e6fbd6-486e-4dce-a249-a4ae5d7c2508)

Observe that bacek.moju has access to the accounting folder, however, the folder is empty.
![FS 7k](https://github.com/TDCybersecurity/Network-File-Shares-and-Permissions/assets/142702123/4916f2f8-34e2-4bce-bf34-8042b0aa67b6)


<h2> Thank you for taking the time to review my Github IT project, it demonstrates my hands-on experience with File Sharing and Permissions.</h2>












