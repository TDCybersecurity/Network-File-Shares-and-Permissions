**CC Lab 7 Network Files Shares and Permissions**

1 Go to **portal.azure.com** and confirm that **DC-B** and **Client-B** are running.

![](RackMultipart20240524-1-trpzuw_html_f2a3ef845e2df67.png)

2 Access **DC-B**\> make a **RDC**\> signing in a **Joe\_Admin**\> from **mydomain.com** to access **Server Manager Dashboard.**

![](RackMultipart20240524-1-trpzuw_html_2483773d757ddf75.png) ![](RackMultipart20240524-1-trpzuw_html_686e5b03a89a6c83.png)

![](RackMultipart20240524-1-trpzuw_html_e2542f62fc894979.png)

3 **RDC** into **Client-B** as a random employee **Bacek.Moju** from the \_ **EMPLOYEES** group on **mydomain.com**.

![](RackMultipart20240524-1-trpzuw_html_49a7627d6e1b4c66.png) ![](RackMultipart20240524-1-trpzuw_html_213060efe5b2f52f.png)

4 On **DB-B** go to **File Explorer**\> **C: Drive**\> and create 3 new folders: **read-access**, **write-access**, and **no-access**.

![](RackMultipart20240524-1-trpzuw_html_9f8cacd49317ec32.png) ![](RackMultipart20240524-1-trpzuw_html_12c15072202bc99a.png)

5 Set the following (Share Folder) **permissions** for the **Domain Users** Group.

| **FOLDER**| **GROUP**| **PERMISSIONS**|
| --- | --- | --- |
| read-access | **Domain Users**| **Read**|
| write-access | **Domain Users**| **Read/Write**|
| no-access | **Domain Admins**| **Read/Write**|
| accounting |
 |
 |

a right click on **read-access**\> Properties \> Sharing \> Share \> type in **domain users**\> Share \> Permission \> **read**\> Share \> Done

b right click on **write-access**\>Properties \> Sharing \> Share \> type in **domain users**\> Share \> Permission \> **read/write**\> Share \> Done

c right click on **no-access**\> Properties \> Sharing \> Share \> type in **domain admins**\> Share \> Permission \> **read/write**\>Share\> Done

read-access\>Properties\>Sharing\>Share\>domain users\>read-access\> read\>Share\>Done

![](RackMultipart20240524-1-trpzuw_html_ed9884895c0ea5a7.png) ![](RackMultipart20240524-1-trpzuw_html_dba692d1829f2e6d.png)

![](RackMultipart20240524-1-trpzuw_html_f0ee9174f970d6b8.png) ![](RackMultipart20240524-1-trpzuw_html_c7dd735e4a5e8008.png)

![](RackMultipart20240524-1-trpzuw_html_da6dc25513224f6a.png) ![](RackMultipart20240524-1-trpzuw_html_7dfb23deea6f1606.png)

![](RackMultipart20240524-1-trpzuw_html_d4ec069b90038a55.png)

6 Go to **Client-B** and navigate to the **root folder** by going to **Start, run,**[**\\DC-B**](////DC-B) **.**

Go to File Explorer Search bar and enter [\\dc-b](////dc-b) and enter \> and the folders appear.

Observe the three folders that you created: read-access, write-access, and no-access

a **read-access**\> double click to open \> you **can read** it \> you **can not write** in it

b **write-access**\> double click to open \> you **can read** it \> and you **can write** in it \> see test folder

c **no access**\> double click to open \> **Network Error Windows cannot access**[**\\dc-b\no-access**](////dc-b/no-access)

In Client-B\>Start\>Run\>\\DC-B\> Observe the three access foldes you created

![](RackMultipart20240524-1-trpzuw_html_48cc9108e0556b6e.png) ![](RackMultipart20240524-1-trpzuw_html_c25a8e4b34decfce.png)

New\>Text\> This is read only, you cannot write.

![](RackMultipart20240524-1-trpzuw_html_b55227f5c33b07c5.png) ![](RackMultipart20240524-1-trpzuw_html_6e420a74edd6f5d0.png)

Write access\>You have write access and can write text, observe "test" document.

![](RackMultipart20240524-1-trpzuw_html_36e70b395f525d17.png) ![](RackMultipart20240524-1-trpzuw_html_484ac86ffc686900.png)

No access\> Generates a Network Error\> You have no access.

![](RackMultipart20240524-1-trpzuw_html_6211ee80d2d4eb01.png)

**7 Go to Active Directory DC-B and create a Security Group called ACCOUNTANTS.**

- Go to Server Manager Dashboard \> Tools \> ADUC \> make a new Organizational Unit called \_SECURITY GROUPS.
- Go to mydomain.com \> Refresh \>
- Go to Security Groups \> New \> Group \> Accountants \> OK
- Go to Domain Controller **File Explorer**\> **C: Drive**\> Accounting Folder\> Properties \>Sharing\>Share\> **ACCOUNTANTS** Add
- Go to Client-B \> [\\DC-B](////DC-B) \> see the folders \> double click on accounting \> No access
- Go back to ADUC and make **Bacek.Moju** a member of make him a member of the Accounts Security Group.
- Go to Security Groups \> Accountants \> Members \> Add\> Bacek.Moju\> Add\>Apply\>OK\>
- Go back to Client-B VM in the portal\> Refresh\> Go to folder and try to access accounting with bacek.moju
- Go to DC-B\> File Explorer \> accounting folder\>Properties\>Sharing\>Share

Have Client-B log out\> Log back in\> Access the accounting folder\>

Go to Server Manager Dashboard \> Tools \> ADUC \> make a new Organizational Unit called \_SECURITY GROUPS.

![](RackMultipart20240524-1-trpzuw_html_8a320a9bdef33d9f.png) ![](RackMultipart20240524-1-trpzuw_html_a03b776a76ae8c58.png) ![](RackMultipart20240524-1-trpzuw_html_378982f4c5aa4173.png)

![](RackMultipart20240524-1-trpzuw_html_83072c095f5c8a93.png) ![](RackMultipart20240524-1-trpzuw_html_f02fc26057eea635.png)

![](RackMultipart20240524-1-trpzuw_html_5a7181cddb588549.png) ![](RackMultipart20240524-1-trpzuw_html_5a7181cddb588549.png)

![](RackMultipart20240524-1-trpzuw_html_9f491c4f18a6be57.png) ![](RackMultipart20240524-1-trpzuw_html_127fd5eda7686b09.png)

![](RackMultipart20240524-1-trpzuw_html_738279b28ac4505e.png) ![](RackMultipart20240524-1-trpzuw_html_86d78e8ae5c505e.png)

![](RackMultipart20240524-1-trpzuw_html_de9a757a3a18e42d.png)
