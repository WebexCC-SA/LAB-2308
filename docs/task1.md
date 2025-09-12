# Task 1 - Integrate Webex Contact Center with Saleforce Using the New CRM Connector



Please use the following credentials to complete the tasks:

| <!-- -->                  | <!-- -->         |
| ------------------------- | ---------------- |
| `Control Hub`             | <a href="https://admin.webex.com" target="_blank">https://admin.webex.com</a> |
| `Salesforce`   | <a href="https://login.salesforce.com" target="_blank">https://login.salesforce.com/</a> |
| `WxCC Username`       | labuser**ID**@wx1.wbx.ai     _(where **ID** is your selected pod number (01 through 10); i.e. labuser**02**@wxccciscolive2024.wbx.ai if selected pod is 2)_       |
| `WxCC Password`       | webexONE1!         |
| `Salesforce Username`       | As provided in the Walk-In Lab (WIL) Assistant portal       |
| `Salesforce Password`       | As provided in the Walk-In Lab (WIL) Assistant portal       |


!!! info "Task Objectives"
	- Define and configure the Call Center in Salesforce and add users.
	- Create a softphone layout and set screen pop preferences.
	- Add the Webex Contact Center softphone to the Salesforce Sales app.
	- Test the Webex Contact Center softphone integration in Salesforce.
 
## **Section 1 - Configure Call Center**

!!! warning "Attention"
	Please use the **Firefox** browser to access, configure, and test within the Salesforce portal.

- Navigate to Salesforce portal and log in with the credentials provided in the Walk-In Lab (WIL) Assistant portal.

!!! note
	The package for the WxCC V2 Salesforce connector is already pre-installed. In production environments, it will need to be installed manually and can be retrieved from <a href="https://login.salesforce.com/packaging/installPackage.apexp?p0=04tUl000000VK45IAG" target="_blank">this link</a>.

- Visit the Github repository to download the latest call center definition file - <a href="https://github.com/webex/webex-contact-center-crm-connectors/blob/main/salesforce/OpenCTI.callCenter-meta.xml" target="_blank">https://github.com/webex/webex-contact-center-crm-connectors/blob/main/salesforce/OpenCTI.callCenter-meta.xml</a> (click **'Download raw file button'**).


![Nav](./assets/t1s1p1.png){ width="600" }

- In the Salesforce portal, navigate to **'Feature Settings > Service > Call Center > Call Centers'** (or type _Call Centers_ in the search bar above the left-hand menu).
- Click **'Import'**, choose the call center definition file (downloaded earlier) and click **'Import'** again.

![Nav](./assets/t1s1p1b.png){ width="800" }
![Nav](./assets/t1s1p3.png){ width="500" }

- After the call center definition file is imported, edit it by clicking **'Edit'**.
- Change **'WxCC Region'** to **'us1'**.

!!! note
	The region defined here should match your Webex Contact Center region (i.e. ca1, anz1, eu1 etc.).

![Nav](./assets/t1s1p4.png){ width="600" }

- Click **'Save'**.
- Add users to the Call Center:
	- Click **'Manage Call Center Users'** at the bottom of the page and then **'Add More Users'**.
	- Click **'Find'**, select the user in use (_User, User_), and click **'Add to Call Center'**.

![Nav](./assets/t1s1p5.png){ width="500" }
![Nav](./assets/t1s1p7.png){ width="800" }



## **Section 2 - Configure Softphone Layout**

- Navigate to **'Feature Settings > Service > Call Center > Softphone Layouts'** (or type _Softphone Layouts_ in the search bar above the left-hand menu).
- Click **'New'**.

![Nav](./assets/t1s1p8.png){ width="800" }

- Provide a name for the **'Softphone Layout'** (e.g., _WxCC layout_).
- Select the **'Is Default Layout'** checkbox.
- Under **'Display these salesforce.com objects'**, add **'Case'**.

![Nav](./assets/t1s1p9.png){ width="600" }

- Under **'Screen Pop Settings'**, expand **'No matching records'**, select **'Pop to new'**, and choose **'Contact'**.

![Nav](./assets/t1s1p10.png){ width="800" }

!!! note
	Other Salesforce objects can be selected here as well. **'Contact'** is used as an example in this exercise. 

- Click **'Save'** at the top.



## **Section 3 - Configure CTI Softphone**

- Navigate to **'Apps > App Manager'** (or type _App Manager_ in the search bar above the left-hand menu).
- For the **'Sales'** app (line number 17; **'LightningSales'** developer) click **'Edit'** on the right-hand side.

![Nav](./assets/t1s1p11.png){ width="800" }

- In the next window, select **'Utility Items (Desktop Only)'**.
- Click **'Add Utility item'** and choose **'Open CTI Softphone'**.

![Nav](./assets/t1s1p12.png){ width="600" }

- Click **'Save'** and return to the previous page by clicking the back arrow icon at the top left corner.



## **Section 4 - Testing**

!!! warning "Attention"
	Please use the **Firefox** browser to access, configure, and test within the Salesforce portal.

- Click on the **'App Launcher'** icon (top left).
- Search for _Sales_ and click on the **'Sales'** option.

![Nav](./assets/t1s2p1.png){ width="400" }

- Open the Webex Contact Center phone widget (bottom left) and login to Webex Contact Center Agent Desktop using the selected Webex Contact Center user credentials (e.g., _labuserID@wxccciscolive2024.wbx.ai_):
  	- For the phone number, select **'Extension'** and enter the extension in the format 10**NN** (where **'NN'** is your lab user number, e.g., _labuser**01**@wxccciscolive2024.wbx.ai_)':
	- For the team use **AITeamN** (where **'N'** is your lab user number, e.g., _labuser0**1**@wxccciscolive2024.wbx.ai_)'.

![Nav](./assets/t1s2p2.png){ width="333" }
![Nav](./assets/t1s2p3a.png){ width="326" }
![Nav](./assets/t1s2p4.png){ width="333" }

- Congratulations! You have complete the task.
