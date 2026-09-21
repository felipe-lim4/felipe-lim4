<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Felipe Lima Vieira — Data Scientist</title>

    <meta
        name="description"
        content="Felipe Lima Vieira — Cientista de Dados focado em Machine Learning, Generative AI e AI Engineering."
    >

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

    <link
        href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap"
        rel="stylesheet"
    >

    <style>

        /* =========================================================
           RESET
        ========================================================= */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg: #070b12;
            --bg-soft: #0b111b;
            --card: rgba(13, 20, 31, .72);
            --border: rgba(255, 255, 255, .08);

            --text: #f1f5f9;
            --muted: #8c9aaa;

            --blue: #38bdf8;
            --cyan: #22d3ee;
            --green: #34d399;
            --purple: #a78bfa;

            --radius: 18px;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background:
                radial-gradient(
                    circle at 15% 15%,
                    rgba(56, 189, 248, .08),
                    transparent 30%
                ),
                radial-gradient(
                    circle at 85% 65%,
                    rgba(52, 211, 153, .05),
                    transparent 30%
                ),
                var(--bg);

            color: var(--text);

            font-family: "Inter", sans-serif;

            min-height: 100vh;

            overflow-x: hidden;
        }

        canvas {
            position: fixed;
            inset: 0;

            width: 100%;
            height: 100%;

            pointer-events: none;

            opacity: .45;

            z-index: 0;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        .container {
            width: min(1180px, calc(100% - 40px));
            margin: auto;
            position: relative;
            z-index: 2;
        }


        /* =========================================================
           NAVBAR
        ========================================================= */

        nav {
            height: 76px;

            display: flex;
            align-items: center;
            justify-content: space-between;

            border-bottom: 1px solid var(--border);
        }

        .logo {
            font-family: "JetBrains Mono", monospace;
            font-size: 14px;
            color: var(--cyan);
        }

        .logo::before {
            content: "> ";
            color: var(--green);
        }

        .nav-links {
            display: flex;
            gap: 28px;

            color: var(--muted);

            font-size: 14px;
        }

        .nav-links a {
            transition: .2s;
        }

        .nav-links a:hover {
            color: var(--text);
        }


        /* =========================================================
           HERO
        ========================================================= */

        .hero {
            min-height: 650px;

            display: grid;
            grid-template-columns: 1.2fr .8fr;

            align-items: center;

            gap: 70px;
        }

        .eyebrow {
            display: inline-flex;
            align-items: center;
            gap: 8px;

            padding: 7px 11px;

            border: 1px solid rgba(52, 211, 153, .2);

            border-radius: 999px;

            background: rgba(52, 211, 153, .05);

            color: var(--green);

            font-family: "JetBrains Mono", monospace;

            font-size: 12px;

            margin-bottom: 24px;
        }

        .status-dot {
            width: 7px;
            height: 7px;

            background: var(--green);

            border-radius: 50%;

            box-shadow: 0 0 12px var(--green);
        }

        h1 {
            font-size: clamp(48px, 7vw, 82px);

            line-height: .95;

            letter-spacing: -4px;

            margin-bottom: 26px;
        }

        h1 span {
            background:
                linear-gradient(
                    100deg,
                    var(--text),
                    var(--blue),
                    var(--cyan)
                );

            -webkit-background-clip: text;
            background-clip: text;

            color: transparent;
        }

        .hero-description {
            max-width: 620px;

            color: var(--muted);

            font-size: 18px;

            line-height: 1.7;

            margin-bottom: 30px;
        }

        .hero-description strong {
            color: var(--text);
            font-weight: 500;
        }

        .buttons {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-flex;

            align-items: center;
            gap: 8px;

            padding: 12px 17px;

            border-radius: 10px;

            border: 1px solid var(--border);

            background: rgba(255, 255, 255, .03);

            font-size: 14px;

            transition: .25s;
        }

        .btn:hover {
            transform: translateY(-2px);

            border-color: rgba(56, 189, 248, .35);

            background: rgba(56, 189, 248, .08);
        }

        .btn.primary {
            background: var(--text);
            color: #071019;
            border-color: var(--text);
        }

        .btn.primary:hover {
            box-shadow: 0 8px 35px rgba(255,255,255,.1);
        }


        /* =========================================================
           TERMINAL
        ========================================================= */

        .terminal {
            background: rgba(5, 10, 17, .86);

            border: 1px solid rgba(255,255,255,.1);

            border-radius: var(--radius);

            box-shadow:
                0 25px 80px rgba(0,0,0,.35),
                0 0 60px rgba(34,211,238,.04);

            overflow: hidden;

            backdrop-filter: blur(15px);
        }

        .terminal-header {
            height: 38px;

            display: flex;
            align-items: center;

            padding: 0 14px;

            border-bottom: 1px solid var(--border);
        }

        .terminal-dots {
            display: flex;
            gap: 6px;
        }

        .terminal-dots span {
            width: 8px;
            height: 8px;

            border-radius: 50%;

            background: #475569;
        }

        .terminal-title {
            margin: auto;

            font-family: "JetBrains Mono", monospace;

            font-size: 11px;

            color: #64748b;
        }

        .terminal-body {
            padding: 24px;

            min-height: 330px;

            font-family: "JetBrains Mono", monospace;

            font-size: 13px;

            line-height: 2;
        }

        .command {
            color: var(--green);
        }

        .output {
            color: #b5c2d1;
        }

        .highlight {
            color: var(--cyan);
        }

        .cursor {
            display: inline-block;

            width: 7px;
            height: 15px;

            background: var(--cyan);

            vertical-align: middle;

            animation: blink 1s infinite;
        }

        @keyframes blink {
            50% {
                opacity: 0;
            }
        }


        /* =========================================================
           SECTIONS
        ========================================================= */

        section {
            padding: 90px 0;
        }

        .section-heading {
            margin-bottom: 35px;
        }

        .section-label {
            font-family: "JetBrains Mono", monospace;

            color: var(--cyan);

            font-size: 12px;

            margin-bottom: 10px;
        }

        h2 {
            font-size: clamp(30px, 4vw, 42px);

            letter-spacing: -1.5px;
        }

        .section-description {
            color: var(--muted);

            margin-top: 10px;

            max-width: 650px;

            line-height: 1.7;
        }


        /* =========================================================
           PIPELINE
        ========================================================= */

        .pipeline {
            display: grid;

            grid-template-columns: repeat(5, 1fr);

            gap: 1px;

            background: var(--border);

            border: 1px solid var(--border);

            border-radius: var(--radius);

            overflow: hidden;
        }

        .pipeline-item {
            position: relative;

            padding: 30px 20px;

            background: rgba(10,16,26,.82);

            transition: .3s;
        }

        .pipeline-item:hover {
            background: rgba(20,32,48,.9);

            transform: translateY(-4px);
        }

        .pipeline-number {
            font-family: "JetBrains Mono", monospace;

            font-size: 11px;

            color: var(--muted);

            margin-bottom: 25px;
        }

        .pipeline-icon {
            font-size: 25px;

            margin-bottom: 18px;
        }

        .pipeline-item h3 {
            font-size: 16px;

            margin-bottom: 8px;
        }

        .pipeline-item p {
            color: var(--muted);

            font-size: 12px;

            line-height: 1.6;
        }


        /* =========================================================
           STACK
        ========================================================= */

        .stack {
            display: flex;

            flex-wrap: wrap;

            gap: 9px;
        }

        .tech {
            padding: 9px 13px;

            border: 1px solid var(--border);

            border-radius: 9px;

            background: rgba(255,255,255,.025);

            color: #b8c4d3;

            font-family: "JetBrains Mono", monospace;

            font-size: 12px;

            transition: .2s;
        }

        .tech:hover {
            border-color: rgba(56,189,248,.35);

            color: var(--cyan);

            transform: translateY(-2px);
        }


        /* =========================================================
           PROJECTS
        ========================================================= */

        .projects {
            display: grid;

            grid-template-columns: repeat(3, 1fr);

            gap: 16px;
        }

        .project {
            padding: 24px;

            border: 1px solid var(--border);

            border-radius: var(--radius);

            background: var(--card);

            backdrop-filter: blur(12px);

            transition: .25s;
        }

        .project:hover {
            transform: translateY(-5px);

            border-color: rgba(56,189,248,.25);
        }

        .project-top {
            display: flex;

            align-items: center;

            justify-content: space-between;

            margin-bottom: 20px;
        }

        .project-icon {
            width: 38px;
            height: 38px;

            display: grid;
            place-items: center;

            border-radius: 10px;

            background: rgba(56,189,248,.08);

            color: var(--cyan);
        }

        .project-lang {
            color: var(--muted);

            font-family: "JetBrains Mono", monospace;

            font-size: 11px;
        }

        .project h3 {
            font-size: 17px;

            margin-bottom: 9px;
        }

        .project p {
            color: var(--muted);

            font-size: 13px;

            line-height: 1.6;

            min-height: 63px;
        }

        .project-footer {
            margin-top: 20px;

            display: flex;

            align-items: center;

            justify-content: space-between;
        }

        .project-link {
            color: var(--cyan);

            font-size: 12px;

            font-family: "JetBrains Mono", monospace;
        }

        .stars {
            color: #64748b;

            font-size: 11px;
        }


        /* =========================================================
           ABOUT GRID
        ========================================================= */

        .about-grid {
            display: grid;

            grid-template-columns: 1fr 1fr;

            gap: 16px;
        }

        .info-card {
            padding: 28px;

            border: 1px solid var(--border);

            border-radius: var(--radius);

            background: var(--card);
        }

        .info-card h3 {
            margin-bottom: 15px;

            font-size: 16px;
        }

        .info-card p {
            color: var(--muted);

            line-height: 1.8;

            font-size: 14px;
        }

        .focus-list {
            list-style: none;
        }

        .focus-list li {
            display: flex;

            align-items: center;

            gap: 10px;

            padding: 10px 0;

            color: #b9c5d3;

            border-bottom: 1px solid rgba(255,255,255,.04);

            font-size: 13px;
        }

        .focus-list li:last-child {
            border-bottom: 0;
        }

        .focus-list li::before {
            content: "→";

            color: var(--green);

            font-family: "JetBrains Mono", monospace;
        }


        /* =========================================================
           STATS
        ========================================================= */

        .stats {
            display: grid;

            grid-template-columns: repeat(4, 1fr);

            border: 1px solid var(--border);

            border-radius: var(--radius);

            overflow: hidden;

            background: rgba(255,255,255,.02);
        }

        .stat {
            padding: 30px 20px;

            text-align: center;

            border-right: 1px solid var(--border);
        }

        .stat:last-child {
            border-right: 0;
        }

        .stat-value {
            font-size: 30px;

            font-weight: 700;

            color: var(--text);
        }

        .stat-label {
            margin-top: 5px;

            font-family: "JetBrains Mono", monospace;

            color: var(--muted);

            font-size: 10px;

            text-transform: uppercase;

            letter-spacing: 1px;
        }


        /* =========================================================
           FOOTER
        ========================================================= */

        footer {
            padding: 45px 0 60px;

            border-top: 1px solid var(--border);

            color: var(--muted);

            font-family: "JetBrains Mono", monospace;

            font-size: 11px;

            text-align: center;
        }

        footer span {
            color: var(--cyan);
        }


        /* =========================================================
           RESPONSIVE
        ========================================================= */

        @media (max-width: 900px) {

            .hero {
                grid-template-columns: 1fr;

                padding: 70px 0;
            }

            .terminal {
                max-width: 650px;
            }

            .pipeline {
                grid-template-columns: 1fr;
            }

            .projects {
                grid-template-columns: repeat(2, 1fr);
            }

        }

        @media (max-width: 600px) {

            .container {
                width: min(100% - 28px, 1180px);
            }

            nav {
                height: 65px;
            }

            .nav-links {
                display: none;
            }

            h1 {
                font-size: 50px;

                letter-spacing: -3px;
            }

            .hero {
                min-height: auto;

                padding: 80px 0;
            }

            .projects {
                grid-template-columns: 1fr;
            }

            .about-grid {
                grid-template-columns: 1fr;
            }

            .stats {
                grid-template-columns: repeat(2, 1fr);
            }

            .stat:nth-child(2) {
                border-right: 0;
            }

            .stat:nth-child(-n+2) {
                border-bottom: 1px solid var(--border);
            }

            section {
                padding: 65px 0;
            }

        }

    </style>
</head>


<body>

<canvas id="network"></canvas>


<div class="container">

    <!-- =======================================================
         NAV
    ======================================================== -->

    <nav>

        <div class="logo">
            felipe.ai
        </div>

        <div class="nav-links">

            <a href="#about">sobre</a>

            <a href="#stack">stack</a>

            <a href="#projects">projetos</a>

            <a href="#focus">foco</a>

        </div>

    </nav>


    <!-- =======================================================
         HERO
    ======================================================== -->

    <header class="hero">

        <div>

            <div class="eyebrow">
                <span class="status-dot"></span>
                OPEN TO BUILD
            </div>


            <h1>
                Felipe<br>
                <span>Lima Vieira.</span>
            </h1>


            <p class="hero-description">

                <strong>Cientista de Dados</strong> trabalhando na interseção
                entre dados, Machine Learning e Inteligência Artificial.

                Construindo soluções que vão do processamento de dados
                até sistemas de IA em produção.

            </p>


            <div class="buttons">

                <a
                    class="btn primary"
                    href="https://github.com/felipe-lim4"
                    target="_blank"
                >
                    GitHub ↗
                </a>

                <!-- TROQUE PELO SEU LINKEDIN -->

                <a
                    class="btn"
                    href="#projects"
                >
                    Ver projetos ↓
                </a>

            </div>

        </div>


        <!-- ===================================================
             TERMINAL
        ==================================================== -->

        <div class="terminal">

            <div class="terminal-header">

                <div class="terminal-dots">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>

                <div class="terminal-title">
                    felipe@data-lab
                </div>

            </div>


            <div class="terminal-body">

                <div>
                    <span class="command">felipe@ai-lab:~$</span>
                    whoami
                </div>

                <div class="output">
                    Felipe Lima Vieira
                </div>

                <br>

                <div>
                    <span class="command">felipe@ai-lab:~$</span>
                    cat focus.txt
                </div>

                <div class="output">
                    → Machine Learning
                </div>

                <div class="output">
                    → Statistics
                </div>

                <div class="output">
                    → Generative AI
                </div>

                <div class="output">
                    → AI Evaluation
                </div>

                <div class="output">
                    → Production Systems
                </div>

                <br>

                <div>
                    <span class="command">felipe@ai-lab:~$</span>
                    status
                </div>

                <div>
                    <span class="highlight">
                        [████████████████░░░░]
                    </span>
                </div>

                <div class="output">
                    constantly learning<span class="cursor"></span>
                </div>

            </div>

        </div>

    </header>



    <!-- =======================================================
         PIPELINE
    ======================================================== -->

    <section id="about">

        <div class="section-heading">

            <div class="section-label">
                / HOW I THINK
            </div>

            <h2>
                Da informação à inteligência.
            </h2>

            <p class="section-description">

                Mais do que trabalhar com uma tecnologia específica,
                gosto de entender o caminho completo entre um problema
                e uma solução que realmente possa ser utilizada.

            </p>

        </div>


        <div class="pipeline">


            <div class="pipeline-item">

                <div class="pipeline-number">
                    01
                </div>

                <div class="pipeline-icon">
                    ◉
                </div>

                <h3>
                    Dados
                </h3>

                <p>
                    Coleta, exploração, tratamento
                    e entendimento dos dados.
                </p>

            </div>


            <div class="pipeline-item">

                <div class="pipeline-number">
                    02
                </div>

                <div class="pipeline-icon">
                    ◇
                </div>

                <h3>
                    ML / Estatística
                </h3>

                <p>
                    Modelagem, experimentação,
                    avaliação e previsão.
                </p>

            </div>


            <div class="pipeline-item">

                <div class="pipeline-number">
                    03
                </div>

                <div class="pipeline-icon">
                    ◎
                </div>

                <h3>
                    GenAI / RAG
                </h3>

                <p>
                    LLMs, RAG, agentes e aplicações
                    inteligentes orientadas a contexto.
                </p>

            </div>


            <div class="pipeline-item">

                <div class="pipeline-number">
                    04
                </div>

                <div class="pipeline-icon">
                    ✓
                </div>

                <h3>
                    Evaluation
                </h3>

                <p>
                    Curadoria, padrão ouro,
                    avaliação e LLM-as-a-Judge.
                </p>

            </div>


            <div class="pipeline-item">

                <div class="pipeline-number">
                    05
                </div>

                <div class="pipeline-icon">
                    →
                </div>

                <h3>
                    Production
                </h3>

                <p>
                    APIs, containers, cloud,
                    CI/CD e observabilidade.
                </p>

            </div>

        </div>

    </section>



    <!-- =======================================================
         STACK
    ======================================================== -->

    <section id="stack">

        <div class="section-heading">

            <div class="section-label">
                / TOOLBOX
            </div>

            <h2>
                Tecnologias que fazem parte do caminho.
            </h2>

        </div>


        <div class="stack">

            <span class="tech">Python</span>

            <span class="tech">Pandas</span>

            <span class="tech">Scikit-Learn</span>

            <span class="tech">Machine Learning</span>

            <span class="tech">FastAPI</span>

            <span class="tech">RAG</span>

            <span class="tech">LLMs</span>

            <span class="tech">LangChain</span>

            <span class="tech">AgentCore</span>

            <span class="tech">Azure</span>

            <span class="tech">Azure AI Search</span>

            <span class="tech">Azure OpenAI</span>

            <span class="tech">PostgreSQL</span>

            <span class="tech">MongoDB</span>

            <span class="tech">Docker</span>

            <span class="tech">GitHub Actions</span>

            <span class="tech">AWS</span>

            <span class="tech">Bedrock</span>

            <span class="tech">Neo4j</span>

        </div>

    </section>



    <!-- =======================================================
         PROJECTS
    ======================================================== -->

    <section id="projects">

        <div class="section-heading">

            <div class="section-label">
                / PUBLIC WORK
            </div>

            <h2>
                Alguns experimentos pelo caminho.
            </h2>

            <p class="section-description">

                Projetos de estudo, experimentação e desenvolvimento.
                Os cards abaixo são carregados diretamente dos meus
                repositórios públicos.

            </p>

        </div>


        <div
            class="projects"
            id="projects-container"
        >

            <div class="project">

                <div class="project-top">

                    <div class="project-icon">
                        ...
                    </div>

                </div>

                <h3>
                    Carregando projetos...
                </h3>

                <p>
                    Consultando GitHub API.
                </p>

            </div>

        </div>

    </section>



    <!-- =======================================================
         ABOUT / FOCUS
    ======================================================== -->

    <section id="focus">

        <div class="about-grid">


            <div class="info-card">

                <h3>
                    Atualmente
                </h3>

                <ul class="focus-list">

                    <li>
                        Aprofundando Machine Learning
                    </li>

                    <li>
                        Fortalecendo fundamentos de Estatística
                    </li>

                    <li>
                        Construindo aplicações com GenAI e RAG
                    </li>

                    <li>
                        Explorando agentes e AgentCore
                    </li>

                    <li>
                        Evoluindo avaliação de aplicações de IA
                    </li>

                    <li>
                        Aprendendo a transformar protótipos em produção
                    </li>

                </ul>

            </div>


            <div class="info-card">

                <h3>
                    O que quero construir
                </h3>

                <p>

                    Meu objetivo é evoluir cada vez mais na interseção
                    entre <strong>Data Science</strong> e
                    <strong>AI Engineering</strong>.

                    <br><br>

                    Não apenas criar modelos ou integrar uma LLM,
                    mas entender o problema, trabalhar os dados,
                    construir a solução, avaliar seus resultados
                    e colocá-la para funcionar de forma confiável.

                </p>

            </div>

        </div>

    </section>



    <!-- =======================================================
         STATS
    ======================================================== -->

    <section>

        <div class="stats">

            <div class="stat">

                <div
                    class="stat-value"
                    id="repo-count"
                >
                    —
                </div>

                <div class="stat-label">
                    Repositories
                </div>

            </div>


            <div class="stat">

                <div
                    class="stat-value"
                    id="followers"
                >
                    —
                </div>

                <div class="stat-label">
                    Followers
                </div>

            </div>


            <div class="stat">

                <div
                    class="stat-value"
                    id="stars"
                >
                    —
                </div>

                <div class="stat-label">
                    Stars
                </div>

            </div>


            <div class="stat">

                <div class="stat-value">
                    ∞
                </div>

                <div class="stat-label">
                    Curiosity
                </div>

            </div>

        </div>

    </section>


</div>


<!-- ===========================================================
     FOOTER
=========================================================== -->

<footer>

    <div class="container">

        <span>felipe@data-lab</span>

        ·

        built with HTML, CSS & JavaScript

        ·

        <a
            href="https://github.com/felipe-lim4"
            target="_blank"
        >
            GitHub ↗
        </a>

    </div>

</footer>



<script>

    /* =========================================================
       CONFIG
    ========================================================= */

    const GITHUB_USER = "felipe-lim4";


    /* =========================================================
       GITHUB API
    ========================================================= */

    async function loadGitHub() {

        try {

            const userResponse =
                await fetch(
                    `https://api.github.com/users/${GITHUB_USER}`
                );

            const user =
                await userResponse.json();


            const reposResponse =
                await fetch(
                    `https://api.github.com/users/${GITHUB_USER}/repos?per_page=100&sort=updated`
                );

            const repos =
                await reposResponse.json();


            document.getElementById("repo-count")
                .textContent = user.public_repos;


            document.getElementById("followers")
                .textContent = user.followers;


            const stars = repos.reduce(
                (total, repo) =>
                    total + repo.stargazers_count,
                0
            );


            document.getElementById("stars")
                .textContent = stars;


            renderProjects(repos);

        }

        catch (error) {

            console.error(
                "Erro ao consultar GitHub:",
                error
            );

            document.getElementById(
                "projects-container"
            ).innerHTML = `

                <div class="project">

                    <h3>
                        GitHub indisponível
                    </h3>

                    <p>
                        Não foi possível carregar os
                        repositórios agora.
                    </p>

                </div>

            `;

        }

    }



    /* =========================================================
       PROJECT RENDER
    ========================================================= */

    function renderProjects(repos) {

        const container =
            document.getElementById(
                "projects-container"
            );


        /*
            Projetos que fazem sentido destacar
            no seu perfil.
        */

        const preferred = [

            "Ai-Agility",

            "study-ml-classification",

            "clean-arch-study",

            "Projeto-Pesquisa-e-Inovacao-III"

        ];


        let selected = [];


        for (const name of preferred) {

            const repo =
                repos.find(
                    r =>
                        r.name.toLowerCase()
                        === name.toLowerCase()
                );

            if (repo) {
                selected.push(repo);
            }

        }


        /*
            Se algum projeto não estiver disponível,
            completa com os repositórios mais recentes.
        */

        if (selected.length < 6) {

            const others =
                repos.filter(
                    repo =>
                        !selected.some(
                            selectedRepo =>
                                selectedRepo.id === repo.id
                        )
                        &&
                        !repo.fork
                );


            selected.push(
                ...others.slice(
                    0,
                    6 - selected.length
                )
            );

        }


        selected =
            selected.slice(0, 6);


        container.innerHTML =
            selected.map(repo => {

                const description =
                    repo.description ||
                    "Projeto de estudo e experimentação.";


                return `

                    <article class="project">

                        <div class="project-top">

                            <div class="project-icon">
                                ◇
                            </div>

                            <div class="project-lang">

                                ${repo.language || "Code"}

                            </div>

                        </div>


                        <h3>
                            ${escapeHTML(repo.name)}
                        </h3>


                        <p>

                            ${escapeHTML(description)}

                        </p>


                        <div class="project-footer">

                            <a
                                class="project-link"
                                href="${repo.html_url}"
                                target="_blank"
                            >
                                view repository ↗
                            </a>


                            <span class="stars">

                                ★ ${repo.stargazers_count}

                            </span>

                        </div>

                    </article>

                `;

            }).join("");

    }



    /* =========================================================
       HTML ESCAPE
    ========================================================= */

    function escapeHTML(value) {

        const div =
            document.createElement("div");

        div.textContent = value;

        return div.innerHTML;

    }



    /* =========================================================
       NETWORK BACKGROUND
    ========================================================= */

    const canvas =
        document.getElementById("network");

    const ctx =
        canvas.getContext("2d");


    let particles = [];

    let mouse = {
        x: null,
        y: null
    };


    function resizeCanvas() {

        canvas.width =
            window.innerWidth;

        canvas.height =
            window.innerHeight;

    }


    window.addEventListener(
        "resize",
        resizeCanvas
    );


    window.addEventListener(
        "mousemove",
        event => {

            mouse.x =
                event.clientX;

            mouse.y =
                event.clientY;

        }
    );


    function createParticles() {

        particles = [];


        const amount =
            window.innerWidth < 600
                ? 35
                : 75;


        for (
            let i = 0;
            i < amount;
            i++
        ) {

            particles.push({

                x:
                    Math.random()
                    * canvas.width,

                y:
                    Math.random()
                    * canvas.height,

                vx:
                    (Math.random() - .5)
                    * .25,

                vy:
                    (Math.random() - .5)
                    * .25,

                radius:
                    Math.random() * 1.5 + .5

            });

        }

    }


    function animateNetwork() {

        ctx.clearRect(
            0,
            0,
            canvas.width,
            canvas.height
        );


        particles.forEach(
            particle => {

                particle.x += particle.vx;

                particle.y += particle.vy;


                if (
                    particle.x < 0 ||
                    particle.x > canvas.width
                ) {

                    particle.vx *= -1;

                }


                if (
                    particle.y < 0 ||
                    particle.y > canvas.height
                ) {

                    particle.vy *= -1;

                }


                ctx.beginPath();

                ctx.arc(
                    particle.x,
                    particle.y,
                    particle.radius,
                    0,
                    Math.PI * 2
                );

                ctx.fillStyle =
                    "rgba(56,189,248,.55)";

                ctx.fill();

            }
        );


        /*
            Liga partículas próximas.
        */

        for (
            let i = 0;
            i < particles.length;
            i++
        ) {

            for (
                let j = i + 1;
                j < particles.length;
                j++
            ) {

                const a =
                    particles[i];

                const b =
                    particles[j];


                const dx =
                    a.x - b.x;

                const dy =
                    a.y - b.y;


                const distance =
                    Math.sqrt(
                        dx * dx +
                        dy * dy
                    );


                if (distance < 130) {

                    const opacity =
                        1 -
                        distance / 130;


                    ctx.beginPath();

                    ctx.moveTo(
                        a.x,
                        a.y
                    );

                    ctx.lineTo(
                        b.x,
                        b.y
                    );


                    ctx.strokeStyle =
                        `rgba(34,211,238,${opacity * .12})`;

                    ctx.lineWidth = .7;

                    ctx.stroke();

                }

            }

        }


        requestAnimationFrame(
            animateNetwork
        );

    }


    resizeCanvas();

    createParticles();

    animateNetwork();

    loadGitHub();


</script>

</body>
</html>
