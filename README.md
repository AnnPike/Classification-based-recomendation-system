# Partner_acceptance_prediction
The task of the project is to optimize redirect Partner Partners that will bring company most revenue.<br />
First, I analyze the dataset in ```1EDA.ipynb``` <br />
Then, I create a baseline model which I chose to be Naive Bias in ```2baseline_NaiveBias.ipynb```  <br />
I found out that this model doesn't work so well for our dataset and I attempt to create more sophisticated models, like KNN in ```1EDA.ipynb``` <br />. Here I run a Cross Validation Grid Search using cutom score, wich is a very simple funcion of f1 of reject and f1 of convergence. <br />Since both are important for us, we force more balanced solutiions to win.<br />![alt text](https://github.com/AnnPike/AnomalyImageDetection/blob/main/dataset.png)<br />
Then I attempt to solve it using Random Forest in ```4RandomForest.ipynb``` <br />. I obtain very high precision but very low recall.<br />
As sumary I chose KNN model since it works best for the stated bussiness problem.
