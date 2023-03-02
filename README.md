# Disclaimer
This Power BI Report only displays estimated charges from "Usage details" table. 

Have a look at [Data available through the connector](https://learn.microsoft.com/en-us/power-bi/connect-data/desktop-connect-azure-cost-management#data-available-through-the-connector) for a list of other tables available.

The idea for this Power BI Report is to give a quick start on how to manage your Azure usage and you can expand it by adding Reserver Instance and Marketplace charges.

# Permission

The Azure Cost Management connector uses OAuth 2.0 for authentication with Azure and identifies users who are going to use the connector. Tokens generated in this process are valid for a specific period. Power BI preserves the token for the next login. OAuth 2.0, is a standard for the process that goes on behind the scenes to ensure the secure handling of these permissions. To connect, you must use an [Enterprise Administrator](https://learn.microsoft.com/en-us/azure/billing/billing-understand-ea-roles) account for Enterprise Agreements, or have [appropriate permissions](https://learn.microsoft.com/en-us/microsoft-365/commerce/billing-and-payments/manage-billing-profiles) at the billing account or billing profile levels for Microsoft Customer Agreements.

More details at ["To connect, you must use an Enterprise Administrator account for Enterprise Agreements, or have appropriate permissions at the billing account or billing profile levels for Microsoft Customer Agreements."](https://learn.microsoft.com/en-us/power-bi/connect-data/desktop-connect-azure-cost-management#considerations-and-limitations:~:text=The%20Azure%20Cost%20Management%20connector%20uses,profile%20levels%20for%20Microsoft%20Customer%20Agreements.)

# How to Setup

You will need your Billing Account ID and permission as per section above.

For more information look the connector documentation on [Connect to an Enterprise Agreement account](https://learn.microsoft.com/en-us/power-bi/connect-data/desktop-connect-azure-cost-management)

> **Note** Data load can take a couple of minutes to several minutes, depending on data volume.

If you have any issue, please have a look at [Considerations and limitations](https://learn.microsoft.com/en-us/power-bi/connect-data/desktop-connect-azure-cost-management#considerations-and-limitations)

# Power BI Azure Consumption 
 In this Power BI report, you will be able to track your organization's Azure usage. I have developed this report using [Azure Cost Management](https://learn.microsoft.com/en-us/power-bi/connect-data/desktop-connect-azure-cost-management) connector.

See below a brief description and notes for each Report page:

- **Azure Usage Overview:** Overall view of service usage by month with month over month comparison, usage by Tag Owner, Tag Environment and Resource Group.
![Azure Usage Overview](/images/1-Azure-Usage-Overview.png)

- **Subscription Trend:** Total Subscriptions Usage, Subscriptions Usage by Month and breakdown by top 15 meter category.
![Subscription Trend](/images/2-Subscription-Trend.png)

- **Billing Detail (Drill through):** Subscription billing detail by Meter Region, Tag Owner, Meter Category and detail table.
![Billing Detail](/images/3-Billing-Details.png)

- **Usage Monthly:** Service Usage with month over month comparison by Account, Subscription, Resource Group and Product. 
> *Important: Data is skewed as some month has 30, 31 or 28/29 days.*
![Usage Monthly](/images/4-Usage-Monthly.png)

- **Usage Daily:** Service Daily Usage comparison by Account, Subscription, Resource Group and Product. 
> *Important: Please select two consecutive months for the comparison.*
![Usage Daily](/images/5-Usage-Daily.png)

- **New Services:** Analysis of new Azure Services provisioned during the selected period.
![New Services](/images/6-New-Services.png)

- **Stopped Services:** Analysis of deprovisioned or stopped Azure Services during the selected period.
![Stopped Services](/images/7-Stopped-Services.png)

- **Services < 30%:** Analysis of Azure Services with a usage reduction of 30% or more.
![Services < 30%](/images/8-Services-Less-30.png)

- **Services > 30%:** Analysis of Azure Services with a usage increase of 30% or more.
![Services > 30%](/images/9-Services-Greater-30.png)

