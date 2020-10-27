Azure EA Billing Summary by Resource Group
==========================================

            

**Azure EA Billing Summary by Resource Group**

NB: this is suitable for Enterprise customers only


 


The Script provides a way to select a Billing Period from your Azure EA Subscriptions.


The Billing Period Defaults to a one month period.


You can then query the Azure EA Billing API for the Resource usage details for that billing period.


This provides all costs for all resources within the EA enrollment.


**The inputs for this script are the:**


**- The Subscription Name to look up the Billing Period**


**- EA Enrollment Number**


**- EA Access Key**


The inputs are saved in a CSV file, to ensure the Access key is not in the script/function.

E.g. D:\azure\billing.csv

Subscription,EnrollmentNo,AccessKey
API-PRODUCTION-APP,123456,asdfqwerlkjhpoiu12sd3456


Information on retrieving these are documented here:


https://docs.microsoft.com/en-us/power-bi/desktop-connect-azure-consumption-insights#connect-to-azure-consumption-insights



** *** *


The main purpose of this Script is to provide a summary of the Cost [per given billing period], broken down per Resource Group.


The Output will be a summary as below, for
**ALL resource groups for that given billing month.**


CostCenter        : 123456
subscriptionName  : API-PRODUCTION-APP
resourcegroup     : AZE2-P02-API
accountName       : Jennifer Holland
accountOwnerEmail : jennifer.holland@contoso.com
departmentId      : 54327
TotalCost         : $5,094.68


The script provides a way to filter the results to search for the total monthly cost for 1 or more Resource Groups (Based on a Search String)


E.g. find all resource groups that have the word PROD in the name . . .


Get-AzureBillingMonthlySummary -usage $usage
**-filter PROD**


 

 





        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
