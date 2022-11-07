# Updates for Sprint 3

**GOALS**  
We want to set up CI/CD (DevOps) features for Databricks. These operations require features outside of Databricks, so we are famialiarizing ourself with these features and determining how we can make use of them for future work.  
We also want to plan what and how we are going to do to develop a complete MLops service for at least one ML use case.

# Relevant Videos

* [Sprint 3 Updates/Status](https://youtu.be/73N3BCdvZJ0) - An introduction video for the current sprint.
* [CI & Testing on GitHub](https://youtu.be/rc7vrvI1EeQ) - This video discusses some basics of using GitHub Actions. Nothing revoluationary in this video, but it was helpful for understanding code management with Git & GitHub, which will be useful later on.
* [Plans for Sprint 4 & 5 (*Short Version*)](https://youtu.be/gjP6LUyXc5k) - This video discusses our plans for the remainder of the semester. We have explored the Databricks platform and operations tools that integrate with Databricks. Now, it is time to put it all together and create a machine learning service on Databricks with help from GitHub and public clouds.
* [Plans for Sprint 4 & 5 (*Long Version*)]() - *coming soon*

# Chronological Updates

#### 11/2 - PGD

Researched CI/CD on Databricks-AWS.  
Takaways:  
* Most operations with code management happen through the Git provider. e.g., GitHub, Azure DevOps, AWS CodeCommit
* For GitHub, for example, there are avaialble features for pull requests, code review, and merges as well as ways to automate these steps with GitHub actions.

Continuous intiegration can be done with GitHub actions. ([Ref.](https://docs.github.com/en/actions/automating-builds-and-tests/about-continuous-integration))
Includes:
* code development - branches, pull requests, merging, etc.
* code testing - part of merging branches
The associated GitHub Actions workflows seems to be language specific and appear to be done with `.yml` files.  
GitHub - [`actions/starter_workflows`](https://github.com/actions/starter-workflows/tree/main/ci)

I'm going to see if I can setup some basic CI using GitHub Actions
.  
"Sticking points"
1. You have to choose to run GitHub Actions workflows on GitHub-hosted VMs or machines you host yourself. **Can I host this process on Databricks?**
* "[About GitHub-hosted runners](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners)"
* "[About self-hosted runners](https://docs.github.com/en/actions/automating-your-workflow-with-github-actions/about-self-hosted-runners)"

#### 11/3 - PGD

Made some headway on learning more about GitHub actions for CI, but got sidetracked before attempting to implement anything.  

I got sidetracked by learning more about MLOps (via [a video](https://www.youtube.com/watch?v=0wT-EJBw2n4) provided via Ata's email)
* Talks about setting up ModelOperations-type stuff
* How to set up a framework for ML pipelines that automate the operations with models
.  
Takeaways:
* Sounds like Databricks allows us to use YAML files to create pipelines that define an ML process and we can define any target script, notebook, data, etc. that we need.
* The code portion of each stage of operations would be in GitHub or Azure DevOps or something...
* But there seems to be flexible resources for working with models directly in DB!

#### 11/5 - PGD

On Friday and Saturday, I tried to create my first GitHub Action.  

You can find the action and associated code in [this repo](https://github.com/pdvnny/mlops-databricks-test-env), which I created separately just for simplicity.  
.  
The GitHub action that I created was designed to run checks on very simple sorting algorithms before allowing new code to be merged to the "main" branch of the repository. Basically, the GitHub Action does some very simple unit testing and CI testing.  
.  
I was get the GitHub workflow running ... you can see successful operation by clicking on the "Actions" tab of the repo above. I'm still getting comfortable with all possibilities and optimizations.

#### 11/6 - PGD

I'm going to create a video explaining what I have learned about CI/CD on GitHub so far.  
.  
Likely content:  
* Contextualizing why this is important
* Demo the GitHub Actions CI set up in Databricks
* This demo is super simple ... what is missing or what might be relevant in the future...
  - automatic repo updates in DB as a GitHub Action
  - No continuous deployment checking
.  

