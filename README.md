<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

</head>
<body>

  <h1>Digit Classification using Multi-layer Perceptrons (MLP)</h1>

  <p><strong>This project performs digit classification using a Multi-layer Perceptron (MLP) on the provided digit images dataset.</strong> The goal is to train a model that can classify digits from a dataset with images of size 3x3 digits, leveraging the <code>MLPClassifier</code> from scikit-learn.</p>



  <h2 id="overview">Overview</h2>
  <p><strong>The task is to classify digit images using a Multi-layer Perceptron (MLP) classifier.</strong> The dataset includes training and test images of handwritten digits, with the goal of classifying each digit correctly. During training, an MLP model is trained, and evaluation is done on the test sets. Different performance scenarios, such as the color and grayscale differences in the test images, were explored.</p>

  <h2 id="data">Data</h2>
  <p>The dataset consists of:</p>
  <ul>
    <li><strong>Training Set:</strong> Images and corresponding digit labels from the file <code>training_3digits.hdf5</code>.</li>
    <li><strong>Testing Sets:</strong> Two testing sets (<code>testing_3digits_part1.hdf5</code> and <code>testing_3digits_part2.hdf5</code>) with images of digits and their corresponding labels.</li>
  </ul>
  <p>The dataset includes 2726 training images and 3147 images in each of the two test sets.</p>

  <h2 id="model-architecture">Model Architecture</h2>
  <p>The model uses a <strong>Multi-layer Perceptron (MLP)</strong> with one hidden layer and 10 neurons. The training process is conducted using the <code>MLPClassifier</code> from scikit-learn, and we evaluate its performance on both test sets.</p>

  <h2 id="results">Results</h2>
  <p>After training the MLP model on the training dataset, the following results were observed:</p>
  <ul>
    <li><strong>Accuracy on Test Set 1:</strong> 99.97%</li>
    <li><strong>Accuracy on Test Set 2:</strong> 0.0%</li>
  </ul>
  <p>The model performed well on Test Set 1, which had the same color distribution as the training set. However, it struggled significantly on Test Set 2 due to differences in color distribution, which highlights the model's reliance on color cues.</p>

  <h2 id="observations">Observations</h2>
  <p><strong>Color Dependence and Shortcut Learning:</strong> The model relied heavily on color cues rather than the actual features of the digits. This is evident from the high accuracy on Test Set 1 (same color distribution) and the extremely poor accuracy on Test Set 2 (different color distribution). This behavior is known as "shortcut learning," where the model exploits superficial correlations in the data rather than understanding the underlying patterns.</p>

  <h2 id="improvements">Improvements</h2>
  <p><strong>Converting Images to Grayscale:</strong> To mitigate the color dependence, images were converted to grayscale before training the model again.</p>
  <p>After converting to grayscale, the results were:</p>
  <ul>
    <li><strong>Accuracy on Test Set 1:</strong> 99.17%</li>
    <li><strong>Accuracy on Test Set 2:</strong> 16.65%</li>
  </ul>
  <p>While the grayscale conversion improved the model's generalization, Test Set 2 still posed a challenge due to possible residual color information and variations in the pixel intensity caused by different color distributions in the original images.</p>

  <h2 id="requirements">Requirements</h2>
  <ul>
    <li><strong>Python 3.x</strong></li>
    <li><strong>scikit-learn</strong> (for MLPClassifier)</li>
    <li><strong>numpy</strong> (for data manipulation)</li>
    <li><strong>matplotlib</strong> (for visualization)</li>
    <li><strong>OpenCV</strong> (for image processing)</li>
  </ul>

  <h2 id="how-to-run">How to Run</h2>
  <p>1. Clone the repository or download the necessary files.</p>
  <p>2. Install the required dependencies:</p>
  <pre><code>pip install scikit-learn numpy matplotlib opencv-python</code></pre>
  <p>3. Run the script to train and test the MLP model:</p>
  <pre><code>python digit_classification_mlp.py</code></pre>

</body>
</html>
