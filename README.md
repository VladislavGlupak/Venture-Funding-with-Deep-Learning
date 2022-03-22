# Venture-Funding-with-Deep-Learning

This repository represents the creating and optimizing a binary classification model using a deep neural network.

---

## Approach

Step 1: Prepare the data for use on a neural network model

Step 2: Compile and evaluate a binary classification model using a neural network

Step 3: Optimize the neural network model

---

## Technologies

This project leverages the following tools for financial analysis:

- [Conda](https://docs.conda.io/en/latest/) - source package management system and environment management system.

- [Pandas](https://pandas.pydata.org) - Python library that’s designed specifically for data analysis.

- [TensorFlow](https://www.tensorflow.org) - open source library to help you develop and train ML models.

---

## Input data

`/Resources/applicants_data.csv` - file contains a variety of information about each business, including whether or not it ultimately became successful.

---

## Running analisys

1. Open Jupyter lab
2. Import the required libraries and dependencies

```
# Imports
import pandas as pd
from pathlib import Path
import tensorflow as tf
from tensorflow.keras.layers import Dense
from tensorflow.keras.models import Sequential
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler, OneHotEncoder
```

3. Run code (wait when it is done)

---

## Compile and Evaluate a Binary Classification Model Using a Neural Network

Pre-settings:

1. Number of features - `116`
2. Activation of hidden layers function - `relu`
3. Number of epoches - `50`

```
Model: "sequential_7"
_________________________________________________________________
 Layer (type)                Output Shape              Param #
=================================================================
 dense_37 (Dense)            (None, 58)                6786

 dense_38 (Dense)            (None, 29)                1711

 dense_39 (Dense)            (None, 1)                 30

=================================================================
Total params: 8,527
Trainable params: 8,527
Non-trainable params: 0
```

Results:

```
268/268 - 0s - loss: 0.5532 - accuracy: 0.7305 - 367ms/epoch - 1ms/step
Loss: 0.553196907043457, Accuracy: 0.7304956316947937
```

## Optimize the neural network model (Alternative MODEL 1)

Pre-settings:

1. Number of features - `116`
2. Activation of hidden layers function - `relu`
3. Number of epoches - `50`

```
Model: "sequential_8"
_________________________________________________________________
 Layer (type)                Output Shape              Param #
=================================================================
 dense_40 (Dense)            (None, 58)                6786

 dense_41 (Dense)            (None, 29)                1711

 dense_42 (Dense)            (None, 15)                450

 dense_43 (Dense)            (None, 8)                 128

 dense_44 (Dense)            (None, 4)                 36

 dense_45 (Dense)            (None, 1)                 5

=================================================================
Total params: 9,116
Trainable params: 9,116
Non-trainable params: 0
```

Results:

```
Alternative Model 1 Results
268/268 - 0s - loss: 0.5510 - accuracy: 0.7318 - 358ms/epoch - 1ms/step
Loss: 0.5510239601135254, Accuracy: 0.7317784428596497
```

## Optimize the neural network model (Alternative MODEL 2)

Pre-settings:

1. Number of features - `116`
2. Activation of hidden layers function - `relu`
3. Number of epoches - `50`

```
Model: "sequential_9"
_________________________________________________________________
 Layer (type)                Output Shape              Param #
=================================================================
 dense_46 (Dense)            (None, 300)               35100

 dense_47 (Dense)            (None, 150)               45150

 dense_48 (Dense)            (None, 75)                11325

 dense_49 (Dense)            (None, 38)                2888

 dense_50 (Dense)            (None, 19)                741

 dense_51 (Dense)            (None, 1)                 20

=================================================================
Total params: 95,224
Trainable params: 95,224
Non-trainable params: 0
```

Results:

```
Alternative Model 2 Results
268/268 - 0s - loss: 0.5621 - accuracy: 0.7315 - 424ms/epoch - 2ms/step
Loss: 0.5620570778846741, Accuracy: 0.7315452098846436
```

## Optimize the neural network model (Alternative MODEL 3)

Pre-settings:

1. Number of features - `116`
2. Activation of hidden layers function - `tanh`
3. Number of epoches - `100`

```
Model: "sequential_10"
_________________________________________________________________
 Layer (type)                Output Shape              Param #
=================================================================
 dense_52 (Dense)            (None, 300)               35100

 dense_53 (Dense)            (None, 150)               45150

 dense_54 (Dense)            (None, 75)                11325

 dense_55 (Dense)            (None, 1)                 76

=================================================================
Total params: 91,651
Trainable params: 91,651
Non-trainable params: 0
```

Results:

```
Alternative Model 3 Results
268/268 - 0s - loss: 0.5598 - accuracy: 0.7294 - 446ms/epoch - 2ms/step
Loss: 0.5597923398017883, Accuracy: 0.7294460535049438
```

## Conclusions

The accuracy of the model helped to increase (not much) the increasing the number of hidden layers and neurons (model 2).

All models saved in the folder `Models`.

---

## Contributors

Vladislav Glupak - [Linkedin](https://www.linkedin.com/in/vladislav-glupak/)

---

## License

It is an Open-source analysis.
