# Power BI Azure Consumption 
 In this Power BI report, you will be able to track your organization's Azure service usage. I have developed this report using [Azure Consumption Insights](https://docs.microsoft.com/en-us/power-bi/connect-data/desktop-connect-azure-consumption-insights) connector that allows you to connect to Azure Enterprise Agreement billing accounts.

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

# How to Setup

In this section, you learn how to get the data you need migrate using the Azure Enterprise Connector. You'll also find a usage details columns mapping available in the ACI (Azure Consumption Insights) API.

To successfully use the Azure Consumption Insights connector, you need access to the Azure portal Enterprise features.

To use the Azure Consumption Insights connector in Power BI Desktop:
 
1. Download and Open Power BI Template (Azure Consumption Usage.pbit)
2. Enter Number of Months (NumberOfMonths) and Azure Enrolment Number (EnrolmentNumber)

![Number of Months and Azure Enrolment Number](/images/Initial-Template-Parameters.png)

* The numberOfMonth parameter is how many months of data you want going back, from the current date. 
* You can get your enrollment number from the [Azure Enterprise Portal](https://ea.azure.com/), in the location shown in the following image:

![Azure EA Portal](/images/azure-enrolment-number.png)

3. Next, provide your Access key to connect.

![Access Key](/images/azure-consumption-insights-key.png)

* Your Access key for enrollment can be found on the [Azure Enterprise Portal](https://ea.azure.com/).

![API Access Key](/images/azure-consumption-insights-api-access-key.png)

> **Note** Data load can take a couple of minutes to several minutes, depending on data volume.