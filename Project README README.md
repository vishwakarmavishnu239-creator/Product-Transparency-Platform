<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Product Transparency Platform - Project Showcase</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- Chosen Palette: Calm Neutrals -->
    <!-- Application Structure Plan: A top-down, single-page application with a sticky navigation bar. The structure is thematic, breaking the README into logical, interactive sections: Overview, Architecture, Features, and Setup/API. This was chosen over a direct mirror of the README to create a more engaging user flow, allowing users to jump directly to the section that interests them. Interactions are designed to reveal details on-demand (e.g., clicking an architecture component) to keep the initial view clean and prevent information overload, enhancing usability. -->
    <!-- Visualization & Content Choices: 
        - Report Info: Project Stack -> Goal: Organize/Inform -> Viz: Interactive Diagram (HTML/CSS Grid) -> Interaction: Click to reveal tech details -> Justification: Visually represents the system's components better than a list. -> Library/Method: Vanilla JS, Tailwind.
        - Report Info: Project Features -> Goal: Inform/Engage -> Viz: Icon-based Grid -> Interaction: Click to show description -> Justification: More scannable and visually appealing than a bulleted list. -> Library/Method: Vanilla JS, Tailwind.
        - Report Info: Setup Commands -> Goal: Inform/Utility -> Viz: Styled Code Blocks -> Interaction: Click-to-copy button -> Justification: Improves developer experience by making setup easier. -> Library/Method: Vanilla JS.
        - Report Info: API Contracts -> Goal: Inform -> Viz: Tabbed API viewer -> Interaction: Click tabs to switch between endpoints -> Justification: Organizes multiple endpoints cleanly. -> Library/Method: Vanilla JS. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body { font-family: 'Inter', sans-serif; background-color: #f8f7f4; }
        .chart-container { position: relative; width: 100%; max-width: 600px; margin-left: auto; margin-right: auto; height: 300px; max-height: 400px; }
        .section-title { @apply text-3xl font-bold text-gray-800 mb-2; }
        .section-subtitle { @apply text-lg text-gray-500 mb-8; }
        .card { @apply bg-white p-6 rounded-xl shadow-sm transition-all duration-300; }
        .nav-link { @apply px-3 py-2 text-sm font-medium text-gray-600 hover:text-indigo-600 rounded-md transition-colors; }
        .nav-link.active { @apply text-indigo-600 bg-indigo-50; }
    </style>
</head>
<body class="text-gray-700">

    <!-- Header & Navigation -->
    <header id="header" class="bg-white/80 backdrop-blur-lg sticky top-0 z-50 shadow-sm">
        <div class="container mx-auto px-4">
            <div class="flex items-center justify-between h-16">
                <div class="flex items-center space-x-2">
                    <div class="w-8 h-8 bg-indigo-500 rounded-lg flex items-center justify-center text-white font-bold text-xl">
                        <span>P</span>
                    </div>
                    <span class="font-bold text-lg text-gray-800">Transparency Platform</span>
                </div>
                <nav class="hidden md:flex space-x-2">
                    <a href="#overview" class="nav-link">Overview</a>
                    <a href="#architecture" class="nav-link">Architecture</a>
                    <a href="#features" class="nav-link">Features</a>
                    <a href="#setup" class="nav-link">Setup & API</a>
                </nav>
            </div>
        </div>
    </header>

    <main class="container mx-auto px-4 py-12">

        <!-- Section 1: Overview -->
        <section id="overview" class="text-center py-16">
            <h1 class="text-5xl font-extrabold text-gray-900 mb-4">A Platform for Product Transparency</h1>
            <p class="max-w-3xl mx-auto text-xl text-gray-600 mb-12">
                A full-stack application that collects detailed product data via intelligent, dynamic questions to generate structured, insightful transparency reports.
            </p>
            <div class="grid md:grid-cols-3 gap-8 max-w-4xl mx-auto">
                <div class="card text-left">
                    <h3 class="font-bold text-lg text-indigo-600 mb-2">🩺 Health</h3>
                    <p class="text-sm text-gray-600">Prioritizes safety, allergens, and harmful additives to build consumer trust.</p>
                </div>
                <div class="card text-left">
                    <h3 class="font-bold text-lg text-indigo-600 mb-2">🧠 Wisdom</h3>
                    <p class="text-sm text-gray-600">Uses dynamic follow-ups to probe risky attributes based on product category.</p>
                </div>
                <div class="card text-left">
                    <h3 class="font-bold text-lg text-indigo-600 mb-2">🛡️ Virtue</h3>
                    <p class="text-sm text-gray-600">Clearly labels unknowns and captures report snapshots for reproducibility and trust.</p>
                </div>
            </div>
        </section>

        <!-- Section 2: Architecture -->
        <section id="architecture" class="py-16">
            <div class="text-center">
                <h2 class="section-title">Scalable & Decoupled Architecture</h2>
                <p class="section-subtitle">A modern, three-service architecture designed for independent evolution and deployment.</p>
            </div>
            <div class="grid md:grid-cols-3 gap-4 max-w-6xl mx-auto items-center text-center font-medium text-gray-500">
                <!-- Frontend -->
                <div class="architecture-card" data-details="frontend-details">
                    <div class="card h-full hover:shadow-lg hover:-translate-y-1 cursor-pointer">
                        <div class="text-4xl mb-4">🖥️</div>
                        <h3 class="font-bold text-lg text-gray-800">Frontend</h3>
                        <p class="text-sm">React & TypeScript</p>
                    </div>
                </div>
                
                <div class="text-3xl text-indigo-300 font-light hidden md:block">↔️</div>

                <!-- Backend -->
                <div class="architecture-card" data-details="backend-details">
                    <div class="card h-full hover:shadow-lg hover:-translate-y-1 cursor-pointer">
                        <div class="text-4xl mb-4">⚙️</div>
                        <h3 class="font-bold text-lg text-gray-800">Backend API</h3>
                        <p class="text-sm">Node.js & Express</p>
                    </div>
                </div>

                <div class="col-span-1 md:col-span-3 text-3xl text-indigo-300 font-light text-center my-4">↕️</div>

                <!-- AI Service -->
                <div class="architecture-card" data-details="ai-details">
                     <div class="card h-full hover:shadow-lg hover:-translate-y-1 cursor-pointer">
                        <div class="text-4xl mb-4">🤖</div>
                        <h3 class="font-bold text-lg text-gray-800">AI Microservice</h3>
                        <p class="text-sm">Python & FastAPI</p>
                    </div>
                </div>
                
                <div class="text-3xl text-indigo-300 font-light hidden md:block">↔️</div>
                
                <!-- Database -->
                <div class="architecture-card" data-details="db-details">
                    <div class="card h-full hover:shadow-lg hover:-translate-y-1 cursor-pointer">
                        <div class="text-4xl mb-4">🗄️</div>
                        <h3 class="font-bold text-lg text-gray-800">Database & Storage</h3>
                        <p class="text-sm">PostgreSQL & S3</p>
                    </div>
                </div>
            </div>
            <!-- Details Pane -->
            <div id="architecture-details-pane" class="mt-8 max-w-4xl mx-auto">
                <div id="frontend-details" class="hidden architecture-detail-content card bg-indigo-50/50">
                    <h4 class="font-bold text-indigo-800 mb-2">Frontend Details</h4>
                    <p class="text-sm text-gray-700">Built with <b class="font-semibold">React</b> and <b class="font-semibold">TypeScript</b> using Vite for a fast development experience. Handles the multi-step form, live report preview, and initiates the PDF download. Deployed statically to <b class="font-semibold">Vercel</b>.</p>
                </div>
                <div id="backend-details" class="hidden architecture-detail-content card bg-indigo-50/50">
                    <h4 class="font-bold text-indigo-800 mb-2">Backend API Details</h4>
                    <p class="text-sm text-gray-700">A stateless API built with <b class="font-semibold">Node.js</b>, <b class="font-semibold">Express</b>, and <b class="font-semibold">TypeScript</b>. Manages persistence via <b class="font-semibold">Prisma</b>, handles JWT-based authentication, and generates PDFs from HTML using <b class="font-semibold">Puppeteer</b>. Deployed to <b class="font-semibold">Railway/Render</b>.</p>
                </div>
                <div id="ai-details" class="hidden architecture-detail-content card bg-indigo-50/50">
                    <h4 class="font-bold text-indigo-800 mb-2">AI Microservice Details</h4>
                    <p class="text-sm text-gray-700">A lightweight Python service using <b class="font-semibold">FastAPI</b>. It exposes endpoints to generate dynamic follow-up questions and calculate transparency scores. This service can evolve from a simple rules engine to a full LLM without affecting the main application. Deployed to <b class="font-semibold">Railway/Render</b>.</p>
                </div>
                 <div id="db-details" class="hidden architecture-detail-content card bg-indigo-50/50">
                    <h4 class="font-bold text-indigo-800 mb-2">Database & Storage Details</h4>
                    <p class="text-sm text-gray-700">Uses a normalized <b class="font-semibold">PostgreSQL</b> database (hosted on <b class="font-semibold">Neon/Supabase</b>) as the single source of truth. Generated PDF reports are streamed to the client or can be stored in an <b class="font-semibold">S3-compatible bucket</b> for persistence.</p>
                </div>
            </div>
        </section>

        <!-- Section 3: Features -->
        <section id="features" class="py-16 bg-white rounded-2xl">
            <div class="text-center">
                <h2 class="section-title">Core Platform Features</h2>
                <p class="section-subtitle">Designed to provide a seamless and insightful user experience.</p>
            </div>
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6 max-w-6xl mx-auto">
                <div class="card">
                    <h3 class="font-bold text-gray-800 mb-2">📝 Multi-Step Dynamic Form</h3>
                    <p class="text-sm text-gray-600">Guides users through a series of questions with conditional logic to gather comprehensive data.</p>
                </div>
                <div class="card">
                    <h3 class="font-bold text-gray-800 mb-2">🤖 AI-Powered Questions</h3>
                    <p class="text-sm text-gray-600">Generates intelligent follow-up questions based on previous answers and product category.</p>
                </div>
                <div class="card">
                    <h3 class="font-bold text-gray-800 mb-2">💯 Optional Scoring</h3>
                    <p class="text-sm text-gray-600">Provides a transparency score to quickly assess a product's disclosure level.</p>
                </div>
                <div class="card">
                    <h3 class="font-bold text-gray-800 mb-2">📄 Live Report Preview</h3>
                    <p class="text-sm text-gray-600">Shows a real-time preview of the final report as the user provides answers.</p>
                </div>
                <div class="card">
                    <h3 class="font-bold text-gray-800 mb-2">⬇️ One-Click PDF Download</h3>
                    <p class="text-sm text-gray-600">Generates and downloads a professional, structured PDF transparency report.</p>
                </div>
                <div class="card">
                    <h3 class="font-bold text-gray-800 mb-2">🔐 Secure & Scoped Auth</h3>
                    <p class="text-sm text-gray-600">Uses JWT for authentication, ensuring all data access is scoped to the correct company.</p>
                </div>
            </div>
        </section>

        <!-- Section 4: Setup & API -->
        <section id="setup" class="py-16">
            <div class="text-center">
                <h2 class="section-title">Get Started Locally</h2>
                <p class="section-subtitle">Follow these steps to run the entire platform on your local machine.</p>
            </div>
            <div class="grid lg:grid-cols-2 gap-12 max-w-6xl mx-auto">
                <!-- Setup Steps -->
                <div>
                    <h3 class="font-semibold text-xl mb-4 text-gray-800">Local Setup Instructions</h3>
                    <div class="space-y-4">
                        <div class="setup-step">
                            <div class="flex items-center mb-2">
                                <div class="bg-indigo-100 text-indigo-600 font-bold rounded-full w-8 h-8 flex items-center justify-center mr-3">1</div>
                                <h4 class="font-semibold text-gray-700">Configure Environment</h4>
                            </div>
                            <p class="text-sm text-gray-600 pl-11 mb-2">Copy `.env.example` to `.env` in both the `frontend` and `backend` directories and fill in your database URL and secrets.</p>
                        </div>
                        <div class="setup-step">
                            <div class="flex items-center mb-2">
                                <div class="bg-indigo-100 text-indigo-600 font-bold rounded-full w-8 h-8 flex items-center justify-center mr-3">2</div>
                                <h4 class="font-semibold text-gray-700">Start Backend & DB</h4>
                            </div>
                            <div class="code-block" data-code="cd backend && npm i && npx prisma migrate dev && npm run dev">
                                <pre class="bg-gray-800 text-white p-4 rounded-lg text-sm overflow-x-auto"><code>cd backend
npm i
npx prisma migrate dev
npm run dev</code></pre>
                                <button class="copy-btn">Copy</button>
                            </div>
                        </div>
                        <div class="setup-step">
                             <div class="flex items-center mb-2">
                                <div class="bg-indigo-100 text-indigo-600 font-bold rounded-full w-8 h-8 flex items-center justify-center mr-3">3</div>
                                <h4 class="font-semibold text-gray-700">Start AI Service</h4>
                            </div>
                            <div class="code-block" data-code="cd ai-service && pip install -r requirements.txt && uvicorn main:app --reload --port 8000">
                                <pre class="bg-gray-800 text-white p-4 rounded-lg text-sm overflow-x-auto"><code>cd ai-service
pip install -r requirements.txt
uvicorn main:app --reload --port 8000</code></pre>
                                <button class="copy-btn">Copy</button>
                            </div>
                        </div>
                         <div class="setup-step">
                            <div class="flex items-center mb-2">
                                <div class="bg-indigo-100 text-indigo-600 font-bold rounded-full w-8 h-8 flex items-center justify-center mr-3">4</div>
                                <h4 class="font-semibold text-gray-700">Start Frontend</h4>
                            </div>
                             <div class="code-block" data-code="cd frontend && npm i && npm run dev">
                                <pre class="bg-gray-800 text-white p-4 rounded-lg text-sm overflow-x-auto"><code>cd frontend
npm i
npm run dev</code></pre>
                                <button class="copy-btn">Copy</button>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- API Explorer -->
                <div>
                    <h3 class="font-semibold text-xl mb-4 text-gray-800">AI Service API</h3>
                    <div class="bg-white rounded-xl shadow-sm">
                        <div class="p-4 border-b border-gray-200">
                            <div id="api-tabs" class="flex space-x-1">
                                <button class="api-tab active" data-target="api-questions">/generate-questions</button>
                                <button class="api-tab" data-target="api-score">/transparency-score</button>
                            </div>
                        </div>
                        <div class="p-4">
                            <div id="api-questions" class="api-content">
                                <div class="flex items-center space-x-2 mb-2">
                                    <span class="px-2 py-1 bg-green-100 text-green-700 text-xs font-bold rounded">POST</span>
                                    <span class="text-sm font-mono text-gray-600">/generate-questions</span>
                                </div>
                                <p class="text-sm text-gray-600 mb-4">Generates follow-up questions based on product info and existing answers.</p>
                                <h5 class="font-semibold text-sm mb-1">Request Body</h5>
                                <pre class="bg-gray-100 p-2 rounded text-xs"><code>{
  "product": { "name": "...", "category": "..." },
  "answers": [{ "key": "...", "value": "..." }]
}</code></pre>
                            </div>
                            <div id="api-score" class="api-content hidden">
                                <div class="flex items-center space-x-2 mb-2">
                                    <span class="px-2 py-1 bg-green-100 text-green-700 text-xs font-bold rounded">POST</span>
                                    <span class="text-sm font-mono text-gray-600">/transparency-score</span>
                                </div>
                                <p class="text-sm text-gray-600 mb-4">Calculates a transparency score.</p>
                                <h5 class="font-semibold text-sm mb-1">Request Body</h5>
                                <pre class="bg-gray-100 p-2 rounded text-xs"><code>{
  "product": { "name": "...", "category": "..." },
  "answers": [{ "key": "...", "value": "..." }]
}</code></pre>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // Architecture Diagram Interaction
            const archCards = document.querySelectorAll('.architecture-card');
            const detailContents = document.querySelectorAll('.architecture-detail-content');

            archCards.forEach(card => {
                card.addEventListener('click', () => {
                    const targetId = card.dataset.details;
                    const targetContent = document.getElementById(targetId);

                    // Hide all detail panes
                    detailContents.forEach(content => {
                        if (content.id !== targetId) {
                            content.classList.add('hidden');
                        }
                    });
                    
                    // Toggle the clicked one
                    if (targetContent) {
                        targetContent.classList.toggle('hidden');
                    }
                });
            });

            // API Tabs
            const apiTabs = document.querySelectorAll('.api-tab');
            const apiContents = document.querySelectorAll('.api-content');
            
            apiTabs.forEach(tab => {
                tab.addEventListener('click', () => {
                    const target = document.getElementById(tab.dataset.target);

                    apiTabs.forEach(t => t.classList.remove('active'));
                    tab.classList.add('active');

                    apiContents.forEach(c => c.classList.add('hidden'));
                    if (target) {
                        target.classList.remove('hidden');
                    }
                });
            });
            
            // Style for API tabs
            document.querySelectorAll('.api-tab').forEach(button => {
                button.classList.add('px-3', 'py-1', 'text-sm', 'font-medium', 'rounded-md', 'transition-colors', 'text-gray-600', 'hover:bg-gray-100');
                if(button.classList.contains('active')) {
                    button.classList.add('bg-indigo-50', 'text-indigo-700');
                    button.classList.remove('text-gray-600');
                }
            });
            
            // Copy Buttons for Code Blocks
            document.querySelectorAll('.code-block').forEach(block => {
                const button = block.querySelector('.copy-btn');
                const code = block.dataset.code;
                
                button.classList.add('absolute', 'top-2', 'right-2', 'px-2', 'py-1', 'text-xs', 'bg-gray-600', 'text-white', 'rounded', 'opacity-50', 'hover:opacity-100', 'transition-opacity');
                block.style.position = 'relative';

                button.addEventListener('click', () => {
                    navigator.clipboard.writeText(code).then(() => {
                        button.textContent = 'Copied!';
                        setTimeout(() => {
                            button.textContent = 'Copy';
                        }, 2000);
                    });
                });
            });

            // Smooth Scrolling & Active Nav Link
            const navLinks = document.querySelectorAll('header nav a');
            const sections = document.querySelectorAll('main section');

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        navLinks.forEach(link => {
                            link.classList.remove('active');
                            if (link.getAttribute('href').substring(1) === entry.target.id) {
                                link.classList.add('active');
                            }
                        });
                    }
                });
            }, { rootMargin: "-50% 0px -50% 0px" });

            sections.forEach(section => {
                observer.observe(section);
            });
        });
    </script>
</body>
</html>
