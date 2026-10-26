<img src="assets/banner.svg" width="100%" alt="Activation Functions, Measured. Sigmoid, tanh and ReLU on the same network and the same data. Which one actually learns?">

## The question

The activation function is one line of code and one of the most consequential choices in a network. This project trains the same model on **MNIST** three times, once each with **sigmoid**, **tanh** and **ReLU**, on a CUDA GPU, and compares how they learn.

## What is inside

- Three activation functions (sigmoid, tanh, ReLU) on one architecture
- Training on a **CUDA GPU**
- Plots of the functions, the training loss and the validation accuracy for a deeper understanding

## Results

In this setup, **tanh** learns fastest (about 70% validation accuracy after ten epochs), **ReLU** follows (about 44%), and **sigmoid stays at chance level** (about 10% on ten classes) with a flat loss: the saturation behaviour that makes sigmoid a poor choice for hidden layers, made visible. Values are read from the plots below.

<table>
<tr><td width="33%" valign="top"><img src="graphs/activation_functions.png" width="100%" alt="The three functions"><br><sub>The three functions</sub></td><td width="33%" valign="top"><img src="graphs/accuracy_of_activation_functions.png" width="100%" alt="Validation accuracy per epoch"><br><sub>Validation accuracy per epoch</sub></td><td width="33%" valign="top"><img src="graphs/loss_of_activation_functions.png" width="100%" alt="Training loss per iteration"><br><sub>Training loss per iteration</sub></td></tr>
</table>

## Run it

1. Download `spec-file.txt`.
2. Follow the instructions in `Conda_Virtual_Env.txt`:

```bash
# a new environment from the spec file
conda create --name myenv --file spec-file.txt
# or install the listed packages into an existing environment
conda install --name myenv --file spec-file.txt
```
The full set of environment commands is in [`Conda_Virtual_Env.txt`](Conda_Virtual_Env.txt).

Then open [`Activation_Functions.ipynb`](Activation_Functions.ipynb).

## Built with

`Python` · `PyTorch` · `Matplotlib`

<br>

<p align="center"><sub><a href="https://github.com/johnnyk1090">← back to the profile</a></sub></p>
