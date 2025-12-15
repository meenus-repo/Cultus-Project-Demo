The Code implements the below tasks:

- Creates fake 2D data.
- Implements logistic regression from scratch.
- Trains it using gradient descent.
- Evaluates accuracy.
- Visualizes decision boundary + training loss.


In detail:

Step 1: Create and Split Data
- make_blobs(...) → generates synthetic 2D data points grouped into 2 clusters (like fake data for testing).
- train_test_split(...) → splits data into training (80%) and testing (20%) sets.
- Prints how many samples are in each set.
- 
Step 2: Helper Functions
- Sigmoid function:
Converts any number into a probability between 0 and 1.
Formula: \sigma (z)=\frac{1}{1+e^{-z}}
- Binary Cross Entropy (Log Loss):
Measures how far predictions are from actual labels (lower = better).
Formula: -\frac{1}{N}\sum [y\log (p)+(1-y)\log (1-p)]

Step 3: Logistic Regression Class
This is a custom implementation of logistic regression using gradient descent.
- Initialization:
- Start with weights = 0, bias = 0.
- fit() method (training loop):
- Compute predictions using sigmoid.
- Calculate gradients (how much to adjust weights/bias).
- Update weights and bias using learning rate.
- Track cost (loss) at each iteration.
- Print cost every 200 iterations.
- predict():
Returns class labels (0 or 1) based on probability ≥ 0.5.
- predict_proba():
Returns raw probabilities (between 0 and 1).
Step 4: Train the Model
- Creates a logistic regression model with learning_rate=0.1 and 1000 iterations.
- Fits (trains) it on training data.
Step 5: Evaluate
- Predicts on test data.
- Calculates accuracy = % of correct predictions.
Step 6: Visualization
- Left plot: Shows test data points (red = class 0, blue = class 1).
- Right plot: Same data but adds the decision boundary (black line) where probability = 0.5.
- Final plot: Shows how training loss decreases over iterations (convergence).






