🧠 Machine Learning Algorithm Atlas
AIML-501 · Portfolio Artifact 7

A visual guide to 10 machine learning algorithms, their learning approaches, application domains, and real-world applications—from structured data to computer vision, natural language processing, and generative AI.

[← Back to Portfolio](../../)
🔍 How Machine Learning Algorithms Connect
<div class="artifact-grid">
  <div class="artifact-card">
    <h3>🔵 Supervised Learning</h3>
    <p><strong>Learn from labeled examples.</strong> Models learn to predict known outcomes, such as a numerical value or category.</p>
    <p><strong>Common tasks:</strong> Regression, classification, and prediction.</p>
  </div>
  <div class="artifact-card">
    <h3>🟢 Unsupervised Learning</h3>
    <p><strong>Discover patterns without labels.</strong> Models identify groups, relationships, or simplified representations.</p>
    <p><strong>Common tasks:</strong> Clustering and dimensionality reduction.</p>
  </div>
  <div class="artifact-card">
    <h3>🟣 Deep Learning & Generative AI</h3>
    <p><strong>Learn complex representations.</strong> Neural networks process images, language, and other high-dimensional data.</p>
    <p><strong>Common tasks:</strong> Image recognition, language understanding, and content generation.</p>
  </div>
</div>Important distinction: Deep learning is a family of models, not a separate learning type. Neural networks can be trained using supervised, self-supervised, or other learning approaches.

🧩 Explore 10 Machine Learning Algorithms
🔵 Supervised Learning
<div class="artifact-grid">
  <div class="artifact-card">
    <h3>01 · Linear Regression</h3>
    <p><strong>How it works:</strong> Fits a linear relationship between input features and a continuous numerical output.</p>
    <p><strong>Domain:</strong> Tabular Data</p>
    <p><strong>Real-world application:</strong> Forecasting energy consumption based on operating conditions.</p>
  </div>
  <div class="artifact-card">
    <h3>02 · Logistic Regression</h3>
    <p><strong>How it works:</strong> Estimates the probability that an observation belongs to a particular class.</p>
    <p><strong>Domains:</strong> Tabular Data, NLP</p>
    <p><strong>Real-world application:</strong> Identifying spam emails using extracted text features.</p>
  </div>
  <div class="artifact-card">
    <h3>03 · Decision Tree</h3>
    <p><strong>How it works:</strong> Splits observations using feature-based questions until reaching a predicted outcome.</p>
    <p><strong>Domain:</strong> Tabular Data</p>
    <p><strong>Real-world application:</strong> Classifying product quality from inspection measurements.</p>
  </div>
  <div class="artifact-card">
    <h3>04 · Random Forest</h3>
    <p><strong>How it works:</strong> Combines predictions from multiple decision trees to improve reliability and reduce overfitting.</p>
    <p><strong>Domain:</strong> Tabular Data</p>
    <p><strong>Real-world application:</strong> Predicting equipment failures from sensor readings.</p>
  </div>
  <div class="artifact-card">
    <h3>05 · K-Nearest Neighbors (KNN)</h3>
    <p><strong>How it works:</strong> Classifies a new example using the labels of the most similar nearby training examples.</p>
    <p><strong>Domains:</strong> Tabular Data, Computer Vision</p>
    <p><strong>Real-world application:</strong> Recognizing image categories using extracted image features.</p>
  </div>
</div>🟢 Unsupervised Learning
<div class="artifact-grid">
  <div class="artifact-card">
    <h3>06 · K-Means Clustering</h3>
    <p><strong>How it works:</strong> Groups observations into K clusters by repeatedly assigning them to the nearest cluster center.</p>
    <p><strong>Domains:</strong> Tabular Data, Computer Vision</p>
    <p><strong>Real-world application:</strong> Grouping customers by purchasing patterns.</p>
  </div>
  <div class="artifact-card">
    <h3>07 · Principal Component Analysis (PCA)</h3>
    <p><strong>How it works:</strong> Projects data onto directions that preserve as much variance as possible while reducing dimensions.</p>
    <p><strong>Domains:</strong> Tabular Data, Computer Vision</p>
    <p><strong>Real-world application:</strong> Simplifying sensor measurements for visualization and analysis.</p>
  </div>
</div>🟣 Deep Learning & Generative AI
<div class="artifact-grid">
  <div class="artifact-card">
    <h3>08 · Convolutional Neural Network (CNN)</h3>
    <p><strong>Learning approach:</strong> Commonly supervised</p>
    <p><strong>How it works:</strong> Learns visual features through convolutional filters that detect patterns in images.</p>
    <p><strong>Domain:</strong> Computer Vision</p>
    <p><strong>Real-world application:</strong> Detecting manufacturing defects in product images.</p>
  </div>
  <div class="artifact-card">
    <h3>09 · Transformer</h3>
    <p><strong>Learning approach:</strong> Often self-supervised pretraining, followed by supervised fine-tuning</p>
    <p><strong>How it works:</strong> Uses attention to identify relationships between tokens or image patches.</p>
    <p><strong>Domains:</strong> NLP, Generative AI, Computer Vision</p>
    <p><strong>Real-world application:</strong> Summarizing technical reports and generating text.</p>
  </div>
  <div class="artifact-card">
    <h3>10 · Generative Adversarial Network (GAN)</h3>
    <p><strong>Learning approach:</strong> Commonly unsupervised adversarial training</p>
    <p><strong>How it works:</strong> Trains a generator to produce synthetic examples while a discriminator learns to distinguish generated examples from real ones.</p>
    <p><strong>Domains:</strong> Generative AI, Computer Vision</p>
    <p><strong>Real-world application:</strong> Creating synthetic images for model development.</p>
  </div>
</div>🧭 How to Choose the Right Model
<div class="artifact-grid">
  <div class="artifact-card">
    <h3>🎯 Predict</h3>
    <p>When labeled examples are available, consider supervised algorithms such as Decision Trees, Random Forests, or Linear Regression.</p>
  </div>
  <div class="artifact-card">
    <h3>🔎 Discover</h3>
    <p>When labels are unavailable, use K-Means to identify groups or PCA to reduce the number of features.</p>
  </div>
  <div class="artifact-card">
    <h3>✨ Create & Understand</h3>
    <p>For complex images and language, consider CNNs and Transformers. For synthetic image generation, consider GANs.</p>
  </div>
</div>📝 Personal Learning Reflection
Creating this algorithm atlas helped me understand that selecting a machine learning model depends on the problem being solved, the available data, and the desired output. Supervised learning is useful when examples have known labels, while unsupervised learning helps reveal patterns without predetermined categories. Deep learning extends these capabilities to complex information such as images and language.

I can connect these concepts to my work in engineering automation and software validation. For example, Random Forest could help identify patterns associated with equipment failures, while a Convolutional Neural Network could support automated visual inspection. Transformer models could also help summarize technical reports and make engineering documentation easier to navigate. This project strengthened my ability to communicate technical concepts and evaluate which AI approaches are most suitable for real-world challenges.
Portfolio Artifact · AIML-501
Educational overview. Some model architectures support multiple training approaches.
