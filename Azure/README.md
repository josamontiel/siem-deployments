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


#### Still to do:
- Connect Data Sources

- Install Built-In Workbooks and Analytics Rules

- Set Up Alerts and Incidents

---
## Tools and Helpful Links

* **KQL Query Reference**: [https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/](https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/)
* **Microsoft Sentinel Documentation**: [https://learn.microsoft.com/en-us/azure/sentinel/](https://learn.microsoft.com/en-us/azure/sentinel/)
* **Sentinel GitHub (Workbooks, Playbooks, Rules)**: [https://github.com/Azure/Azure-Sentinel](https://github.com/Azure/Azure-Sentinel)
