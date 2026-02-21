# Multilayer Perceptron (MLP) — Simple Explanation, Examples, and Interview Q&A

## What is a Multilayer Perceptron (MLP)?

A **Multilayer Perceptron (MLP)** is a type of neural network made of layers of small computing units called *neurons*.  
It is used for tasks like sentiment analysis, emotion recognition, and image classification.

Think of it like a factory assembly line:
- Input layer = raw materials
- Hidden layers = processing steps
- Output layer = final product (prediction)

---

## Example Architecture

Suppose we design an MLP with:
- Input layer: 4 neurons  
- Hidden layer 1: 5 neurons  
- Hidden layer 2: 6 neurons  
- Output layer: 3 neurons  

This means:

Input → Hidden1 → Hidden2 → Output  
4 → 5 → 6 → 3

---

## What decides input and output size?

### Input layer size
It depends on your data.

Examples:
- Image: number of pixels  
- Text: number of features or embeddings  
- Tabular data: number of columns  

Example:
If a dataset has 4 features per sample → input layer = 4 neurons.

---

### Output layer size
It depends on number of classes.

Examples:
- Sentiment analysis: positive, negative, neutral → 3 neurons  
- Emotion recognition: 7 emotions → 7 neurons  
- Image classification: 1000 categories → 1000 neurons  

So output neurons = number of categories.

---

## Hidden layers — how many and why?

Hidden layers learn patterns and relationships in data.

There is no fixed rule:
- More complex task → more neurons/layers  
- More data → larger network  
- Limited GPU → smaller network  

So choosing hidden layers = trial and error + experience.

---

## How does a single neuron work?

Each neuron does 3 steps:

1. Multiply inputs with weights  
2. Add them (dot product)  
3. Apply activation function  

Formula:

z = w₁x₁ + w₂x₂ + … + wₙxₙ + b  
y = activation(z)

Where:
- x = inputs  
- w = weights  
- b = bias  
- y = output  

---

## Forward Pass (How prediction happens)

Forward pass = data moving from input → output.

Steps:
1. Input enters network  
2. Each neuron computes output  
3. Output goes to next layer  
4. Final layer produces prediction  

Example:

Input: [Age=25, Income=50k, Score=700, Balance=20k]

Network processes through hidden layers → Output:

[0.1, 0.8, 0.1]

Meaning:
- Class 1: 10%
- Class 2: 80% ← predicted
- Class 3: 10%

---

## How does the network learn?

After prediction, we compare with true answer.

Error = predicted − actual

Then:
- Adjust weights
- Reduce error
- Improve prediction

This learning step is called **backpropagation** (covered later).

---

# Real‑World Analogy

Imagine hiring decision:

Input:
- Experience
- Skills
- Education
- Interview score

Hidden layers:
- Evaluate competence
- Evaluate cultural fit
- Evaluate risk

Output:
- Hire
- Maybe
- Reject

The company learns from past mistakes → improves hiring decisions.

That is exactly how MLP learns.

---

# Key Formulas Summary

Neuron output:
y = activation(w·x + b)

Layer output:
y = activation(Wx + b)

Where:
- W = weight matrix
- x = input vector
- b = bias vector

---

# Interview Questions and Answers

## Basic

**Q1. What is a Multilayer Perceptron?**  
A feed‑forward neural network with input, hidden, and output layers used for classification or regression.

---

**Q2. What determines input layer size?**  
Number of features in the dataset.

---

**Q3. What determines output layer size?**  
Number of classes (for classification).

---

**Q4. What is a hidden layer?**  
Intermediate layer that learns patterns from data.

---

## Intermediate

**Q5. How does a neuron compute output?**  
Weighted sum of inputs + bias followed by activation function.

Formula:
y = activation(w·x + b)

---

**Q6. What is forward pass?**  
Process of sending input through layers to produce prediction.

---

**Q7. Why do we need hidden layers?**  
To learn complex nonlinear relationships.

---

## Practical

**Q8. How to choose number of hidden layers?**  
Trial and error based on:
- data complexity
- dataset size
- compute power

---

**Q9. Can MLP handle images directly?**  
Yes, but CNNs perform better because they exploit spatial structure.

---

**Q10. What happens after forward pass?**  
Loss is computed and backpropagation updates weights.

---

# One‑Line Summary

MLP = stacked neurons that transform input features into predictions through weighted connections and activations.

