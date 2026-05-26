---
layout: page
title: Experience
permalink: /Experience/
feature-img: "assets/img/pexels/travel2.JPG"
position: 3
---
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
 
  :root {
    --bg: #0b0e13;
    --surface: #13171f;
    --border: #1e2430;
    --accent: #4ef0c4;
    --accent2: #7b6ef6;
    --text: #dde3ef;
    --muted: #6b7589;
    --tag-bg: #1a1f2e;
  }
 
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Mono', monospace;
    min-height: 100vh;
    padding: 4rem 1.5rem;
    overflow-x: hidden;
  }
 
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(78,240,196,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(78,240,196,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }
 
  .container {
    max-width: 860px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
  }
 
  .section-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.2em;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 0.5rem;
    opacity: 0;
    animation: fadeUp 0.5s ease forwards;
  }
 
  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2.2rem, 5vw, 3.5rem);
    font-weight: 800;
    line-height: 1;
    margin-bottom: 3.5rem;
    opacity: 0;
    animation: fadeUp 0.5s ease 0.1s forwards;
  }
 
  .section-title span {
    -webkit-text-stroke: 1px var(--accent2);
    color: transparent;
  }
 
  .timeline {
    position: relative;
    padding-left: 2rem;
  }
 
  .timeline::before {
    content: '';
    position: absolute;
    left: 0;
    top: 8px;
    bottom: 8px;
    width: 1px;
    background: linear-gradient(to bottom, var(--accent), var(--accent2), transparent);
  }
 
  .entry {
    position: relative;
    margin-bottom: 3rem;
    opacity: 0;
    transform: translateX(-16px);
  }
 
  .entry.visible {
    animation: slideIn 0.55s ease forwards;
  }
 
  .entry::before {
    content: '';
    position: absolute;
    left: -2.375rem;
    top: 8px;
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 10px var(--accent);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
 
  .entry:hover::before {
    transform: scale(1.5);
    box-shadow: 0 0 18px var(--accent);
  }
 
  .entry-inner {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.5rem 1.75rem;
    transition: border-color 0.3s ease, transform 0.3s ease, box-shadow 0.3s ease;
    cursor: default;
  }
 
  .entry-inner:hover {
    border-color: var(--accent);
    transform: translateX(6px);
    box-shadow: -4px 0 24px rgba(78,240,196,0.08);
  }
 
  .date {
    display: inline-block;
    font-size: 0.68rem;
    letter-spacing: 0.12em;
    color: var(--accent);
    background: rgba(78,240,196,0.08);
    border: 1px solid rgba(78,240,196,0.2);
    border-radius: 4px;
    padding: 0.2rem 0.55rem;
    margin-bottom: 0.85rem;
  }
 
  .role {
    font-family: 'Syne', sans-serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: #fff;
    margin-bottom: 0.2rem;
    line-height: 1.3;
  }
 
  /* Thesis title link */
  .thesis {
    font-size: 0.75rem;
    color: var(--accent2);
    font-style: italic;
    margin-bottom: 0.85rem;
    display: block;
  }
 
  .thesis::before {
    content: '⌗ ';
    color: var(--muted);
    font-style: normal;
  }
 
  .org {
    font-size: 0.75rem;
    color: var(--muted);
    margin-bottom: 1rem;
    letter-spacing: 0.05em;
  }
 
  .org span {
    color: var(--accent2);
    font-style: italic;
  }
 
  .bullets {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }
 
  .bullets li {
    font-size: 0.8rem;
    line-height: 1.6;
    color: #9aa3b8;
    padding-left: 1.1rem;
    position: relative;
  }
 
  .bullets li::before {
    content: '›';
    position: absolute;
    left: 0;
    color: var(--accent);
    font-size: 1rem;
    line-height: 1.4;
  }
 
  .tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
    margin-top: 1.1rem;
  }
 
  .tag {
    font-size: 0.62rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--accent2);
    background: rgba(123,110,246,0.1);
    border: 1px solid rgba(123,110,246,0.25);
    border-radius: 3px;
    padding: 0.18rem 0.5rem;
  }
 
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(12px); }
    to   { opacity: 1; transform: translateY(0); }
  }
 
  @keyframes slideIn {
    from { opacity: 0; transform: translateX(-16px); }
    to   { opacity: 1; transform: translateX(0); }
  }
 
  .entry:nth-child(1) { animation-delay: 0.2s; }
  .entry:nth-child(2) { animation-delay: 0.35s; }
  .entry:nth-child(3) { animation-delay: 0.5s; }
  .entry:nth-child(4) { animation-delay: 0.65s; }
</style>
 
<div class="container">
  <p class="section-label">// academic background</p>
  <h2 class="section-title">Edu<span>cation</span></h2>
 
  <div class="timeline">
 
    <!-- Entry 1 -->
    <div class="entry visible">
      <div class="entry-inner">
        <span class="date">09.2023 — 09.2025</span>
        <p class="role">Master of Digital Text Analysis</p>
        <p class="org"><span>University of Antwerp</span> · Antwerp, Belgium</p>
        <span class="thesis">Enhancing LLM Evaluation: A Synthetic Data Approach to Context Understanding</span>
        <ul class="bullets">
          <li>Applying Large Language Models, NLP, Machine Learning, and Data Science to perform computational tasks on diverse textual and numerical content.</li>
        </ul>
        <div class="tags">
          <span class="tag">LLMs</span>
          <span class="tag">NLP</span>
          <span class="tag">Machine Learning</span>
          <span class="tag">RAG</span>
          <span class="tag">Synthetic Data</span>
        </div>
      </div>
    </div>
 
    <!-- Entry 2 -->
    <div class="entry visible">
      <div class="entry-inner">
        <span class="date">03.2017 — 10.2021</span>
        <p class="role">Ph.D. in Physics</p>
        <p class="org"><span>University of Antwerp</span> · Antwerp, Belgium</p>
        <span class="thesis">Charge Transport in Magnetic Topological Insulators</span>
        <div class="tags">
          <span class="tag">Condensed Matter</span>
          <span class="tag">Topology</span>
          <span class="tag">Quantum Transport</span>
          <span class="tag">HPC</span>
          <span class="tag">VASP</span>
        </div>
      </div>
    </div>
 
    <!-- Entry 3 -->
    <div class="entry visible">
      <div class="entry-inner">
        <span class="date">09.2011 — 04.2014</span>
        <p class="role">M.Sc. in Physics</p>
        <p class="org"><span>Institute for Advanced Studies in Basic Science</span> · Iran</p>
        <ul class="bullets">
          <li>Studying quantum interaction effects on the anisotropic properties of materials.</li>
        </ul>
        <div class="tags">
          <span class="tag">Quantum Mechanics</span>
          <span class="tag">Anisotropy</span>
          <span class="tag">Materials Science</span>
        </div>
      </div>
    </div>
 
    <!-- Entry 4 -->
    <div class="entry visible">
      <div class="entry-inner">
        <span class="date">09.2003 — 04.2008</span>
        <p class="role">B.Sc. in Physics</p>
        <p class="org"><span>University of Tehran</span> · Tehran, Iran</p>
        <ul class="bullets">
          <li>Image processing of interferometric patterns for semiconductor surface topography.</li>
        </ul>
        <div class="tags">
          <span class="tag">Image Processing</span>
          <span class="tag">Interferometry</span>
          <span class="tag">Semiconductors</span>
        </div>
      </div>
    </div>
 
  </div>
</div>
