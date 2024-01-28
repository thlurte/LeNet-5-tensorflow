 <h2 align="center">LeNet-5</h2>
Tensorflow implementation of (Lecun et al., 1998)
<br>
<img src='https://www.datasciencecentral.com/wp-content/uploads/2021/10/1lvvWF48t7cyRWqct13eU0w.jpeg'>


### Instructions

- Set Up Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
source venv/bin/activate 
```

- Clone the repository
```bash
git clone https://github.com/thlurte/LeNet-5-tensorflow.git

```

- Change into the directory of the repository

```bash

cd LeNet-5-tensorflow
```

- Install Dependancies

```bash
pip install -r requirments.txt
```

- To Train the model

```bash
python main.py --data_dir <path-to-dataset>

```


###  Architecture

LeNet-5 comprises seven layers, not counting the input, all
of which contain trainable parameters (weights). The input
is a 32 x 32 pixel image.

First layer is a convolutional layer with six feature maps.
Each unit in each feature map is connected to a 5 x 5 neigh-
borhood in the input.

A subsampling layer follows the first layer with six feature maps of
size 14 14. Each unit in each feature map is connected to a
2 x 2 neighborhood in the corresponding feature map in layer one.

Second convolutional layer contains 16 feature maps.
Each unit in each feature map is connected to several
5 x 5 neighborhoods at identical locations in a subset of
previous sub sampling layer’s feature maps.

Second subsampling layer contains 16 feature maps of
size 5 x 5. Each unit in each feature map is connected to a
2 x 2 neighborhood in the corresponding feature map in second convolutional layer.

Final convolutional layer contains 120 feature maps.
Each unit is connected to a 5 x 5 neighborhood on all 16
of S4’s feature maps.

Fully connected layer contains 84 units is fully connected to final convolutional layer.

Output layer of this archtecture contains number of classes as units with `softmax` as the activation function.

### Activation 

Sigmoid activation function follows both sub sampling layers in the convolutional blocks. TanH activation function follows both fully connected layers in the later part of the architecture.

### Loss Function
Mean Squared Error is used as loss function to calculate the error.

### Optimizer
Stochastic gradient descent is used to find the global minima in this architecture.

### References

- [Gradient-based learning applied to document recognition](https://ieeexplore.ieee.org/document/726791)
- [LeNet-5: Summary and Implementation](https://hackmd.io/@machine-learning/S1WvJyqmI)
- [LeNet-5 TensorFlow 2.0](https://colab.research.google.com/github/maticvl/dataHacker/blob/master/CNN/LeNet_5_TensorFlow_2_0_datahacker.ipynb)
