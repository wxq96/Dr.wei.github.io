---
layout: archive
title: "Profile"
permalink: /
author_profile: true
---

<style>
.profile-hero {
  display: flex;
  align-items: center;
  gap: 42px;
  margin: 10px 0 42px 0;
  padding: 34px;
  border-radius: 26px;
  background: linear-gradient(135deg, #f8fafc 0%, #eef7fb 45%, #ffffff 100%);
  box-shadow: 0 12px 34px rgba(15, 23, 42, 0.10);
  border: 1px solid #e6eef3;
}

.profile-hero-text {
  flex: 1;
}

.profile-kicker {
  color: #2f80a0;
  font-weight: 700;
  font-size: 14px;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  margin-bottom: 8px;
}

.profile-hero h1 {
  font-size: 38px;
  line-height: 1.15;
  margin: 0 0 12px 0;
  color: #2f3437;
}

.profile-subtitle {
  font-size: 18px;
  line-height: 1.75;
  color: #4b5563;
  margin-bottom: 22px;
}

.profile-photo-main {
  width: 230px;
  height: 230px;
  object-fit: cover;
  border-radius: 50%;
  box-shadow: 0 14px 36px rgba(15, 23, 42, 0.22);
  border: 5px solid #ffffff;
}

.profile-buttons a {
  display: inline-block;
  padding: 10px 18px;
  margin: 6px 8px 6px 0;
  border-radius: 999px;
  text-decoration: none;
  font-size: 14px;
  font-weight: 700;
  background: #2f80a0;
  color: #ffffff;
  box-shadow: 0 5px 12px rgba(47, 128, 160, 0.22);
}

.profile-buttons a.secondary {
  background: #ffffff;
  color: #2f80a0;
  border: 1px solid #2f80a0;
  box-shadow: none;
}

.profile-buttons a:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 18px rgba(47, 128, 160, 0.28);
}

.profile-buttons a.secondary:hover {
  background: #eef7fb;
}

.section-title {
  margin-top: 42px;
  margin-bottom: 18px;
  font-size: 25px;
  color: #2f3437;
  border-bottom: 1px solid #e5e7eb;
  padding-bottom: 8px;
}

/* Fancy hover research cards */

.research-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 22px;
  margin-top: 22px;
  margin-bottom: 42px;
}

.research-card {
  position: relative;
  overflow: hidden;
  padding: 26px 24px 24px 24px;
  min-height: 255px;
  border-radius: 24px;
  background: rgba(255, 255, 255, 0.92);
  border: 1px solid rgba(226, 232, 240, 0.95);
  box-shadow: 0 10px 26px rgba(15, 23, 42, 0.08);
  cursor: default;
  transition:
    transform 0.28s ease,
    box-shadow 0.28s ease,
    border-color 0.28s ease,
    background 0.28s ease;
}

.research-card::before {
  content: "";
  position: absolute;
  inset: 0;
  background:
    radial-gradient(circle at top right, rgba(47, 128, 160, 0.22), transparent 35%),
    linear-gradient(135deg, rgba(238, 247, 251, 0.88), rgba(255, 255, 255, 0.95));
  opacity: 0;
  transition: opacity 0.28s ease;
  z-index: 0;
}

.research-card:hover {
  transform: translateY(-9px) scale(1.015);
  border-color: rgba(47, 128, 160, 0.48);
  box-shadow: 0 22px 48px rgba(15, 23, 42, 0.16);
}

.research-card:hover::before {
  opacity: 1;
}

.research-card-content {
  position: relative;
  z-index: 1;
}

.research-icon {
  width: 48px;
  height: 48px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 18px;
  border-radius: 16px;
  background: #eef7fb;
  color: #2f80a0;
  font-size: 24px;
  transition:
    transform 0.28s ease,
    background 0.28s ease,
    color 0.28s ease;
}

.research-card:hover .research-icon {
  transform: rotate(-6deg) scale(1.12);
  background: #2f80a0;
  color: #ffffff;
}

.research-card h3 {
  margin: 0 0 10px 0;
  color: #2f3437;
  font-size: 20px;
  line-height: 1.35;
}

.research-card p {
  color: #4b5563;
  line-height: 1.7;
  margin-bottom: 0;
}

.research-hover-detail {
  max-height: 0;
  opacity: 0;
  transform: translateY(12px);
  overflow: hidden;
  margin-top: 0;
  color: #4b5563;
  line-height: 1.65;
  transition:
    max-height 0.32s ease,
    opacity 0.32s ease,
    transform 0.32s ease,
    margin-top 0.32s ease;
}

.research-card:hover .research-hover-detail {
  max-height: 130px;
  opacity: 1;
  transform: translateY(0);
  margin-top: 14px;
}

.research-tags {
  position: absolute;
  left: 24px;
  right: 24px;
  bottom: 22px;
  display: flex;
  flex-wrap: wrap;
  gap: 7px;
  opacity: 0.72;
  transform: translateY(6px);
  transition:
    opacity 0.28s ease,
    transform 0.28s ease;
  z-index: 1;
}

.research-card:hover .research-tags {
  opacity: 1;
  transform: translateY(0);
}

.research-tag {
  padding: 5px 10px;
  border-radius: 999px;
  background: rgba(47, 128, 160, 0.10);
  color: #2f80a0;
  font-size: 12px;
  font-weight: 700;
}

.card-shine {
  position: absolute;
  top: -90px;
  left: -90px;
  width: 110px;
  height: 280px;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255,255,255,0.7),
    transparent
  );
  transform: rotate(28deg) translateX(-180px);
  opacity: 0;
  transition: transform 0.65s ease, opacity 0.65s ease;
  z-index: 2;
  pointer-events: none;
}

.research-card:hover .card-shine {
  opacity: 1;
  transform: rotate(28deg) translateX(460px);
}

/* Pipeline */

.pipeline-box {
  margin-top: 18px;
  padding: 26px;
  border-radius: 22px;
  background: #0f172a;
  color: #e5e7eb;
  box-shadow: 0 10px 30px rgba(15, 23, 42, 0.18);
}

.pipeline-title {
  color: #ffffff;
  font-weight: 800;
  margin-bottom: 18px;
  font-size: 18px;
}

.pipeline-flow {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  align-items: center;
}

.pipeline-node {
  padding: 10px 14px;
  border-radius: 14px;
  background: rgba(255,255,255,0.10);
  border: 1px solid rgba(255,255,255,0.16);
  font-weight: 700;
  color: #ffffff;
  transition: transform 0.25s ease, background 0.25s ease;
}

.pipeline-node:hover {
  transform: translateY(-3px);
  background: rgba(255,255,255,0.18);
}

.pipeline-arrow {
  color: #93c5fd;
  font-weight: 900;
}

/* Publication cards */

.pub-card {
  padding: 20px 22px;
  margin-bottom: 16px;
  border-radius: 18px;
  background: #ffffff;
  border-left: 5px solid #2f80a0;
  box-shadow: 0 6px 20px rgba(15, 23, 42, 0.07);
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}

.pub-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 14px 30px rgba(15, 23, 42, 0.13);
}

.pub-card h3 {
  margin-top: 0;
  margin-bottom: 8px;
  color: #2f3437;
  font-size: 18px;
}

.pub-card p {
  margin: 6px 0;
  color: #4b5563;
  line-height: 1.65;
}

.pub-links a {
  margin-right: 10px;
  font-weight: 700;
  color: #2f80a0;
}

/* Timeline */

.timeline-block {
  padding-left: 20px;
  border-left: 4px solid #2f80a0;
  margin-bottom: 26px;
}

.timeline-block h3 {
  margin-bottom: 4px;
  color: #2f3437;
}

.timeline-block p {
  color: #4b5563;
  line-height: 1.7;
}

/* Badges */

.badge {
  display: inline-block;
  padding: 7px 13px;
  margin: 5px 7px 5px 0;
  border-radius: 999px;
  background: #eef7fb;
  color: #2f80a0;
  font-size: 14px;
  font-weight: 700;
  transition: transform 0.22s ease, background 0.22s ease;
}

.badge:hover {
  transform: translateY(-2px);
  background: #dff1f8;
}

.highlight-box {
  margin-top: 22px;
  padding: 20px 24px;
  border-radius: 18px;
  background: #f8fafc;
  border: 1px solid #e5e7eb;
  color: #4b5563;
  line-height: 1.75;
}

/* Responsive design */

@media (max-width: 768px) {
  .profile-hero {
    flex-direction: column-reverse;
    text-align: center;
    padding: 26px;
  }

  .profile-photo-main {
    width: 190px;
    height: 190px;
  }

  .research-grid {
    grid-template-columns: 1fr;
  }

  .research-card {
    min-height: 250px;
  }

  .pipeline-flow {
    flex-direction: column;
    align-items: stretch;
  }

  .pipeline-arrow {
    text-align: center;
  }
}
</style>

<div class="profile-hero">

  <div class="profile-hero-text">
    <div class="profile-kicker">AI Accelerators · Reinforcement Learning · FPGA/NPU</div>

    <h1>Wei Xiangqing</h1>

    <p class="profile-subtitle">
      I am a doctoral researcher focusing on <strong>hardware–software co-design</strong>
      for deep learning accelerators. My research interests include
      <strong>AI accelerator architecture</strong>,
      <strong>hardware-aware scheduling</strong>,
      <strong>reinforcement-learning-based optimization</strong>,
      and <strong>digital circuit design</strong>.
    </p>

    <div class="profile-buttons">
      <a href="{{ site.baseurl }}/publications/">Publications</a>
      <a class="secondary" href="https://github.com/wxq96">GitHub</a>
      <a class="secondary" href="https://scholar.google.com/citations?user=PS_CX0AAAAAJ">Google Scholar</a>
    </div>
  </div>

  <img class="profile-photo-main"
       src="{{ site.baseurl }}/images/profile_photo_wei.png"
       alt="Wei Xiangqing profile photo">

</div>

<h2 class="section-title">Research Interests</h2>

<div class="research-grid">

  <div class="research-card">
    <div class="card-shine"></div>

    <div class="research-card-content">
      <div class="research-icon">⚙️</div>
      <h3>AI Hardware Architecture</h3>
      <p>
        I am interested in hardware architectures for deep learning acceleration,
        especially computation units, memory access, and system-level efficiency.
      </p>

      <div class="research-hover-detail">
        I focus on how neural network workloads interact with accelerator structures
        and how limited hardware resources can be used more efficiently.
      </div>
    </div>

    <div class="research-tags">
      <span class="research-tag">NPU</span>
      <span class="research-tag">FPGA</span>
      <span class="research-tag">Accelerator</span>
    </div>
  </div>

  <div class="research-card">
    <div class="card-shine"></div>

    <div class="research-card-content">
      <div class="research-icon">🧩</div>
      <h3>Accelerator Scheduling</h3>
      <p>
        I am studying scheduling and resource-allocation problems in accelerator systems,
        including task mapping and execution-order optimization.
      </p>

      <div class="research-hover-detail">
        This direction aims to improve latency, resource utilization, and data-movement efficiency
        under limited processing and memory resources.
      </div>
    </div>

    <div class="research-tags">
      <span class="research-tag">Scheduling</span>
      <span class="research-tag">Mapping</span>
      <span class="research-tag">PE Array</span>
    </div>
  </div>

  <div class="research-card">
    <div class="card-shine"></div>

    <div class="research-card-content">
      <div class="research-icon">🤖</div>
      <h3>RL-based Optimization</h3>
      <p>
        I am exploring reinforcement learning as a potential method for automatic optimization
        in hardware-aware scheduling and design-space exploration.
      </p>

      <div class="research-hover-detail">
        The goal is to connect workload features, hardware constraints, and feedback signals
        into a learning-based optimization loop.
      </div>
    </div>

    <div class="research-tags">
      <span class="research-tag">RL</span>
      <span class="research-tag">DSE</span>
      <span class="research-tag">Optimization</span>
    </div>
  </div>

  <div class="research-card">
    <div class="card-shine"></div>

    <div class="research-card-content">
      <div class="research-icon">🔬</div>
      <h3>Digital Circuit Design</h3>
      <p>
        My previous work includes digital circuit design and processor-related modules,
        such as arithmetic units, Booth multiplication, and SRT division.
      </p>

      <div class="research-hover-detail">
        This background supports my interest in connecting algorithm-level optimization
        with RTL-level hardware implementation.
      </div>
    </div>

    <div class="research-tags">
      <span class="research-tag">RTL</span>
      <span class="research-tag">RISC-V</span>
      <span class="research-tag">Arithmetic</span>
    </div>
  </div>

</div>

<h2 class="section-title">Research Pipeline</h2>

<div class="pipeline-box">
  <div class="pipeline-title">Hardware-aware optimization flow that I am currently exploring</div>

  <div class="pipeline-flow">
    <div class="pipeline-node">DNN Workloads</div>
    <div class="pipeline-arrow">→</div>
    <div class="pipeline-node">Workload Modeling</div>
    <div class="pipeline-arrow">→</div>
    <div class="pipeline-node">Scheduling Strategy</div>
    <div class="pipeline-arrow">→</div>
    <div class="pipeline-node">Accelerator Resources</div>
    <div class="pipeline-arrow">→</div>
    <div class="pipeline-node">Performance Feedback</div>
  </div>
</div>

<h2 class="section-title">Selected Publications</h2>

<div class="pub-card">
  <h3>RL-Based Scheduling and Allocation of MAC Units in Multi-Precision Edge CNN Accelerators</h3>
  <p>
    <strong>Wei Xiangqing</strong>, Yun-ju Baek.
    <em>NOLTA 2025 — International Symposium on Nonlinear Theory and Its Applications</em>, 2025.
  </p>
  <p class="pub-links">
    <a href="#">PDF</a>
    <a href="#">Code</a>
  </p>
</div>

<div class="pub-card">
  <h3>Design and Optimization of Integer Divider Based on SRT4</h3>
  <p>
    <strong>Wei Xiangqing</strong>, Qin Shuijie.
    <em>Microprocessors</em>, Vol. 43, No. 2, pp. 1–5, 2022.
  </p>
  <p class="pub-links">
    <a href="#">PDF</a>
  </p>
</div>

<h2 class="section-title">Academic Background</h2>

<div class="timeline-block">
  <h3>Research Assistant</h3>
  <p>
    <strong>Chiba University, Japan</strong><br>
    Research area: AI accelerators, hardware-aware scheduling, reinforcement learning, and FPGA/NPU-related accelerator design.
  </p>
</div>

<div class="timeline-block">
  <h3>Master’s Degree in Integrated Circuit Engineering</h3>
  <p>
    <strong>Guizhou University, China</strong><br>
    Research area: RISC-V processor design, integer execution units, Booth multiplication,
    SRT division, and digital circuit design.
  </p>
</div>

<h2 class="section-title">Research Keywords</h2>

<p>
  <span class="badge">AI Accelerators</span>
  <span class="badge">NPU</span>
  <span class="badge">FPGA</span>
  <span class="badge">Reinforcement Learning</span>
  <span class="badge">Hardware-aware Scheduling</span>
  <span class="badge">Design Space Exploration</span>
  <span class="badge">Computer Architecture</span>
  <span class="badge">Digital IC Design</span>
  <span class="badge">RTL Design</span>
  <span class="badge">RISC-V</span>
</p>

<div class="highlight-box">
  <strong>Current research direction:</strong>
  I am interested in building hardware-aware optimization methods for deep learning accelerators,
  aiming to connect neural network workload characteristics, scheduling strategies, and accelerator-level performance feedback.
</div>
