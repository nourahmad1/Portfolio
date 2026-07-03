<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nour Albzoor — Computer Systems Engineer</title>
<meta name="description" content="Portfolio of Nour Albzoor — Computer Systems Engineering student specializing in Backend, QA, and embedded hardware.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#0B1520;
    --panel:#101C2C;
    --panel-2:#0E1826;
    --line:#1E2E40;
    --teal:#35C9C1;
    --teal-dim:#1F7C77;
    --amber:#F5A623;
    --paper:#EDF2F4;
    --muted:#7C93A6;
    --radius:10px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--ink);
    color:var(--paper);
    font-family:'Inter',sans-serif;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,.mono{font-family:'Space Grotesk',sans-serif;}
  .mono-utility{font-family:'JetBrains Mono',monospace;}
  a{color:inherit;text-decoration:none;}
  ::selection{background:var(--teal);color:var(--ink);}

  /* focus visibility */
  a:focus-visible, button:focus-visible{
    outline:2px solid var(--teal);
    outline-offset:3px;
  }

  .wrap{max-width:1040px;margin:0 auto;padding:0 28px;}

  /* NAV */
  header.nav{
    position:sticky;top:0;z-index:50;
    background:rgba(11,21,32,0.86);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--line);
  }
  .nav-inner{
    max-width:1040px;margin:0 auto;padding:16px 28px;
    display:flex;align-items:center;justify-content:space-between;
  }
  .brand{
    font-family:'JetBrains Mono',monospace;
    font-size:15px;color:var(--teal);letter-spacing:1px;
  }
  .brand span{color:var(--muted);}
  nav.links{display:flex;gap:26px;font-size:14px;color:var(--muted);}
  nav.links a{transition:color .2s;}
  nav.links a:hover{color:var(--teal);}

  /* HERO */
  .hero{
    padding:96px 0 64px;
    border-bottom:1px solid var(--line);
    position:relative;
    overflow:hidden;
  }
  .hero::before{
    content:"";
    position:absolute;inset:0;
    background-image:
      linear-gradient(var(--line) 1px, transparent 1px),
      linear-gradient(90deg, var(--line) 1px, transparent 1px);
    background-size:42px 42px;
    opacity:0.18;
    mask-image:radial-gradient(ellipse 60% 60% at 30% 20%, black, transparent);
  }
  .hero-inner{position:relative;z-index:1;}
  .prompt-line{
    font-family:'JetBrains Mono',monospace;
    color:var(--teal);
    font-size:14px;
    margin-bottom:18px;
    display:flex;align-items:center;gap:8px;
  }
  .prompt-line .caret{
    display:inline-block;width:8px;height:16px;background:var(--teal);
    animation:blink 1.1s steps(1) infinite;
  }
  @keyframes blink{50%{opacity:0;}}
  .hero h1{
    font-size:clamp(38px,6vw,64px);
    font-weight:700;
    letter-spacing:-1px;
    margin:0 0 6px;
    color:var(--paper);
  }
  .hero h1 .accent{color:var(--teal);}
  .hero .role{
    font-size:clamp(16px,2.2vw,20px);
    color:var(--muted);
    margin:0 0 30px;
    font-weight:500;
  }
  .status-strip{
    display:flex;flex-wrap:wrap;gap:10px;margin-bottom:36px;
  }
  .status-pill{
    font-family:'JetBrains Mono',monospace;
    font-size:12.5px;
    padding:8px 14px;
    border:1px solid var(--line);
    border-radius:6px;
    background:var(--panel);
    color:var(--paper);
    display:flex;align-items:center;gap:8px;
  }
  .status-pill b{color:var(--teal);font-weight:600;}
  .hero-cta{display:flex;gap:14px;flex-wrap:wrap;}
  .btn{
    font-family:'Space Grotesk',sans-serif;
    font-weight:600;font-size:14.5px;
    padding:13px 24px;
    border-radius:7px;
    display:inline-block;
    transition:transform .15s ease, box-shadow .15s ease, background .15s ease;
  }
  .btn-primary{background:var(--teal);color:var(--ink);}
  .btn-primary:hover{transform:translateY(-2px);box-shadow:0 8px 22px rgba(53,201,193,0.25);}
  .btn-ghost{border:1px solid var(--line);color:var(--paper);}
  .btn-ghost:hover{border-color:var(--teal);color:var(--teal);}

  /* SECTION shared */
  section{padding:64px 0;border-bottom:1px solid var(--line);}
  .eyebrow{
    font-family:'JetBrains Mono',monospace;
    color:var(--amber);
    font-size:12.5px;
    letter-spacing:2px;
    margin:0 0 10px;
  }
  section h2{
    font-size:clamp(24px,3.4vw,32px);
    margin:0 0 28px;
    color:var(--paper);
  }

  /* ABOUT */
  .about-grid{display:grid;grid-template-columns:1.4fr 1fr;gap:48px;}
  .about-grid p{color:#C7D5DE;font-size:15.5px;margin:0 0 14px;}
  .facts{
    font-family:'JetBrains Mono',monospace;
    font-size:13px;
    border:1px solid var(--line);
    border-radius:var(--radius);
    background:var(--panel);
    padding:20px;
  }
  .facts div{display:flex;justify-content:space-between;padding:7px 0;border-bottom:1px dashed var(--line);}
  .facts div:last-child{border-bottom:none;}
  .facts span:first-child{color:var(--muted);}
  .facts span:last-child{color:var(--paper);text-align:right;}

  /* SKILLS */
  .skill-groups{display:grid;grid-template-columns:repeat(2,1fr);gap:22px;}
  .skill-card{
    border:1px solid var(--line);
    border-radius:var(--radius);
    background:var(--panel);
    padding:22px;
  }
  .skill-card h3{
    font-size:14px;
    color:var(--teal);
    margin:0 0 14px;
    font-family:'JetBrains Mono',monospace;
    letter-spacing:1px;
  }
  .tag-row{display:flex;flex-wrap:wrap;gap:8px;}
  .tag{
    font-size:12.5px;
    padding:6px 11px;
    border-radius:5px;
    background:var(--panel-2);
    border:1px solid var(--line);
    color:#D7E4EA;
  }

  /* EXPERIENCE timeline */
  .timeline{position:relative;padding-left:26px;}
  .timeline::before{
    content:"";position:absolute;left:5px;top:6px;bottom:6px;width:2px;
    background:linear-gradient(var(--teal), var(--line));
  }
  .t-item{position:relative;padding-bottom:34px;}
  .t-item:last-child{padding-bottom:0;}
  .t-item::before{
    content:"";position:absolute;left:-26px;top:4px;width:11px;height:11px;
    border-radius:50%;background:var(--ink);border:2px solid var(--teal);
  }
  .t-date{
    font-family:'JetBrains Mono',monospace;font-size:12.5px;color:var(--amber);
    margin-bottom:6px;display:block;
  }
  .t-item h3{margin:0 0 6px;font-size:17px;color:var(--paper);}
  .t-item p{margin:0;color:#B9C8D2;font-size:14.5px;}

  /* PROJECTS */
  .project-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:20px;}
  .card{
    border:1px solid var(--line);
    border-radius:var(--radius);
    background:var(--panel);
    padding:22px;
    display:flex;flex-direction:column;gap:12px;
    transition:border-color .2s, transform .2s;
  }
  .card:hover{border-color:var(--teal-dim);transform:translateY(-3px);}
  .card-top{display:flex;justify-content:space-between;align-items:flex-start;gap:10px;}
  .card h3{font-size:17px;margin:0;color:var(--paper);}
  .badge{
    font-family:'JetBrains Mono',monospace;
    font-size:10.5px;letter-spacing:.5px;
    padding:4px 9px;border-radius:4px;white-space:nowrap;
  }
  .badge-hw{background:rgba(245,166,35,0.14);color:var(--amber);border:1px solid rgba(245,166,35,0.35);}
  .badge-sw{background:rgba(53,201,193,0.12);color:var(--teal);border:1px solid rgba(53,201,193,0.35);}
  .badge-qa{background:rgba(167,139,250,0.14);color:#B7A6F7;border:1px solid rgba(167,139,250,0.35);}
  .card p{margin:0;color:#B9C8D2;font-size:14px;flex-grow:1;}
  .card-link{
    font-family:'JetBrains Mono',monospace;font-size:12.5px;color:var(--teal);
    display:inline-flex;align-items:center;gap:6px;margin-top:4px;
  }
  .card-link:hover{text-decoration:underline;}

  /* EDUCATION */
  .edu-item{margin-bottom:20px;}
  .edu-item:last-child{margin-bottom:0;}
  .edu-item .t-date{margin-bottom:4px;}
  .edu-item h3{margin:0 0 4px;font-size:16px;}
  .edu-item p{margin:0;color:#B9C8D2;font-size:14.5px;}

  /* CONTACT */
  .contact-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:16px;}
  .contact-card{
    border:1px solid var(--line);border-radius:var(--radius);
    background:var(--panel);padding:20px;text-align:center;
    transition:border-color .2s, transform .2s;
  }
  .contact-card:hover{border-color:var(--teal);transform:translateY(-2px);}
  .contact-card .label{
    font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--muted);
    letter-spacing:1px;margin-bottom:8px;
  }
  .contact-card .value{font-size:13.5px;color:var(--paper);word-break:break-word;}

  footer{padding:30px 0;text-align:center;color:var(--muted);font-size:13px;font-family:'JetBrains Mono',monospace;}

  /* responsive */
  @media (max-width:760px){
    .about-grid,.skill-groups,.project-grid{grid-template-columns:1fr;}
    .contact-grid{grid-template-columns:repeat(2,1fr);}
    nav.links{display:none;}
  }

  @media (prefers-reduced-motion: reduce){
    html{scroll-behavior:auto;}
    .caret{animation:none;}
    *{transition:none !important;}
  }

  .reveal{opacity:0;transform:translateY(16px);transition:opacity .6s ease, transform .6s ease;}
  .reveal.in{opacity:1;transform:none;}
</style>
</head>
<body>

<header class="nav">
  <div class="nav-inner">
    <div class="brand">nour<span>@</span>albzoor<span>:~$</span></div>
    <nav class="links">
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#experience">Experience</a>
      <a href="#projects">Projects</a>
      <a href="#education">Education</a>
      <a href="#contact">Contact</a>
    </nav>
  </div>
</header>

<section class="hero">
  <div class="wrap hero-inner">
    <div class="prompt-line">&gt; whoami <span class="caret"></span></div>
    <h1>Nour <span class="accent">Albzoor</span></h1>
    <p class="role">Computer Systems Engineering Student — Backend &amp; QA</p>

    <div class="status-strip">
      <div class="status-pill"><b>✓</b> HARDWARE — ESP32 / Arduino</div>
      <div class="status-pill"><b>✓</b> BACKEND — MVC / Oracle APEX</div>
      <div class="status-pill"><b>✓</b> QA — Manual &amp; Automation</div>
    </div>

    <div class="hero-cta">
      <a class="btn btn-primary" href="#projects">View Projects</a>
      <a class="btn btn-ghost" href="#contact">Contact Me</a>
    </div>
  </div>
</section>

<section id="about">
  <div class="wrap">
    <p class="eyebrow">01 — ABOUT</p>
    <h2>Building things, then breaking them on purpose.</h2>
    <div class="about-grid reveal">
      <div>
        <p>I'm a Computer Systems Engineering student at Arab American University, working across the full stack of a product: firmware on ESP32 boards, backend logic with MVC and Oracle APEX, and — most of all — the discipline of testing it properly before it ships.</p>
        <p>My field training at ITG put me inside a real QA pipeline: writing test cases and test plans, automating flows with Selenium and Playwright, and filing bug reports that development teams could actually act on. I bring that same rigor to the hardware and software I build myself.</p>
      </div>
      <div class="facts">
        <div><span>Location</span><span>Jenin, Palestine</span></div>
        <div><span>Focus</span><span>Backend + QA</span></div>
        <div><span>Degree</span><span>B.Sc. Computer Systems Eng.</span></div>
        <div><span>GPA (Tawjihi)</span><span>98.3%</span></div>
        <div><span>Status</span><span>Open to training / internship</span></div>
      </div>
    </div>
  </div>
</section>

<section id="skills">
  <div class="wrap">
    <p class="eyebrow">02 — SKILLS</p>
    <h2>What I test with, and what I build with.</h2>
    <div class="skill-groups reveal">
      <div class="skill-card">
        <h3>QA &amp; TESTING</h3>
        <div class="tag-row">
          <span class="tag">API Testing</span><span class="tag">Manual Testing</span>
          <span class="tag">Automation Testing</span><span class="tag">Selenium</span>
          <span class="tag">Playwright</span><span class="tag">TestNG</span>
          <span class="tag">Bug Reporting</span><span class="tag">Jira</span>
          <span class="tag">Postman</span><span class="tag">Fiddler</span>
          <span class="tag">Agile / Scrum</span>
        </div>
      </div>
      <div class="skill-card">
        <h3>BACKEND &amp; SOFTWARE</h3>
        <div class="tag-row">
          <span class="tag">MVC Architecture</span><span class="tag">Oracle APEX</span>
          <span class="tag">C++</span><span class="tag">OOP</span>
          <span class="tag">HTML / CSS / JS</span><span class="tag">Flutter</span>
          <span class="tag">Dart</span><span class="tag">Git / GitHub</span>
        </div>
      </div>
      <div class="skill-card">
        <h3>HARDWARE &amp; FIRMWARE</h3>
        <div class="tag-row">
          <span class="tag">ESP32</span><span class="tag">Arduino</span>
          <span class="tag">BLE</span><span class="tag">ESP-NOW</span>
          <span class="tag">Sensors &amp; Motors</span>
        </div>
      </div>
      <div class="skill-card">
        <h3>SOFT SKILLS</h3>
        <div class="tag-row">
          <span class="tag">Time Management</span><span class="tag">Teamwork</span>
          <span class="tag">Problem-Solving</span><span class="tag">Communication</span>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="experience">
  <div class="wrap">
    <p class="eyebrow">03 — EXPERIENCE</p>
    <h2>Where I've put the skills to work.</h2>
    <div class="timeline reveal">
      <div class="t-item">
        <span class="t-date">OCT 5 — DEC 9, 2025</span>
        <h3>QA Field Training — ITG</h3>
        <p>316 hours in the QA department: manual &amp; automation testing (Selenium, TestNG, Maven, Playwright), Test Cases, Test Plans, Traceability Matrix, and documented Bug Reports tracked in Jira.</p>
      </div>
      <div class="t-item">
        <span class="t-date">OCT 2024 — PRESENT</span>
        <h3>Automation Testing Training — Hope International Company</h3>
        <p>Automating core test flows and building repeatable test suites for web software.</p>
      </div>
      <div class="t-item">
        <span class="t-date">JULY 2024 — SEP 2024</span>
        <h3>Manual Testing Training — Hope International Company</h3>
        <p>Manual functional testing, test case design, and defect logging.</p>
      </div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="wrap">
    <p class="eyebrow">04 — PROJECTS</p>
    <h2>Selected work.</h2>
    <div class="project-grid reveal">

      <div class="card">
        <div class="card-top"><h3>IRFPE</h3><span class="badge badge-hw">HARDWARE</span></div>
        <p>ESP32 dual-microcontroller firmware for an educational robot: BLE control, ESP-NOW inter-board communication, and motor / sensor / display / audio modules.</p>
        <a class="card-link" href="https://github.com/nourahmad1/Senior-Hardware" target="_blank" rel="noopener">↳ github.com/nourahmad1/Senior-Hardware</a>
      </div>

      <div class="card">
        <div class="card-top"><h3>RoboLearn</h3><span class="badge badge-sw">SOFTWARE</span></div>
        <p>Flutter mobile app + Firebase backend that pairs with the IRFPE robot over BLE to teach programming concepts interactively.</p>
        <a class="card-link" href="https://github.com/nourahmad1" target="_blank" rel="noopener">↳ github.com/nourahmad1</a>
      </div>

      <div class="card">
        <div class="card-top"><h3>Selenium Test Suite</h3><span class="badge badge-qa">QA</span></div>
        <p>Automated testing project built with Selenium covering core user flows end-to-end.</p>
        <a class="card-link" href="https://github.com/nourahmad1/nourahmad1-Selenium" target="_blank" rel="noopener">↳ github.com/nourahmad1/nourahmad1-Selenium</a>
      </div>

      <div class="card">
        <div class="card-top"><h3>QA Training Docs</h3><span class="badge badge-qa">QA</span></div>
        <p>Test cases, test plans, and documentation produced during hands-on software testing training.</p>
        <a class="card-link" href="https://github.com/nourahmad1/Qa-training-" target="_blank" rel="noopener">↳ github.com/nourahmad1/Qa-training-</a>
      </div>

      <div class="card">
        <div class="card-top"><h3>Heritage Center</h3><span class="badge badge-sw">SOFTWARE</span></div>
        <p>.NET application built for a Heritage Center, covering data management and a user-facing interface.</p>
        <a class="card-link" href="https://github.com/nourahmad1" target="_blank" rel="noopener">↳ github.com/nourahmad1</a>
      </div>

      <div class="card">
        <div class="card-top"><h3>Mall Management System</h3><span class="badge badge-sw">SOFTWARE</span></div>
        <p>Oracle APEX application for managing mall operations, tenants, and reporting.</p>
        <a class="card-link" href="https://github.com/nourahmad1" target="_blank" rel="noopener">↳ github.com/nourahmad1</a>
      </div>

      <div class="card">
        <div class="card-top"><h3>Omesha Shop</h3><span class="badge badge-sw">SOFTWARE</span></div>
        <p>Flutter e-commerce app (Dart) with product browsing, cart, and checkout flow.</p>
        <a class="card-link" href="https://github.com/nourahmad1/Flutter" target="_blank" rel="noopener">↳ github.com/nourahmad1/Flutter</a>
      </div>

    </div>
  </div>
</section>

<section id="education">
  <div class="wrap">
    <p class="eyebrow">05 — EDUCATION</p>
    <h2>Academic background.</h2>
    <div class="reveal">
      <div class="edu-item">
        <span class="t-date">OCT 2021 — PRESENT</span>
        <h3>B.Sc. Computer Systems Engineering</h3>
        <p>Arab American University, Jenin, Palestine.</p>
      </div>
      <div class="edu-item">
        <span class="t-date">JULY 2021</span>
        <h3>Tawjihi — Scientific Stream</h3>
        <p>Raba Secondary Girls' School, Raba, Jenin, Palestine — GPA 98.3%.</p>
      </div>
    </div>
  </div>
</section>

<section id="contact" style="border-bottom:none;">
  <div class="wrap">
    <p class="eyebrow">06 — CONTACT</p>
    <h2>Let's talk.</h2>
    <div class="contact-grid reveal">
      <a class="contact-card" href="mailto:nourbzour65@gmail.com">
        <div class="label">EMAIL</div>
        <div class="value">nourbzour65@gmail.com</div>
      </a>
      <a class="contact-card" href="tel:+970569084903">
        <div class="label">PHONE</div>
        <div class="value">0569084903</div>
      </a>
      <a class="contact-card" href="https://github.com/nourahmad1" target="_blank" rel="noopener">
        <div class="label">GITHUB</div>
        <div class="value">nourahmad1</div>
      </a>
      <a class="contact-card" href="https://www.linkedin.com/in/nour-bzour-5aa5092b8" target="_blank" rel="noopener">
        <div class="label">LINKEDIN</div>
        <div class="value">nour-bzour</div>
      </a>
    </div>
  </div>
</section>

<footer>
  &copy; <span id="year"></span> Nour Albzoor — built with HTML, CSS &amp; a lot of test cases.
</footer>

<script>
  document.getElementById('year').textContent = new Date().getFullYear();

  // scroll reveal
  const revealEls = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if(e.isIntersecting){
        e.target.classList.add('in');
        io.unobserve(e.target);
      }
    });
  }, { threshold: 0.15 });
  revealEls.forEach(el => io.observe(el));
</script>

</body>
</html>
