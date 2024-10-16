# Azure Data Lake Storage Setup

This guide provides a step-by-step process for setting up Azure Data Lake Storage, from creating a resource group to uploading files and managing access controls.

---

## Step 1: Create a Resource Group

A **Resource Group** helps manage your Azure resources efficiently. To create a resource group:

1. Go to the **Azure Portal**.
2. Navigate to **Resource Groups**.
3. Select **+ Create** to create a new resource group.
4. Name your resource group and choose the region that suits your needs.
5. Click **Review + Create** and then **Create**.

---

## Step 2: Create a Storage Account

Now, you need to create a **Storage Account** that will serve as your Azure Data Lake.

1. Go to the **Azure Portal** and search for **Storage Accounts**.
2. Select **+ Create** to create a new storage account.
3. Fill in the details:
   - **Resource Group**: Select the resource group you created.
   - **Storage Account Name**: Use only lowercase letters and numbers.
   - **Region**: Choose your preferred region.
   - **Performance**: Select your desired performance tier.
   - **Replication**: Choose your replication option.

4. In the **Advanced** section:
   - Enable **Hierarchical Namespaces** to activate Data Lake Storage Gen2 features.

5. For the **Networking**, **Data Protection**, **Encryption**, and **Tags** sections, keep the default settings.

6. Click **Review + Create** and then **Create** to deploy your storage account.

---

## Step 3: Create a Container and Upload Data

### Create a Container

Once the storage account is deployed:

1. Navigate to your storage account.
2. Under **Data Storage**, select **Containers**.
3. Click **+ Container** to create a new container.
   - Name your container (use lowercase letters and numbers).
   - Click **Create**.

### Upload Files

1. Navigate to the container you just created.
2. Click **Upload** to add your data files from your local machine.
3. After uploading, the files will appear in the container.

### Create Directories

To structure your data:

1. Click **+ Add Directory** next to the **Upload** button.
2. Name the directory, and it will appear in your container.

---

## Step 4: Manage Data Tiers

You can assign your data to different **storage tiers** based on access frequency and cost:

| Tier      | Use Case                         | Access Frequency    | Retrieval Time | Cost       | Minimum Retention |
|-----------|----------------------------------|---------------------|----------------|------------|-------------------|
| **Hot**   | Frequently accessed data         | Frequent            | Immediate      | Very High  | N/A               |
| **Cool**  | Less frequently accessed data    | Less Frequent       | Immediate      | High       | 30 days           |
| **Cold**  | Rarely accessed data             | Rare                | Immediate      | Cheap      | 90 days           |
| **Archive** | Data for long-term storage     | Very Rare           | Hours          | Very Cheap | 180 days          |

You can change the data tier by selecting a file and adjusting its properties.

---

## Step 5: Configure Access Control (ACL)

To manage permissions for users and applications, you can configure **Access Control Lists (ACLs)**:

1. Go to the **Settings** section of your storage account.
2. Select **Manage ACL**.
3. Assign appropriate permissions to users or applications.

---

## Optional: Use Azure Storage Explorer

You can also manage your Data Lake using **Azure Storage Explorer**:

1. Download and install **Azure Storage Explorer** on your local machine.
2. Connect it to your Azure subscription.
3. Use it to create containers, upload data, and manage directories, similar to the steps outlined above.

---

## Conclusion

By following these steps, you have successfully set up Azure Data Lake Storage, created containers, uploaded data, and configured access controls. You now have a scalable and efficient data storage system ready for use in Azure.
