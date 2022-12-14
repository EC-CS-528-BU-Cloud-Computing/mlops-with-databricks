# Updates for Sprint 4

## GOALS  

### Make progress on creating a financial fraud ML service.

Realistic goals for this sprint:
1. Set up (*most*) DevOps operations
  - [X] Automatic Databricks Repo updates
  - [] Short Unit tests
  - [] Trigger ML pipeline in Databricks that trains a model
2. Write ML foundational code
  - [] We can't do much without code that will actually train and evaluate a model
  - [] It shouldn't be too bad. We can basically copy parts of the original demo that we worked on.
3. Write deployement code for trained model
  - [] I am referring to a version of deployment that allows me to test if a model can be deployed and interacted with ... it will be as simple as possible
  - [] Meant to resemble the "CI testing before merging code into staging"


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

* [A video on triggering actions in Databricks from external sources (GitHub in this case)](https://youtu.be/LMruWIGrgek)

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
 
#### PGD - Nov 17

* First session today (I didn't have much time, but) I made some progress. Most importantly, I think I understand how to use the Databricks APIs.
* The Databricks documentation [here](https://docs.databricks.com/dev-tools/api/latest/index.html) is actually pretty helpful ... I had some initial trouble/confusion due to my lack of experience working with APIs ... the docs were just a little hard to read.
* Anyway, I'm believe I have the authentication system down and should be able to get do some GET/POST requests to the Databricks APIs
  - I'll look into converting them to Python scripts too ... not sure when though.

Resources:
* [Databricks API Docs page](https://docs.databricks.com/dev-tools/api/latest/index.html)
  * [Repos API](https://docs.databricks.com/dev-tools/api/latest/repos.html)
* [Databricks API Authentication information](https://docs.databricks.com/dev-tools/api/latest/authentication.html)
* Using `curl` documentation
  - [ReqBin](https://reqbin.com/req/c-1n4ljxb9/curl-get-request-example)
  - [Curl.se](https://curl.se/docs/httpscripting.html)
  
#### PGD - Nov 18

Locked down the automatic Databricks repos updates! It's not perfect, but at least it works.
* Benefits
  - I feel like I can continue to find robust ways to work with the Databricks APIs. It was hard to get familiar with it at first, but it's getting easier each time I try to use it.
* Problems
  - I am **SEVERELY** lacking SECURITY
  - I am currently storing a Databricks access token in a public manner ... As soon as I get a chance, I need to look into using a more secure method. I think there is something called secrets on GitHub that protects private information.
  - I am going to remove the access granted to the current access token very soon!!
  
* I will make a video on interacting with the Databricks API

Made some headway in setting up the code/structure that is the foundation of the ML model side of operations.
* There is a lot of setup with YAML files and Notebooks that I am gettting used to ... progress might be a little slow.

Here are some of the resources that I have been looking ata:
1. [MLflow Classification Task template](https://github.com/mlflow/recipes-classification-template)
  - A new version of something that was in an MLOps demo - the old version is  [here](https://github.com/mlflow/mlp-regression-template)
2. MLflow recipes - these seem to be the recommended structure for setting up robust MLOps configurations
  - [MLflow recipes - Quickstart](https://mlflow.org/docs/latest/recipes.html#quickstarts)
  - [MLflow recipes - Templates](https://mlflow.org/docs/latest/recipes.html#recipe-templates)
