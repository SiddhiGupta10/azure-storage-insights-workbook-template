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
  
## What is added and improved?
We have enhanced the capability of Storage insights by updating the default workbook to give more visual information related to detailed subscription/resource group information of storage account, blob information on count, capacity and backup, fileshare capacity utilisation at sorage level and DfS cost estimation to help monitor and optimize our storage resources effectively. This asset aims to provides workbook template as a valuable tool which can be intergrated in any environment, designed to provide a detailed overview of Azure Storage Accounts.

- It lets you filter the view by selecting subscription, storage account and time range.
- Number of storage account for which information is presented shown on top.
- Workbook is curated to show 10 sections, as mentioned below:
  - **Resource Group Section:** Here one can view the structural hierarchy of storage account i.e., to which resource group and subscription it belong, count of storage account under each resource group.
  - **Overview Section:** Its gives grid-view information on storage transactions with timeline, E2E and server latency, account availibilty and errors. One can easily hover and click on specific storage account from table to navigate to that resource. 
  - **Capacity Section:** This section provides
  - **Count By Type:**
  - **Blob Count:**
  - **Blob Capacity:**
  - **Blob Backup:**
  - **FileShare Info**
  - **Cost Estimation:**
 
## How to deploy?

## References
- https://learn.microsoft.com/en-us/azure/storage/common/storage-insights-overview
- https://learn.microsoft.com/en-us/azure/azure-monitor/visualize/workbooks-automate



