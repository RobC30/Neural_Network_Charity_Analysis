# __Neural Network Charity Analysis__

## __Overview__
The aim of this project is to predict whether applicants will be successful if their project is funded by Alphabet Soup. We are to use a Neural Network Model utiliozing TensorFlow platform in Python.

## __Results__

### __Data Preprocessing__

Looking at our dataset, we can infer that the columns __EIN & NAME__ can be removed for our training model as these two columns will only add noise to our predicting model. Our main goal is to predict if the project will be successful if funded so our target variable will be __IS_SUCCESSFUL__. With these considered, every other column not mentioned will be our feature. Binning _(for APPLICATION_TYPE & CLASSIFICATION)_, encoding, merging & scaling will be applied to our features  to standardize our data.

### __Compiling, Training, and Evaluating the Model__

Our target of accuracy is set at 75% for it to be acceptable. 

For our initial attempt, the following parameters were set:<br>
43 Features<br>
1st Hidden Layer - 80 Neurons - ReLU Activation<br>
2nd Hidden Layer - 30 Neurons - ReLU Activation<br>
1 Output Layer - Sigmoid Activation<br>
Epochs - 100<br>

__Accuracy: 72.49%__

Since this is below our acceptable rate, we then modified our Layers, Activations & Epochs hoping to achieve better results.

Attempt # 1 - Adding Hidden Layer<br>
43 Features<br>
1st Hidden Layer - 80 Neurons - ReLU Activation<br>
2nd Hidden Layer - 50 Neurons - ReLU Activation<br>
3rd Hidden Layer - 40 Neurons - ReLU Activation<br>
1 Output Layer - Sigmoid Activation<br>
Epochs - 100<br>

__Accuracy: 72.48%__

Attempt # 2 - Adding Neurons, Changing Output Activation & Reducing Epochs<br>
43 Features<br>
1st Hidden Layer - 120 Neurons - ReLU Activation<br>
2nd Hidden Layer - 80 Neurons - ReLU Activation<br>
3rd Hidden Layer - 35 Neurons - ReLU Activation<br>
1 Output Layer - TanH Activation<br>
Epochs - 100<br>

__Accuracy: 72.57%__

Attempt # 3 - Adding Neurons & Changing Activations<br>
43 Features<br>
1st Hidden Layer - 180 Neurons - TanH Activation<br>
2nd Hidden Layer - 70 Neurons - TanH Activation<br>
3rd Hidden Layer - 40 Neurons - TanH Activation<br>
1 Output Layer - Hard Sigmoid Activation<br>
Epochs - 50<br>

__Accuracy: 72.60%__

Attempt # 4 - Adding Neurons & Changing Activations<br>
43 Features<br>
1st Hidden Layer - 180 Neurons - ReLU Activation<br>
2nd Hidden Layer - 70 Neurons - ReLU Activation<br>
3rd Hidden Layer - 40 Neurons - ReLU Activation<br>
1 Output Layer -  Sigmoid Activation<br>
Epochs - 30<br>

__Accuracy: 72.73%__

## __Summary__
After numerous attempts to increase our model's accuracy by increasing layers, changing activations & increasing/decreasing epochs, all attempts had little differences between accuracies. It is then not recommended to use deep-learning neural networks for this dataset.