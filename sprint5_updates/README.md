# Updates for Sprint 5

## GOALS  

### Make progress on creating a financial fraud ML service.

Realistic goals for this sprint:
1. Set up (*most*) DevOps operations
  - [X] Automatic Databricks Repo updates
  - [ ] Short Unit tests
  - [ ] Trigger ML pipeline in Databricks that trains a model
2. Write ML foundational code
  - [X] We can't do much without code that will actually train and evaluate a model
  - [X] It shouldn't be too bad. We can basically copy parts of the original demo that we worked on.
3. Write deployement code for trained model
  - [ ] I am referring to a version of deployment that allows me to test if a model can be deployed and interacted with ... it will be as simple as possible
  - [ ] Meant to resemble the "CI testing before merging code into staging"

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

*No videos yet*

# Chronological Updates

### PGD - Nov 24, 2022

* Working on setting up model training and evaluation pipeline in Databricks
	- uses MLflow to manage models and metrics
	- Uses __MLflow recipes__ setup to design a repeatable training & evaluation process
