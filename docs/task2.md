# Task 2 - Integrate Saleforce Connector with WebRTC



Please use the following credentials to complete the tasks:

| <!-- -->                  | <!-- -->         |
| ------------------------- | ---------------- |
| `Control Hub`             | <a href="https://admin.webex.com" target="_blank">https://admin.webex.com</a> |
| `Salesforce`   | <a href="https://login.salesforce.com" target="_blank">https://login.salesforce.com/</a> |
| `WxCC Username`       | labuser**ID**@wx1.wbx.ai     _(where **ID** is your selected pod number (01 through 10); i.e. labuser**02**@wxccciscolive2024.wbx.ai if selected pod is 2)_       |
| `WxCC Password`       | webexONE1!         |
| `Salesforce Username`       | As provided by the instructor       |
| `Salesforce Password`       | As provided by the instructor       |


!!! info "Task Objectives"
	- Login with WebRTC on Salesforce.
	- Troubleshoot and configure the steps needed to enable WebRTC login

 
## **Section 1 - Login with WebRTC Option**

!!! warning "Attention"
	Please use the **Firefox** browser to access, configure, and test within the Salesforce portal.

- Navigate to Agent Desktop and select the Avatar on the top right

![Nav](./assets/task2/1.png){ width="300" }

- Navigate to **'Profile Settings > Desktop > Save'** (or type _Call Centers_ in the search bar above the left-hand menu).

![Nav](./assets/task2/2.png){ width="300" }

![Nav](./assets/task2/3.png){ width="300" }

![Nav](./assets/task2/4.png){ width="300" }

- Once the Save button is hit, the error message pops up "WebRTC domain is not configured" 

![Nav](./assets/task2/5.png){ width="300" }


- In order to mitigate this issue, on the Salesforce portal, navigate to 'Feature Settings > Service > Call Center > Call Centers' (or type Call Centers in the search bar above the left-hand menu).
- Click 'Edit' on the the call center definition file `WxCC Call Center`
  
![Nav](./assets/task2/6.png){ width="300" }

- Enter **'rtw.prod-us1.rtmsprod.net'** in the **'WxCC WebRTC Domain'**

![Nav](./assets/task2/7.png){ width="300" }

- Click **'Save'**.
  
- Logout and log back in to salesforce.

![Nav](./assets/task2/8.png){ width="300" }

- Open the Webex Contact Center phone widget (bottom left) and login to Webex Contact Center Agent Desktop using the selected Webex Contact Center user credentials (e.g., _labuserID@wxccciscolive2024.wbx.ai_):
- Enable the microphone option as show below. 
![Nav](./assets/task2/9.png)){ width="200" }
![Nav](./assets/task2/10.png)){ width="200" }


- Congratulations! You have complete the task.




