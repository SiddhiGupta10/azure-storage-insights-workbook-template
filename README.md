# azure-storage-insights-workbook-template

Storage insights provides comprehensive monitoring of your Azure Storage accounts by delivering a unified view of your Azure Storage services performance, capacity, and availability. You can observe storage capacity, and performance in two ways, view directly from a storage account or view from Azure Monitor to see across groups of storage accounts. 

## What it Delivers?

- **At scale perspective** showing a snapshot view of their availability based on the health of the storage service or the API operation, utilization showing total number of requests that the storage service receives, and latency showing the average time the storage service or API operation type is taking to process requests. You can also view capacity by blob, file, table, and queue.

- **Drill down analysis** of a particular storage account to help diagnose issues or perform detailed analysis by category - availability, performance, failures, and capacity. Selecting any one of those options provides an in-depth view of metrics.

- **Customizable** where you can change which metrics you want to see, modify or set thresholds that align with your limits, and save as your own workbook. Charts in the workbook can be pinned to Azure dashboard.

## How it is helpful?

- **Improved Storage Performance**: Storage Insights can help improve storage performance by providing valuable data and insights to optimize storage systems and enhance operational efficiency.
- **Resource Utilization Optimization**: Storage Insights enable you to optimize resource utilization, ensuring that storage resources are efficiently allocated and utilized to meet business needs.
- **Cost Reduction**: By using Storage Insights, you can reduce costs associated with storage by identifying inefficiencies and implementing cost-saving strategies based on data-driven insights.
- **Enhanced Security and Compliance**: Storage Insights help ensure the security and compliance of your storage environment by providing insights into data protection measures and regulatory compliance requirements

This capability can be useful in scenarios like:
- Deploying org- or domain-specific analytics reports along with resources deployments. For instance, you can deploy org-specific performance and failure workbooks for your new apps or virtual machines.
- Deploying standard reports or dashboards by using workbooks for existing resources.

## What is added and improved?

We have enhanced the capability of Storage insights by updating the default workbook to give more visual information related to detailed subscription/resource group information of storage account, blob information on count, capacity and backup, fileshare capacity utilisation at sorage level and DfS cost estimation to help monitor and optimize our storage resources effectively. Visuals are generally in the form of grid view and to fetch data metrics, and graph queries are used with merge operations on  tables.

This asset aims to provides workbook template as a valuable tool which can be intergrated in any environment, designed to provide a detailed overview of Azure Storage Accounts.

- It lets you filter the view by selecting subscription, storage account and time range.
- Number of storage account for which information is presented shown on top.
- Workbook is curated to show 10 sections, as mentioned below:
  - **Resource Group Section:** Here one can view the structural hierarchy of storage account i.e., to which resource group and subscription it belong, count of storage account under each resource group.
  - **Overview Section:** Its gives grid-view information on storage transactions with timeline, E2E and server latency, account availibilty and errors. One can easily hover and click on specific storage account from table to navigate to that resource. 
  - **Capacity Section:** This section shows the total amount of storage used for each storage data object in the account.
  - **Redundancy Zone:** Here you get to see data on to which zone, tier and account kind storage service belongs.
  - **Count By Type:** This section shows how many data objects are stored in the account in a grid view and count sumed up at subscription level.
  - **Blob Count:** This tab shows blob count information as per the choosen way - either by _Type_ or by _Tier_.
    - If Type is selected it shows blob count spiltted into ADLS, page blob and block blob.
    - If Tier is selected count of blob as per Hot, Cool, Archive and Cold tier will be shown.
  - **Blob Capacity:** Similar to Blob Count, this section also gives 2 data views - Type and Tier for same variables.  
  - **Blob Backup:** This gives grid view information backup vauly, policy, policy rule and associated storage account for type _microsoft.dataprotection/backupvaults/backupinstances_.
  - **FileShare Info** This section provides capacity utilisation information of fileshares at storage level with their count and capacity.
  - **Cost Estimation:** Here DfS cost estimation is shown.
    > Note - Few assumptions are made for the calculation. Please consider that it will not give the actual billing amount.
 
## How to deploy?

Resource owners can create and manage their workbooks programmatically via Azure Resource Manager templates (ARM templates). The workbook will be created in the desired sub/resource-group and with the content specified in the ARM templates. There are two types of workbook resources can be managed programmatically:
- [Workbook templates](https://github.com/SiddhiGupta10/azure-storage-insights-workbook-template/blob/main/workbook-template.json)
- [Workbook instances](https://github.com/SiddhiGupta10/azure-storage-insights-workbook-template/blob/main/workbook-instance.json)

These ARM templates can be deployed by using either the Azure portal, the CLI, PowerShell or pipeline. Use [sample-pipeline.yaml](https://github.com/SiddhiGupta10/azure-storage-insights-workbook-template/blob/main/sample-pipeline.yaml) for refernece.

## Pricing

There is no charge to access this feature and you will only be charged for the Azure Monitor essential features you configure or enable, as described on the [Azure Monitor pricing details](https://azure.microsoft.com/en-us/pricing/details/monitor/) page.

## What are the limitations?

- **Scope and Scale:** 
Limited to Storage Accounts: Storage Insights primarily focuses on Azure Storage accounts, therefore its not suitable for other types of storage solutions or third-party storage services. Also, the number of selected storage accounts has a limit of 200.
Data Volume: When dealing with numerous storage accounts, the analysis might take longer to complete, and there could be performance impacts.

- **Limited Customization Options:** It may not be as flexible as other specialized monitoring tools. Users might find it challenging to tailor the insights to specific needs beyond the provided metrics.

- **Latency in Data Collection:** There can be a delay in data collection and reporting, which means it might not be suitable for real-time monitoring needs.

## References
- https://learn.microsoft.com/en-us/azure/storage/common/storage-insights-overview
- https://learn.microsoft.com/en-us/azure/azure-monitor/visualize/workbooks-automate
- https://learn.microsoft.com/en-us/azure/azure-monitor/visualize/workbooks-create-workbook



