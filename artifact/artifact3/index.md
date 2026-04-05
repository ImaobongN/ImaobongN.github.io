---
layout: default
title: Artifact 3 – Deep Learning and Neural Networks
---

<a href="../../" class="back-btn">← Back to Portfolio</a>

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
  <h2 style="margin-top:0;">Understanding AI Concepts Through Visual Explanation</h2>
  <p>
    This artifact builds on my earlier machine learning work by focusing on neural networks, deep learning, and model selection.
    I wanted the page to match the clean card-based feel of my portfolio while using visuals and interactive sections to explain ideas more clearly.
  </p>
  <div class="badge-row">
    <span class="badge">Neural Networks</span>
    <span class="badge">Deep Learning</span>
    <span class="badge">Model Selection</span>
    <span class="badge">Portfolio Artifact</span>
  </div>
</div>

## Why This Artifact Matters

<div class="artifact-grid">
  <div class="artifact-card">
    <h3>🧩 Simplifies Complexity</h3>
    <p>This page explains technical concepts in a way that feels clear, practical, and approachable.</p>
  </div>
  <div class="artifact-card">
    <h3>🎯 Supports Decision Making</h3>
    <p>It shows when machine learning works best and when deep learning is the stronger choice.</p>
  </div>
  <div class="artifact-card">
    <h3>🌍 Connects to Real Use Cases</h3>
    <p>Examples like house pricing and autonomous driving make the concepts easier to see and remember.</p>
  </div>
</div>

## A Simple Explanation of a Neural Network

<div class="callout">
  A neural network is a system that learns patterns from data. It takes in information, processes it through layers, and produces a prediction or decision.
</div>

<div class="visual-block">
  <h3 style="margin-top:0;">Deep Learning / Neural Network Flow</h3>
  <img src="assets/dl-pipeline.svg" alt="Deep learning pipeline diagram showing input, hidden layers, feature extraction, and output">
</div>

<div class="quick-points">
  <div><strong>Input Layer</strong><br>Receives data such as numbers, text, or images.</div>
  <div><strong>Hidden Layers</strong><br>Detect patterns and relationships within the data.</div>
  <div><strong>Output Layer</strong><br>Produces a result such as a prediction, label, or recommendation.</div>
</div>

## Machine Learning vs Deep Learning

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
      <td>Images, speech, text, and other complex data</td>
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
      <td>Often needs larger datasets</td>
    </tr>
    <tr>
      <td>Complexity</td>
      <td>Lower</td>
      <td>Higher</td>
    </tr>
  </tbody>
</table>

<div class="visual-block">
  <h3 style="margin-top:0;">Machine Learning Flow</h3>
  <img src="assets/ml-pipeline.svg" alt="Machine learning pipeline diagram showing input data, feature selection, model training, and output prediction">
</div>

## Real-World Scenarios

<div class="artifact-grid">
  <div class="visual-block">
    <h3 style="margin-top:0;">🏠 House Price Prediction</h3>
    
    <a href="assets/house-pricing-flow.svg" target="_blank">
      <img src="assets/house-pricing-flow.svg" alt="Diagram showing house features flowing into a model to predict house price">
    </a>

    <p>This scenario fits machine learning well because the data is structured and the goal is a direct prediction.</p>
  </div>

  <div class="visual-block">
    <h3 style="margin-top:0;">🚗 Autonomous Driving</h3>
    
    <a href="assets/autonomous-driving-flow.svg" target="_blank">
      <img src="assets/autonomous-driving-flow.svg" alt="Diagram showing camera image, object detection, and driving decision output">
    </a>

    <p>This scenario fits deep learning because the system must interpret images and make fast, complex decisions.</p>
  </div>
</div>

## Choosing the Right Approach

<div class="visual-block">
  <h3 style="margin-top:0;">Model Selection Decision Tree</h3>
  <img src="assets/model-decision-tree.svg" alt="Decision tree showing whether to use machine learning or deep learning based on data type and dataset size">
</div>

## Click to Explore What I Learned

<details class="details-card">
  <summary>📘 Neural Networks</summary>
  <p>
    I learned that neural networks become powerful because each layer helps the model recognize patterns at a deeper level.
    Instead of relying only on human-defined rules, the system learns from examples and improves through training.
  </p>
</details>

<details class="details-card">
  <summary>📘 Deep Learning</summary>
  <p>
    Deep learning is especially useful for unstructured data. It can automatically extract meaningful features from images, audio, and text, which makes it valuable for modern AI applications.
  </p>
</details>

<details class="details-card">
  <summary>📘 Key Insight</summary>
  <p>
    My biggest takeaway is that understanding AI is not just about defining terms. It is about explaining concepts simply, selecting the right method, and connecting technical ideas to real-world use.
  </p>
</details>

## Tools and Technologies Used

- GitHub Pages
- Markdown with embedded HTML/CSS
- SVG diagrams for visual explanation
- ChatGPT for brainstorming, structure, and clarity support

