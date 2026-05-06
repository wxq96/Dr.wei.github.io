---
layout: single
title: "News"
permalink: /
author_profile: false
---

<style>
:root {
  --main-blue: #2f80a0;
  --dark: #0f172a;
  --glass: rgba(255, 255, 255, 0.76);
  --glass-dark: rgba(15, 23, 42, 0.64);
}

body {
  overflow-x: hidden;
}

body::before {
  content: "";
  position: fixed;
  inset: 0;
  background-image:
    linear-gradient(rgba(15, 23, 42, 0.35), rgba(15, 23, 42, 0.45)),
    url("{{ site.baseurl }}/images/cat_bg.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  transform: scale(1.06);
  z-index: -3;
}

body::after {
  content: "";
  position: fixed;
  inset: 0;
  background:
    radial-gradient(circle at var(--mouse-x, 50%) var(--mouse-y, 50%),
    rgba(47, 128, 160, 0.24), transparent 28%);
  pointer-events: none;
  z-index: -2;
}

.page {
  background: transparent !important;
}

.page__content {
  max-width: 1120px;
  margin: 0 auto;
}

.news-wrapper {
  min-height: 92vh;
  padding: 42px 24px 80px 24px;
  color: #ffffff;
}

.news-hero {
  position: relative;
  overflow: hidden;
  padding: 46px 42px;
  border-radius: 32px;
  background: var(--glass-dark);
  border: 1px solid rgba(255, 255, 255, 0.20);
  box-shadow: 0 24px 70px rgba(0, 0, 0, 0.34);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  margin-bottom: 34px;
}

.news-hero::before {
  content: "";
  position: absolute;
  top: -120px;
  right: -100px;
  width: 280px;
  height: 280px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(147, 197, 253, 0.36), transparent 64%);
  pointer-events: none;
}

.news-kicker {
  color: #93c5fd;
  font-weight: 800;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  font-size: 14px;
  margin-bottom: 12px;
}

.news-hero h1 {
  margin: 0 0 14px 0;
  color: #ffffff;
  font-size: 46px;
  line-height: 1.1;
}

.news-hero p {
  color: #e5e7eb;
  font-size: 18px;
  line-height: 1.8;
  max-width: 780px;
}

.news-buttons {
  margin-top: 24px;
}

.news-buttons a {
  display: inline-block;
  padding: 11px 18px;
  margin: 6px 10px 6px 0;
  border-radius: 999px;
  text-decoration: none;
  font-size: 14px;
  font-weight: 800;
  background: #ffffff;
  color: #0f172a;
  transition: transform 0.24s ease, box-shadow 0.24s ease, background 0.24s ease;
}

.news-buttons a:hover {
  transform: translateY(-3px);
  box-shadow: 0 14px 28px rgba(0, 0, 0, 0.22);
  background: #e0f2fe;
}

.news-buttons a.secondary {
  background: rgba(255, 255, 255, 0.12);
  color: #ffffff;
  border: 1px solid rgba(255, 255, 255, 0.24);
}

.news-section-title {
  color: #ffffff;
  font-size: 26px;
  margin: 36px 0 20px 0;
  text-shadow: 0 2px 14px rgba(0, 0, 0, 0.45);
}

.news-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 22px;
}

.news-card {
  position: relative;
  overflow: hidden;
  min-height: 230px;
  padding: 24px 24px 62px 24px;
  border-radius: 26px;
  background: var(--glass);
  color: #0f172a;
  border: 1px solid rgba(255, 255, 255, 0.42);
  box-shadow: 0 16px 42px rgba(0, 0, 0, 0.24);
  backdrop-filter: blur(13px);
  -webkit-backdrop-filter: blur(13px);
  cursor: grab;
  transition:
    transform 0.28s ease,
    box-shadow 0.28s ease,
    border-color 0.28s ease,
    background 0.28s ease;
}

.news-card:active {
  cursor: grabbing;
}

.news-card::before {
  content: "";
  position: absolute;
  inset: 0;
  background:
    radial-gradient(circle at top right, rgba(47, 128, 160, 0.20), transparent 36%),
    linear-gradient(135deg, rgba(255,255,255,0.96), rgba(238,247,251,0.80));
  opacity: 0;
  transition: opacity 0.28s ease;
  z-index: 0;
}

.news-card:hover {
  transform: translateY(-10px) scale(1.015);
  box-shadow: 0 28px 60px rgba(0, 0, 0, 0.34);
  border-color: rgba(147, 197, 253, 0.78);
}

.news-card:hover::before {
  opacity: 1;
}

.news-card-content {
  position: relative;
  z-index: 2;
}

.news-date {
  display: inline-block;
  padding: 6px 12px;
  border-radius: 999px;
  background: rgba(47, 128, 160, 0.12);
  color: #2f80a0;
  font-weight: 800;
  font-size: 13px;
  margin-bottom: 14px;
}

.news-card h3 {
  margin: 0 0 10px 0;
  color: #0f172a;
  font-size: 21px;
  line-height: 1.35;
}

.news-card p {
  margin: 0;
  color: #475569;
  line-height: 1.72;
}

.news-card-more {
  max-height: 0;
  opacity: 0;
  overflow: hidden;
  transform: translateY(10px);
  margin-top: 0;
  color: #475569;
  line-height: 1.68;
  transition:
    max-height 0.34s ease,
    opacity 0.34s ease,
    transform 0.34s ease,
    margin-top 0.34s ease;
}

.news-card:hover .news-card-more {
  max-height: 120px;
  opacity: 1;
  transform: translateY(0);
  margin-top: 12px;
}

.news-tags {
  position: absolute;
  left: 24px;
  right: 24px;
  bottom: 22px;
  display: flex;
  flex-wrap: wrap;
  gap: 7px;
  z-index: 2;
}

.news-tag {
  padding: 5px 10px;
  border-radius: 999px;
  background: rgba(15, 23, 42, 0.08);
  color: #334155;
  font-size: 12px;
  font-weight: 800;
}

.card-shine {
  position: absolute;
  top: -90px;
  left: -90px;
  width: 120px;
  height: 300px;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255,255,255,0.82),
    transparent
  );
  transform: rotate(28deg) translateX(-210px);
  opacity: 0;
  transition: transform 0.7s ease, opacity 0.7s ease;
  z-index: 3;
  pointer-events: none;
}

.news-card:hover .card-shine {
  opacity: 1;
  transform: rotate(28deg) translateX(520px);
}

.news-footer {
  margin-top: 34px;
  padding: 24px;
  border-radius: 24px;
  background: rgba(15, 23, 42, 0.62);
  color: #e5e7eb;
  border: 1px solid rgba(255, 255, 255, 0.18);
  backdrop-filter: blur(14px);
  -webkit-backdrop-filter: blur(14px);
  line-height: 1.75;
}

.cursor-dot {
  position: fixed;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  background: rgba(147, 197, 253, 0.52);
  pointer-events: none;
  z-index: 9999;
  transform: translate(-50%, -50%);
  mix-blend-mode: screen;
  box-shadow: 0 0 24px rgba(147, 197, 253, 0.8);
}

.click-ripple {
  position: fixed;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  pointer-events: none;
  z-index: 9998;
  border: 2px solid rgba(147, 197, 253, 0.9);
  animation: ripple 0.75s ease-out forwards;
}

@keyframes ripple {
  from {
    opacity: 1;
    transform: translate(-50%, -50%) scale(0.6);
  }
  to {
    opacity: 0;
    transform: translate(-50%, -50%) scale(7);
  }
}

.dragging {
  opacity: 0.92;
  transform: scale(1.03) rotate(1deg) !important;
  z-index: 999;
}

@media (max-width: 768px) {
  .news-wrapper {
    padding: 24px 12px 64px 12px;
  }

  .news-hero {
    padding: 32px 24px;
  }

  .news-hero h1 {
    font-size: 34px;
  }

  .news-grid {
    grid-template-columns: 1fr;
  }

  .cursor-dot {
    display: none;
  }
}
</style>

<div class="cursor-dot" id="cursorDot"></div>

<div class="news-wrapper">

  <section class="news-hero">
    <div class="news-kicker">Latest Updates · Research Notes · Personal News</div>

    <h1>News from Wei Xiangqing</h1>

    <p>
      Welcome to my personal update page. Here I share my latest research progress,
      academic activities, website updates, and selected notes on AI accelerators,
      hardware-aware scheduling, reinforcement learning, FPGA/NPU systems, and digital IC design.
    </p>

    <div class="news-buttons">
      <a href="{{ site.baseurl }}/publications/">Publications</a>
      <a class="secondary" href="https://github.com/wxq96">GitHub</a>
      <a class="secondary" href="https://scholar.google.com/citations?user=PS_CX0AAAAAJ">Google Scholar</a>
    </div>
  </section>

  <h2 class="news-section-title">Latest News</h2>

  <div class="news-grid">

    <article class="news-card draggable-card">
      <div class="card-shine"></div>
      <div class="news-card-content">
        <span class="news-date">May 2026</span>
        <h3>Personal Website Updated</h3>
        <p>
          I redesigned this website into a more interactive academic homepage with a news-style layout.
        </p>
        <div class="news-card-more">
          The new version includes a cat-photo background, glass-style cards, hover animations,
          click ripples, and draggable news cards.
        </div>
      </div>
      <div class="news-tags">
        <span class="news-tag">Website</span>
        <span class="news-tag">UI</span>
        <span class="news-tag">Academic Page</span>
      </div>
    </article>

    <article class="news-card draggable-card">
      <div class="card-shine"></div>
      <div class="news-card-content">
        <span class="news-date">2026</span>
        <h3>Research Direction Refinement</h3>
        <p>
          I am refining my research direction around AI accelerator architecture,
          hardware-aware scheduling, and RL-based optimization.
        </p>
        <div class="news-card-more">
          My current interest is to connect neural network workload features,
          accelerator resource constraints, and performance feedback.
        </div>
      </div>
      <div class="news-tags">
        <span class="news-tag">AI Accelerator</span>
        <span class="news-tag">Scheduling</span>
        <span class="news-tag">RL</span>
      </div>
    </article>

    <article class="news-card draggable-card">
      <div class="card-shine"></div>
      <div class="news-card-content">
        <span class="news-date">2025</span>
        <h3>RL-based CNN Accelerator Scheduling</h3>
        <p>
          I worked on reinforcement-learning-based scheduling and allocation for CNN accelerator systems.
        </p>
        <div class="news-card-more">
          This work explores how learning-based methods can assist accelerator resource allocation
          and improve hardware utilization.
        </div>
      </div>
      <div class="news-tags">
        <span class="news-tag">CNN</span>
        <span class="news-tag">MAC</span>
        <span class="news-tag">NPU</span>
      </div>
    </article>

    <article class="news-card draggable-card">
      <div class="card-shine"></div>
      <div class="news-card-content">
        <span class="news-date">Ongoing</span>
        <h3>Hardware-aware Research Notes</h3>
        <p>
          I am gradually organizing notes on FPGA/NPU acceleration, digital IC design,
          and computer architecture.
        </p>
        <div class="news-card-more">
          These notes will support future research projects and help document my learning path
          from RTL-level design to system-level accelerator optimization.
        </div>
      </div>
      <div class="news-tags">
        <span class="news-tag">FPGA</span>
        <span class="news-tag">RTL</span>
        <span class="news-tag">Architecture</span>
      </div>
    </article>

  </div>

  <div class="news-footer">
    <strong>Note:</strong>
    This page is designed as a lightweight interactive news board. You can hover over each card
    to reveal more information, click anywhere to create ripple effects, and drag the news cards
    around slightly for interaction.
  </div>

</div>

<script>
(function () {
  const root = document.documentElement;
  const cursorDot = document.getElementById("cursorDot");

  document.addEventListener("mousemove", function (e) {
    const x = (e.clientX / window.innerWidth) * 100;
    const y = (e.clientY / window.innerHeight) * 100;

    root.style.setProperty("--mouse-x", x + "%");
    root.style.setProperty("--mouse-y", y + "%");

    if (cursorDot) {
      cursorDot.style.left = e.clientX + "px";
      cursorDot.style.top = e.clientY + "px";
    }

    const moveX = (e.clientX / window.innerWidth - 0.5) * 18;
    const moveY = (e.clientY / window.innerHeight - 0.5) * 18;
    document.body.style.backgroundPosition = `${50 + moveX}% ${50 + moveY}%`;
  });

  document.addEventListener("click", function (e) {
    const ripple = document.createElement("div");
    ripple.className = "click-ripple";
    ripple.style.left = e.clientX + "px";
    ripple.style.top = e.clientY + "px";
    document.body.appendChild(ripple);

    setTimeout(function () {
      ripple.remove();
    }, 760);
  });

  const cards = document.querySelectorAll(".draggable-card");

  cards.forEach(function (card) {
    let isDragging = false;
    let startX = 0;
    let startY = 0;
    let offsetX = 0;
    let offsetY = 0;

    card.addEventListener("mousedown", function (e) {
      isDragging = true;
      startX = e.clientX - offsetX;
      startY = e.clientY - offsetY;
      card.classList.add("dragging");
      card.style.transition = "none";
    });

    document.addEventListener("mousemove", function (e) {
      if (!isDragging) return;

      offsetX = e.clientX - startX;
      offsetY = e.clientY - startY;

      const limitedX = Math.max(Math.min(offsetX, 80), -80);
      const limitedY = Math.max(Math.min(offsetY, 60), -60);

      card.style.transform = `translate(${limitedX}px, ${limitedY}px) scale(1.03)`;
    });

    document.addEventListener("mouseup", function () {
      if (!isDragging) return;

      isDragging = false;
      card.classList.remove("dragging");
      card.style.transition = "transform 0.35s ease, box-shadow 0.28s ease";
      card.style.transform = "";

      offsetX = 0;
      offsetY = 0;
    });
  });
})();
</script>
