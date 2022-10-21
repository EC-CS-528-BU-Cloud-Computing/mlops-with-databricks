# Notes on End of Chapter 5 in "Big Book of Machine Learning Use Cases"

Created by Parker Dunn  
Created on 20 Oct 2022

# Purpose

I wanted to keep track of the takeways from this assignment (according to the book).  
My personal takeaways will be in a PowerPoint and other presentation prep on Google Drive.

# Notes

### Review the results

* The number of misidentifications goes down quite a bit with the *balanced* data.
* You can see this by noting how the top-right and bottom-left quadrants have lower values compared to the unbalanced data.

### Model feedback and using MLflow

1. Continued evaluation after developement
	- Need verified labels (by humans) for continuous evaluation
	- Important to carefully choose cases for human to validate
	- e.g., predictions where the model has low certainty
	- This is how we continue to improve and evolve models with a changing landscape
2. Continued evaluation with MLflow
	- MLflow can track each model version we train
	- For Data Scientists,
		* track all model metrics
		* create visualizations
		* save artifacts (extra objects like picture) that provide info about the model
	- For Data Engineers,
		* Easily retrieve any saved model *along with (!!)* the library versions used for training!

### Conclusion

ACCOMPLISHED: "how to use rule-based fraud detection labels and convert them into an ML model using Databricks and MLflow"
.  
.  
Key values of this:
* scalable, modular solution
* ML model allows us to create a "feedback loop"
	- something about allowing the model to learn new fraudulent patterns
	- I'm a little tired ... probably want to revisit this one
* DT model is great intro. approach to a problem
	- great interpretability
	- strong accuracy
