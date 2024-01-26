 <h2 align="center">LeNet-5</h2>
Tensorflow implementation of (Lecun et al., 1998)
<br>
<img src='https://github.com/thlurte/LeNet-5-tensorflow/blob/main/assets/a.png'>


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
