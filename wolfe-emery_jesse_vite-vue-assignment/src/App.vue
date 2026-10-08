<script setup>
const ideas = ['Collect a spark', 'Shape a small plan', 'Make it real']
</script>

<template>
  <main class="page-shell">
    <nav class="topbar" aria-label="Main navigation">
      <a class="brand" href="#" aria-label="Daybreak home">
        <span class="brand-mark" aria-hidden="true">✳</span>
        <span>daybreak</span>
      </a>
      <span class="edition">A little space to begin</span>
    </nav>

    <section class="hero" aria-labelledby="hero-title">
      <div class="hero-copy">
        <p class="eyebrow"><span></span> YOUR NEXT GOOD THING STARTS HERE</p>
        <h1 id="hero-title">Make room<br />for <em>bold ideas.</em></h1>
        <p class="intro">
          A bright little corner for the projects, plans, and possibilities you can’t stop thinking
          about.
        </p>
        <a class="start-button" href="#first-steps">
          Find your starting point
          <span aria-hidden="true">↗</span>
        </a>
        <p class="byline">Made with curiosity by <strong>Jesse</strong></p>
      </div>

      <aside class="idea-card" aria-label="A reminder to start small">
        <div class="card-topline">
          <span class="sun-icon" aria-hidden="true">☼</span>
          <span>NOTE TO SELF</span>
          <span class="card-menu" aria-hidden="true">···</span>
        </div>
        <p class="card-quote">
          “You don’t have to see the whole staircase, just take the first step.”
        </p>
        <div class="card-footer">
          <span class="avatar" aria-hidden="true">J</span>
          <span>One step at a time</span>
          <span class="heart" aria-hidden="true">♡</span>
        </div>
        <span class="sparkle sparkle-one" aria-hidden="true">✳</span>
        <span class="sparkle sparkle-two" aria-hidden="true">✦</span>
      </aside>

      <span class="orbit orbit-one" aria-hidden="true"></span>
      <span class="orbit orbit-two" aria-hidden="true"></span>
    </section>

    <section id="first-steps" class="bottom-panel" aria-labelledby="steps-title">
      <div>
        <p class="eyebrow">THE CREATIVE PROCESS</p>
        <h2 id="steps-title">Start small. Stay curious.</h2>
      </div>
      <ol class="steps">
        <li v-for="(idea, index) in ideas" :key="idea">
          <span>0{{ index + 1 }}</span>
          {{ idea }}
        </li>
      </ol>
    </section>

    <footer class="footer">
      <span
        >Built with <strong>Vue</strong> and <strong>Vite</strong> — fast tools for bringing ideas
        to life.</span
      >
      <span class="footer-note">A fresh start, every day <span aria-hidden="true">✳</span></span>
    </footer>
  </main>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,600;0,700;1,600;1,700&display=swap');

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-width: 320px;
  background: #f6f4ed;
  color: #202c26;
  font-family: 'DM Sans', sans-serif;
}

a {
  color: inherit;
}

.page-shell {
  width: min(1160px, calc(100% - 80px));
  margin: 0 auto;
}

.topbar {
  height: 94px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 1px solid #dfdfd6;
}

.brand {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  text-decoration: none;
  font-size: 21px;
  font-weight: 700;
  letter-spacing: -1px;
}

.brand-mark {
  display: grid;
  width: 31px;
  height: 31px;
  place-items: center;
  border-radius: 50%;
  background: #e6a84d;
  color: #20382e;
  font-size: 21px;
}

.edition {
  color: #777b70;
  font-size: 13px;
}

.hero {
  min-height: 515px;
  display: grid;
  grid-template-columns: 1fr 0.9fr;
  align-items: center;
  position: relative;
  overflow: hidden;
}

.hero-copy {
  position: relative;
  z-index: 1;
  padding: 65px 0 55px;
}

.eyebrow {
  margin: 0 0 22px;
  color: #728071;
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 1.8px;
}

.hero-copy .eyebrow {
  display: flex;
  align-items: center;
  gap: 9px;
}

.hero-copy .eyebrow span {
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: #d5903d;
}

h1,
h2,
p {
  margin-top: 0;
}

h1 {
  margin-bottom: 20px;
  font-family: 'Playfair Display', Georgia, serif;
  font-size: clamp(54px, 6.6vw, 79px);
  font-weight: 600;
  letter-spacing: -3.8px;
  line-height: 1.03;
}

h1 em {
  color: #66836d;
  font-weight: 600;
}

.intro {
  max-width: 400px;
  margin-bottom: 27px;
  color: #6f746b;
  font-size: 15px;
  line-height: 1.8;
}

.start-button {
  display: inline-flex;
  align-items: center;
  gap: 28px;
  padding: 15px 19px;
  border-radius: 6px;
  background: #253a30;
  color: #fffdf7;
  font-size: 12px;
  font-weight: 600;
  text-decoration: none;
  transition:
    background 160ms ease,
    transform 160ms ease;
}

.start-button:hover {
  transform: translateY(-2px);
  background: #3b5a49;
}

.start-button span {
  color: #edbc70;
  font-size: 17px;
}

.byline {
  margin: 17px 0 0;
  color: #85877f;
  font-size: 11px;
}

.byline strong {
  color: #445448;
}

.idea-card {
  width: min(100%, 340px);
  min-height: 265px;
  justify-self: center;
  position: relative;
  z-index: 1;
  padding: 24px 26px 19px;
  transform: rotate(3deg);
  border: 1px solid #e4dfd2;
  border-radius: 9px;
  background: #fffdf8;
  box-shadow: 0 24px 55px #24382c1c;
}

.card-topline,
.card-footer {
  display: flex;
  align-items: center;
}

.card-topline {
  gap: 9px;
  color: #84877c;
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 1.6px;
}

.sun-icon {
  color: #d69443;
  font-size: 21px;
}

.card-menu {
  margin-left: auto;
  font-size: 19px;
  letter-spacing: 2px;
}

.card-quote {
  margin: 26px 0 25px;
  color: #2e4035;
  font-family: 'Playfair Display', Georgia, serif;
  font-size: 23px;
  font-weight: 600;
  line-height: 1.45;
}

.card-footer {
  gap: 9px;
  padding-top: 14px;
  border-top: 1px solid #eeeae1;
  color: #7b7f75;
  font-size: 10px;
}

.avatar {
  display: grid;
  width: 24px;
  height: 24px;
  place-items: center;
  border-radius: 50%;
  background: #dce6d7;
  color: #45604b;
  font-weight: 700;
}

.heart {
  margin-left: auto;
  color: #d18c69;
  font-size: 19px;
}

.sparkle {
  position: absolute;
  color: #db9d4d;
}

.sparkle-one {
  top: -24px;
  right: 40px;
  font-size: 30px;
}

.sparkle-two {
  right: -32px;
  bottom: 34px;
  color: #879c7d;
  font-size: 24px;
}

.orbit {
  position: absolute;
  width: 430px;
  height: 430px;
  right: -118px;
  top: 50%;
  border: 1px solid #e7e5db;
  border-radius: 50%;
  transform: translateY(-50%);
}

.orbit-two {
  width: 360px;
  height: 360px;
  right: -83px;
  border-color: #ece9df;
}

.bottom-panel {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 30px;
  padding: 27px 31px;
  border-radius: 8px;
  background: #e9ece3;
}

.bottom-panel .eyebrow {
  margin-bottom: 7px;
  font-size: 9px;
}

h2 {
  margin-bottom: 0;
  color: #2e4035;
  font-family: 'Playfair Display', Georgia, serif;
  font-size: 23px;
  letter-spacing: -0.5px;
}

.steps {
  display: flex;
  gap: 26px;
  margin: 0;
  padding: 0;
  list-style: none;
}

.steps li {
  display: flex;
  align-items: center;
  gap: 9px;
  color: #4d5e50;
  font-size: 11px;
  white-space: nowrap;
}

.steps li span {
  color: #9b7650;
  font-size: 9px;
  font-weight: 700;
}

.footer {
  display: flex;
  justify-content: space-between;
  gap: 20px;
  padding: 22px 0 28px;
  color: #83867c;
  font-size: 10px;
}

.footer strong {
  color: #4c6251;
}

.footer-note span {
  padding-left: 5px;
  color: #d69443;
}

@media (max-width: 760px) {
  .page-shell {
    width: min(100% - 40px, 540px);
  }

  .topbar {
    height: 76px;
  }

  .hero {
    grid-template-columns: 1fr;
    gap: 25px;
    padding-bottom: 42px;
  }

  .hero-copy {
    padding: 55px 0 0;
  }

  .idea-card {
    margin: 0 0 18px;
    justify-self: center;
  }

  .orbit {
    top: 68%;
    right: -275px;
  }

  .orbit-two {
    right: -240px;
  }

  .bottom-panel {
    align-items: flex-start;
    flex-direction: column;
    padding: 24px;
  }

  .steps {
    flex-wrap: wrap;
    gap: 13px 20px;
  }

  .footer {
    flex-direction: column;
    gap: 8px;
    line-height: 1.7;
  }
}

@media (max-width: 420px) {
  .page-shell {
    width: calc(100% - 32px);
  }

  .edition {
    font-size: 11px;
  }

  h1 {
    font-size: 54px;
  }

  .idea-card {
    width: calc(100% - 20px);
  }
}
</style>
