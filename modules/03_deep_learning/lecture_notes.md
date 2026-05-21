# Module 3: Deep Learning Fundamentals
## Duration: 60 minutes

### Learning Objectives
By the end of this module, students will understand:
- ✅ How neural networks are structured and why
- ✅ How data flows through a network (forward pass)
- ✅ How networks learn (backpropagation)
- ✅ Activation functions and why they're necessary
- ✅ The mathematical foundations behind deep learning

---

## Part 1: From Logistic Regression to Neural Networks (15 minutes)

### 1.1 The Perceptron

**Simplest neural network:** One artificial neuron

```
Inputs: x₁, x₂, ..., xₙ
    ↓
Multiply by weights: w₁, w₂, ..., wₙ
    ↓
Sum: z = w₁x₁ + w₂x₂ + ... + wₙxₙ + b
    ↓
Apply activation function: a = f(z)
    ↓
Output: a (prediction)
```

### 1.2 Stacking Perceptrons = Neural Network

**Multiple neurons in hidden layers:** Powerful learning

**Why multiple layers?**
- Each layer learns increasingly complex features
- Layer 1: learns simple patterns
- Layer 2: learns more complex patterns
- Layer 3: learns high-level concepts

---

## Part 2: Forward Propagation (15 minutes)

### 2.1 Computing the Forward Pass

**Step 1: Input to First Hidden Layer**
```
z₁ = W₁ x + b₁
a₁ = σ(z₁)
```

**Step 2: Hidden to Output Layer**
```
z₂ = W₂ a₁ + b₂
output = softmax(z₂)  [for multi-class]
       or σ(z₂)        [for binary]
```

---

## Part 3: Activation Functions (10 minutes)

### 3.1 Why We Need Activation Functions

**Without activation functions:**
- All layers become linear combinations
- Can't learn non-linear patterns

**With activation functions:**
- Introduce non-linearity
- Enable learning of complex patterns

### 3.2 Common Activation Functions

**Sigmoid**
```
σ(z) = 1 / (1 + e^(-z))
Range: (0, 1)
```

**ReLU**
```
f(z) = max(0, z)
Range: [0, ∞)
```

**Tanh**
```
f(z) = (e^z - e^(-z)) / (e^z + e^(-z))
Range: (-1, 1)
```

---

## Part 4: Backpropagation (15 minutes)

### 4.1 The Problem: Computing Gradients

How do we compute gradients for all weights?

**Solution: Use Chain Rule!**

### 4.2 Backpropagation Algorithm

**Forward pass:**
```
Compute predictions
```

**Backward pass:**
```
Using chain rule, compute gradients:
∂Loss/∂W = ∂Loss/∂output × ∂output/∂hidden × ... × ∂hidden/∂W
```

### 4.3 Weight Update

**After computing gradients:**
```
W_new = W_old - learning_rate × ∂Loss/∂W
```

---

## Part 5: Training Loop (5 minutes)

**Complete Training Process:**
```
1. Initialize weights randomly
2. For each epoch:
   a. For each batch:
      i. Forward pass
      ii. Compute loss
      iii. Backward pass
      iv. Update weights
   b. Evaluate on validation data
3. Evaluate on test data
```

---

## Key Takeaways

| Concept | Formula | Purpose |
|---------|---------|----------|
| **Forward Pass** | a = σ(Wx + b) | Compute predictions |
| **Activation** | σ(z) = 1/(1+e^(-z)) | Non-linearity |
| **Loss** | Cross-entropy or MSE | Measure error |
| **Backward Pass** | ∂Loss/∂W via chain rule | Compute gradients |
| **Weight Update** | W ← W - lr × ∇Loss | Improve model |

---

## Next Steps
- Complete notebook: `03_neural_networks.ipynb`
- Build a neural network from scratch
- Train on MNIST dataset
- Visualize learning process