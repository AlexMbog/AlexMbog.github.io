<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Labs | Alex Mbogo</title>
  <link rel="stylesheet" href="/assets/css/style.css">
</head>

<body>

  <!-- NAVBAR -->
  <header class="navbar">
    <div class="logo">Alex Mbogo</div>
    <nav>
      <a href="/">Home</a>
      <a href="/projects.html">Projects</a>
      <a href="/labs.html">Labs</a>
      <a href="/resume.html">Resume</a>
      <a href="/contact.html">Contact</a>
    </nav>
  </header>

  <!-- HEADER -->
  <section class="container">
    <h1>Labs & Case Studies</h1>
    <p style="max-width:700px; opacity:0.7;">
      Real-world cybersecurity labs, cloud configurations, and system exploitation case studies.
    </p>
  </section>

  <!-- FILTER -->
  <section class="container">
    <div class="filter-bar">
      <button onclick="filterLabs('all')">All</button>
      <button onclick="filterLabs('web')">Web</button>
      <button onclick="filterLabs('cloud')">Cloud</button>
      <button onclick="filterLabs('linux')">Linux</button>
    </div>
  </section>

  <!-- LAB GRID -->
  <section class="container">
    <div class="grid" id="labGrid">
 <!-- HACKTHISITE -->
     <div class="card lab web">
      <h3>HackThisSite Labs</h3>
        <p>Web exploitation challenges and vulnerability analysis.</p>

  <div class="badges">
          <span class="badge medium">Intermediate</span>
          <span class="badge">Web</span>
        </div>
   <a href="/HackThisSite.html" class="btn secondary">Open Lab →</a>
      </div>
 <!-- HOME LAB -->
   <div class="card lab linux">
        <h3>Home Lab</h3>
        <p>Recon, scanning, and privilege escalation practice.</p>
  <div class="badges">
          <span class="badge hard">Advanced</span>
          <span class="badge">Linux</span>
        </div>
  <a href="/HomeLab.html" class="btn secondary">Open Lab →</a>
      </div>

      <!-- CLOUD -->
  <div class="card lab cloud">
        <h3>Cloud Security</h3>
        <p>IAM, RBAC, governance and secure cloud configs.</p>

  <div class="badges">
          <span class="badge easy">Beginner</span>
          <span class="badge">Cloud</span>
        </div>

<a href="/CloudSecurity.html" class="btn secondary">Open Lab →</a>
      </div>

  </div>
  </section>

</body>

<!-- FILTER SCRIPT -->
<script>
function filterLabs(type) {
  const labs = document.querySelectorAll(".lab");

  labs.forEach(lab => {
    if (type === "all" || lab.classList.contains(type)) {
      lab.style.display = "block";
    } else {
      lab.style.display = "none";
    }
  });
}
</script>

</html>
