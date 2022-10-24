# Setting Up Git Repo on Databricks

1. Generate a personal access token (PAT) - ["Set up Databricks Repos access a remote repo"](https://docs.databricks.com/repos/set-up-git-provider-access.html)
* Databricks repos is the repo service offered by Databrikcs
* You can also connect to external repos
.  
.  
Steps
* On GitHub site, use the instructions at the link above to generate and copy a personal access token

2. In Databricks...
* Select your name in the top right
* Select "User Settings"
* Select "Git Integeration"
* Select GitHub as the Git provider
* Paste your PAT from GitHub

3. I updated our repo to work with non-notebook files
* Select your username in the top right
* Open "Admin Console"
* Select "Workspace settings"
* In "Repos" section...
	- Changed the "Files in Repos" setting to "DBR 11.0+"

