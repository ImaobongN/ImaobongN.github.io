<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>AIML-505 | AI Portfolio Project</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI",
                         Roboto, Helvetica, Arial, sans-serif;
            background: #f7f8fa;
            color: #17202a;
            line-height: 1.6;
        }

        /* NAVIGATION */

        nav {
            position: sticky;
            top: 0;
            z-index: 1000;
            background: rgba(255,255,255,0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid #e5e7eb;
        }

        .nav-container {
            max-width: 1150px;
            margin: auto;
            padding: 16px 24px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 20px;
            font-weight: 800;
        }

        .logo span {
            color: #2563eb;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 25px;
        }

        nav a {
            text-decoration: none;
            color: #374151;
            font-size: 14px;
            font-weight: 600;
        }

        nav a:hover {
            color: #2563eb;
        }

        /* HERO */

        .hero {
            min-height: 650px;
            display: flex;
            align-items: center;
            background:
                radial-gradient(circle at top right, #dbeafe, transparent 40%),
                linear-gradient(135deg, #ffffff, #f4f7fb);
        }

        .hero-container {
            max-width: 1150px;
            margin: auto;
            padding: 80px 24px;
            width: 100%;
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 70px;
            align-items: center;
        }

        .eyebrow {
            color: #2563eb;
            font-weight: 800;
            font-size: 14px;
            letter-spacing: 1.5px;
            text-transform: uppercase;
            margin-bottom: 15px;
        }

        .hero h1 {
            font-size: clamp(42px, 6vw, 72px);
            line-height: 1.05;
            margin-bottom: 25px;
            letter-spacing: -2px;
        }

        .hero h1 span {
            color: #2563eb;
        }

        .hero p {
            max-width: 650px;
            font-size: 19px;
            color: #5b6470;
            margin-bottom: 30px;
        }

        .buttons {
            display: flex;
            gap: 14px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            padding: 13px 22px;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 700;
            transition: 0.25s ease;
        }

        .btn-primary {
            background: #2563eb;
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            background: #1d4ed8;
        }

        .btn-secondary {
            background: white;
            color: #17202a;
            border: 1px solid #d1d5db;
        }

        .btn-secondary:hover {
            transform: translateY(-3px);
            border-color: #2563eb;
        }

        /* HERO VISUAL */

        .hero-visual {
            background: white;
            border: 1px solid #e5e7eb;
            border-radius: 25px;
            padding: 25px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.08);
        }

        .visual-header {
            display: flex;
            gap: 7px;
            margin-bottom: 25px;
        }

        .dot {
            width: 10px;
            height: 10px;
            background: #d1d5db;
            border-radius: 50%;
        }

        .ai-screen {
            padding: 20px;
            background: #f8fafc;
            border-radius: 15px;
        }

        .ai-message {
            background: white;
            padding: 14px;
            border-radius: 10px;
            margin-bottom: 12px;
            border: 1px solid #e5e7eb;
            font-size: 14px;
        }

        .ai-message.highlight {
            background: #eff6ff;
            border-color: #bfdbfe;
        }

        /* GENERAL */

        section {
            padding: 90px 24px;
        }

        .container {
            max-width: 1150px;
            margin: auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 40px;
            margin-bottom: 12px;
        }

        .section-title p {
            color: #6b7280;
            max-width: 650px;
            margin: auto;
        }

        /* INFO CARDS */

        .info-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 18px;
        }

        .info-card {
            background: white;
            border: 1px solid #e5e7eb;
            border-radius: 18px;
            padding: 28px;
            cursor: pointer;
            transition: 0.3s ease;
        }

        .info-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.07);
        }

        .icon {
            font-size: 30px;
            margin-bottom: 15px;
        }

        .info-card h3 {
            margin-bottom: 8px;
        }

        .info-card p {
            color: #6b7280;
            font-size: 14px;
        }

        .card-details {
            display: none;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid #e5e7eb;
            font-size: 14px;
        }

        .info-card.active .card-details {
            display: block;
        }

        /* PROCESS */

        .process {
            background: #111827;
            color: white;
        }

        .process .section-title p {
            color: #9ca3af;
        }

        .timeline {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 12px;
        }

        .step {
            padding: 25px;
            border: 1px solid #374151;
            border-radius: 16px;
            cursor: pointer;
            transition: 0.3s ease;
        }

        .step:hover,
        .step.active {
            background: #1f2937;
            transform: translateY(-5px);
        }

        .step-number {
            font-size: 13px;
            color: #60a5fa;
            font-weight: 800;
            margin-bottom: 12px;
        }

        .step h3 {
            margin-bottom: 8px;
        }

        .step p {
            color: #9ca3af;
            font-size: 14px;
        }

        /* LEADERSHIP */

        .leadership-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
        }

        .leadership-card {
            background: white;
            border: 1px solid #e5e7eb;
            padding: 35px;
            border-radius: 20px;
        }

        .leadership-card h3 {
            margin-bottom: 15px;
        }

        .leadership-card p {
            color: #5b6470;
        }

        /* SKILLS */

        .skills {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 12px;
        }

        .skill {
            background: white;
            border: 1px solid #dbe1e8;
            padding: 10px 17px;
            border-radius: 50px;
            font-size: 14px;
            font-weight: 700;
        }

        /* ARTIFACT */

        .artifact {
            background: #eef4ff;
        }

        .artifact-box {
            background: white;
            border-radius: 24px;
            padding: 45px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 45px;
            align-items: center;
            border: 1px solid #dbeafe;
        }

        .artifact-preview {
            min-height: 300px;
            border-radius: 18px;
            background: linear-gradient(135deg, #dbeafe, #eff6ff);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 30px;
        }

        .artifact-preview h3 {
            font-size: 28px;
        }

        .artifact-info h2 {
            font-size: 35px;
            margin-bottom: 15px;
        }

        .artifact-info p {
            color: #5b6470;
            margin-bottom: 25px;
        }

        /* FOOTER */

        footer {
            background: #111827;
            color: white;
            text-align: center;
            padding: 40px 24px;
        }

        footer p {
            color: #9ca3af;
            font-size: 14px;
        }

        /* MOBILE */

        @media (max-width: 900px) {

            .hero-container {
                grid-template-columns: 1fr;
            }

            .info-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .timeline {
                grid-template-columns: 1fr;
            }

            .leadership-grid,
            .artifact-box {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 600px) {

            nav ul {
                display: none;
            }

            .hero {
                min-height: auto;
            }

            .hero-container {
                padding: 70px 20px;
            }

            .hero h1 {
                font-size: 44px;
            }

            .info-grid {
                grid-template-columns: 1fr;
            }

            section {
                padding: 65px 20px;
            }

            .artifact-box {
                padding: 25px;
            }
        }
    </style>
</head>

<body>

<!-- NAVIGATION -->

<nav>
    <div class="nav-container">

        <div class="logo">
            AI<span>Portfolio</span>
        </div>

        <ul>
            <li><a href="#overview">Overview</a></li>
            <li><a href="#process">Process</a></li>
            <li><a href="#leadership">Leadership</a></li>
            <li><a href="#artifact">Artifact</a></li>
        </ul>

    </div>
</nav>


<!-- HERO -->

<header class="hero">

    <div class="hero-container">

        <div>

            <div class="eyebrow">
                AIML-505 Portfolio Project
            </div>

            <h1>
                Turning AI Ideas Into
                <span>Practical Solutions.</span>
            </h1>

            <p>
                A portfolio case study demonstrating how I applied
                artificial intelligence concepts, strategic thinking,
                and responsible AI principles to solve a real-world
                business problem.
            </p>

            <div class="buttons">

                <a href="#overview" class="btn btn-primary">
                    Explore Project
                </a>

                <a href="#artifact" class="btn btn-secondary">
                    View Artifact
                </a>

            </div>

        </div>


        <div class="hero-visual">

            <div class="visual-header">
                <div class="dot"></div>
                <div class="dot"></div>
                <div class="dot"></div>
            </div>

            <div class="ai-screen">

                <div class="ai-message">
                    <strong>Challenge</strong><br>
                    How can AI create meaningful business value?
                </div>

                <div class="ai-message highlight">
                    <strong>AI Strategy</strong><br>
                    Identify the problem → Design the solution →
                    Evaluate → Refine
                </div>

                <div class="ai-message">
                    <strong>Outcome</strong><br>
                    A practical, responsible, and scalable AI solution.
                </div>

            </div>

        </div>

    </div>

</header>


<!-- OVERVIEW -->

<section id="overview">

    <div class="container">

        <div class="section-title">

            <div class="eyebrow">
                Project Overview
            </div>

            <h2>Explore the Project</h2>

            <p>
                Click each card to see the key elements behind
                the project.
            </p>

        </div>


        <div class="info-grid">

            <!-- OBJECTIVE -->

            <div class="info-card" onclick="toggleCard(this)">

                <div class="icon">🎯</div>

                <h3>Objective</h3>

                <p>
                    What problem was I trying to solve?
                </p>

                <div class="card-details">

                    Define a meaningful business problem and
                    explore how AI could provide a practical,
                    measurable solution.

                </div>

            </div>


            <!-- PROCESS -->

            <div class="info-card" onclick="toggleCard(this)">

                <div class="icon">⚙️</div>

                <h3>Process</h3>

                <p>
                    How did I approach the challenge?
                </p>

                <div class="card-details">

                    Research → Analyze → Design → Test →
                    Evaluate → Refine.

                </div>

            </div>


            <!-- TOOLS -->

            <div class="info-card" onclick="toggleCard(this)">

                <div class="icon">🛠️</div>

                <h3>Tools</h3>

                <p>
                    What technologies supported the project?
                </p>

                <div class="card-details">

                    Generative AI, data analytics, AI frameworks,
                    research resources, and digital collaboration
                    tools.

                </div>

            </div>


            <!-- VALUE -->

            <div class="info-card" onclick="toggleCard(this)">

                <div class="icon">💡</div>

                <h3>Value</h3>

                <p>
                    Why does this project matter?
                </p>

                <div class="card-details">

                    Demonstrates the ability to connect AI
                    technology with business objectives,
                    responsible implementation, and user needs.

                </div>

            </div>

        </div>

    </div>

</section>


<!-- PROCESS -->

<section id="process" class="process">

    <div class="container">

        <div class="section-title">

            <div class="eyebrow">
                My Approach
            </div>

            <h2>From Problem to Solution</h2>

            <p>
                A simplified view of the decisions and activities
                that shaped the project.
            </p>

        </div>


        <div class="timeline">

            <div class="step active">

                <div class="step-number">01</div>

                <h3>Identify</h3>

                <p>
                    Define the business challenge and
                    identify where AI can create value.
                </p>

            </div>


            <div class="step">

                <div class="step-number">02</div>

                <h3>Design</h3>

                <p>
                    Develop an AI-driven approach aligned
                    with user and organizational needs.
                </p>

            </div>


            <div class="step">

                <div class="step-number">03</div>

                <h3>Build</h3>

                <p>
                    Use AI tools and technical resources
                    to develop the solution.
                </p>

            </div>


            <div class="step">

                <div class="step-number">04</div>

                <h3>Evaluate</h3>

                <p>
                    Assess accuracy, usefulness, risks,
                    limitations, and overall effectiveness.
                </p>

            </div>


            <div class="step">

                <div class="step-number">05</div>

                <h3>Refine</h3>

                <p>
                    Incorporate findings and improve the
                    final solution.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- AI LEADERSHIP -->

<section id="leadership">

    <div class="container">

        <div class="section-title">

            <div class="eyebrow">
                What I Demonstrated
            </div>

            <h2>AI Leadership in Practice</h2>

            <p>
                This project goes beyond using AI. It demonstrates
                how I think about implementing AI responsibly.
            </p>

        </div>


        <div class="leadership-grid">

            <div class="leadership-card">

                <h3>🧠 Strategic Thinking</h3>

                <p>
                    Connected AI capabilities to a specific
                    organizational problem rather than treating
                    AI as technology for technology's sake.
                </p>

            </div>


            <div class="leadership-card">

                <h3>🤖 Generative AI</h3>

                <p>
                    Used generative AI as a collaborative tool
                    for ideation, analysis, development, and
                    refinement.
                </p>

            </div>


            <div class="leadership-card">

                <h3>⚖️ Responsible AI</h3>

                <p>
                    Considered ethical risks, transparency,
                    privacy, bias, security, and human oversight.
                </p>

            </div>


            <div class="leadership-card">

                <h3>📊 Critical Evaluation</h3>

                <p>
                    Evaluated AI-generated outputs rather than
                    accepting them automatically, using revision
                    and critical judgment to improve results.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- SKILLS -->

<section>

    <div class="container">

        <div class="section-title">

            <div class="eyebrow">
                Skills
            </div>

            <h2>Capabilities Demonstrated</h2>

        </div>


        <div class="skills">

            <div class="skill">Artificial Intelligence</div>
            <div class="skill">Generative AI</div>
            <div class="skill">AI Strategy</div>
            <div class="skill">Data Analytics</div>
            <div class="skill">Responsible AI</div>
            <div class="skill">Critical Thinking</div>
            <div class="skill">Prompt Engineering</div>
            <div class="skill">Problem Solving</div>
            <div class="skill">AI Governance</div>
            <div class="skill">Business Analysis</div>

        </div>

    </div>

</section>


<!-- ARTIFACT -->

<section id="artifact" class="artifact">

    <div class="container">

        <div class="artifact-box">

            <div class="artifact-preview">

                <div>

                    <div style="font-size:60px;">
                        🤖
                    </div>

                    <h3>
                        AI Project Artifact
                    </h3>

                    <p>
                        Interactive project showcase
                    </p>

                </div>

            </div>


            <div class="artifact-info">

                <div class="eyebrow">
                    Featured Artifact
                </div>

                <h2>
                    AIML-505 Project
                </h2>

                <p>
                    Explore the completed project, the decisions
                    behind it, and the AI capabilities demonstrated.
                </p>

                <!-- Replace # with your actual artifact URL -->

                <a href="#" class="btn btn-primary">
                    Explore Artifact →
                </a>

            </div>

        </div>

    </div>

</section>


<!-- FOOTER -->

<footer>

    <h3>AI Portfolio</h3>

    <p>
        AIML-505 • Artificial Intelligence & Data Analytics
    </p>

    <p style="margin-top:10px;">
        © 2026
    </p>

</footer>


<!-- JAVASCRIPT -->

<script>

    function toggleCard(card) {

        card.classList.toggle("active");

    }


    // Add interactive behavior to process steps

    const steps = document.querySelectorAll(".step");

    steps.forEach(step => {

        step.addEventListener("click", function() {

            steps.forEach(s => s.classList.remove("active"));

            this.classList.add("active");

        });

    });

</script>

</body>
</html>
