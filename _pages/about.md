---
layout: archive
title: "Profile"
permalink: /
author_profile: true
---

<section class="research-section circuit-bg" id="research">
  <h2 class="section-title">Research Interests</h2>

  <div class="research-grid">

    <div class="research-card">
      <div class="research-icon">⚙️</div>
      <h3>AI Hardware Architecture</h3>
      <p>
        I am interested in hardware architectures for deep learning acceleration,
        especially computation units, memory access, and system-level efficiency.
      </p>
      <div class="research-tags">
        <span>NPU</span>
        <span>FPGA</span>
        <span>Accelerator</span>
      </div>
    </div>

    <div class="research-card">
      <div class="research-icon">🧩</div>
      <h3>Accelerator Scheduling</h3>
      <p>
        I am studying scheduling and resource-allocation problems in accelerator
        systems, including task mapping and execution-order optimization.
      </p>
      <div class="research-tags">
        <span>Scheduling</span>
        <span>Mapping</span>
        <span>PE Array</span>
      </div>
    </div>

    <div class="research-card">
      <div class="research-icon">🤖</div>
      <h3>RL-based Optimization</h3>
      <p>
        I am exploring reinforcement learning as a potential method for automatic
        optimization in hardware-aware scheduling and design-space exploration.
      </p>
      <div class="research-tags">
        <span>RL</span>
        <span>DSE</span>
        <span>Optimization</span>
      </div>
    </div>

    <div class="research-card">
      <div class="research-icon">🔬</div>
      <h3>Digital Circuit Design</h3>
      <p>
        My previous work includes digital circuit design and processor-related
        modules, such as arithmetic units, Booth multiplication, and SRT division.
      </p>
      <div class="research-tags">
        <span>RTL</span>
        <span>RISC-V</span>
        <span>Arithmetic</span>
      </div>
    </div>

  </div>
</section>

<style>
/* =========================
   Research Section Base
========================= */

.research-section {
  position: relative;
  max-width: 980px;
  margin: 0 auto;
  padding: 18px 18px 42px;
  overflow: hidden;
}

.section-title {
  position: relative;
  z-index: 2;
  margin: 0 0 20px;
  padding-bottom: 12px;
  font-size: 26px;
  font-weight: 800;
  color: #2f3a40;
  border-bottom: 1px solid rgba(90, 130, 150, 0.22);
}

/* =========================
   Circuit Background
========================= */

.circuit-bg::before {
  content: "";
  position: absolute;
  inset: -80px;
  z-index: 0;
  pointer-events: none;

  background:
    linear-gradient(90deg, rgba(70, 160, 190, 0.08) 1px, transparent 1px),
    linear-gradient(0deg, rgba(70, 160, 190, 0.08) 1px, transparent 1px),
    radial-gradient(circle at 18% 20%, rgba(90, 210, 235, 0.18), transparent 30%),
    radial-gradient(circle at 82% 62%, rgba(120, 130, 255, 0.13), transparent 32%),
    radial-gradient(circle at 52% 92%, rgba(80, 220, 180, 0.10), transparent 26%);

  background-size:
    34px 34px,
    34px 34px,
    100% 100%,
    100% 100%,
    100% 100%;

  opacity: 0.9;
}

.circuit-bg::after {
  content: "";
  position: absolute;
  inset: 0;
  z-index: 0;
  pointer-events: none;

  background:
    linear-gradient(90deg, transparent 0 18%, rgba(70, 185, 215, 0.20) 18% 19%, transparent 19% 100%),
    linear-gradient(0deg, transparent 0 28%, rgba(70, 185, 215, 0.16) 28% 29%, transparent 29% 100%),
    linear-gradient(90deg, transparent 0 63%, rgba(140, 170, 255, 0.13) 63% 64%, transparent 64% 100%),
    linear-gradient(0deg, transparent 0 72%, rgba(100, 220, 190, 0.12) 72% 73%, transparent 73% 100%);

  background-size:
    220px 180px,
    220px 180px,
    260px 220px,
    260px 220px;

  mask-image: radial-gradient(circle at center, black 38%, transparent 82%);
  -webkit-mask-image: radial-gradient(circle at center, black 38%, transparent 82%);
  opacity: 0.72;
}

/* =========================
   Research Grid / Cards
========================= */

.research-grid {
  position: relative;
  z-index: 2;

  display: grid;
  grid-template-columns: repeat(2, minmax(280px, 1fr));
  gap: 22px;
}

.research-card {
  position: relative;
  min-height: 255px;
  padding: 24px 22px 20px;
  border-radius: 22px;

  display: flex;
  flex-direction: column;

  background:
    linear-gradient(145deg, rgba(255, 255, 255, 0.88), rgba(248, 253, 255, 0.72));
  border: 1px solid rgba(110, 170, 200, 0.25);
  box-shadow:
    0 16px 36px rgba(35, 70, 100, 0.08),
    inset 0 1px 0 rgba(255, 255, 255, 0.7);

  backdrop-filter: blur(14px);
  -webkit-backdrop-filter: blur(14px);

  overflow: hidden;
  transition:
    transform 0.25s ease,
    box-shadow 0.25s ease,
    border-color 0.25s ease;
}

.research-card::before {
  content: "";
  position: absolute;
  inset: 0;
  pointer-events: none;

  background:
    radial-gradient(circle at 20% 20%, rgba(90, 210, 240, 0.12), transparent 28%),
    linear-gradient(120deg, transparent 0%, rgba(255, 255, 255, 0.35) 45%, transparent 70%);

  opacity: 0.9;
}

.research-card:hover {
  transform: translateY(-6px);
  border-color: rgba(70, 190, 225, 0.48);
  box-shadow:
    0 22px 48px rgba(30, 80, 120, 0.15),
    0 0 34px rgba(90, 205, 240, 0.14);
}

.research-icon {
  position: relative;
  z-index: 2;

  width: 44px;
  height: 44px;
  border-radius: 14px;

  display: flex;
  align-items: center;
  justify-content: center;

  font-size: 22px;
  background: rgba(218, 242, 249, 0.95);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.8);
}

.research-card h3 {
  position: relative;
  z-index: 2;

  margin: 18px 0 16px;
  font-size: 19px;
  line-height: 1.35;
  font-weight: 800;
  color: #2f373d;
}

.research-card p {
  position: relative;
  z-index: 2;

  margin: 0;
  font-size: 15.5px;
  line-height: 1.75;
  color: #536171;
}

/* Tags will stay at the bottom and never overlap text */
.research-tags {
  position: relative;
  z-index: 2;

  margin-top: auto;
  padding-top: 18px;

  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.research-tags span {
  display: inline-flex;
  align-items: center;

  padding: 5px 10px;
  border-radius: 999px;

  font-size: 12px;
  font-weight: 700;
  color: #3d8da9;
  background: rgba(105, 185, 215, 0.14);
  border: 1px solid rgba(105, 185, 215, 0.12);
}

/* =========================
   Mouse Pulse Effect
========================= */

.circuit-pulse {
  position: absolute;
  width: 12px;
  height: 12px;
  pointer-events: none;
  border-radius: 50%;
  transform: translate(-50%, -50%);
  z-index: 1;

  background: rgba(90, 215, 245, 0.48);
  box-shadow:
    0 0 12px rgba(80, 205, 245, 0.7),
    0 0 30px rgba(80, 205, 245, 0.35);

  animation: circuitPulse 0.95s ease-out forwards;
}

@keyframes circuitPulse {
  0% {
    opacity: 0.95;
    transform: translate(-50%, -50%) scale(0.45);
  }

  65% {
    opacity: 0.36;
  }

  100% {
    opacity: 0;
    transform: translate(-50%, -50%) scale(8);
  }
}

/* =========================
   Responsive
========================= */

@media (max-width: 760px) {
  .research-grid {
    grid-template-columns: 1fr;
  }

  .research-card {
    min-height: 235px;
  }

  .section-title {
    font-size: 23px;
  }
}

@media (prefers-reduced-motion: reduce) {
  .research-card,
  .circuit-pulse {
    animation: none;
    transition: none;
  }
}
</style>

<script>
document.addEventListener("DOMContentLoaded", () => {
  const section = document.querySelector(".circuit-bg");
  if (!section) return;

  let lastTime = 0;

  section.addEventListener("mousemove", (e) => {
    const now = Date.now();

    // 控制脉冲生成频率，避免鼠标移动时生成过多元素
    if (now - lastTime < 85) return;
    lastTime = now;

    const rect = section.getBoundingClientRect();
    const pulse = document.createElement("span");

    pulse.className = "circuit-pulse";
    pulse.style.left = `${e.clientX - rect.left}px`;
    pulse.style.top = `${e.clientY - rect.top}px`;

    section.appendChild(pulse);

    setTimeout(() => {
      pulse.remove();
    }, 950);
  });
});
</script>
