<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Kingdom Learning Hub | By Richard</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

:root {
    --gold: #d4a017;
    --gold-light: #f3c85b;
    --dark: #070a10;
    --dark2: #101521;
    --card: rgba(255,255,255,0.06);
    --border: rgba(255,255,255,0.12);
    --text: #f4f5f7;
    --muted: #9da5b5;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background: var(--dark);
    color: var(--text);
    line-height: 1.6;
}

.container {
    width: 90%;
    max-width: 1150px;
    margin: auto;
}

/* NAVIGATION */

header {
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 1000;

    background: rgba(7,10,16,0.88);
    backdrop-filter: blur(18px);

    border-bottom: 1px solid var(--border);
}

nav {
    height: 75px;

    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-size: 19px;
    font-weight: bold;
}

.logo span {
    color: var(--gold-light);
}

.logo small {
    display: block;
    color: #777;
    font-size: 9px;
    letter-spacing: 2px;
}

.menu {
    display: flex;
    gap: 28px;
    list-style: none;
}

.menu a {
    color: #ddd;
    text-decoration: none;
    font-size: 14px;
    transition: .3s;
}

.menu a:hover {
    color: var(--gold-light);
}

.menu-button {
    display: none;
    font-size: 28px;
    cursor: pointer;
}

/* HERO */

.hero {
    min-height: 100vh;

    display: flex;
    align-items: center;
    text-align: center;

    background:
        radial-gradient(
            circle at center,
            rgba(212,160,23,0.15),
            transparent 50%
        ),
        linear-gradient(135deg,#070a10,#121927);
}

.hero-content {
    max-width: 850px;
    margin: auto;
    padding-top: 70px;
}

.badge {
    display: inline-block;

    padding: 8px 16px;

    border: 1px solid rgba(212,160,23,.35);
    border-radius: 50px;

    color: var(--gold-light);

    font-size: 11px;
    letter-spacing: 2px;

    margin-bottom: 25px;
}

.hero h1 {
    font-size: clamp(42px,7vw,76px);
    line-height: 1.05;
    letter-spacing: -3px;
    margin-bottom: 18px;
}

.hero h1 span {
    color: var(--gold-light);
}

.hero h2 {
    font-size: 20px;
    font-weight: normal;
    color: #ccc;
    margin-bottom: 20px;
}

.hero p {
    max-width: 680px;
    margin: auto;
    color: var(--muted);
    font-size: 17px;
}

.hero strong {
    color: var(--gold-light);
}

/* BUTTONS */

.buttons {
    margin-top: 35px;

    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
}

.btn {
    min-width: 200px;

    padding: 15px 25px;

    border-radius: 9px;

    font-size: 14px;
    font-weight: bold;

    text-decoration: none;

    display: inline-flex;
    justify-content: center;
    align-items: center;

    transition: .3s;
}

.primary {
    background: linear-gradient(
        135deg,
        var(--gold),
        var(--gold-light)
    );

    color: #111;

    box-shadow:
        0 10px 30px rgba(212,160,23,.18);
}

.primary:hover {
    transform: translateY(-4px);
    box-shadow:
        0 15px 35px rgba(212,160,23,.3);
}

.secondary {
    background: rgba(255,255,255,.04);

    color: white;

    border: 1px solid var(--border);
}

.secondary:hover {
    transform: translateY(-4px);

    border-color: var(--gold);

    color: var(--gold-light);
}

/* INTRO */

.intro {
    padding: 100px 0;
    background: #0b0f17;
    text-align: center;
}

.intro h2 {
    font-size: 38px;
    margin-bottom: 15px;
}

.intro p {
    max-width: 700px;
    margin: auto;
    color: var(--muted);
}

/* TWO MAIN WORLDS */

.worlds {
    padding: 100px 0;
}

.section-title {
    text-align: center;
    margin-bottom: 50px;
}

.section-title span {
    color: var(--gold-light);
    font-size: 11px;
    letter-spacing: 2px;
    font-weight: bold;
}

.section-title h2 {
    font-size: 40px;
    margin: 10px 0;
}

.section-title p {
    color: var(--muted);
}

/* WORLD CARDS */

.world-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 25px;
}

.world {
    padding: 45px 35px;

    border-radius: 20px;

    border: 1px solid var(--border);

    background:
        linear-gradient(
            145deg,
            rgba(255,255,255,.07),
            rgba(255,255,255,.025)
        );

    transition: .35s;
}

.world:hover {
    transform: translateY(-8px);

    border-color: rgba(212,160,23,.45);

    box-shadow:
        0 25px 60px rgba(0,0,0,.25);
}

.world-icon {
    font-size: 48px;
    margin-bottom: 20px;
}

.world h3 {
    font-size: 28px;
    margin-bottom: 12px;
}

.world p {
    color: var(--muted);
    margin-bottom: 25px;
}

.world-link {
    display: inline-block;

    padding: 12px 20px;

    border-radius: 8px;

    background: var(--gold);

    color: #111;

    font-size: 13px;
    font-weight: bold;
}

/* VERSE */

.verse {
    padding: 100px 20px;

    text-align: center;

    background:
        radial-gradient(
            circle at center,
            rgba(212,160,23,.12),
            transparent 55%
        );

    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
}

.verse blockquote {
    max-width: 800px;
    margin: auto;

    font-size: clamp(21px,4vw,30px);

    font-style: italic;
}

.verse cite {
    display: block;

    margin-top: 20px;

    color: var(--gold-light);

    font-weight: bold;
}

/* ABOUT */

.about {
    padding: 100px 0;
    background: #0b0f17;
}

.about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: center;
}

.about h2 {
    font-size: 40px;
    margin-bottom: 20px;
}

.about p {
    color: var(--muted);
    margin-bottom: 18px;
}

.mission {
    padding: 35px;

    border-radius: 18px;

    background: rgba(212,160,23,.08);

    border: 1px solid rgba(212,160,23,.2);
}

.mission h3 {
    color: var(--gold-light);
    margin-bottom: 10px;
}

/* FOOTER */

footer {
    padding: 45px 20px;

    text-align: center;

    background: #05070b;

    border-top: 1px solid var(--border);
}

footer strong {
    color: var(--gold-light);
}

footer p {
    color: var(--muted);
    font-size: 13px;
    margin: 7px;
}

/* MOBILE */

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

        background: #080b12;

        flex-direction: column;

        gap: 0;

        border-bottom: 1px solid var(--border);
    }

    .menu.active {
        display: flex;
    }

    .menu li {
        text-align: center;
        padding: 15px;
    }

    .world-grid,
    .about-grid {
        grid-template-columns: 1fr;
    }

    .hero h1 {
        letter-spacing: -2px;
    }

    .btn {
        width: 90%;
        max-width: 320px;
    }

}

</style>
</head>

<body>

<!-- NAVIGATION -->

<header>

<div class="container">

<nav>

<div class="logo">
Kingdom <span>Learning Hub</span>
<small>BY RICHARD</small>
</div>

<div class="menu-button"
onclick="toggleMenu()">
☰
</div>

<ul class="menu" id="menu">

<li><a href="#home">Home</a></li>

<li><a href="worship.html">Worship</a></li>

<li><a href="learning.html">Learning</a></li>

<li><a href="#about">About</a></li>

</ul>

</nav>

</div>

</header>


<!-- HERO -->

<section class="hero" id="home">

<div class="container">

<div class="hero-content">

<div class="badge">
FAITH • KNOWLEDGE • PURPOSE
</div>

<h1>
Kingdom <span>Learning Hub</span>
</h1>

<h2>
By Richard
</h2>

<p>
A Christian-centered platform where
spiritual growth, education and practical
skills come together.
</p>

<div class="buttons">

<a href="worship.html"
class="btn primary">
📖 Start Bible Study
</a>

<a href="learning.html"
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


<!-- INTRO -->

<section class="intro">

<div class="container">

<h2>
One Platform. Two Paths.
</h2>

<p>
Whether you are seeking to understand God's Word
or develop practical knowledge and skills,
Kingdom Learning Hub gives you a place to learn,
grow and move forward.
</p>

</div>

</section>


<!-- WORSHIP & LEARNING -->

<section class="worlds">

<div class="container">

<div class="section-title">

<span>CHOOSE YOUR PATH</span>

<h2>
Where Would You Like To Begin?
</h2>

<p>
Choose a path below and explore the resources available.
</p>

</div>


<div class="world-grid">


<!-- WORSHIP -->

<div class="world">

<div class="world-icon">
🙏
</div>

<h3>
Worship & Bible Study
</h3>

<p>
Explore Scripture, prayer, devotionals,
Christian living and biblical teachings
designed to encourage spiritual growth.
</p>

<a href="worship.html"
class="world-link">
Enter Worship →
</a>

</div>


<!-- LEARNING -->

<div class="world">

<div class="world-icon">
🎓
</div>

<h3>
Learning Center
</h3>

<p>
Develop practical knowledge through
Forex education, basic education,
digital skills, finance and entrepreneurship.
</p>

<a href="learning.html"
class="world-link">
Enter Learning Center →
</a>

</div>


</div>

</div>

</section>


<!-- VERSE -->

<section class="verse">

<blockquote>
"The fear of the LORD is the beginning
of wisdom: and the knowledge of the holy
is understanding."
</blockquote>

<cite>
Proverbs 9:10
</cite>

</section>


<!-- ABOUT -->

<section class="about" id="about">

<div class="container">

<div class="about-grid">

<div>

<h2>
Faith. Knowledge. Purpose.
</h2>

<p>
Kingdom Learning Hub is a Christian-centered
learning platform created by Richard to bring
spiritual learning and practical education together.
</p>

<p>
Our goal is to help people discover God's Word,
develop useful skills, gain knowledge and become
people who can make a positive impact in their
communities.
</p>

</div>


<div class="mission">

<h3>
Our Mission
</h3>

<p>
To make faith-based learning and practical
education accessible to everyone.
</p>

<h3 style="margin-top:25px;">
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


<!-- FOOTER -->

<footer>

<p>
<strong>Kingdom Learning Hub</strong>
</p>

<p>
By Richard
</p>

<p>
Grow in Faith. Grow in Knowledge. Grow in Life.
</p>

<p>
© <span id="year"></span>
Kingdom Learning Hub
</p>

</footer>


<script>

function toggleMenu() {

    document
    .getElementById("menu")
    .classList.toggle("active");

}

document
.querySelectorAll(".menu a")
.forEach(function(link) {

    link.addEventListener("click", function() {

        document
        .getElementById("menu")
        .classList.remove("active");

    });

});

document
.getElementById("year")
.textContent = new Date().getFullYear();

</script>

</body>
</html>
