<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Kingdom Learning Hub | By Richard</title>

<meta name="description"
content="Kingdom Learning Hub by Richard — Grow in Faith. Grow in Knowledge. Grow in Life.">

<style>

/* =========================
   RESET
========================= */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

:root {
    --bg: #080b12;
    --bg-light: #101522;
    --card: rgba(255,255,255,0.06);
    --gold: #d4a017;
    --gold-light: #f1c75b;
    --white: #ffffff;
    --text: #e8eaf0;
    --muted: #9da5b5;
    --border: rgba(255,255,255,0.10);
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background: var(--bg);
    color: var(--text);
    line-height: 1.7;
    overflow-x: hidden;
}

a {
    text-decoration: none;
    color: inherit;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: auto;
}


/* =========================
   NAVBAR
========================= */

header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;

    background: rgba(8,11,18,0.82);
    backdrop-filter: blur(18px);
    border-bottom: 1px solid var(--border);
}

nav {
    height: 75px;

    display: flex;
    align-items: center;
    justify-content: space-between;
}

.logo {
    font-size: 20px;
    font-weight: 800;
    letter-spacing: -0.5px;
}

.logo span {
    color: var(--gold-light);
}

.logo small {
    display: block;
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 2px;
    text-transform: uppercase;
}

.menu {
    display: flex;
    list-style: none;
    gap: 28px;
}

.menu a {
    color: #d9dce5;
    font-size: 14px;
    transition: 0.3s;
}

.menu a:hover {
    color: var(--gold-light);
}

.menu-button {
    display: none;
    font-size: 28px;
    cursor: pointer;
}


/* =========================
   HERO
========================= */

.hero {
    min-height: 100vh;

    display: flex;
    align-items: center;
    text-align: center;

    position: relative;
    overflow: hidden;

    background:
        radial-gradient(circle at 50% 20%, rgba(212,160,23,0.15), transparent 35%),
        linear-gradient(135deg,#080b12,#111827);
}

.hero::before {
    content: "";
    position: absolute;

    width: 500px;
    height: 500px;

    border-radius: 50%;

    background: rgba(212,160,23,0.08);

    filter: blur(80px);

    top: 10%;
    left: 50%;

    transform: translateX(-50%);
}

.hero-content {
    position: relative;
    z-index: 2;

    max-width: 850px;
    margin: auto;
    padding-top: 70px;
}

.badge {
    display: inline-block;

    padding: 8px 15px;

    border: 1px solid rgba(212,160,23,0.35);
    border-radius: 50px;

    color: var(--gold-light);

    background: rgba(212,160,23,0.08);

    font-size: 12px;
    letter-spacing: 1px;

    margin-bottom: 25px;
}

.hero h1 {
    font-size: clamp(42px,7vw,78px);

    line-height: 1.05;

    letter-spacing: -3px;

    margin-bottom: 18px;
}

.hero h1 span {
    color: var(--gold-light);
}

.hero h2 {
    color: #cbd0dc;
    font-size: 20px;
    font-weight: 400;
    margin-bottom: 22px;
}

.hero p {
    color: var(--muted);
    font-size: 17px;
    max-width: 680px;
    margin: auto;
}

.hero strong {
    color: var(--gold-light);
}


/* =========================
   BUTTONS
========================= */

.buttons {
    margin-top: 35px;

    display: flex;
    justify-content: center;
    gap: 15px;

    flex-wrap: wrap;
}

.btn {
    min-width: 180px;

    padding: 14px 25px;

    border-radius: 8px;

    font-size: 14px;
    font-weight: 700;

    display: inline-flex;
    align-items: center;
    justify-content: center;

    transition: 0.3s;
}

.primary {
    background: linear-gradient(135deg,var(--gold),var(--gold-light));
    color: #111;

    box-shadow: 0 10px 30px rgba(212,160,23,0.18);
}

.primary:hover {
    transform: translateY(-4px);
    box-shadow: 0 15px 35px rgba(212,160,23,0.28);
}

.secondary {
    border: 1px solid var(--border);
    background: rgba(255,255,255,0.04);
    color: white;
}

.secondary:hover {
    border-color: var(--gold);
    color: var(--gold-light);
    transform: translateY(-4px);
}


/* =========================
   SECTIONS
========================= */

section {
    padding: 100px 0;
}

.section-title {
    text-align: center;
    max-width: 700px;
    margin: 0 auto 55px;
}

.section-title span {
    color: var(--gold-light);
    font-size: 12px;
    font-weight: bold;
    letter-spacing: 2px;
    text-transform: uppercase;
}

.section-title h2 {
    font-size: clamp(30px,5vw,45px);
    margin: 10px 0 12px;
}

.section-title p {
    color: var(--muted);
}


/* =========================
   FEATURE CARDS
========================= */

.cards {
    display: grid;

    grid-template-columns:
        repeat(auto-fit,minmax(250px,1fr));

    gap: 22px;
}

.card {
    background: linear-gradient(
        145deg,
        rgba(255,255,255,0.07),
        rgba(255,255,255,0.025)
    );

    border: 1px solid var(--border);

    border-radius: 16px;

    padding: 30px;

    transition: 0.35s;

    position: relative;
    overflow: hidden;
}

.card::before {
    content: "";

    position: absolute;

    width: 120px;
    height: 120px;

    background: rgba(212,160,23,0.08);

    border-radius: 50%;

    top: -60px;
    right: -60px;
}

.card:hover {
    transform: translateY(-8px);

    border-color: rgba(212,160,23,0.4);

    box-shadow:
        0 20px 50px rgba(0,0,0,0.25);
}

.icon {
    width: 55px;
    height: 55px;

    display: flex;
    align-items: center;
    justify-content: center;

    border-radius: 12px;

    background: rgba(212,160,23,0.10);

    font-size: 27px;

    margin-bottom: 20px;
}

.card h3 {
    margin-bottom: 10px;
    font-size: 20px;
}

.card p {
    color: var(--muted);
    font-size: 14px;
    margin-bottom: 20px;
}

.card-link {
    color: var(--gold-light);
    font-size: 13px;
    font-weight: bold;
}


/* =========================
   WORSHIP
========================= */

.worship {
    background:
        linear-gradient(
            180deg,
            #080b12,
            #0d111b
        );
}


/* =========================
   LEARNING
========================= */

.learning {
    background: #0b0f18;
}


/* =========================
   VERSE
========================= */

.verse {
    text-align: center;

    background:
        radial-gradient(
            circle at center,
            rgba(212,160,23,0.10),
            transparent 55%
        );

    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
}

.verse blockquote {
    max-width: 800px;

    margin: auto;

    font-size: clamp(20px,4vw,30px);

    font-style: italic;

    line-height: 1.6;
}

.verse cite {
    display: block;

    margin-top: 20px;

    color: var(--gold-light);

    font-size: 14px;

    font-style: normal;
    font-weight: bold;
}


/* =========================
   STATS
========================= */

.stats {
    display: grid;

    grid-template-columns:
        repeat(auto-fit,minmax(180px,1fr));

    gap: 20px;

    margin-top: 50px;
}

.stat {
    text-align: center;

    padding: 30px;

    background: var(--card);

    border: 1px solid var(--border);

    border-radius: 14px;
}

.stat h3 {
    color: var(--gold-light);

    font-size: 32px;
}

.stat p {
    color: var(--muted);
    font-size: 13px;
}


/* =========================
   ABOUT
========================= */

.about {
    background: #0d111b;
}

.about-grid {
    display: grid;

    grid-template-columns:
        1fr 1fr;

    gap: 60px;

    align-items: center;
}

.about-text span {
    color: var(--gold-light);

    font-size: 12px;

    letter-spacing: 2px;

    text-transform: uppercase;
}

.about-text h2 {
    font-size: 42px;

    margin: 12px 0 20px;
}

.about-text p {
    color: var(--muted);

    margin-bottom: 18px;
}

.mission {
    padding: 40px;

    border-radius: 18px;

    background:
        linear-gradient(
            145deg,
            rgba(212,160,23,0.12),
            rgba(255,255,255,0.03)
        );

    border: 1px solid rgba(212,160,23,0.2);
}

.mission h3 {
    color: var(--gold-light);

    margin-bottom: 10px;
}

.mission p {
    color: #c6cad3;
}


/* =========================
   CONTACT
========================= */

.contact {
    background: #080b12;
}

.contact-box {
    max-width: 700px;

    margin: auto;

    padding: 35px;

    background: var(--card);

    border: 1px solid var(--border);

    border-radius: 18px;
}

input,
textarea {
    width: 100%;

    background: rgba(255,255,255,0.04);

    border: 1px solid var(--border);

    color: white;

    padding: 14px;

    margin-bottom: 15px;

    border-radius: 8px;

    outline: none;

    font-size: 14px;
}

input:focus,
textarea:focus {
    border-color: var(--gold);
}

textarea {
    min-height: 150px;

    resize: vertical;
}

button {
    width: 100%;

    padding: 14px;

    border: none;

    border-radius: 8px;

    background:
        linear-gradient(
            135deg,
            var(--gold),
            var(--gold-light)
        );

    color: #111;

    font-weight: bold;

    cursor: pointer;

    transition: 0.3s;
}

button:hover {
    transform: translateY(-2px);
}


/* =========================
   FOOTER
========================= */

footer {
    background: #05070b;

    border-top: 1px solid var(--border);

    padding: 50px 0 25px;

    text-align: center;
}

.footer-logo {
    font-size: 22px;

    font-weight: bold;

    margin-bottom: 12px;
}

.footer-logo span {
    color: var(--gold-light);
}

footer p {
    color: var(--muted);

    font-size: 13px;
}

.social {
    margin: 20px 0;
}

.social a {
    display: inline-block;

    margin: 5px 8px;

    color: #ddd;

    font-size: 13px;

    transition: 0.3s;
}

.social a:hover {
    color: var(--gold-light);
}


/* =========================
   MOBILE
========================= */

@media(max-width:800px) {

    .menu-button {
        display: block;
    }

    .menu {
        display: none;

        position: absolute;

        top: 75px;
        left: 0;

        width: 100%;

        flex-direction: column;

        gap: 0;

        background: rgba(8,11,18,0.98);

        border-bottom: 1px solid var(--border);
    }

    .menu.active {
        display: flex;
    }

    .menu li {
        text-align: center;

        padding: 15px;
    }

    .about-grid {
        grid-template-columns: 1fr;
    }

    .hero h1 {
        letter-spacing: -2px;
    }

    section {
        padding: 75px 0;
    }

    .btn {
        width: 90%;
        max-width: 320px;
    }

}


/* =========================
   ANIMATION
========================= */

@keyframes fadeUp {

    from {
        opacity: 0;
        transform: translateY(25px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }

}

.hero-content {
    animation: fadeUp 1s ease;
}

</style>
</head>


<body>


<!-- =========================
     NAVIGATION
========================= -->

<header>

<div class="container">

<nav>

<div class="logo">
Kingdom <span>Learning Hub</span>
<small>By Richard</small>
</div>

<div class="menu-button"
onclick="toggleMenu()">
☰
</div>

<ul class="menu" id="menu">

<li><a href="#home">Home</a></li>

<li><a href="#worship">Worship</a></li>

<li><a href="#learning">Learning</a></li>

<li><a href="#about">About</a></li>

<li><a href="#contact">Contact</a></li>

</ul>

</nav>

</div>

</header>


<!-- =========================
     HERO
========================= -->

<section class="hero" id="home">

<div class="container">

<div class="hero-content">

<div class="badge">
FAITH • KNOWLEDGE • PURPOSE
</div>

<h1>
Kingdom
<span>Learning Hub</span>
</h1>

<h2>
By Richard
</h2>

<p>
A Christian-centered platform where faith,
knowledge and practical skills come together
to help people grow spiritually and intellectually.
</p>

<div class="buttons">

<a href="#worship"
class="btn primary">
📖 Start Bible Study
</a>

<a href="#learning"
class="btn secondary">
🎓 Start Learning
</a>

</div>

<p style="margin-top:30px;">
<strong>
Grow in Faith. Grow in Knowledge. Grow in Life.
</strong>
</p>

</div>

</div>

</section>


<!-- =========================
     WORSHIP
========================= -->

<section class="worship" id="worship">

<div class="container">

<div class="section-title">

<span>WORSHIP</span>

<h2>
Grow Spiritually
</h2>

<p>
Explore God's Word, strengthen your faith
and develop a deeper relationship with God.
</p>

</div>


<div class="cards">


<div class="card">

<div class="icon">📖</div>

<h3>Bible Study</h3>

<p>
Study Scripture and discover biblical
principles that can guide everyday life.
</p>

<a class="card-link" href="#">
Explore Bible Studies →
</a>

</div>


<div class="card">

<div class="icon">🙏</div>

<h3>Prayer</h3>

<p>
Develop a consistent prayer life and
grow in your relationship with God.
</p>

<a class="card-link" href="#">
Prayer Resources →
</a>

</div>


<div class="card">

<div class="icon">🌅</div>

<h3>Daily Devotional</h3>

<p>
Start each day with Scripture,
reflection and spiritual encouragement.
</p>

<a class="card-link" href="#">
Read Devotional →
</a>

</div>


<div class="card">

<div class="icon">✝️</div>

<h3>Christian Living</h3>

<p>
Learn about faith, love, forgiveness,
character and Christian living.
</p>

<a class="card-link" href="#">
Learn More →
</a>

</div>


</div>

</div>

</section>


<!-- =========================
     LEARNING
========================= -->

<section class="learning" id="learning">

<div class="container">

<div class="section-title">

<span>LEARNING CENTER</span>

<h2>
Build Knowledge & Skills
</h2>

<p>
Practical education designed to help
you develop useful skills for life.
</p>

</div>


<div class="cards">


<div class="card">

<div class="icon">📈</div>

<h3>Forex Academy</h3>

<p>
Learn forex terminology, market analysis,
risk management and trading discipline.
</p>

<a class="card-link" href="#">
Enter Forex Academy →
</a>

</div>


<div class="card">

<div class="icon">📚</div>

<h3>Basic Education</h3>

<p>
Improve mathematics, English,
general knowledge and study skills.
</p>

<a class="card-link" href="#">
Start Learning →
</a>

</div>


<div class="card">

<div class="icon">💻</div>

<h3>Digital Skills</h3>

<p>
Learn computers, internet skills,
web development and digital tools.
</p>

<a class="card-link" href="#">
Learn Digital Skills →
</a>

</div>


<div class="card">

<div class="icon">💰</div>

<h3>Financial Education</h3>

<p>
Understand budgeting, saving,
money management and financial planning.
</p>

<a class="card-link" href="#">
Learn Finance →
</a>

</div>


<div class="card">

<div class="icon">🌱</div>

<h3>Personal Growth</h3>

<p>
Develop discipline, confidence,
purpose and useful life skills.
</p>

<a class="card-link" href="#">
Start Growing →
</a>

</div>


<div class="card">

<div class="icon">🚀</div>

<h3>Entrepreneurship</h3>

<p>
Learn business fundamentals,
entrepreneurship and practical opportunities.
</p>

<a class="card-link" href="#">
Explore Business →
</a>

</div>


</div>

</div>

</section>


<!-- =========================
     VERSE
========================= -->

<section class="verse">

<div class="container">

<blockquote>

"The fear of the LORD is the beginning
of wisdom: and the knowledge of the holy
is understanding."

</blockquote>

<cite>
Proverbs 9:10
</cite>

</div>

</section>


<!-- =========================
     STATS
========================= -->

<section>

<div class="container">

<div class="section-title">

<span>OUR PURPOSE</span>

<h2>
Learning That Creates Impact
</h2>

<p>
Kingdom Learning Hub is built around
spiritual growth, knowledge and practical development.
</p>

</div>


<div class="stats">

<div class="stat">
<h3>01</h3>
<p>Faith First</p>
</div>

<div class="stat">
<h3>02</h3>
<p>Learn Continuously</p>
</div>

<div class="stat">
<h3>03</h3>
<p>Develop Skills</p>
</div>

<div class="stat">
<h3>04</h3>
<p>Serve Others</p>
</div>

</div>

</div>

</section>


<!-- =========================
     ABOUT
========================= -->

<section class="about" id="about">

<div class="container">

<div class="about-grid">

<div class="about-text">

<span>ABOUT THE HUB</span>

<h2>
Faith + Knowledge + Purpose
</h2>

<p>
Kingdom Learning Hub is a Christian-centered
learning platform created to help people grow
spiritually, intellectually and practically.
</p>

<p>
We believe education should develop more than
knowledge. It should encourage wisdom,
discipline, character and meaningful action.
</p>

<p>
Our goal is to create a community where people
can study God's Word while also developing
skills that can help them navigate life.
</p>

</div>


<div class="mission">

<h3>
Our Mission
</h3>

<p>
To make faith-based learning and practical
education accessible to people from different
backgrounds.
</p>

<br>

<h3>
Our Vision
</h3>

<p>
To build a generation that pursues God,
knowledge, wisdom, purpose and positive impact.
</p>

</div>

</div>

</div>

</section>


<!-- =========================
     CONTACT
========================= -->

<section class="contact" id="contact">

<div class="container">

<div class="section-title">

<span>GET IN TOUCH</span>

<h2>
Contact Kingdom Learning Hub
</h2>

<p>
Questions, suggestions, ideas or prayer requests?
Send us a message.
</p>

</div>


<div class="contact-box">

<form onsubmit="sendMessage(event)">

<input
type="text"
id="name"
placeholder="Your Name"
required
>

<input
type="email"
id="email"
placeholder="Your Email"
required
>

<textarea
id="message"
placeholder="Your message..."
required
></textarea>

<button type="submit">
Send Message
</button>

</form>

</div>

</div>

</section>


<!-- =========================
     FOOTER
========================= -->

<footer>

<div class="container">

<div class="footer-logo">
Kingdom <span>Learning Hub</span>
</div>

<p>
By Richard
</p>

<div class="social">

<a href="#">Facebook</a>

<a href="#">TikTok</a>

<a href="#">YouTube</a>

</div>

<p>
Grow in Faith. Grow in Knowledge. Grow in Life.
</p>

<p style="margin-top:20px;">
© <span id="year"></span>
Kingdom Learning Hub. All Rights Reserved.
</p>

</div>

</footer>


<script>

/* MOBILE MENU */

function toggleMenu() {

    const menu =
        document.getElementById("menu");

    menu.classList.toggle("active");

}


/* CLOSE MOBILE MENU AFTER CLICK */

document.querySelectorAll(".menu a")
.forEach(function(link) {

    link.addEventListener("click", function() {

        document
        .getElementById("menu")
        .classList.remove("active");

    });

});


/* CONTACT FORM */

function sendMessage(event) {

    event.preventDefault();

    const name =
        document.getElementById("name").value;

    alert(
        "Thank you, " +
        name +
        "! Your message has been received."
    );

}


/* COPYRIGHT YEAR */

document.getElementById("year")
.textContent = new Date().getFullYear();

</script>

</body>
</html>
