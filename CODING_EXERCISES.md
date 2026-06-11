# HANDS-ON CODING EXERCISES
# Complete Exercise Set for All Modules

---

# MODULE 1: MATHEMATICAL FOUNDATIONS - CODING EXERCISES

## Exercise Set 1: Vectors and Matrices Operations

### Exercise 1.1: Create and Manipulate Vectors
```python
import numpy as np

# TODO: Create a vector with values [1, 2, 3, 4, 5]
# TODO: Print its shape
# TODO: Calculate the sum of all elements
# TODO: Multiply each element by 2
# TODO: Calculate the mean

# SOLUTION:
v = np.array([1, 2, 3, 4, 5])
print(f"Shape: {v.shape}")
print(f"Sum: {np.sum(v)}")
v_doubled = v * 2
print(f"Doubled: {v_doubled}")
print(f"Mean: {np.mean(v)}")
```

### Exercise 1.2: Matrix Operations
```python
# TODO: Create two 2x2 matrices A and B
# TODO: Add them together
# TODO: Multiply them element-wise
# TODO: Transpose matrix A

# SOLUTION:
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])
print(f"A + B =\n{A + B}")
print(f"A * B (element-wise) =\n{A * B}")
print(f"A.T =\n{A.T}")
```

### Exercise 1.3: Dot Product Calculation
```python
# TODO: Create vectors u = [1, 2, 3] and v = [4, 5, 6]
# TODO: Calculate dot product
# TODO: Verify by manual calculation
# TODO: Check if perpendicular vectors [1,0] and [0,1] have dot product 0

# SOLUTION:
u = np.array([1, 2, 3])
v = np.array([4, 5, 6])
dot = np.dot(u, v)
manual = 1*4 + 2*5 + 3*6
print(f"Dot product (numpy): {dot}")
print(f"Dot product (manual): {manual}")

perp1 = np.array([1, 0])
perp2 = np.array([0, 1])
print(f"Dot product of perpendicular vectors: {np.dot(perp1, perp2)}")
```

---

## Exercise Set 2: Matrix Multiplication

### Exercise 2.1: Matrix-Vector Multiplication
```python
# TODO: Create matrix A (3x2) and vector x (2x1)
# TODO: Multiply A @ x
# TODO: Verify result manually

# SOLUTION:
A = np.array([[1, 2], [3, 4], [5, 6]])
x = np.array([1, 2])
result = A @ x
print(f"A @ x = {result}")
print(f"Manual: {[1*1 + 2*2, 3*1 + 4*2, 5*1 + 6*2]}")
```

### Exercise 2.2: Matrix-Matrix Multiplication
```python
# TODO: Create A (2x3) and B (3x2)
# TODO: Multiply A @ B
# TODO: What shape is result? (Expected: 2x2)
# TODO: Try B @ A. What shape? (Expected: 3x3)

# SOLUTION:
A = np.array([[1, 2, 3], [4, 5, 6]])
B = np.array([[1, 2], [3, 4], [5, 6]])
AB = A @ B
BA = B @ A
print(f"A @ B shape: {AB.shape}, result:\n{AB}")
print(f"B @ A shape: {BA.shape}, result:\n{BA}")
print("Note: Matrix multiplication is NOT commutative!")
```

---

## Exercise Set 3: Vector Norms

### Exercise 3.1: Calculate L2 Norm
```python
# TODO: Create vector v = [3, 4]
# TODO: Calculate norm manually: sqrt(3^2 + 4^2)
# TODO: Calculate using np.linalg.norm()
# TODO: Verify they match

# SOLUTION:
v = np.array([3, 4])
norm_manual = np.sqrt(3**2 + 4**2)
norm_numpy = np.linalg.norm(v)
print(f"Manual norm: {norm_manual}")
print(f"NumPy norm: {norm_numpy}")
```

### Exercise 3.2: Normalize Vectors
```python
# TODO: Create vector v = [1, 2, 2]
# TODO: Calculate its norm
# TODO: Normalize it: v_normalized = v / norm
# TODO: Verify normalized vector has norm = 1

# SOLUTION:
v = np.array([1, 2, 2])
norm = np.linalg.norm(v)
v_normalized = v / norm
print(f"Original norm: {np.linalg.norm(v)}")
print(f"Normalized: {v_normalized}")
print(f"Normalized norm: {np.linalg.norm(v_normalized)}")
```

---

## Exercise Set 4: Derivatives

### Exercise 4.1: Calculate Derivative Manually
```python
# For f(x) = x^2, derivative f'(x) = 2x
# TODO: Calculate f'(x) at x = 1, 2, 3
# TODO: Plot f(x) and f'(x)

# SOLUTION:
import matplotlib.pyplot as plt

x_vals = np.array([1, 2, 3])
f_prime = 2 * x_vals
print(f"f'(x) at x=1,2,3: {f_prime}")

x = np.linspace(-3, 3, 100)
f = x**2
f_prime_plot = 2*x

plt.figure(figsize=(10, 4))
plt.subplot(1, 2, 1)
plt.plot(x, f)
plt.title("f(x) = x^2")
plt.grid()

plt.subplot(1, 2, 2)
plt.plot(x, f_prime_plot)
plt.title("f'(x) = 2x")
plt.grid()
plt.show()
```

---

## Exercise Set 5: Gradient Descent

### Exercise 5.1: Gradient Descent Step-by-Step
```python
# TODO: Implement gradient descent to minimize f(x) = (x-5)^2
# TODO: Start from x = 0
# TODO: Use learning rate = 0.1
# TODO: Run for 10 iterations
# TODO: Print x at each iteration

# SOLUTION:
def f(x):
    return (x - 5)**2

def df(x):
    return 2 * (x - 5)

x = 0
learning_rate = 0.1

for i in range(10):
    gradient = df(x)
    x = x - learning_rate * gradient
    print(f"Iteration {i}: x = {x:.4f}, f(x) = {f(x):.4f}")
```

---

# MODULE 2: SUPERVISED LEARNING - CODING EXERCISES

## Exercise Set 1: Linear Regression

### Exercise 1.1: Implement MSE Loss
```python
# TODO: Given actual values and predictions
# TODO: Calculate MSE loss manually
# TODO: Verify with formula: MSE = mean((y_true - y_pred)^2)

# SOLUTION:
y_true = np.array([100, 200, 300])
y_pred = np.array([95, 210, 290])

mse = np.mean((y_true - y_pred)**2)
print(f"MSE: {mse}")

# Manual calculation
errors = y_true - y_pred
squared_errors = errors**2
mse_manual = np.mean(squared_errors)
print(f"MSE (manual): {mse_manual}")
```

---

## Exercise Set 2: Logistic Regression

### Exercise 2.1: Sigmoid Function
```python
# TODO: Implement sigmoid function
# TODO: Calculate sigmoid(0), sigmoid(-5), sigmoid(5)
# TODO: Plot sigmoid curve

# SOLUTION:
def sigmoid(z):
    return 1 / (1 + np.exp(-z))

print(f"sigmoid(0) = {sigmoid(0)}")
print(f"sigmoid(-5) = {sigmoid(-5)}")
print(f"sigmoid(5) = {sigmoid(5)}")

z = np.linspace(-10, 10, 100)
y = sigmoid(z)
plt.plot(z, y)
plt.axhline(y=0.5, color='r', linestyle='--', label='threshold')
plt.xlabel('z')
plt.ylabel('sigmoid(z)')
plt.title('Sigmoid Function')
plt.legend()
plt.grid()
plt.show()
```

---

# MODULE 3: DEEP LEARNING - CODING EXERCISES

## Exercise Set 1: Forward Propagation

### Exercise 1.1: Manual Forward Pass
```python
# TODO: Implement forward pass for 2-layer network
# TODO: Input: x = [1, 2]
# TODO: Layer 1: 2 neurons with ReLU
# TODO: Layer 2: 1 neuron with sigmoid

# SOLUTION:
def relu(z):
    return np.maximum(0, z)

def sigmoid(z):
    return 1 / (1 + np.exp(-np.clip(z, -500, 500)))

x = np.array([1, 2])
W1 = np.random.randn(2, 2)
b1 = np.zeros(2)
W2 = np.random.randn(2, 1)
b2 = np.zeros(1)

# Forward pass
z1 = x @ W1 + b1
a1 = relu(z1)
z2 = a1 @ W2 + b2
a2 = sigmoid(z2)

print(f"z1: {z1}, a1: {a1}")
print(f"z2: {z2}, a2: {a2}")
```

---

# CHALLENGE EXERCISES

## Challenge 1: Compare Learning Rates
```python
# TODO: Train model with learning rates: 0.001, 0.01, 0.1, 1.0
# TODO: Plot loss curves for all
# TODO: Which converges fastest?

# Expected: Learning rate too small → slow, too large → diverges
```

## Challenge 2: Implement Custom Activation Function
```python
# TODO: Create Leaky ReLU: f(z) = z if z > 0 else 0.01*z
# TODO: Compare with regular ReLU on a training task
# TODO: Which performs better?
```

## Challenge 3: Build Your Own Neural Network
```python
# TODO: Create a 2-layer network from scratch
# TODO: Implement forward and backward pass
# TODO: Train on synthetic data
# TODO: Achieve > 80% accuracy

# Expected: Functional neural network with good understanding
```

---

# SOLUTIONS SUMMARY

All solutions are provided above. Key concepts:
1. Always verify calculations manually before trusting code
2. Visualize results to understand what's happening
3. Try different hyperparameters and compare
4. Start simple, then add complexity
5. Test on both training and test data
