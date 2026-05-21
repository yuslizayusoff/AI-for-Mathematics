# Module 1: Mathematical Foundations
## Duration: 60 minutes

### Learning Objectives
By the end of this module, students will understand:
- ✅ Core linear algebra concepts (vectors, matrices, operations)
- ✅ Essential calculus concepts (derivatives, gradients)
- ✅ Why these concepts are crucial for machine learning
- ✅ How to manipulate mathematical objects in Python

---

## Part 1: Linear Algebra Fundamentals (30 minutes)

### 1.1 Vectors and Matrices

**What is a Vector?**
- An ordered list of numbers
- In ML: represents data points, features, or weights
- Example: A student's test scores = [85, 90, 78, 92]

**What is a Matrix?**
- A 2D array of numbers organized in rows and columns
- Represents multiple data points or transformations

### 1.2 Matrix Operations

**Addition & Subtraction**
- Add/subtract corresponding elements

**Matrix Multiplication**
- Used extensively in neural networks
- Not element-wise multiplication!

**Why it matters for ML:**
- Neural network forward pass: `output = weight_matrix × input_vector`
- Batch processing: multiply matrix of data by weight matrix

### 1.3 Key Linear Algebra Concepts

**Transpose**
- Flip rows and columns
- Symbol: A^T

**Dot Product**
- Measure of similarity between two vectors
- Core operation in ML algorithms

**Norm (Magnitude)**
- Length of a vector
- L2 norm (Euclidean): ||v|| = √(v1² + v2² + ... + vn²)

---

## Part 2: Calculus Foundations (20 minutes)

### 2.1 Derivatives

**What is a Derivative?**
- Rate of change of a function
- Shows how quickly a function changes
- Critical for optimization in ML

**Intuition:**
- Derivative is the slope of the tangent line
- Tells us which direction to move to increase/decrease the function

### 2.2 Gradients

**What is a Gradient?**
- Derivative for functions with multiple variables
- Vector of partial derivatives

**Why gradients matter:**
- **Gradient Descent**: Move in opposite direction of gradient to minimize error
- Foundation of training neural networks
- Tells us: "Which way should I change my weights to reduce error?"

### 2.3 Chain Rule

**The Chain Rule**
- How to compute derivatives of composite functions
- Essential for backpropagation in neural networks

**Backpropagation is just the chain rule applied repeatedly!**

---

## Part 3: Optimization (10 minutes)

### 3.1 Gradient Descent

**The Algorithm:**
1. Start with random weights
2. Calculate gradient (which way to change weights?)
3. Move in opposite direction of gradient
4. Repeat until convergence

```
w_new = w_old - learning_rate × ∇error
```

### 3.2 Learning Rate

**What is Learning Rate?**
- Controls how big each step is
- Too small: takes forever to converge
- Too large: might overshoot the minimum

---

## Key Takeaways

| Concept | Purpose | ML Application |
|---------|---------|----------------|
| **Vectors & Matrices** | Store & manipulate data | Represent features, weights |
| **Matrix Multiplication** | Transform data | Neural network forward pass |
| **Derivatives** | Measure change | Optimization |
| **Gradients** | Direction of steepest change | Training direction |
| **Chain Rule** | Composite derivatives | Backpropagation |
| **Gradient Descent** | Find minimum | Train models |

---

## Next Steps
- Complete the hands-on notebook: `01_linear_algebra_calculus.ipynb`
- Implement basic operations in Python
- Visualize gradients and optimization