<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=180&section=header&text=Handwritten%20Digits&fontSize=44&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=A%20neural%20network%20from%20scratch%20vs%20Keras&descAlignY=60&descSize=18" width="100%"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&pause=1000&color=36BCF7&center=true&vCenter=true&width=600&lines=Reads+handwritten+digits+0-9;Neural+network+built+with+NumPy+only;Same+task+with+Keras;95.8%25+test+accuracy" alt="Typing SVG"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white"/>
  <img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white"/>
</p>

## What is this?

The model looks at an image of a handwritten digit (0 to 9) and says which digit it is.

I built it **two times** to learn how neural networks really work:

1. **From scratch with NumPy**: I wrote the forward pass, backpropagation and gradient descent myself.
2. **With Keras**: the same idea in a few lines.

Data: **EMNIST Digits** (28 × 28 pixel images).

## Results

| Version | Test accuracy |
|---------|:-------------:|
| NumPy (from scratch) | 92.6% |
| Keras | **95.8%** |

## How it works

```mermaid
flowchart LR
    A[28x28 image] --> B[784 pixels]
    B --> C[Hidden layer]
    C --> D[Hidden layer]
    D --> E[10 outputs<br/>one per digit]
    E --> F[Highest score = answer]
```

**NumPy version**
- Sigmoid activation
- Mini-batch gradient descent
- 1500 epochs

**Keras version**
- 2 hidden layers with 64 neurons each (ReLU)
- Softmax output, Adam optimizer
- 10 epochs

## Files

| File | What is inside |
|------|----------------|
| `emnist_digits_(Numpy).ipynb` | Neural network from scratch |
| `emnist_digits_(Keras).ipynb` | Same task with Keras |

## How to run

```bash
pip install numpy pandas matplotlib scikit-learn tensorflow
```

Download the EMNIST Digits CSV files from [Kaggle](https://www.kaggle.com/datasets/crawford/emnist), then open a notebook and run all cells.

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,50:203a43,100:0f2027&height=100&section=footer" width="100%"/>
</p>
