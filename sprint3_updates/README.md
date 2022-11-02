# Updates for Sprint 3

**GOALS**  
We want to set up CI/CD (DevOps) features for Databricks. These operations require features outside of Databricks, so we are famialiarizing ourself with these features and determining how we can make use of them for future work.  
We also want to plan what and how we are going to do to develop a complete MLops service for at least one ML use case.

# Chronological Updates

#### 11/2 - PGD

Researched CI/CD on Databricks-AWS.  
Takaways:  
* Most operations with code management happen through the Git provider. e.g., GitHub, Azure DevOps, AWS CodeCommit
* For GitHub, for example, there are avaialble features for pull requests, code review, and merges as well as ways to automate these steps with GitHub actions.

Continuous intiegration can be done with GitHub actions.  
Includes:
* code development - branches, pull requests, merging, etc.
* code testing - part of merging branches
The associated GitHub Actions workflows seems to be language specific and appear to be done with `.yml` files.  
GitHub - [`actions/starter_workflows`](https://github.com/actions/starter-workflows/tree/main/ci)

I'm going to see if I can setup some basic CI using GitHub Actions
