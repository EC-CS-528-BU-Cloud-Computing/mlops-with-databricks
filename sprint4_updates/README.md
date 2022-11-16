# Updates for Sprint 4

## GOALS  

### Make progress on creating a financial fraud ML service.

Realistic goals for this sprint:
1. Set up (*most*) DevOps operations
  - Automatic Databricks Repo updates
  - Short Unit tests
  - Trigger ML pipeline in Databricks that trains a model
2. Write ML foundational code
  - We can't do much without code that will actually train and evaluate a model
  - It shouldn't be too bad. We can basically copy parts of the original demo that we worked on.
3. Write deployement code for trained model
  - I am referring to a version of deployment that allows me to test if a model can be deployed and interacted with ... it will be as simple as possible
  - Meant to resemble the "CI testing before merging code into staging"


### Research Datarobot

- We have been slacking on this, but it is something we originally set out to accomplish, so we should still work on it.
- Things we need to learn...
  * Where MLOps operations take place?
    - Model training env?
    - Code development env?
    - Deployment env?
  * How do you structure the service/platform?
    - Do you need to write YAMLs/scripts that handle operations?
    - How are models stored/saved?

I came up with this list very quickly, so the structure might not be very logical. It is meant suggest the types of things we need to learn, not provide a comprehensive research list.

# Relevant Videos



# Chronological Updates

#### PGD - Nov 16

* First, working on setting up automatic repo updates in Databricks using the Repos API
  - For now this was the only thing that I got to work on... GitHub actions was giving me lots of problems
  - I have a working action for now, but I was having a lot of trouble with syntax and formatting
  - DECISION: I am going to use `databricks-cli` to perform interaction between GitHub Action and Databricks
  - The `databricks-cli` is an experimental service that allows python scripts to interact with the Databricks APIs
  
NEXT UP:
1. Continue working on Databricks automatic updates

Resources
* GitHub Actions
  - [Python GitHub Actions template](https://github.com/cicirello/python-github-action-template/blob/main/.github/workflows/build.yml)
  - [Python Build and Test GitHub Action](https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-python)
* Databricks
  - [Databricks CLI](https://docs.databricks.com/dev-tools/cli/index.html)
  - [Databricks Repos API](https://docs.databricks.com/dev-tools/api/latest/repos.html)
 
 
