
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kisal-De-Silva | Repository</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    --bg: #0d1117;
    --panel: #161b22;
    --border: #30363d;
    --text: #e6edf3;
    --muted: #9198a1;
    --blue: #4493f8;
    --green: #238636;
}

body {
    background: var(--bg);
    color: var(--text);
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI",
                 Helvetica, Arial, sans-serif;
    font-size: 14px;
}

/* Top navigation */
.topbar {
    min-height: 64px;
    display: flex;
    align-items: center;
    gap: 18px;
    padding: 14px 24px;
    border-bottom: 1px solid var(--border);
}

.github-logo {
    width: 34px;
    height: 34px;
    border-radius: 50%;
    background: white;
    color: #0d1117;
    display: grid;
    place-items: center;
    font-size: 22px;
    font-weight: bold;
}

.username {
    font-weight: 600;
    color: var(--text);
    text-decoration: none;
}

.search {
    margin-left: auto;
    padding: 9px 14px;
    width: 220px;
    border: 1px solid var(--border);
    border-radius: 7px;
    color: var(--muted);
    background: transparent;
}

/* Repository navigation */
.nav {
    display: flex;
    gap: 24px;
    padding: 0 24px;
    border-bottom: 1px solid var(--border);
    overflow-x: auto;
}

.nav a {
    color: var(--text);
    text-decoration: none;
    padding: 16px 0;
    white-space: nowrap;
    border-bottom: 2px solid transparent;
}

.nav a.active {
    border-bottom-color: #fd8c73;
}

/* Main content */
.container {
    max-width: 1250px;
    margin: 30px auto;
    padding: 0 24px;
}

.repo-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 16px;
    padding-bottom: 22px;
    border-bottom: 1px solid var(--border);
}

.repo-title {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 22px;
}

.repo-icon {
    font-size: 27px;
}

.badge {
    border: 1px solid var(--border);
    border-radius: 20px;
    color: var(--muted);
    font-size: 12px;
    padding: 3px 9px;
    font-weight: normal;
}

.actions {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
}

button {
    cursor: pointer;
    color: var(--text);
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 8px 12px;
    font-size: 13px;
    font-weight: 600;
}

button:hover {
    background: #30363d;
}

button.selected {
    color: #7ee787;
    border-color: #238636;
}

/* Repository description */
.description {
    color: var(--muted);
    margin: 20px 0;
    line-height: 1.7;
}

/* Main two-column layout */
.layout {
    display: grid;
    grid-template-columns: minmax(0, 2fr) minmax(240px, 1fr);
    gap: 22px;
    margin-top: 22px;
}

.panel {
    border: 1px solid var(--border);
    border-radius: 8px;
    overflow: hidden;
    margin-bottom: 20px;
}

.panel-title {
    padding: 15px;
    border-bottom: 1px solid var(--border);
    font-weight: 600;
    background: rgba(255,255,255,0.015);
}

.file-row {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 13px 16px;
    border-bottom: 1px solid #21262d;
    text-decoration: none;
    color: var(--text);
}

.file-row:last-child {
    border-bottom: none;
}

.file-row:hover {
    background: #161b22;
}

.file-icon {
    color: var(--muted);
}

.file-name {
    flex: 1;
    overflow-wrap: anywhere;
}

.file-message {
    color: var(--muted);
    font-size: 12px;
}

/* README */
.readme {
    padding: 26px;
    line-height: 1.8;
}

.readme h2 {
    font-size: 23px;
    margin-bottom: 14px;
    padding-bottom: 10px;
    border-bottom: 1px solid var(--border);
}

.readme p {
    margin-bottom: 14px;
}

.readme a {
    color: var(--blue);
}

.readme h3 {
    margin: 20px 0 8px;
}

/* Sidebar */
.sidebar-section {
    padding: 18px;
    border-bottom: 1px solid var(--border);
}

.sidebar-section:last-child {
    border-bottom: none;
}

.sidebar-section h3 {
    margin-bottom: 12px;
    font-size: 15px;
}

.sidebar-section p {
    color: var(--muted);
    line-height: 1.7;
}

.language-bar {
    height: 8px;
    border-radius: 5px;
    background: linear-gradient(
        to right,
        #f1e05a 0% 60%,
        #3572a5 60% 85%,
        #563d7c 85% 100%
    );
    margin: 12px 0;
}

/* Footer */
footer {
    text-align: center;
    color: var(--muted);
    border-top: 1px solid var(--border);
    padding: 25px;
    margin-top: 35px;
    font-size: 12px;
}

@media (max-width: 760px) {
    .topbar {
        padding: 12px;
    }

    .search {
        display: none;
    }

    .nav {
        padding: 0 14px;
        gap: 18px;
    }

    .container {
        padding: 0 14px;
        margin-top: 20px;
    }

    .layout {
        grid-template-columns: 1fr;
    }

    .repo-title {
        font-size: 19px;
    }

    .file-message {
        display: none;
    }
}
</style>
</head>

<body>

<header class="topbar">
    <div class="github-logo">⌘</div>
    <a class="username" href="#">kisal-prabhashwara</a>
    <input class="search" type="search" placeholder="Search repositories...">
</header>

<nav class="nav">
    <a href="#" class="active">〈〉 Code</a>
    <a href="#issues">Issues</a>
    <a href="#pulls">Pull requests</a>
    <a href="#actions">Actions</a>
    <a href="#projects">Projects</a>
    <a href="#wiki">Wiki</a>
    <a href="#security">Security</a>
    <a href="#settings">Settings</a>
</nav>

<main class="container">

    <section class="repo-header">
        <div class="repo-title">
            <span class="repo-icon">🟠</span>
            <strong>Kisal-De-Silva</strong>
            <span class="badge">Public</span>
        </div>

        <div class="actions">
            <button id="watchBtn">◉ Watch <span id="watchCount">0</span></button>
            <button id="starBtn">☆ Star <span id="starCount">0</span></button>
            <button id="forkBtn">⑂ Fork <span id="forkCount">0</span></button>
        </div>
    </section>

    <p class="description">
        Welcome to my repository! Explore my projects, source code,
        experiments, and development journey.
    </p>

    <section class="layout">

        <div class="main-column">

            <div class="panel">
                <div class="panel-title">📁 Repository files</div>

                <a class="file-row" href="#readme">
                    <span class="file-icon">📁</span>
                    <span class="file-name">src</span>
                    <span class="file-message">Source code</span>
                </a>

                <a class="file-row" href="#assets">
                    <span class="file-icon">📁</span>
                    <span class="file-name">assets</span>
                    <span class="file-message">Images and resources</span>
                </a>

                <a class="file-row" href="#index">
                    <span class="file-icon">📄</span>
                    <span class="file-name">index.html</span>
                    <span class="file-message">Main page</span>
                </a>

                <a class="file-row" href="#style">
                    <span class="file-icon">🎨</span>
                    <span class="file-name">style.css</span>
                    <span class="file-message">Website styling</span>
                </a>

                <a class="file-row" href="#readme">
                    <span class="file-icon">📘</span>
                    <span class="file-name">README.md</span>
                    <span class="file-message">Project documentation</span>
                </a>
            </div>

            <div class="panel" id="readme">
                <div class="panel-title">📖 README.md</div>

                <div class="readme">
                    <h2>👋 Welcome to Kisal-De-Silva</h2>

                    <p>
                        Hi! I'm Kisal, and this is my personal development
                        space. Here you'll find my projects, coding
                        experiments, and things I'm learning.
                    </p>

                    <h3>🚀 About this repository</h3>
                    <p>
                        This repository is a starting point for showcasing
                        projects and sharing ideas with the developer community.
                    </p>

                    <h3>🛠️ Technologies</h3>
                    <p>HTML · CSS · JavaScript · Java · Git</p>

                    <h3>📌 Future plans</h3>
                    <p>
                        More projects, improved designs, and new features
                        will be added here.
                    </p>

                    <h3>📫 Connect with me</h3>
                    <p>
                        GitHub:
                        <a href="https://github.com/kisal-prabhashwara"
                           target="_blank" rel="noopener noreferrer">
                            kisal-prabhashwara
                        </a>
                    </p>
                </div>
            </div>

        </div>

        <aside class="sidebar">

            <div class="panel">
                <div class="sidebar-section">
                    <h3>About</h3>
                    <p>
                        Personal repository for projects, code, and
                        development experiments.
                    </p>
                </div>

                <div class="sidebar-section">
                    <h3>📌 Repository details</h3>
                    <p>🌐 Public repository</p>
                    <p>📄 README available</p>
                    <p>🌿 Main branch</p>
                </div>

                <div class="sidebar-section">
                    <h3>💻 Languages</h3>
                    <div class="language-bar"></div>
                    <p>JavaScript · Java · HTML · CSS</p>
                </div>

                <div class="sidebar-section">
                    <h3>🔗 Links</h3>
                    <p>
                        <a href="https://github.com/kisal-prabhashwara"
                           style="color:#4493f8">
                            GitHub Profile ↗
                        </a>
                    </p>
                </div>
            </div>

        </aside>
    </section>
</main>

<footer>
    Built with HTML, CSS & JavaScript · Kisal-De-Silva
</footer>

<script>
const buttons = [
    { button: "starBtn", count: "starCount", label: "☆ Star", active: "★ Star" },
    { button: "watchBtn", count: "watchCount", label: "◉ Watch", active: "◉ Watching" },
    { button: "forkBtn", count: "forkCount", label: "⑂ Fork", active: "⑂ Forked" }
];

buttons.forEach(item => {
    const btn = document.getElementById(item.button);
    const count = document.getElementById(item.count);
    let selected = false;

    btn.addEventListener("click", () => {
        selected = !selected;
        count.textContent = selected ? "1" : "0";
        btn.classList.toggle("selected", selected);
        btn.childNodes[0].textContent =
            selected ? item.active + " " : item.label + " ";
    });
});
</script>

</body>
</html>
