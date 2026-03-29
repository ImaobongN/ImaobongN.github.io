---
layout: default
title: Artifact 3 – Deep Learning and Neural Networks
---

<style>
.artifact-hero {
  background: linear-gradient(135deg, #f8fafc 0%, #eef4ff 100%);
  border: 1px solid #e5e7eb;
  border-radius: 18px;
  padding: 1.5rem;
  margin: 1rem 0 1.5rem 0;
  box-shadow: 0 8px 24px rgba(15, 23, 42, 0.06);
}

.artifact-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1rem;
  margin: 1.25rem 0;
}

.artifact-card {
  background: #ffffff;
  border: 1px solid #e5e7eb;
  border-radius: 16px;
  padding: 1rem;
  box-shadow: 0 6px 18px rgba(15, 23, 42, 0.05);
}

.artifact-card h3 {
  margin-top: 0;
  margin-bottom: 0.5rem;
}

.visual-block {
  background: #ffffff;
  border: 1px solid #e5e7eb;
  border-radius: 18px;
  padding: 1rem;
  margin: 1rem 0;
  box-shadow: 0 6px 18px rgba(15, 23, 42, 0.05);
}

.visual-block img {
  width: 100%;
  border-radius: 12px;
}

.callout {
  border-left: 4px solid #c4b5fd;
  background: #faf5ff;
  padding: 0.9rem 1rem;
  border-radius: 10px;
  margin: 1rem 0;
}

.quick-points {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 0.85rem;
  margin: 1rem 0;
}

.quick-points div {
  background: #f8fafc;
  border: 1px solid #e5e7eb;
  border-radius: 14px;
  padding: 0.9rem;
}

.compare-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 0.75rem;
}

.compare-table th,
.compare-table td {
  border: 1px solid #e5e7eb;
  padding: 0.8rem;
  text-align: left;
}

.compare-table th {
  background: #f8fafc;
}

summary {
  cursor: pointer;
  font-weight: 700;
  padding: 0.75rem 0;
}

.details-card {
  background: #ffffff;
  border: 1px solid #e5e7eb;
  border-radius: 16px;
  padding: 0 1rem 0.75rem 1rem;
  margin: 0.9rem 0;
  box-shadow: 0 6px 18px rgba(15, 23, 42, 0.04);
}

.badge-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-top: 0.75rem;
}

.badge {
  background: #eef2ff;
  color: #4338ca;
  border-radius: 999px;
  padding: 0.35rem 0.75rem;
  font-size: 0.9rem;
}
</style>

# 🧠 Artifact 3: Deep Learning and Neural Networks

<div class="artifact-hero">
  <h2 style="margin-top:0;">From Understanding Concepts to Explaining Them Visually</h2>
  <p>
    This artifact highlights what I learned about neural networks, deep learning, and model selection in machine learning.
    My goal was to move beyond text-heavy explanation and present these concepts in a way that is simple, visual, and practical.
  </p>
  <div class="badge-row">
    <span class="badge">Neural Networks</span>
    <span class="badge">Deep Learning</span>
    <span class="badge">Model Selection</span>
    <span class="badge">Visual Communication</span>
  </div>
</div>

## Why This Artifact Matters

<div class="artifact-grid">
  <div class="artifact-card">
    <h3>Clear Explanation</h3>
    <p>I focused on making technical concepts easier to understand without losing accuracy.</p>
  </div>
  <div class="artifact-card">
    <h3>Decision Making</h3>
    <p>I show not only what machine learning and deep learning are, but when each one makes sense.</p>
  </div>
  <div class="artifact-card">
    <h3>Real World Relevance</h3>
    <p>The examples connect theory to familiar use cases like house pricing, speech recognition, and autonomous driving.</p>
  </div>
</div>

## Simple Explanation of a Neural Network

<div class="callout">
  A neural network is a system that learns patterns from data. It takes in information, processes it through layers, and produces a prediction or decision.
</div>

<div class="visual-block">
  <h3 style="margin-top:0;">Neural Network / Deep Learning Pipeline</h3>
  <img src="assets/dl-pipeline.svg" alt="Deep learning pipeline diagram showing input, hidden layers, feature extraction, and output">
</div>

<div class="quick-points">
  <div><strong>Input Layer</strong><br>Receives data such as numbers, text, or images.</div>
  <div><strong>Hidden Layers</strong><br>Identify patterns and relationships inside the data.</div>
  <div><strong>Output Layer</strong><br>Produces a result such as a label, prediction, or recommendation.</div>
</div>

## Machine Learning vs. Deep Learning

<table class="compare-table">
  <thead>
    <tr>
      <th>Feature</th>
      <th>Machine Learning</th>
      <th>Deep Learning</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Best for</td>
      <td>Structured data</td>
      <td>Images, audio, text, and other complex data</td>
    </tr>
    <tr>
      <td>Feature Engineering</td>
      <td>Usually manual</td>
      <td>Usually automatic</td>
    </tr>
    <tr>
      <td>Interpretability</td>
      <td>Higher</td>
      <td>Lower</td>
    </tr>
    <tr>
      <td>Data Requirements</td>
      <td>Works with smaller datasets</td>
      <td>Usually benefits from larger datasets</td>
    </tr>
    <tr>
      <td>Complexity</td>
      <td>Lower</td>
      <td>Higher</td>
    </tr>
  </tbody>
</table>

<div class="visual-block">
  <h3 style="margin-top:0;">Machine Learning Pipeline</h3>
  <img src="assets/ml-pipeline.svg" alt="Machine learning pipeline diagram showing input data, feature selection, model training, and output prediction">
</div>

## Real World Scenarios

<div class="artifact-grid">
  <div class="visual-block">
    <h3 style="margin-top:0;">🏠 House Price Prediction</h3>
    <img src="assets/house-pricing-flow.svg" alt="Diagram showing house features flowing into a model to predict house price">
    <p>This is a good example of machine learning because the data is structured and the relationship between features and output can be modeled directly.</p>
  </div>
  <div class="visual-block">
    <h3 style="margin-top:0;">🚗 Autonomous Driving</h3>
    <img src="assets/autonomous-driving-flow.svg" alt="Diagram showing camera image, object detection, and driving decision output">
    <p>This is a strong deep learning example because the system must process images, detect objects, and make fast decisions in real time.</p>
  </div>
</div>

## Choosing the Right Approach

<div class="visual-block">
  <h3 style="margin-top:0;">Model Selection Decision Tree</h3>
  <img src="assets/model-decision-tree.svg" alt="Decision tree showing whether to use machine learning or deep learning based on data type and dataset size">
</div>

## Click to Explore Key Learnings

<details class="details-card">
  <summary>📘 What I Learned About Neural Networks</summary>
  <p>
    Neural networks are powerful because they can detect patterns that may be too complex for traditional models.
    I learned that their strength comes from layer-based learning, where each layer captures increasingly meaningful information.
  </p>
</details>

<details class="details-card">
  <summary>📘 What I Learned About Deep Learning</summary>
  <p>
    Deep learning is especially useful for unstructured data because it can automatically extract features.
    This makes it valuable for tasks like image recognition, voice assistants, and autonomous systems.
  </p>
</details>

<details class="details-card">
  <summary>📘 What I Learned From Quiz Topics and Class Discussions</summary>
  <p>
    A major takeaway from class was the importance of understanding not just what a model does, but why one approach fits a problem better than another.
    I also strengthened my understanding of training, pattern recognition, feature extraction, prediction, and the tradeoff between simplicity and model complexity.
  </p>
</details>

<details class="details-card">
  <summary>📘 Key Insight</summary>
  <p>
    The most important lesson for me is that understanding machine learning and deep learning is not only about definitions.
    It is about knowing how to explain them simply, apply them thoughtfully, and select the right method for the problem at hand.
  </p>
</details>

## Reflection

This artifact reflects my growth in two areas. First, I developed a stronger understanding of neural networks and deep learning as practical tools for solving different types of problems. Second, I recognized that strong technical communication is not just about writing clearly. It is also about using visuals that help people understand concepts quickly.

In earlier work, I relied too heavily on explanation through text. In this version, I focused on visual reinforcement through diagrams, structured sections, and interactive collapsible content. That shift helped me communicate the material more effectively and made the artifact feel more like a professional portfolio piece rather than a class summary.

## Tools and Technologies Used

- GitHub Pages
- Markdown with embedded HTML/CSS
- SVG diagrams for visual explanation
- ChatGPT for brainstorming, structure, and clarity support

## AI Disclosure

ChatGPT was used to assist with brainstorming, organizing the artifact structure, and refining explanations for clarity.

[⬅ Back to Landing Page](index.html)
