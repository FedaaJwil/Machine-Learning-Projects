# Simple Loan Approval System 🏦

## Overview
This project implements a **Single Layer Perceptron (SLP)** from scratch using Python and NumPy. It simulates a basic AI-driven decision-making system that evaluates bank loan applications. By training on simple data, the neural network learns to classify whether a bank client should be "Approved" or "Rejected" based on two features: their **Credit Score** and **Income level**.

This project serves as a practical, foundational example of Supervised Learning and Linear Classification without relying on heavy machine learning frameworks like Scikit-Learn or TensorFlow.

---

## Mathematical Foundation 🧮

The core of this project is based on the mathematical model of an artificial neuron. Below are the equations that drive the learning and prediction process:

### 1. The Weighted Sum (Net Input)
The perceptron calculates the net input by multiplying each input feature ($x$) by its corresponding learned weight ($w$) and adding a bias term ($b$):

$$Net = \sum_{i=1}^{n} (x_i \cdot w_i) + b$$

For our specific 2-feature model (where $x_1$ is Credit Score and $x_2$ is Income):

$$Net = (x_1 \cdot w_1) + (x_2 \cdot w_2) + b$$

### 2. Activation Function (Step Function)
To convert the continuous numerical output into a binary decision (Yes/No), the model passes the Net Input through a Step Function. If the value is greater than 0, the loan is approved ($1$). Otherwise, it is rejected ($0$).

$$Output = \begin{cases} 1 & \text{if } Net > 0 \\ 0 & \text{otherwise} \end{cases}$$

### 3. Perceptron Learning Rule (Weight Update)
During the training phase (Epochs), if the model makes an incorrect prediction, it adjusts its weights and bias to "learn" from the mistake. The weights are updated using the following rule:

$$W_{new} = W_{old} + \eta \cdot (Target - Output) \cdot X$$
$$b_{new} = b_{old} + \eta \cdot (Target - Output)$$

*(Where $\eta$ represents the Learning Rate, controlling how big of a step the model takes to correct its error).*

---

## Technologies Used
* **Python 3.x**
* **NumPy:** Used for efficient matrix/array operations and calculating the dot product (weighted sum).
