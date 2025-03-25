# ClickUp Flow Connector
A swagger file to build a custom connector for Microsoft Flow to connect to ClickUp API. Follow the step by step instructions to get it running.

> You have to be on a paid plan since connectors like HTTP Request (needed for listening to ClickUp Webhooks and trigger actions based on events like e.g. TaskCreated or TaskUpdated) and creating custom connectors for Power Automate (Flow) are premium features only! Keep that in mind. 

## ClickUp API Token

1. Go to ClickUp and hit your face (not literally) at the bottom left
2. Klick on **Apps** and generate your API Token 

## Create custom connector

3. Navigate to **Power Automate** (formerly Flows) > **Data** > **Custom connectors**
4. Klick on **+ New custom connector** > **Import an OpenAPI file**
5. **Enter a name** (eg. ClickUp Connector), **import the JSON-file** from the repo and hit **Continue**

## General

6. **Upload the ClickUp logo** from the repo, **add the ClickUp brand color** (`#7b68ee`) and submit by hitting Security

## Security (should be prefilled, else enter the following)

7. For Authentication type **choose API Key**
8. For Parameter label enter `API Key`
9. For Parameter name enter `Authorization`
10. For Parameter location **choose Header**

## Definitions

| Definition | Description |
|--|--|
| GetTeams  | Gets the teams that you are a member of |
| GetSpaces | Gets the spaces from a team you choose |
| GetFolders | Enter a space id and get the folders that belong to that space |
| GetTaskByID | Enter a task id and get a whole lot of dynamic content you can work with in further action steps |
| GetAccessableCustomFields | Enter a list id and get all the custom fields |
| PostTaskComment | Enter a task id and post a comment |
| GetTasksFromList | Enter a list id and get all the tasks that live in there |
| CreateTask | Enter a list id and create a new task |
| PostAttachment | Enter a attachment and add attachment to task  |
| Update a Custom Field | Enter a value to update custom field |

You are now ready to play around with your custom connector. You will be prompted to enter your ClickUp API Token when using it for the first time within your Flows. Remember.. you generated it at the beginning. Go to ClickUp, again hit your face ..just jokin - you already know where to find it :P

Happy flowing.. ehhh automating!
