---
layout: default
title: Artifact 4 - AI Evolution Timeline
---

<a href="../../" class="back-btn">← Back to Portfolio</a>

# Artifact 4: 🧠 The Evolution of AI

<div class="timeline-hero">

  <div class="timeline-copy">
    <span class="timeline-tag">Interactive AI Timeline</span>
    <p>
      Explore how artificial intelligence evolved from early rule-based systems 
      into deep learning, transformers, and today’s multimodal AI.
      <br><br>
      👉 Click image to view AI timeline
    </p>
  </div>

  <div class="timeline-preview">
    <img 
      src="assets/ai-timeline-visual.svg" 
      alt="AI timeline preview"
      onclick="openTimelineModal(this.src)"
    >
  </div>

</div>

---

## 🧭 Explore the Timeline

<div class="timeline-container">

  <div class="timeline-line"></div>

  <div class="timeline-item" onclick="showInfo('1950')">1950</div>
  <div class="timeline-item" onclick="showInfo('1956')">1956</div>
  <div class="timeline-item" onclick="showInfo('1966')">1966</div>
  <div class="timeline-item" onclick="showInfo('1986')">1986</div>
  <div class="timeline-item" onclick="showInfo('1997')">1997</div>
  <div class="timeline-item" onclick="showInfo('2011')">2011</div>
  <div class="timeline-item" onclick="showInfo('2012')">2012</div>
  <div class="timeline-item" onclick="showInfo('2017')">2017</div>
  <div class="timeline-item" onclick="showInfo('2022')">2022</div>

</div>

<div id="timeline-info" class="timeline-info">
  <p>Click a year to see what happened.</p>
</div>

---

<details class="dropdown-section">
  <summary>✨ What stands out from AI history</summary>
  <div class="dropdown-content">
    <ul>
      <li>AI evolved through cycles of hype and setbacks</li>
      <li>Breakthroughs often followed improvements in computing power</li>
      <li>Modern AI is built on decades of foundational research</li>
    </ul>
  </div>
</details>

---

<details class="dropdown-section">
  <summary>💡 Why I included this in my portfolio</summary>
  <div class="dropdown-content">
    <p>
      I included this artifact to show AI as a long-term evolution rather than a sudden trend. 
      Looking at the timeline makes it easier to understand how today’s tools were shaped by 
      decades of experimentation, setbacks, and breakthroughs.
    </p>
  </div>
</details>

---

<!-- MODAL -->
<div id="timelineModal" class="timeline-modal" onclick="closeTimelineModal()">
  <span class="timeline-modal-close">&times;</span>
  <img id="timelineModalImg" class="timeline-modal-content">
</div>

---

<style>

/* HERO */
.timeline-hero {
  display: flex;
  gap: 40px;
  align-items: center;
  margin-bottom: 40px;
}

.timeline-copy {
  max-width: 420px;
}

.timeline-tag {
  display: inline-block;
  background: #eaf1ff;
  padding: 6px 12px;
  border-radius: 20px;
  font-size: 0.85rem;
  margin-bottom: 10px;
}

.timeline-preview img {
  width: 100%;
  max-width: 500px;
  border-radius: 16px;
  cursor: zoom-in;
  transition: 0.3s;
}

.timeline-preview img:hover {
  transform: scale(1.02);
}

/* TIMELINE */
.timeline-container {
  display: flex;
  gap: 20px;
  margin: 30px 0;
  flex-wrap: wrap;
}

.timeline-item {
  background: #f0f4ff;
  padding: 10px 14px;
  border-radius: 10px;
  cursor: pointer;
  font-weight: 600;
}

.timeline-item:hover {
  background: #dbe7ff;
}

.timeline-info {
  margin-top: 20px;
  padding: 20px;
  border-radius: 12px;
  background: #f9fbff;
}

/* DROPDOWN */
.dropdown-section {
  margin-top: 20px;
  border-radius: 12px;
  overflow: hidden;
  border: 1px solid #e0e6f0;
  background: #f9fbff;
}

.dropdown-section summary {
  cursor: pointer;
  padding: 14px;
  font-weight: 600;
}

.dropdown-content {
  padding: 14px;
}

/* MODAL */
.timeline-modal {
  display: none;
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.8);
  align-items: center;
  justify-content: center;
}

.timeline-modal-content {
  max-width: 90%;
  max-height: 90%;
}

.timeline-modal-close {
  position: absolute;
  top: 20px;
  right: 30px;
  color: white;
  font-size: 30px;
  cursor: pointer;
}

</style>

<script>

function showInfo(year) {
  const content = {
    "1950": "Alan Turing introduces the idea of machine intelligence.",
    "1956": "Dartmouth Conference establishes AI as a field.",
    "1966": "ELIZA demonstrates early natural language processing.",
    "1986": "Backpropagation advances neural networks.",
    "1997": "IBM Deep Blue defeats chess champion.",
    "2011": "IBM Watson wins Jeopardy.",
    "2012": "AlexNet sparks deep learning revolution.",
    "2017": "Transformers change NLP forever.",
    "2022": "Generative AI like ChatGPT emerges."
  };

  document.getElementById("timeline-info").innerHTML = `<p>${content[year]}</p>`;
}

function openTimelineModal(src) {
  document.getElementById("timelineModal").style.display = "flex";
  document.getElementById("timelineModalImg").src = src;
}

function closeTimelineModal() {
  document.getElementById("timelineModal").style.display = "none";
}

</script>
