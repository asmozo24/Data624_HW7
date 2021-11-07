# Data624_HW7


6.2. Developing a model to predict permeability (see Sect. 1.4) could save sig-
nificant resources for a pharmaceutical company, while at the same time more

rapidly identifying molecules that have a sufficient permeability to become a
drug:
(a) Start R and use these commands to load the data:
> library(AppliedPredictiveModeling)
> data(permeability)
The matrix fingerprints contains the 1,107 binary molecular predictors for the 165 compounds, while permeability contains permeability
response.
(b) The fingerprint predictors indicate the presence or absence of substructures of a molecule and are often sparse meaning that relatively few of the
molecules contain each substructure. Filter out the predictors that have low frequencies using the nearZeroVar function from the caret package.
How many predictors are left for modeling?
(c) Split the data into a training and a test set, pre-process the data, and tune a PLS model. How many latent variables are optimal and what is the corresponding resampled estimate of R2?
(d) Predict the response for the test set. What is the test set estimate of R2? 
(e) Try building other models discussed in this chapter. Do any have better predictive performance?
(f) Would you recommend any of your models to replace the permeability laboratory experiment?



6.3. A chemical manufacturing process for a pharmaceutical product was
discussed in Sect. 1.4. In this problem, the objective is to understand the re-
lationship between biological measurements of the raw materials (predictors),measurements of the manufacturing process (predictors), and the response of
product yield. Biological predictors cannot be changed but can be used to
assess the quality of the raw material before processing. On the other hand,
manufacturing process predictors can be changed in the manufacturing pro-
cess. Improving product yield by 1 % will boost revenue by approximately

one hundred thousand dollars per batch:
(a) Start R and use these commands to load the data:
> library(AppliedPredictiveModeling)
> data(chemicalManufacturing)
The matrix processPredictors contains the 57 predictors (12 describing the input biological material and 45 describing the process predictors) for the 176 manufacturing runs. yield contains the percent yield for each run.
(b) A small percentage of cells in the predictor set contain missing values. Use an imputation function to fill in these missing values (e.g., see Sect. 3.8).
(c) Split the data into a training and a test set, pre-process the data, and tune a model of your choice from this chapter. What is the optimal value
of the performance metric?
(d) Predict the response for the test set. What is the value of the performance metric and how does this compare with the resampled performance metric
on the training set?
(e) Which predictors are most important in the model you have trained? Do either the biological or process predictors dominate the list?
(f) Explore the relationships between each of the top predictors and the response. How could this information be helpful in improving yield in future runs of the manufacturing process?
