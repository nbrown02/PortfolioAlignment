# Portfolio Alignment for Azure DevOps and Jira (Cloud)
Understand how much of a team's backlog links all the way to the top-level portfolio in your organisation.

### What is this report? 
This will detail the percentage of alignment a teams backlog has with the overall 'top-level' portfolio in your organisation. Use it to understand just how much of a teams effort is being placed on the top priorities and/or if they should be saying no to work that is not aligned.

### Why would you use it? 
Understand how much of a team's work contributes towards the highest priority/big picture for the organisation. Help teams understand the 'purpose' in their work.

### When would you use it?
You can use the report page on a forntightly/monthly basis. Use it to keep a handle on the backlog and what can be removed as it is no longer aligned with organisational priorities.

### Prerequisites
* Your team needs to have the following practices in place:
  - For Jira, you use a 3-level hierarchy of Story > Epic > Whatever you call the third level
  - For ADO, you use a 4-level hierarchy of PBI > Feature > Epic > Whatever you call the fourth level
* Download the appropriate template file:
  - [Azure DevOps / Azure DevOps Server / TFS version](https://github.com/nbrown02/PortfolioAlignment/raw/refs/heads/main/Portfolio%20Alignment%20(ADO).pbit)
  - [Jira version](https://github.com/nbrown02/PortfolioAlignment/raw/refs/heads/main/Portfolio%20Alignment%20(Jira).pbit) 
* Create/save an access token 
  - [Personal Access Token (PAT) if using Azure DevOps (make sure you have 'Read' Analytics access)](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=Windows)
  - [Jira API token if using Jira](https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account/)
* Then you're good to get started!

### Connectivity (Azure DevOps Version)
* Open the .pbit file in Power BI Desktop
* Select http/https (only choose http if your Azure DevOps Server is HTTP)
* Add the Analytics / Azure DevOps Server URL - for Azure DevOps services enter 'analytics.dev.azure.com' / for Azure DevOps Server enter your server details
* Add your organization, project name for each backlog level, the name of the work item type you use above Epic and the team name

Don't confuse the team name with the project name, a common mistake. If the URL you use is "http://dev.azure.com/Microsoft-UK/AzureDevOpsTeam/Database", then Microsoft-UK is the Organization Name, AzureDevOpsTeam is the Project name, Database is the team name.

* It should then look something like this:

<img width="500" alt="image" src="https://github.com/user-attachments/assets/fd0057c9-3d9a-4159-b17f-9ddbcf117961" />

* Hit 'Load' 
* You will be prompted for a login, choose Basic and enter:
  - Your PAT you created in the Prerequisites in the password field
  - Leave the username as blank or enter 'Dummy'
  
<img width="500" alt="image" src="https://github.com/user-attachments/assets/22e31394-9eee-412c-9f29-b52bedef6afe" />

* Once signed in hit 'Load' and wait for your charts to populate!

### Connectivity (Jira Version)
* Open the .pbit file in Power BI Desktop
* Add your Jira URL 
* Add your Jira Project Key(s) depending on where your stories/epics reside

Don't confuse the project name with the project key, a common mistake! Your project key will be in the URL when viewing an item.

* It should then look something like this:
![image](https://github.com/nbrown02/Capacity-Planning-Feature-Monte-Carlo/assets/29369962/2a24cc23-d6d5-4768-9bcf-12e6bf27bc58)

* Hit 'Load' 
* You will be prompted for a login, choose Basic and enter:
  - Your email associated with your Jira account for your username
  - Your API token you created in the Prerequisities

![alt text](https://raw.githubusercontent.com/nbrown02/FlowViz-Jira/main/Screenshots/Login2.png)

* Then hit 'Connect' and wait for the data and charts to load!

## Using the report
There are two main charts the report shows. The first is the alignment over the selected period (default is 12 weeks). This will show you what the alignment is right now (furthest right value in the line chart) as well as the average over the given period.

![Filtering2](https://github.com/user-attachments/assets/64987e18-7f82-4a31-bd43-9092347e7840)

In addition to this, you can view the list of items and see which respective items they link to. The filter for 'All items' vs. 'In flight items' works for both charts.

![image (1)](https://github.com/user-attachments/assets/1e228a04-0222-4d6c-8397-b1c2ceed078e)

