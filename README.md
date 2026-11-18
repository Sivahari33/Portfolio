# Ex01 Portfolio
## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
index.html:

```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sivaharibalan Karthikeyan | Portfolio</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <nav>
        <h2>SK.</h2>
        <div class="nav-links">
            <a href="#about">About</a>
            <a href="#skills">Skills</a>
            <a href="#experience">Experience</a>
            <a href="#projects">Projects</a>
            <a href="#contact">Let's Talk</a>
        </div>
    </nav>
</header>

<!-- Home Section -->
<section id="home" class="hero">
    <div class="hero-copy">
        <p>ENGINEERING STUDENT · CHENNAI, INDIA</p>

        <h1>Building ideas<br>
            into <span>digital reality.</span>
        </h1>

        <p>
            Hi, I'm <b>Sivaharibalan Karthikeyan</b>.
            I enjoy exploring technology, solving problems,
            and creating useful digital experiences.
        </p>

        <a href="#projects">Explore My Work</a>
    </div>

    <div class="hero-image">
        <img src="assets/profile.png" alt="My Profile">
    </div>
</section>

<!-- About Section -->
<section id="about">
    <h2>About Me</h2>

    <p>
        I'm an engineering student with a strong interest
        in software, cybersecurity, and emerging technologies.
        I enjoy learning new skills and developing practical projects.
    </p>

    <p>Location: Chennai, India</p>
    <p>Education: Engineering Student</p>
    <p>Specialization: Cybersecurity & Software Development</p>
    <p>Mobile: 9952186063</p>
    <p>Email: sivahari5030@gmail.com</p>
</section>

<!-- Skills Section -->
<section id="skills">
    <h2>Skills & Interests</h2>

    <div class="skill">
        <h3>Programming</h3>
        <p>C, Python, Java Basics</p>
    </div>

    <div class="skill">
        <h3>Web Development</h3>
        <p>HTML, CSS, JavaScript Basics</p>
    </div>

    <div class="skill">
        <h3>Cybersecurity</h3>
        <p>Kali Linux, TryHackMe, Cryptography</p>
    </div>
</section>

<!-- Experience Section -->
<section id="experience">
    <h2>Experience</h2>

    <h3>Cybersecurity Intern</h3>
    <h4>ReTech - Tambaram</h4>

    <p>
        Explored cybersecurity fundamentals and practical
        security workflows using TryHackMe and Kali Linux.
    </p>
</section>

<!-- Projects Section -->
<section id="projects">
    <h2>My Projects</h2>

    <div class="project">
        <h3>Fitness & Smart Health App</h3>
        <p>
            An application concept focused on fitness habits
            and tracking everyday health information.
        </p>
    </div>

    <div class="project">
        <h3>Cybersecurity Labs</h3>
        <p>
            Hands-on practice exploring cybersecurity
            fundamentals and Linux-based tools.
        </p>
    </div>
</section>

<!-- Contact Section -->
<section id="contact">
    <h2>Let's Connect</h2>

    <p>Mobile: <a href="tel:+919952186063">9952186063</a></p>

    <p>
        Email:
        <a href="mailto:sivahari5030@gmail.com">
            sivahari5030@gmail.com
        </a>
    </p>

    <a href="mailto:sivahari5030@gmail.com">
        Send Me an Email
    </a>
</section>

<footer>
    <p>© 2026 Sivaharibalan Karthikeyan. All Rights Reserved.</p>
</footer>

</body>
</html>
```
style.css:
```

:root {
    --bg: #090e18;
    --panel: #111a29;
    --panel2: #0d1522;
    --text: #f4f7fb;
    --muted: #9ba8ba;
    --line: rgba(255,255,255,.1);
    --cyan: #65e2d0;
    --blue: #7b9cff;
    --font: 'DM Sans', sans-serif;
    --display: 'Space Grotesk', sans-serif;
}

* {
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    margin: 0;
    background: var(--bg);
    color: var(--text);
    font-family: var(--font);
    line-height: 1.65;
}

a {
    color: inherit;
    text-decoration: none;
}

.container {
    width: min(1160px, calc(100% - 48px));
    margin: auto;
}

/* Header */

.site-header {
    position: sticky;
    top: 0;
    z-index: 20;
    background: rgba(9,14,24,.86);
    backdrop-filter: blur(18px);
    border-bottom: 1px solid var(--line);
}

.nav {
    height: 78px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.brand {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    font: 700 21px var(--display);
}

.brand-mark {
    display: grid;
    place-items: center;
    width: 34px;
    height: 34px;
    border-radius: 10px;
    background: linear-gradient(135deg,var(--cyan),var(--blue));
    color: #09121e;
}

.nav-links {
    display: flex;
    align-items: center;
    gap: 34px;
    color: #b9c3d2;
    font-size: 13px;
}

.nav-links a:hover {
    color: var(--cyan);
}

.nav-cta {
    border: 1px solid rgba(101,226,208,.5);
    padding: 10px 17px;
    border-radius: 6px;
    color: var(--cyan);
}

.menu-toggle {
    display: none;
}

/* Hero Section */

.hero {
    min-height: 690px;
    display: grid;
    grid-template-columns: 1.05fr .95fr;
    align-items: center;
    position: relative;
    padding: 35px 0 85px;
}

.eyebrow {
    font-size: 10px;
    letter-spacing: 2.3px;
    font-weight: 700;
    color: var(--cyan);
    margin-bottom: 22px;
}

.status-dot {
    display: inline-block;
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: var(--cyan);
    margin-right: 9px;
    box-shadow: 0 0 12px var(--cyan);
}

h1, h2 {
    font-family: var(--display);
    letter-spacing: -2.8px;
    line-height: 1.06;
}

h1 {
    font-size: clamp(48px,6vw,76px);
    margin-bottom: 24px;
}

.gradient-text {
    background: linear-gradient(100deg,var(--cyan),#9bb3ff);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
}

.hero-intro {
    max-width: 490px;
    color: var(--muted);
    font-size: 16px;
    line-height: 1.9;
}

.hero-intro strong {
    color: white;
}

.hero-actions {
    display: flex;
    align-items: center;
    gap: 28px;
    margin-top: 32px;
}

.button {
    display: inline-flex;
    align-items: center;
    gap: 24px;
    padding: 14px 20px;
    border-radius: 6px;
    font-size: 13px;
    font-weight: 700;
    transition: .2s;
}

.button:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 30px rgba(101,226,208,.15);
}

.primary {
    background: linear-gradient(110deg,var(--cyan),#9ab1ff);
    color: #09121e;
}

.text-link {
    font-size: 13px;
    color: #c8d1df;
}

/* Hero Image */

.hero-visual {
    height: 535px;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
}

.image-frame {
    width: 345px;
    height: 455px;
    position: relative;
    z-index: 2;
    border-radius: 180px 180px 16px 16px;
    overflow: hidden;
    border: 1px solid rgba(255,255,255,.22);
    box-shadow: 0 30px 90px rgba(0,0,0,.5);
}

.image-frame img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center 27%;
}

.image-glow {
    position: absolute;
    width: 380px;
    height: 380px;
    background: radial-gradient(circle,rgba(84,197,193,.2),transparent 68%);
    filter: blur(12px);
}

.orbit {
    position: absolute;
    border: 1px solid rgba(101,226,208,.2);
    border-radius: 50%;
}

.orbit-one {
    width: 500px;
    height: 270px;
    transform: rotate(-28deg);
}

.orbit-two {
    width: 550px;
    height: 340px;
    transform: rotate(38deg);
    border-color: rgba(123,156,255,.17);
}

/* About Section */

.section {
    padding: 105px 0;
}

.about-section,
.experience-section {
    background: var(--panel2);
    border-top: 1px solid var(--line);
    border-bottom: 1px solid var(--line);
}

.about-grid {
    display: grid;
    grid-template-columns: .85fr 1.15fr;
    gap: 90px;
}

.muted-heading {
    color: #78869b;
}

.about-content {
    padding-top: 7px;
    max-width: 620px;
}

.large-copy {
    font: 500 23px/1.5 var(--display);
    color: #e9eef6;
}

.about-content p {
    color: var(--muted);
    font-size: 14px;
    line-height: 1.9;
}

.info-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 27px;
}

.info-pills span {
    font-size: 10px;
    color: #bdc9d9;
    border: 1px solid var(--line);
    border-radius: 4px;
    padding: 7px 10px;
}

/* Skills Section */

.section-heading {
    display: flex;
    justify-content: space-between;
    align-items: end;
    margin-bottom: 42px;
}

.skill-grid {
    display: grid;
    grid-template-columns: repeat(3,1fr);
    gap: 17px;
}

.skill-card {
    position: relative;
    min-height: 255px;
    padding: 27px;
    background: var(--panel);
    border: 1px solid var(--line);
    border-radius: 9px;
    transition: .2s;
}

.skill-card:hover {
    transform: translateY(-5px);
    border-color: rgba(101,226,208,.4);
}

.skill-icon {
    font-size: 26px;
    color: var(--cyan);
    margin-bottom: 22px;
}

.skill-card h3 {
    font: 600 20px var(--display);
}

.skill-card p {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.8;
}

/* Experience Section */

.experience-section h2 {
    margin-bottom: 44px;
}

.timeline {
    border-left: 1px solid rgba(101,226,208,.45);
    margin-left: 8px;
    padding-left: 36px;
    position: relative;
    max-width: 720px;
}

.timeline-marker {
    position: absolute;
    left: -6px;
    top: 5px;
    width: 11px;
    height: 11px;
    border-radius: 50%;
    background: var(--cyan);
    box-shadow: 0 0 0 6px rgba(101,226,208,.1);
}

.timeline-content {
    background: var(--panel);
    border: 1px solid var(--line);
    border-radius: 9px;
    padding: 27px 30px;
}

.timeline-content h3 {
    font: 600 22px var(--display);
}

.timeline-content h4 {
    font-size: 12px;
    color: var(--cyan);
}

/* Projects Section */

.projects-section {
    background: #0b111d;
}

.project-grid {
    display: grid;
    grid-template-columns: 1.1fr .9fr;
    gap: 20px;
}

.project-card {
    background: var(--panel);
    border: 1px solid var(--line);
    border-radius: 9px;
    overflow: hidden;
    transition: .2s;
}

.project-card:hover {
    transform: translateY(-5px);
    border-color: rgba(101,226,208,.4);
}

.project-art {
    height: 245px;
    position: relative;
    display: grid;
    place-items: center;
}

.art-health {
    background: radial-gradient(circle,#214d5a,#122b3b 50%,#101b2a);
}

.art-security {
    background: radial-gradient(circle,#263d62,#111b30 58%,#0c1422);
}

.project-info {
    padding: 24px 26px 28px;
}

.project-info h3 {
    font: 600 20px var(--display);
}

.project-info p {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.8;
}

/* Contact Section */

.contact-section {
    padding: 110px 0;
    text-align: center;
    background: radial-gradient(ellipse at 50% 100%,#1b3545 0%,#0b1421 55%,#090e18 100%);
}

.contact-inner h2 {
    font-size: clamp(45px,6vw,68px);
    margin-bottom: 20px;
}

.contact-inner p {
    font-size: 13px;
    color: var(--muted);
}

.contact-details {
    display: flex;
    justify-content: center;
    gap: 18px;
    flex-wrap: wrap;
    margin: 0 auto 26px;
}

.contact-details a {
    display: flex;
    flex-direction: column;
    gap: 4px;
    min-width: 220px;
    padding: 14px 20px;
    border: 1px solid var(--line);
    border-radius: 7px;
    background: rgba(17,26,41,.55);
}

.contact-details a span {
    font-size: 9px;
    color: var(--cyan);
}

.contact-details a strong {
    font-size: 13px;
    color: var(--text);
}

/* Footer */

.footer {
    border-top: 1px solid var(--line);
    padding: 23px 0;
}

.footer-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

/* Responsive Design */

@media(max-width:800px) {

    .container {
        width: min(100% - 36px,600px);
    }

    .nav {
        height: 68px;
    }

    .menu-toggle {
        display: block;
    }

    .nav-links {
        display: none;
        position: absolute;
        top: 68px;
        left: 0;
        right: 0;
        padding: 20px 24px;
        background: #0d1522;
        flex-direction: column;
        align-items: flex-start;
        gap: 18px;
    }

    .nav-links.open {
        display: flex;
    }

    .hero {
        grid-template-columns: 1fr;
        padding-top: 70px;
        gap: 20px;
    }

    .hero-visual {
        height: 420px;
    }

    .image-frame {
        height: 370px;
        width: 280px;
    }

    .about-grid {
        grid-template-columns: 1fr;
        gap: 30px;
    }

    .section {
        padding: 75px 0;
    }

    .skill-grid {
        grid-template-columns: 1fr;
    }

    .project-grid {
        grid-template-columns: 1fr;
    }

    .contact-section {
        padding: 80px 0;
    }
}

@media(max-width:460px) {

    h1 {
        font-size: 48px;
    }

    .hero-visual {
        height: 365px;
    }

    .image-frame {
        height: 330px;
        width: 250px;
    }

    .hero-actions {
        gap: 18px;
        flex-wrap: wrap;
    }

    .large-copy {
        font-size: 20px;
    }

    .timeline {
        padding-left: 22px;
    }

    .timeline-content {
        padding: 22px 18px;
    }

    .footer-inner {
        gap: 12px;
        flex-wrap: wrap;
    }
}
```

## OUTPUT

<img width="1440" height="3947" alt="image" src="https://github.com/user-attachments/assets/15c1cbef-d845-49eb-a04e-b2af0b971c29" />

## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
