# ASSESSMENT MATERIALS: Quizzes & Projects
# Complete Assessment Suite for AI for Mathematics Course

---

# MODULE 1: MATHEMATICAL FOUNDATIONS - QUIZ

## Quiz 1.1: Vectors and Matrices (15 minutes)

**Question 1.1.1:** What is the dimension of the following vector?
```
v = [2, 3, 5, 7]
```
a) 1  
b) 4 ✓  
c) 2  
d) 7  

**Question 1.1.2:** Calculate the dot product of:
```
a = [1, 2, 3]
b = [4, 5, 6]
```
a) [4, 10, 18]  
b) 32 ✓  
c) 24  
d) [5, 7, 9]  

**Question 1.1.3:** What is the norm of vector v = [3, 4]?
a) 7  
b) 1  
c) 5 ✓  
d) 25  

**Question 1.1.4:** When is the dot product of two vectors equal to zero?
a) Always  
b) When they point in the same direction  
c) When they are perpendicular ✓  
d) Never  

**Question 1.1.5:** For matrix A (3×2) and matrix B (2×4), what is the shape of A × B?
a) 3×4 ✓  
b) 2×2  
c) Cannot be multiplied  
d) 4×3  

---

## Quiz 1.2: Calculus and Optimization (15 minutes)

**Question 1.2.1:** What is the derivative of f(x) = x²?
a) x  
b) 2x ✓  
c) 1  
d) 2  

**Question 1.2.2:** What does a gradient point to?
a) The steepest uphill direction ✓  
b) The steepest downhill direction  
c) The direction of maximum speed  
d) The direction perpendicular to the surface  

**Question 1.2.3:** In gradient descent, what does the learning rate control?
a) The number of iterations  
b) The size of each step ✓  
c) The initial weights  
d) The final accuracy  

**Question 1.2.4:** What is the chain rule used for?
a) Combining probabilities  
b) Computing derivatives of composite functions ✓  
c) Multiplying matrices  
d) Normalizing vectors  

**Question 1.2.5:** If learning rate is too large in gradient descent:
a) It converges faster  
b) It might diverge or overshoot ✓  
c) It has no effect  
d) It always reaches the minimum  

---

## Module 1 Project: Gradient Descent Optimization (30 minutes)

**Objective:** Implement gradient descent to minimize a quadratic function

**Problem:**
```
Minimize: f(x, y) = (x - 4)² + (y + 2)²
```

**Tasks:**
1. Write Python code to implement gradient descent
2. Start from point (0, 0)
3. Use learning rate = 0.1
4. Run for 50 iterations
5. Plot the optimization path

**Deliverables:**
- Code file showing gradient descent implementation
- Plot showing path to minimum
- Final values of x and y (should be close to 4 and -2)
- Number of iterations needed to converge within 0.01 of minimum

**Success Criteria:**
- ✓ Correctly implements gradient descent
- ✓ Reaches minimum (x ≈ 4, y ≈ -2)
- ✓ Clean, well-commented code
- ✓ Clear visualization

---

# MODULE 2: SUPERVISED LEARNING - QUIZ

## Quiz 2.1: Linear & Logistic Regression (15 minutes)

**Question 2.1.1:** In linear regression y = mx + b, what does m represent?
a) The y-intercept  
b) The slope ✓  
c) The prediction  
d) The error  

**Question 2.1.2:** What does MSE Loss measure?
a) Average absolute error  
b) Average squared error ✓  
c) Maximum error  
d) Minimum error  

**Question 2.1.3:** Why do we square the errors in MSE?
a) To make them always positive  
b) To penalize large errors more  
c) Both A and B ✓  
d) To make calculations easier  

**Question 2.1.4:** What range of values does sigmoid output?
a) Any value (−∞ to +∞)  
b) 0 to 1 ✓  
c) −1 to 1  
d) Depends on input  

**Question 2.1.5:** When should you use logistic regression instead of linear regression?
a) Always  
b) For classification problems ✓  
c) For continuous predictions  
d) Never  

---

## Quiz 2.2: Model Evaluation (15 minutes)

**Question 2.2.1:** What does accuracy measure?
a) Proportion of correct predictions ✓  
b) Proportion of positive predictions that were correct  
c) Proportion of actual positives that were predicted  
d) Average prediction value  

**Question 2.2.2:** What is precision?
a) TP / (TP + FN)  
b) TP / (TP + FP) ✓  
c) TP / (TP + TN)  
d) TP / (All predictions)  

**Question 2.2.3:** When is F1 score most useful?
a) Always  
b) For balanced datasets  
c) For imbalanced datasets ✓  
d) Never  

**Question 2.2.4:** A model predicts "sick" for everyone. What is its recall?
a) 0  
b) 50%  
c) 100% ✓  
d) Undefined  

**Question 2.2.5:** What does a confusion matrix show?
a) Network confusion  
b) Distribution of predictions vs actual ✓  
c) Model confusion probability  
d) Confused predictions only  

---

## Module 2 Project: Build a Classifier (30 minutes)

**Objective:** Build and evaluate a logistic regression classifier

**Dataset:** Generate your own or use a provided dataset with at least 200 samples

**Tasks:**
1. Load/generate data with 2+ features and binary labels
2. Split into train/test (80/20)
3. Train logistic regression model from scratch (or use sklearn)
4. Calculate accuracy, precision, recall, F1 score
5. Plot decision boundary
6. Create confusion matrix

**Deliverables:**
- Well-organized Python code
- Train/test accuracy
- All 4 metrics calculated
- Decision boundary visualization
- Confusion matrix visualization
- Brief report (1 page) explaining results

**Success Criteria:**
- ✓ Code runs without errors
- ✓ All metrics calculated correctly
- ✓ Clear visualizations
- ✓ Test accuracy > 70%
- ✓ Thoughtful interpretation of results

---

# MODULE 3: DEEP LEARNING - QUIZ

## Quiz 3.1: Neural Network Basics (15 minutes)

**Question 3.1.1:** What is a neuron in a neural network?
a) A biological cell  
b) A unit that performs weighted sum + activation ✓  
c) A layer in the network  
d) The output of the network  

**Question 3.1.2:** What is the purpose of activation functions?
a) To add randomness  
b) To introduce non-linearity ✓  
c) To normalize data  
d) To count neurons  

**Question 3.1.3:** Which activation function is most popular for hidden layers?
a) Sigmoid  
b) Tanh  
c) ReLU ✓  
d) Linear  

**Question 3.1.4:** What does forward propagation do?
a) Updates weights based on errors  
b) Computes predictions by passing data through network ✓  
c) Calculates gradients  
d) Normalizes inputs  

**Question 3.1.5:** A network has 100 neurons in input, 50 in hidden, 10 in output. How many weight parameters?
a) 160  
b) 5000 ✓  
c) 1000  
d) 500  

---

## Quiz 3.2: Backpropagation (15 minutes)

**Question 3.2.1:** What is backpropagation?
a) Reversing the network  
b) Computing gradients using chain rule ✓  
c) Undoing training  
d) Going backward through data  

**Question 3.2.2:** Why do we use the chain rule in backpropagation?
a) To multiply by chain links  
b) To compute how deep weights affect output ✓  
c) To avoid computing gradients  
d) To speed up training  

**Question 3.2.3:** In which direction do we update weights during training?
a) Uphill (positive gradient direction)  
b) Perpendicular to gradient  
c) Downhill (negative gradient direction) ✓  
d) Random direction  

**Question 3.2.4:** What is the relationship between backpropagation and the chain rule from Module 1?
a) No relationship  
b) Backpropagation is chain rule applied multiple times ✓  
c) They are opposites  
d) Chain rule is more advanced  

**Question 3.2.5:** If a weight has gradient = 0.5 and learning rate = 0.01, how much does weight change?
a) 0.5  
b) 0.01  
c) 0.005 ✓  
d) 50  

---

## Module 3 Project: Build Your Own Neural Network (45 minutes)

**Objective:** Build a multi-layer neural network from scratch or using TensorFlow

**Dataset:** Use MNIST (provided) or another image classification dataset

**Tasks:**
1. Build network: [784, 128, 64, 10] (or similar)
2. Implement or use forward pass
3. Implement or use backpropagation
4. Train for 20+ epochs
5. Evaluate on test set
6. Visualize sample predictions

**Deliverables:**
- Well-organized, commented code
- Network architecture diagram
- Training loss curve
- Final test accuracy
- Visualization of 10 sample predictions
- Brief report explaining architecture choices

**Success Criteria:**
- ✓ Code runs without errors
- ✓ Test accuracy > 95%
- ✓ Clear visualizations
- ✓ Understands why you chose that architecture
- ✓ Can explain forward/backward pass

---

# FINAL CAPSTONE PROJECT (60 minutes)

## Integrate All Modules: Build End-to-End ML Pipeline

**Objective:** Create a complete machine learning project from data to evaluation

**Project Options:**
1. **Iris Classification** - Predict flower species from measurements
2. **Housing Price Prediction** - Predict prices from features
3. **Handwritten Digit Recognition** - MNIST classification
4. **Custom Dataset** - Your choice of real-world problem

**Requirements:**

### Part 1: Data Preparation (Module 1 - Math Foundations)
- Load data
- Explore dimensions (vectors, matrices)
- Normalize/scale features
- Visualize relationships

### Part 2: Model Selection & Training (Module 2 - Supervised Learning)
- Try at least 2 algorithms (linear regression, logistic regression, etc.)
- Train both models
- Calculate loss functions
- Plot learning curves

### Part 3: Deep Learning Enhancement (Module 3 - Deep Learning)
- Build a neural network
- Train with backpropagation
- Compare to simpler models
- Visualize predictions

### Part 4: Evaluation & Report
- Compare all models on test set
- Create comprehensive metrics report
- Visualize confusion matrices and decision boundaries
- Write 2-3 page technical report including:
  - Problem statement
  - Data description
  - Models tested
  - Results and comparison
  - Conclusions
  - Future improvements

**Deliverables:**
- Complete Python code (well-organized, commented)
- Jupyter notebook showing all steps
- Visualizations and plots
- Technical report (PDF, 2-3 pages)
- Presentation slides (5-10 slides)

**Success Criteria:**
- ✓ All components working correctly
- ✓ Coherent project from start to finish
- ✓ Thoughtful model selection
- ✓ Comprehensive evaluation
- ✓ Clear communication of results
- ✓ Demonstrates understanding of all 3 modules

**Grading Rubric:**
- Code quality: 20%
- Mathematical correctness: 20%
- Model performance: 20%
- Visualization and presentation: 20%
- Technical report quality: 20%

---

# ANSWER KEY

## Module 1 Quiz Answers:
```
1.1.1: b) 4
1.1.2: b) 32
1.1.3: c) 5
1.1.4: c) Perpendicular
1.1.5: a) 3×4
1.2.1: b) 2x
1.2.2: a) Steepest uphill
1.2.3: b) Step size
1.2.4: b) Composite functions
1.2.5: b) Diverge or overshoot
```

## Module 2 Quiz Answers:
```
2.1.1: b) Slope
2.1.2: b) Average squared error
2.1.3: c) Both A and B
2.1.4: b) 0 to 1
2.1.5: b) Classification
2.2.1: a) Correct predictions
2.2.2: b) TP / (TP + FP)
2.2.3: c) Imbalanced
2.2.4: c) 100%
2.2.5: b) Predictions vs actual
```

## Module 3 Quiz Answers:
```
3.1.1: b) Weighted sum + activation
3.1.2: b) Non-linearity
3.1.3: c) ReLU
3.1.4: b) Pass through network
3.1.5: b) 5000
3.2.1: b) Chain rule
3.2.2: b) How weights affect output
3.2.3: c) Downhill
3.2.4: b) Chain rule applied multiple times
3.2.5: c) 0.005
```

---

# GRADING GUIDELINES

## Quiz Grading:
- 5 questions per quiz
- 2 points each = 10 points total
- 8+ = Pass, 6-8 = Review, <6 = Retest

## Project Grading (100 points each):
- Correctness: 40 points
- Code quality: 20 points
- Visualization: 20 points
- Report: 20 points

## Capstone Grading (200 points):
- Implementation: 80 points
- Analysis: 50 points
- Documentation: 40 points
- Presentation: 30 points
