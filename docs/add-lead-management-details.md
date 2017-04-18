# Add lead management details for your add-ins in the Seller Dashboard

To get information about users who acquire your add-in, you can submit lead configuration details for your customer relationship management (CRM) system in the Seller Dashboard. 

You can use leads to follow up with customers directly to ensure that they have a successful experience with your solution. 

For customers who acquire your add-in via the Office Store or AppSource, the following details are sent to your lead management system:

>	First Name, Last Name, Email Address

## Submit lead management information to the Seller Dashboard

As part of the submission process, you will be prompted to submit lead configuration details so that you can receive lead information. On the **Lead Management** tab, choose the **I want to receive lead information from users who acquire my add-in** check box, and provide the following information.


|**Field**|**Description**|
|:-----|:-----|
|Offer Display Name|A title to annotate how the lead was generated. For example, "Contoso Business Planner Add-in".|
|Publisher Display Name|A title to represent your publisher information within the lead. For example, "Contoso Add-in Development team".|
|Lead Destination|Choose the applicable CRM or storage service from the dropdown.|

The steps to complete your lead submission process will vary based on the CRM system provider that you choose.  

>**Note:** If your CRM system provider is not listed, we recommend that you select Azure Table. Most popular CRM services can integrate with this storage service.

### Dynamics CRM Online

For Microsoft Dynamics CRM systems, you will need to provide the following information:

- **CRM Url**
- **User Name**
- **Password** 

For information about setting up a new Dynamics service for leads, see the [Appsource Dynamics documentation](https://aka.ms/leadsettingfordynamicscrm).

>**Note:** Configuring leads will need services that require the user to be an admin on your Dynamics CRM instance, and a tenant admin to create a new service account.  

### Azure Table

This process will output lead information into an Azure-hosted storage table. Click [here](https://azure.microsoft.com/en-us/free/) to get started with Azure.
You must submit a **Connection String** value to submit your lead management details. To find or generate this value, please follow these steps:

 1. Inside the Azure management portal, select the **Storage Account** the lead should be sent to.
 2. To create a new Storage account, go to Storage Account in the navbar and select Add in the top left of the header.
 3. Once you have selected the Storage account, select **Access Keys** under the Settings section.
 4. Copy the storage account key shown under **Primary Connection String**.
 5. Submit this string as the **Connection String** within **Seller Dashboard**.

### Salesforce

In order to direct your lead information to a Salesforce CRM system, you must provide an **Object Identifier** value. To find this value, please follow these steps:

 1. Within your Salesforce CRM system, navigate to **Setup**.
 2. In the Quick Find search bar, type in **“Web-to-Lead”**.
 3. Select **Create Web-to-Lead Form** on the next page. 
 4. Ignore the form on the next page and select **Generate**.
 5. Within the generated form, find the **oid value**, with the format:

		<input type=hidden name="oid" value="00XXXXXXXXXXXXX">

 6. Copy this value and submit it as the **Object Identifier** within **Seller Dashboard**.

### Marketo

In order to direct your lead information to a Marketo CRM system, you must provide **Form Id** , **Munchkin Id** and **Server Id** values. To find these values, please follow these steps:

1.	Go to **Design Studio** within Marketo.
2.	Click on **New Form**.
3.	Fill in the fields in the New Form popup.
4.	Click on **Finish** on the Field Details form. Approve and close the form.
5.	Under Form Actions, select **Embed Code**.
6.	Within the embed code, look for the following line:

	    <script>MktoFormsExample.loadForm("//app-ys11.marketo.com", "123-PQR-789", 1169);</script>

>In this example, the following values need to be extracted as such:
>|**Parameter Name**|**Example Value**|
|:-----|:-----|
|Form Id|ys11|
|Munchkin Id|123-PQR-789|
|Server Id|1169|

Submit your system's values within **Seller Dashboard**. 

### Azure Blob

This process will output lead information in a CSV format within an Azure-hosted blob. Click [here](https://azure.microsoft.com/en-us/free/) to get started with Azure.
You must submit a **Connection String** value as well as a **Container Name** value to submit your lead management details. To find or generate these values, please follow these steps:

 1. Inside the Azure management portal, select the **Storage Account** you
    want to the leads sent to.
 2. To create a new Storage account, Storage Account in the navbar and
    “Add” in the top left of the header.
 3. Once you have selected the Storage account, **Access Keys** under the
    Settings section.
 4. Copy the storage account key shown under **Primary Connection String**.
 5. Submit this string as the **Connection String** within **Seller Dashboard**.
 6. Select **Containers** under the Blob Services section for the same Storage Account.
 7. Click on the Container you wish to send the csv data to, or create anew Container.
 8. Copy the **Name** of the chosen Container.
 9. Submit this string as the **Container Name** within **Seller Dashboard**.

## Submit your lead management details

Once your form has been completed as required, choose **Next**. 

If you receive an error message, make sure that your details are correct or try again later. 

>**Note:** If your add-in is already in the Store, your lead management details will be saved regardless of whether your submission passes validation. You don't have to resubmit lead management details unless you want to update where your leads are sent to.

 

## Communication guidelines

Make sure that any correspondence you send to customers includes an option to unsubscribe from future communications. 
