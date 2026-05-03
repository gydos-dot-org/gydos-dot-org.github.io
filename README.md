<!doctype html>

<html lang="en">
<head>
  <!--
    github.gydos.org — public landing page draftPurpose:
  This single-file page is designed for the root of:
    gydos-dot-org/gydos-dot-org.github.io

  GitHub Pages will serve this file as the primary homepage when it is
  committed as index.html at the top level of the publishing branch.

Design goals:
  - No build step.
  - No external CSS or JavaScript dependencies.
  - Readable on phones, laptops, and GitHub Pages' static hosting.
  - Present the public work as an intentional portfolio/workbench,
    not as a loose collection of unfinished experiments.

Stewardship:
  Project owner / public identity: Paul Gydos, gydos-dot-org
  Drafted with assistance from OpenAI ChatGPT.

--> <meta charset="utf-8"> <meta name="viewport" content="width=device-width, initial-scale=1"> <meta name="description" content="Gydos.org public workbench: vishgit, Smellinux, local-first tools, Siftlog Cathedral, Meditation Soundbox, and text-first computing.">

  <title>Gydos.org | Small Tools. Deep Practice.</title>
  <style>
    :root {
      --bg: #0f172a;
      --panel: #111827;
      --panel-soft: #1f2937;
      --text: #f8fafc;
      --muted: #cbd5e1;
      --line: rgba(255, 255, 255, 0.14);
      --accent: #facc15;
      --accent-2: #38bdf8;
      --good: #86efac;
      --shadow: 0 24px 70px rgba(0, 0, 0, 0.35);
      --radius: 24px;
      --max: 1120px;
    }* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  font-family: ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  background:
    radial-gradient(circle at top left, rgba(56, 189, 248, 0.20), transparent 34rem),
    radial-gradient(circle at top right, rgba(250, 204, 21, 0.16), transparent 30rem),
    var(--bg);
  color: var(--text);
  line-height: 1.6;
}

a {
  color: inherit;
}

.shell {
  width: min(var(--max), calc(100% - 32px));
  margin: 0 auto;
}

.skip-link {
  position: absolute;
  left: -999px;
  top: 12px;
  background: var(--accent);
  color: #111827;
  padding: 8px 12px;
  border-radius: 999px;
  z-index: 10;
}

.skip-link:focus {
  left: 12px;
}

header {
  position: sticky;
  top: 0;
  z-index: 5;
  backdrop-filter: blur(16px);
  background: rgba(15, 23, 42, 0.76);
  border-bottom: 1px solid var(--line);
}

.topbar {
  min-height: 72px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}

.brand {
  display: flex;
  flex-direction: column;
  text-decoration: none;
  letter-spacing: -0.02em;
}

.brand strong {
  font-size: 1.15rem;
}

.brand span {
  color: var(--muted);
  font-size: 0.88rem;
}

nav {
  display: flex;
  align-items: center;
  gap: 14px;
  flex-wrap: wrap;
  justify-content: flex-end;
  font-size: 0.94rem;
}

nav a {
  text-decoration: none;
  color: var(--muted);
}

nav a:hover,
nav a:focus {
  color: var(--text);
}

.hero {
  padding: 84px 0 44px;
}

.eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  color: #111827;
  background: var(--accent);
  border-radius: 999px;
  padding: 7px 12px;
  font-weight: 800;
  font-size: 0.86rem;
  letter-spacing: 0.02em;
  text-transform: uppercase;
}

h1,
h2,
h3 {
  line-height: 1.1;
  letter-spacing: -0.04em;
  margin: 0;
}

h1 {
  max-width: 900px;
  margin-top: 24px;
  font-size: clamp(2.7rem, 7vw, 6.6rem);
}

h2 {
  font-size: clamp(2rem, 4vw, 3.35rem);
  margin-bottom: 18px;
}

h3 {
  font-size: 1.35rem;
}

.lead {
  max-width: 760px;
  color: var(--muted);
  font-size: clamp(1.1rem, 2vw, 1.3rem);
  margin: 24px 0 0;
}

.button-row {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
  margin-top: 34px;
}

.button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-height: 46px;
  padding: 0 18px;
  border-radius: 999px;
  text-decoration: none;
  font-weight: 800;
  border: 1px solid var(--line);
  background: rgba(255, 255, 255, 0.06);
  color: var(--text);
}

.button.primary {
  background: var(--accent);
  color: #111827;
  border-color: transparent;
}

.button:hover,
.button:focus {
  transform: translateY(-1px);
  box-shadow: 0 12px 28px rgba(0, 0, 0, 0.20);
}

.section {
  padding: 54px 0;
}

.section-intro {
  max-width: 780px;
  color: var(--muted);
  margin: 0 0 24px;
  font-size: 1.06rem;
}

.grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 18px;
}

.card {
  grid-column: span 6;
  background: linear-gradient(180deg, rgba(255, 255, 255, 0.08), rgba(255, 255, 255, 0.04));
  border: 1px solid var(--line);
  border-radius: var(--radius);
  padding: 24px;
  box-shadow: var(--shadow);
}

.card.featured {
  grid-column: span 12;
  background:
    linear-gradient(135deg, rgba(250, 204, 21, 0.16), rgba(56, 189, 248, 0.12)),
    linear-gradient(180deg, rgba(255, 255, 255, 0.10), rgba(255, 255, 255, 0.05));
}

.card p {
  color: var(--muted);
  margin: 12px 0 0;
}

.tag-row {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 16px;
}

.tag {
  display: inline-flex;
  border: 1px solid var(--line);
  border-radius: 999px;
  color: var(--muted);
  padding: 4px 9px;
  font-size: 0.84rem;
}

.project-list {
  margin: 16px 0 0;
  padding-left: 1.15rem;
  color: var(--muted);
}

.project-list li + li {
  margin-top: 8px;
}

.project-list strong {
  color: var(--text);
}

.project-link {
  display: inline-flex;
  margin-top: 18px;
  color: var(--accent);
  text-decoration: none;
  font-weight: 800;
}

.project-link:hover,
.project-link:focus {
  text-decoration: underline;
}

.principles {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 14px;
  margin-top: 22px;
}

.principle {
  border: 1px solid var(--line);
  border-radius: 18px;
  padding: 18px;
  background: rgba(255, 255, 255, 0.045);
}

.principle strong {
  display: block;
  margin-bottom: 6px;
  color: var(--good);
}

.principle span {
  color: var(--muted);
  font-size: 0.96rem;
}

.terminal {
  background: #020617;
  border: 1px solid var(--line);
  border-radius: var(--radius);
  padding: 22px;
  overflow-x: auto;
  box-shadow: var(--shadow);
}

code,
pre {
  font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace;
}

pre {
  margin: 0;
  color: #d1fae5;
  font-size: 0.96rem;
}

footer {
  border-top: 1px solid var(--line);
  padding: 36px 0 48px;
  color: var(--muted);
}

footer .shell {
  display: flex;
  justify-content: space-between;
  gap: 18px;
  flex-wrap: wrap;
}

footer a {
  color: var(--text);
  text-decoration: none;
}

footer a:hover,
footer a:focus {
  text-decoration: underline;
}

@media (max-width: 820px) {
  .topbar {
    align-items: flex-start;
    flex-direction: column;
    padding: 14px 0;
  }

  nav {
    justify-content: flex-start;
  }

  .hero {
    padding-top: 58px;
  }

  .card,
  .card.featured {
    grid-column: span 12;
  }

  .principles {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 540px) {
  .principles {
    grid-template-columns: 1fr;
  }

  .button {
    width: 100%;
  }
}

  </style>
</head>
<body>
  <a class="skip-link" href="#main">Skip to main content</a>  <header>
    <div class="shell topbar">
      <a class="brand" href="#top" aria-label="Gydos.org home">
        <strong>Gydos.org</strong>
        <span>small tools · deep practice · local-first software</span>
      </a>
      <nav aria-label="Primary navigation">
        <a href="#work">Work</a>
        <a href="#practice">Practice</a>
        <a href="#roadmap">Roadmap</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>  <main id="main">
    <section id="top" class="hero shell">
      <span class="eyebrow">Public workbench</span>
      <h1>Plain text, local tools, versioned learning, and creative systems that can be understood.</h1>
      <p class="lead">
        Gydos.org is a growing public workspace for text-first computing, small reproducible environments,
        local-first document tools, and scriptable sound-and-reading systems for study, focus, prayer,
        recovery, and creative work.
      </p>
      <div class="button-row">
        <a class="button primary" href="https://github.com/gydos-dot-org">View GitHub profile</a>
        <a class="button" href="https://github.com/gydos-dot-org/gydos-dot-org.github.io">View this site repository</a>
      </div>
    </section><section id="work" class="section shell">
  <h2>Current public projects</h2>
  <p class="section-intro">
    Some work is already public. Some work is still being cleaned up before it deserves a repository.
    The common thread is reducing friction between thought, text, command, memory, and publication —
    while keeping the tools small enough to understand, repair, and teach.
  </p>

  <div class="grid">
    <article class="card featured">
      <h3>Smellinux + vishgit</h3>
      <p>
        The cornerstone project is <strong>Smellinux</strong>: a small Linux learning and working environment
        built around a plain, memorable discipline — edit with <strong>vim</strong>, execute with
        <strong>sh</strong>, and remember with <strong>git</strong>. The public repository is not rushed yet;
        the project is being shaped carefully so the first committed version can be readable,
        reproducible, and worth teaching from.
      </p>
      <div class="tag-row" aria-label="Project tags">
        <span class="tag">pre-public cornerstone</span>
        <span class="tag">vim</span>
        <span class="tag">POSIX sh</span>
        <span class="tag">git</span>
        <span class="tag">Alpine Linux</span>
        <span class="tag">CSV literacy</span>
      </div>
      <a class="project-link" href="#roadmap">See where it fits →</a>
    </article>

    <article class="card">
      <h3>Android-on-Android Development Toolchain</h3>
      <p>
        A reproducible Termux-based Android app development workflow that builds real APKs directly
        on an Android phone, using OpenJDK, Gradle, Android SDK command-line tools, Kotlin/Java,
        and <code>aapt2</code>.
      </p>
      <p>
        Demonstrated targets include Falling Blocks, Pong Invaders, KJVOnTap experiments, and the
        planned Android port of Meditation Soundbox.
      </p>
      <ul class="project-list">
        <li><strong>Current status:</strong> successfully building toward local APK generation from Android itself.</li>
        <li><strong>Best use cases:</strong> education, prototyping, phone-native development, and reproducible public documentation.</li>
        <li><strong>Production note:</strong> Google Play production readiness requires API 35+ targeting.</li>
        <li><strong>Known blocker:</strong> the available Termux <code>aapt2</code> package links API 34 but appears to fail against Android 35/36 platform jars, so Play-compliant builds require further <code>aapt2</code> / toolchain work.</li>
      </ul>
      <div class="tag-row" aria-label="Project tags">
        <span class="tag">Termux</span>
        <span class="tag">Android SDK</span>
        <span class="tag">Gradle</span>
        <span class="tag">OpenJDK</span>
        <span class="tag">Kotlin / Java</span>
        <span class="tag">aapt2</span>
        <span class="tag">APK builds</span>
      </div>
      <a class="project-link" href="#roadmap">Document the toolchain →</a>
    </article>

    <article class="card">
      <h3>Siftlog Cathedral</h3>
      <p>
        A local-first C# application for gathering scattered writing and documents into a uniform,
        reverse-chronological HTML reading surface. This repository is public, but still being cleaned up:
        the next pass is about a proper <code>.gitignore</code>, clearer boundaries, and a more deliberate push history.
      </p>
      <div class="tag-row" aria-label="Project tags">
        <span class="tag">C#</span>
        <span class="tag">.NET</span>
        <span class="tag">local web</span>
        <span class="tag">Markdown</span>
        <span class="tag">personal knowledge</span>
      </div>
      <a class="project-link" href="https://github.com/gydos-dot-org/siftlog_cathedral">Open repository →</a>
    </article>

    <article class="card">
      <h3>Meditation Soundbox</h3>
      <p>
        A Windows-first, local-first console instrument for generated meditative/electronic soundscapes,
        live frequency changes, rhythm and synthesis variation, Piper text-to-speech, pasted readings,
        and KJV / Meta-V scripture loading.
      </p>
      <div class="tag-row" aria-label="Project tags">
        <span class="tag">C#</span>
        <span class="tag">audio</span>
        <span class="tag">Piper TTS</span>
        <span class="tag">KJV / Meta-V</span>
        <span class="tag">scriptable sessions</span>
      </div>
      <a class="project-link" href="https://github.com/gydos-dot-org/meditation-soundbox">Open repository →</a>
    </article>
  </div>
</section>

<section id="practice" class="section shell">
  <h2>The practice</h2>
  <p class="section-intro">
    This work is not only about apps. It is about building an understandable way to work: readable text,
    repeatable commands, visible history, and tools that can be explained line by line.
  </p>

  <div class="principles">
    <div class="principle">
      <strong>Edit</strong>
      <span>Use plain text as the common surface for notes, code, data, documentation, and reflection.</span>
    </div>
    <div class="principle">
      <strong>Execute</strong>
      <span>Prefer small shell scripts and transparent command-line flows over hidden machinery.</span>
    </div>
    <div class="principle">
      <strong>Remember</strong>
      <span>Let git preserve the work as history: drafts, changes, experiments, and decisions.</span>
    </div>
    <div class="principle">
      <strong>Publish</strong>
      <span>Use public repositories and simple pages to turn learning into shared artifacts.</span>
    </div>
  </div>
</section>

<section id="roadmap" class="section shell">
  <h2>Near-term direction</h2>
  <p class="section-intro">
    The immediate goal is to make the public work easier to enter without pretending every project is finished.
    The Android-on-Android toolchain deserves a reproducible guide and repository, with KJVOnTap,
    Falling Blocks, Pong Invaders, and the Meditation Soundbox Android 16 port documented as concrete proof
    of the workflow. Smellinux should become a first-class public project when it is ready; Siftlog Cathedral
    needs cleanup; Meditation Soundbox needs clearer release notes, install paths, and roadmap language.
  </p>

  <div class="terminal" aria-label="Roadmap shown as terminal-style text">
    <pre><code>$ next

1. Give github.gydos.org a true landing page.


2. Document the Android-on-Android development toolchain as a reproducible public project.


3. Add review pages for KJVOnTap, Falling Blocks, Pong Invaders, and the Meditation Soundbox Android 16 port.


4. Keep Smellinux central, but do not publish it carelessly.


5. Prepare Smellinux / vishgit as a first-class repository with scripts, lessons, and logs.


6. Clean up Siftlog Cathedral: .gitignore, generated files, README, and push history.


7. Grow Meditation Soundbox toward mixer buses, logs, scripts, voice selection, and smoother sessions.


8. Split each project page into: purpose, status, install, roadmap, and development log.


9. Keep everything small enough to read, run, explain, and version.</code></pre>

   </div>
 </section> <section id="contact" class="section shell">
   <h2>Contact and links</h2>
   <p class="section-intro">
     The best public entry point is the GitHub profile and the project repositories. For project-related contact,
     use the public Gydos.org email listed with the repositories.
   </p>
   <div class="button-row">
     <a class="button primary" href="https://github.com/gydos-dot-org">github.com/gydos-dot-org</a>
     <a class="button" href="mailto:paul@gydos.org">paul@gydos.org</a>
   </div>
 </section>

  </main>  <footer>
    <div class="shell">
      <span>© 2026 Gydos.org. Built as a static GitHub Pages site.</span>
      <span><a href="https://github.com/gydos-dot-org/gydos-dot-org.github.io">Improve this page on GitHub</a></span>
    </div>
  </footer>
</body>
</html>