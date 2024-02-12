# Partner_acceptance_prediction
The task of the project is to optimize redirect Partner Partners that will bring the company the most revenue.<br />
First, I analyze the dataset in ```1EDA.ipynb``` <br />, do relevant transformations and prepare dataset for training<br />
Then, I created a baseline model which I chose to be Naive Bias in ```2baseline_NaiveBias.ipynb```  <br />
I found out that this model doesn't work so well for our dataset and I attempted to create more sophisticated models, like KNN in ```1EDA.ipynb``` <br /> Here I run a Cross-Validation Grid Search using the custom score, which is a very simple function of f1 of reject and f1 of convergence. <br />Since both are important for us, we force more balanced solutions to win.<br />![alt text](https://github.com/AnnPike/Partner_acceptance_prediction/blob/main/custom_score.png)<br />
Then I attempt to solve it using Random Forest in ```4RandomForest.ipynb``` <br />. I obtain very high precision but very low recall.<br />
In summary, I chose the KNN model, since it works best for the stated business problem.<br />
But, in general, I am not satisfied with the solution, because it predicts no partner for some leads. As I familiarized myself with the data and ranking problem, I would continue learning more about it and building more suitable solutions.

Follow-up questions
1. What kind of additional data would you want to develop your solution? What features would you expect to be predictive and reasonable to gather?<br />
Income, expenses, age, gender, marital status - anything relevant to the partners. Features that our partners use would be very valuable.
2. What architecture/service would you prefer to use to deploy the solution to production?
Consider several alternatives.<br />
Amazon Web Services (AWS), Microsoft Azure, Google Cloud
3. How would you validate that your solution works as expected in production? How would
you monitor its performance and stability?<br />
Monitoring statistics of output. Another option is computational monitoring - the number of requests, and CPU usage. To ensure a smooth introduction to a new model we can deploy in a canary - meaning that a small portion of the data is predicted with the new model.
5. What would be other important considerations to keep in mind when working on this
problem?<br />
Impretability - we would prefer models that can assist us in accessing links and causes for better data driver decisions.
Because the real value for most of the partners for a specific lead is unknown, we should test different ranking models in production using A/B tests. Or algorithms that help us collect more data - enhancing the rank for rare partners, but in this case we need to calculate how much we gain vs. how much we may lose.
