---
layout: default
title: The Evolution of AI
---

<a href="../../" class="back-btn">← Back to Portfolio</a>

<style>
  .timeline-page {
    --bg: #f8fafc;
    --card: #ffffff;
    --text: #1f2937;
    --muted: #6b7280;
    --line: #dbeafe;
    --accent: #2563eb;
    --accent-soft: #eff6ff;
    --shadow: 0 10px 30px rgba(15, 23, 42, 0.08);
  }

  .timeline-page h1,
  .timeline-page h2,
  .timeline-page h3,
  .timeline-page p,
  .timeline-page li,
  .timeline-page button,
  .timeline-page summary,
  .timeline-page span {
    color: var(--text);
  }

  .timeline-hero {
    display: grid;
    grid-template-columns: 1.1fr 0.9fr;
    gap: 24px;
    align-items: center;
    margin: 1.5rem 0 2rem 0;
    background: linear-gradient(135deg, #eff6ff 0%, #f8fafc 100%);
    border: 1px solid #dbeafe;
    border-radius: 24px;
    padding: 24px;
    box-shadow: var(--shadow);
  }

  .timeline-hero-copy p {
    font-size: 1.02rem;
    line-height: 1.7;
    margin-bottom: 0;
  }

  .timeline-hero-copy .hero-tag {
    display: inline-block;
    background: var(--accent-soft);
    color: var(--accent);
    border: 1px solid #bfdbfe;
    border-radius: 999px;
    padding: 6px 12px;
    font-size: 0.85rem;
    font-weight: 600;
    margin-bottom: 12px;
  }

  .timeline-hero-visual img {
    width: 100%;
    border-radius: 18px;
    box-shadow: var(--shadow);
  }

  .timeline-instructions {
    margin: 0 0 1rem 0;
    font-size: 0.98rem;
    color: var(--muted);
  }

  .timeline-shell {
    background: var(--card);
    border: 1px solid #e5e7eb;
    border-radius: 24px;
    padding: 22px;
    box-shadow: var(--shadow);
    margin-bottom: 1.75rem;
  }

  .timeline-track {
    position: relative;
    display: flex;
    gap: 14px;
    overflow-x: auto;
    padding: 12px 4px 18px 4px;
    scroll-snap-type: x proximity;
  }

  .timeline-track::before {
    content: "";
    position: absolute;
    left: 0;
    right: 0;
    top: 36px;
    height: 4px;
    background: linear-gradient(90deg, #bfdbfe, #60a5fa, #2563eb);
    border-radius: 999px;
    z-index: 0;
  }

  .timeline-point {
    position: relative;
    z-index: 1;
    min-width: 104px;
    scroll-snap-align: start;
    border: 1px solid #dbeafe;
    background: #fff;
    border-radius: 18px;
    padding: 12px 10px;
    text-align: center;
    cursor: pointer;
    transition: transform 0.2s ease, box-shadow 0.2s ease, background 0.2s ease;
    box-shadow: 0 4px 16px rgba(37, 99, 235, 0.08);
  }

  .timeline-point:hover,
  .timeline-point:focus-visible {
    transform: translateY(-3px);
    outline: none;
    box-shadow: 0 10px 24px rgba(37, 99, 235, 0.16);
  }

  .timeline-point.active {
    background: var(--accent);
    border-color: var(--accent);
  }

  .timeline-point.active .timeline-year,
  .timeline-point.active .timeline-label {
    color: #fff;
  }

  .timeline-dot {
    width: 14px;
    height: 14px;
    border-radius: 50%;
    background: var(--accent);
    margin: 0 auto 8px auto;
    border: 3px solid #dbeafe;
  }

  .timeline-point.active .timeline-dot {
    background: #fff;
    border-color: #bfdbfe;
  }

  .timeline-year {
    font-weight: 800;
    font-size: 1rem;
    line-height: 1.2;
  }

  .timeline-label {
    margin-top: 5px;
    font-size: 0.8rem;
    color: var(--muted);
    line-height: 1.3;
  }

  .timeline-detail {
    margin-top: 10px;
    background: linear-gradient(180deg, #ffffff 0%, #f8fbff 100%);
    border: 1px solid #dbeafe;
    border-radius: 22px;
    padding: 24px;
    display: grid;
    grid-template-columns: 1fr 220px;
    gap: 18px;
    align-items: start;
  }

  .detail-year {
    font-size: 0.9rem;
    font-weight: 700;
    color: var(--accent);
    letter-spacing: 0.04em;
    text-transform: uppercase;
    margin-bottom: 8px;
  }

  .detail-title {
    margin: 0 0 10px 0;
    font-size: 1.6rem;
  }

  .detail-body {
    margin: 0 0 14px 0;
    line-height: 1.75;
  }

  .detail-why {
    background: #fff;
    border: 1px solid #e5e7eb;
    border-radius: 16px;
    padding: 14px;
  }

  .detail-why span {
    display: block;
    font-size: 0.82rem;
    font-weight: 700;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.04em;
    margin-bottom: 6px;
  }

  .detail-era {
    display: inline-block;
    background: var(--accent-soft);
    color: var(--accent);
    border-radius: 999px;
    padding: 6px 10px;
    font-size: 0.82rem;
    font-weight: 700;
    margin-top: 4px;
  }

  .standout-dropdown {
    background: #fff;
    border: 1px solid #e5e7eb;
    border-radius: 20px;
    box-shadow: var(--shadow);
    overflow: hidden;
    margin: 1rem 0 1.75rem 0;
  }

  .standout-dropdown summary {
    list-style: none;
    cursor: pointer;
    padding: 18px 20px;
    font-size: 1.08rem;
    font-weight: 700;
    background: linear-gradient(135deg, #eff6ff 0%, #ffffff 100%);
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .standout-dropdown summary::-webkit-details-marker {
    display: none;
  }

  .standout-content {
    padding: 4px 20px 20px 20px;
  }

  .standout-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 14px;
    margin-top: 10px;
  }

  .standout-card {
    background: #f8fafc;
    border: 1px solid #e5e7eb;
    border-radius: 18px;
    padding: 16px;
  }

  .standout-card h3 {
    margin-top: 0;
    margin-bottom: 8px;
    font-size: 1rem;
  }

  .standout-card p {
    margin-bottom: 0;
    line-height: 1.65;
  }

  .portfolio-note {
    background: #f8fafc;
    border-left: 4px solid var(--accent);
    border-radius: 14px;
    padding: 18px;
    line-height: 1.7;
  }

  @media (max-width: 860px) {
    .timeline-hero,
    .timeline-detail {
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="timeline-page">

# The Evolution of AI

<div class="timeline-hero">
  <div class="timeline-hero-copy">
    <span class="hero-tag">Interactive AI Timeline</span>
    <p>Explore how artificial intelligence evolved from early ideas and rule-based systems into deep learning, transformers, and today’s multimodal tools. Hover over or click a year to see a quick overview.</p>
  </div>
  <div class="timeline-hero-visual">
    <img src="assets/ai-timeline-visual.svg" alt="Visual timeline of AI history from 1950 to the present, showing major breakthroughs and turning points.">
  </div>
</div>

<p class="timeline-instructions"><strong>How to explore:</strong> Hover over a date for a quick preview or click to keep that milestone open.</p>

<div class="timeline-shell">
  <div class="timeline-track" id="aiTimelineTrack">
    <button class="timeline-point active" type="button" data-year="1950" data-title="Turing asks the big question" data-label="Can machines think?" data-era="Foundations" data-body="Alan Turing’s paper, <em>Computing Machinery and Intelligence</em>, introduced the Turing Test and challenged people to think seriously about machine intelligence." data-why="This milestone gave AI an early philosophical and scientific starting point.">
      <div class="timeline-dot"></div>
      <div class="timeline-year">1950</div>
      <div class="timeline-label">Turing Test</div>
    </button>

    <button class="timeline-point" type="button" data-year="1956" data-title="Dartmouth launches the field" data-label="AI gets its name" data-era="Foundations" data-body="At the Dartmouth Conference, John McCarthy and other researchers formalized the field and introduced the term <strong>Artificial Intelligence</strong>." data-why="This was the moment AI became an official research discipline instead of just an idea.">
      <div class="timeline-dot"></div>
      <div class="timeline-year">1956</div>
      <div class="timeline-label">Dartmouth</div>
    </button>

    <button class="timeline-point" type="button" data-year="1966" data-title="ELIZA simulates conversation" data-label="Early chatbot" data-era="Symbolic AI" data-body="ELIZA showed that a machine could mimic human conversation with simple pattern-matching rules, even though it did not truly understand meaning." data-why="It revealed how quickly people can attribute intelligence to language-based systems.">
      <div class="timeline-dot"></div>
      <div class="timeline-year">1966</div>
      <div class="timeline-label">ELIZA</div>
    </button>

    <button class="timeline-point" type="button" data-year="1974–1980" data-title="The first AI winter" data-label="Momentum slows" data-era="AI Winter" data-body="Early optimism ran ahead of real computing power and real-world results. Funding dropped and enthusiasm cooled as expectations were not met." data-why="It showed that big ideas alone are not enough without data, compute, and practical results.">
      <div class="timeline-dot"></div>
      <div class="timeline-year">1974</div>
      <div class="timeline-label">AI Winter</div>
    </button>

    <button class="timeline-point" type="button" data-year="1986" data-title="Backpropagation gains traction" data-label="Learning from errors" data-era="Neural Networks" data-body="Backpropagation helped neural networks improve by adjusting weights based on error. This became one of the most important learning methods behind deep learning." data-why="It provided a practical way for neural networks to learn complex patterns.">
      <div class="timeline-dot"></div>
      <div class="timeline-year">1986</div>
      <div class="timeline-label">Backprop</div>
    </button>

    <button class="timeline-point" type="button" data-year="1987–1993" data-title="The second AI winter" data-label="Expert systems fade" data-era="AI Winter" data-body="Expert systems became expensive and difficult to maintain, and another period of reduced investment followed." data-why="This reminded the field that narrow systems can struggle to scale in the real world.">
      <div class="timeline-dot"></div>
      <div class="timeline-year">1987</div>
      <div class="timeline-label">2nd Winter</div>
    </button>

    <button class="timeline-point" type="button" data-year="1997" data-title="Deep Blue defeats Kasparov" data-label="AI beats chess champion" data-era="Narrow AI" data-body="IBM’s Deep Blue defeated world chess champion Garry Kasparov, proving that machines could outperform humans in high-level strategic gameplay." data-why="It became one of the first highly visible moments when AI beat a human expert at a complex task.">
      <div class="timeline-dot"></div>
      <div class="timeline-year">1997</div>
      <div class="timeline-label">Deep Blue</div>
    </button>

    <button class="timeline-point" type="button" data-year="2011" data-title="Watson wins on Jeopardy!" data-label="Language + retrieval" data-era="Applied AI" data-body="IBM Watson combined language processing, search, and ranking to win on <em>Jeopardy!</em>, showing how AI could work across messy language-based tasks." data-why="It showed that AI could handle more than structured games and enter broader knowledge tasks.">
      <div class="timeline-dot"></div>
      <div class="timeline-year">2011</div>
      <div class="timeline-label">Watson</div>
    </button>

    <button class="timeline-point" type="button" data-year="2012" data-title="AlexNet changes computer vision" data-label="Deep learning breakthrough" data-era="Deep Learning" data-body="AlexNet dramatically improved image classification performance and showed how GPUs, data, and neural networks could outperform older methods at scale." data-why="This milestone accelerated the deep learning era and reshaped AI research.">
      <div class="timeline-dot"></div>
      <div class="timeline-year">2012</div>
      <div class="timeline-label">AlexNet</div>
    </button>

    <button class="timeline-point" type="button" data-year="2017" data-title="Transformers redefine language AI" data-label="Attention is all you need" data-era="Modern AI" data-body="The transformer architecture introduced a new way to process sequences using attention, becoming the foundation for modern large language models." data-why="It made today’s generative AI and advanced language systems possible.">
      <div class="timeline-dot"></div>
      <div class="timeline-year">2017</div>
      <div class="timeline-label">Transformers</div>
    </button>

    <button class="timeline-point" type="button" data-year="2022–2023" data-title="Generative AI goes mainstream" data-label="ChatGPT era" data-era="Generative AI" data-body="Generative AI tools became widely accessible, bringing writing, coding, image generation, and AI assistants into everyday workflows." data-why="This is when AI became visible to the general public at a massive scale.">
      <div class="timeline-dot"></div>
      <div class="timeline-year">2022</div>
      <div class="timeline-label">Gen AI</div>
    </button>

    <button class="timeline-point" type="button" data-year="Today" data-title="Multimodal AI expands what systems can do" data-label="Text, image, audio, video" data-era="Current Era" data-body="Modern AI systems can work across multiple data types, support automation, and help with reasoning, content generation, and decision support." data-why="It shows that AI is moving beyond single-task tools into more connected, flexible systems.">
      <div class="timeline-dot"></div>
      <div class="timeline-year">Now</div>
      <div class="timeline-label">Multimodal</div>
    </button>
  </div>

  <div class="timeline-detail" id="timelineDetail" aria-live="polite">
    <div>
      <div class="detail-year" id="detailYear">1950</div>
      <h2 class="detail-title" id="detailTitle">Turing asks the big question</h2>
      <p class="detail-body" id="detailBody">Alan Turing’s paper, <em>Computing Machinery and Intelligence</em>, introduced the Turing Test and challenged people to think seriously about machine intelligence.</p>
      <span class="detail-era" id="detailEra">Foundations</span>
    </div>
    <div class="detail-why">
      <span>Why it matters</span>
      <p id="detailWhy" style="margin:0; line-height:1.7;">This milestone gave AI an early philosophical and scientific starting point.</p>
    </div>
  </div>
</div>

<details class="standout-dropdown">
  <summary>✨ What stands out from AI history</summary>
  <div class="standout-content">
    <div class="standout-grid">
      <div class="standout-card">
        <h3>Progress was not linear</h3>
        <p>AI moved through excitement, setbacks, and reinvention. The field grew in waves rather than in a straight line.</p>
      </div>
      <div class="standout-card">
        <h3>Breakthroughs needed scale</h3>
        <p>Ideas mattered, but real progress often came when compute power, data, and usable methods finally caught up.</p>
      </div>
      <div class="standout-card">
        <h3>AI expanded beyond narrow tasks</h3>
        <p>What started with single-purpose systems now supports language, images, reasoning, automation, and everyday productivity.</p>
      </div>
      <div class="standout-card">
        <h3>The field keeps evolving</h3>
        <p>The path from symbolic AI to deep learning to transformers shows that AI continues to change with each technical leap.</p>
      </div>
    </div>
  </div>
</details>

## Why I included this in my portfolio

<div class="portfolio-note">
  I included this artifact to show AI as a long-term evolution rather than a sudden trend. Looking at the timeline makes it easier to understand how today’s tools were shaped by decades of experimentation, setbacks, and breakthroughs.
</div>

</div>

<script>
  (function () {
    const points = Array.from(document.querySelectorAll('.timeline-point'));
    const detailYear = document.getElementById('detailYear');
    const detailTitle = document.getElementById('detailTitle');
    const detailBody = document.getElementById('detailBody');
    const detailEra = document.getElementById('detailEra');
    const detailWhy = document.getElementById('detailWhy');

    function updateDetail(point, persistActive) {
      detailYear.textContent = point.dataset.year || '';
      detailTitle.textContent = point.dataset.title || '';
      detailBody.innerHTML = point.dataset.body || '';
      detailEra.textContent = point.dataset.era || '';
      detailWhy.textContent = point.dataset.why || '';

      if (persistActive) {
        points.forEach((btn) => btn.classList.remove('active'));
        point.classList.add('active');
      }
    }

    points.forEach((point) => {
      point.addEventListener('mouseenter', () => updateDetail(point, false));
      point.addEventListener('focus', () => updateDetail(point, false));
      point.addEventListener('click', () => updateDetail(point, true));
    });
  })();
</script>
