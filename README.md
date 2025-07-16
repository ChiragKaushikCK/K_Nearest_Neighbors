# K_Nearest_Neighbors
KNN
<h2 id="knn-explanation-section" style="color: #333; font-family: 'Segoe UI', sans-serif; font-size: 2.5em; border-bottom: 3px solid #FFC107; padding-bottom: 10px;">
  📏 Understanding K-Nearest Neighbors (KNN) Regression
</h2>
<p style="font-size: 1.1em; color: #444; line-height: 1.6;">
  **K-Nearest Neighbors (KNN)** is a simple, non-parametric, and "lazy" machine learning algorithm that can be used for both classification and regression tasks. For regression, it predicts the value of a new data point by looking at the values of its "K" nearest neighbors in the training data.
</p>
<h3 style="color: #28A745; font-size: 1.8em; margin-top: 25px;">How KNN Regression Works:</h3>
<p style="font-size: 1.1em; color: #444; line-height: 1.6;">
  Imagine you want to predict the price of a new house. With KNN, you would:
</p>
<ul style="list-style-type: none; padding: 0; font-size: 1.1em; color: #444;">
  <li style="margin-bottom: 10px; background-color: #D4EDDA; padding: 10px 15px; border-radius: 8px; box-shadow: 0 1px 5px rgba(0,0,0,0.05);">
    <strong style="color: #28A745;">1. Choose 'K':</strong>
    <p style="margin-top: 5px;">Decide on the number of neighbors, 'K', you want to consider. This is a crucial hyperparameter. For example, if K=5, you'll look at the 5 closest houses.</p>
  </li>
  <li style="margin-bottom: 10px; background-color: #D4EDDA; padding: 10px 15px; border-radius: 8px; box-shadow: 0 1px 5px rgba(0,0,0,0.05);">
    <strong style="color: #28A745;">2. Calculate Distances:</strong>
    <p style="margin-top: 5px;">For a new data point (e.g., a new house whose price you want to predict), calculate its distance to every other data point in your training set. Common distance metrics include Euclidean distance, Manhattan distance, etc.</p>
  </li>
  <li style="margin-bottom: 10px; background-color: #D4EDDA; padding: 10px 15px; border-radius: 8px; box-shadow: 0 1px 5px rgba(0,0,0,0.05);">
    <strong style="color: #28A745;">3. Find the K-Nearest Neighbors:</strong>
    <p style="margin-top: 5px;">Identify the 'K' data points from the training set that are closest (have the smallest distances) to your new data point.</p>
  </li>
  <li style="margin-bottom: 10px; background-color: #D4EDDA; padding: 10px 15px; border-radius: 8px; box-shadow: 0 1px 5px rgba(0,0,0,0.05);">
    <strong style="color: #28A745;">4. Make the Prediction:</strong>
    <p style="margin-top: 5px;">For regression, the predicted value for the new data point is the **average (mean)** of the target variable values of its K-nearest neighbors. For example, if the 5 nearest houses sold for $300k, $310k, $290k, $320k, and $305k, the predicted price would be their average.</p>
  </li>
</ul>
<h3 style="color: #28A745; font-size: 1.8em; margin-top: 25px;">Key Characteristics of KNN:</h3>
<ul style="list-style-type: disc; padding-left: 20px; font-size: 1.1em; color: #444;">
  <li><strong style="color: #28A745;">Lazy Learning:</strong> KNN is a "lazy" algorithm because it does not build a model during the training phase. It simply stores the training data. All computation is performed during the prediction phase when a new data point arrives.</li>
  <li><strong style="color: #28A745;">Non-Parametric:</strong> It makes no assumptions about the underlying distribution of the data.</li>
  <li><strong style="color: #28A745;">Sensitive to Feature Scaling:</strong> Since it relies on distance calculations, features with larger scales will disproportionately influence the distance. It's crucial to scale your features (e.g., using StandardScaler) before applying KNN.</li>
  <li><strong style="color: #28A745;">Impact of 'K':</strong>
    <ul>
      <li>**Small K:** Can make the model sensitive to noise and outliers (high variance).</li>
      <li>**Large K:** Can smooth out predictions but might miss local patterns (high bias).</li>
    </ul>
  </li>
  <li><strong style="color: #28A745;">Computationally Intensive at Prediction:</strong> For large datasets, finding the nearest neighbors for each new prediction can be computationally expensive.</li>
</ul>
<h3 style="color: #28A745; font-size: 1.8em; margin-top: 25px;">When to Use KNN:</h3>
<ul style="list-style-type: disc; padding-left: 20px; font-size: 1.1em; color: #444;">
  <li>When the data is clean and low-dimensional.</li>
  <li>When the decision boundary is complex and non-linear.</li>
  <li>As a baseline model due to its simplicity.</li>
</ul>
