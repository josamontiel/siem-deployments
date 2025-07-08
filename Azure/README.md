# Azure Sentinel Deployment
### Step 1: Create a resource group
As per the [Documentation](https://learn.microsoft.com/en-us/azure/sentinel/prerequisites#dedicated-resource-group-recommended), "a dedicated resource group for your Log Analytics workspace enabled for Microsoft Sentinel. This resource group should only contain the resources that Microsoft Sentinel uses, including the Log Analytics workspace, any playbooks, workbooks, and so on."
Creating this isn the portal was pretty straight forward. 

<img width="1364" alt="Screenshot 2025-07-08 at 13 54 40" src="https://github.com/user-attachments/assets/ed057bf7-b091-4a5e-8c2a-462ec4205e8a" />

---
### **Step 2: Create a Log Analytics Workspace**

Microsoft Sentinel is built on top of a **Log Analytics Workspace**. 

1. Search for **“Log Analytics workspaces”**.
2. Click **“+ Create”**:
3. Assign values to the following:
   * **Subscription**
   * **Resource Group**
   * **Name**: Give your workspace a name (e.g., `la-test-wp-1`)
   * **Region**
4. Click **“Review + Create”**, then **“Create”**.

<img width="1568" alt="Screenshot 2025-07-08 at 13 50 28" src="https://github.com/user-attachments/assets/1880fc92-ef54-4c9d-a94f-ce0f8e373585" />

---

### **Step 3: Enable Microsoft Sentinel**

1. Go to the **Azure Portal**.
2. Search for **“Microsoft Sentinel”**.
3. Click **“+ Add”**.
4. Select the **Log Analytics Workspace** you just created.
5. Click **“Add Microsoft Sentinel”**.

---

If I had to vizualize it, it'd look something like this:

![Log Analytics Worskpace](https://github.com/user-attachments/assets/6e296347-7f93-4200-9f8a-66b819492e09)

### Step 4: ***Create a test VM to generate logs***
To do this, I asked **copilot** to create me a cheap VM. This VM is only to confirm that everything else works so I was not too focused on the config of this. I did enable RDP access so I can create my own events by using the machine.

### ***Step 5: Enable Data Connectors***

I wanted to keep this as simple and as minimal as possible because I did not want to run up a cloud bill of $20,000! I am only configuring the Windows Security Event data connector just to reinforce the learning. 
To add your own data connectors you will need to do the following:

1. From your sentinel deployment, under ```configuration```, navigate to Data Conectors
2. Go to content Hub
3. Search for for Windows Security Events
4. Select ```Open Connector page```
5. Create a new data connector rule
6. Select all logs, select the VM you created and create

A video that helped me with this was [here](https://www.youtube.com/watch?v=zqtm-od6HqQ)

And within minutes you will have logs being ingested into your SIEM

<img width="761" alt="Screenshot 2025-07-08 at 18 44 40" src="https://github.com/user-attachments/assets/57a680c8-0e3f-47c2-b90e-5a249d3fe561" />


## Tools and Helpful Links

* **KQL Query Reference**: [https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/](https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/)
* **Microsoft Sentinel Documentation**: [https://learn.microsoft.com/en-us/azure/sentinel/](https://learn.microsoft.com/en-us/azure/sentinel/)
* **Sentinel GitHub (Workbooks, Playbooks, Rules)**: [https://github.com/Azure/Azure-Sentinel](https://github.com/Azure/Azure-Sentinel)
