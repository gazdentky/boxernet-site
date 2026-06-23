---
layout: default
lang: en
title: Business | Boxernet Inc.
heading: Our Business
description: Boxernet's business. Introducing Tsubusukun, the Pickup Station, and our state-transition detection platform.
permalink: /en/business/
alt_url: /business/
hero: true
hero_class: hero-shinjuku
lead: An urban-infrastructure OS that manages IoT devices in logistics, recycling, and public spaces through state transitions.
---

Boxernet is building an **urban-infrastructure OS** that manages the state of IoT devices placed in logistics, recycling, and public spaces as a series of "state transitions" — **reserved, occupied, full, error, and collected**.

## Two Core Businesses

<div class="card-grid" markdown="0">
  <div class="card">
    <h3>Reservable Pickup Stations</h3>
    <p>An <strong>urban infrastructure</strong> that eliminates the inefficiency of redelivery and the last mile. In partnership with e-commerce and delivery operators, stations are installed in front of stations, in commercial facilities, and in apartment entrances. The cloud manages the reserve → store → receive state transition.</p>
  </div>
  <div class="card">
    <h3>Smart Recycling Box (Tsubusukun)</h3>
    <p>An <strong>urban resource-circulation infrastructure</strong> that brings IoT to collection operations beside vending machines and in public spaces. By detecting the deposit, compression, fill, and collection of PET bottles and other items as state transitions, it optimizes collection frequency while preventing overflow incidents.</p>
  </div>
</div>

## Common Platform

Both businesses are powered by Boxernet's proprietary state-transition management platform.

**MQTT / Sensors / Reservation / Notifications / State Transition / Operations Automation**

Using a lightweight protocol (MQTT) and a variety of sensors, we capture on-site events and deliver reservation, notification, a state-transition engine, and operations automation end to end. Even as the application changes, our goal is an architecture that lets new urban-infrastructure services launch simply by placing them on top of the common platform.

<style>
  .biz-demo-wrap{
    margin:32px 0 8px;
    border:1px solid var(--color-border);
    border-radius:var(--radius);
    overflow:hidden;
    background:#fff;
    box-shadow:var(--shadow);
  }
  .biz-demo-frame{
    width:100%;
    height:1080px;
    border:0;
    display:block;
    transition:height 0.3s ease;
  }
  .biz-demo-cta{
    text-align:center;
    margin:8px 0 32px;
  }
  .biz-demo-cta .btn{
    background:var(--color-primary);
    color:#fff !important;
    padding:10px 24px;
    border-radius:999px;
    font-size:14px;
    font-weight:600;
    text-decoration:none;
    display:inline-block;
  }
  .biz-demo-cta .btn:hover{
    background:var(--color-primary-dark);
    text-decoration:none;
  }
  .biz-demo-note{
    font-size:12px;
    color:var(--color-text-sub);
    margin-top:8px;
  }
  @media (max-width:720px){
    .biz-demo-frame{ height:1700px; }
  }
</style>

<script>
  // Receive height notifications from the embedded demo iframe and auto-resize
  // (applies to the Tsubusukun demo only; pickup-station-demo is separate)
  window.addEventListener('message', function(e){
    var d = e.data;
    if(d && d.source === 'tsubusukun-demo' && d.type === 'resize' && typeof d.height === 'number'){
      var iframes = document.querySelectorAll('iframe.biz-demo-frame');
      iframes.forEach(function(f){
        if(f.classList.contains('biz-demo-frame--pickup')) return;
        f.style.height = Math.max(d.height + 20, 600) + 'px';
      });
    }
  });
</script>

## Tsubusukun Interactive Demo

Experience how it works right in your browser. Click the "▶ Start Demo" button to play through the 6 steps in order: deposit → compression → collection request → full shutdown → collection complete. *(Demo labels are in Japanese.)*

<div class="biz-demo-wrap">
  <iframe class="biz-demo-frame" src="{{ '/assets/demo/tsubusukun-demo.html' | relative_url }}" title="Tsubusukun Interactive Demo (simplified)" loading="lazy"></iframe>
</div>
<div class="biz-demo-cta">
  <a href="{{ '/demo/' | relative_url }}" class="btn">View the demo in full screen →</a>
  <div class="biz-demo-note">Opens a dedicated page with commentary for investors and partners (Japanese).</div>
</div>

## Pickup Station Interactive Demo

This shows how a **reservation-based smart pickup point** installed in front of stations or in commercial facilities works. It reproduces the 3 steps from specifying a station at e-commerce checkout, to the courier unlocking with a QR code to store the parcel, to the recipient retrieving it with a QR code.

<div class="biz-demo-wrap">
  <iframe class="biz-demo-frame biz-demo-frame--pickup" src="{{ '/assets/demo/pickup-station-demo.html' | relative_url }}" title="Pickup Station Interactive Demo" loading="lazy"></iframe>
</div>
<div class="biz-demo-cta">
  <div class="biz-demo-note">State transition: <strong>EMPTY</strong> → <strong>RESERVED</strong> → <strong>OCCUPIED</strong> → <strong>EMPTY</strong> (returns to available)</div>
</div>

<style>
  .biz-demo-frame--pickup{ height:840px; }
  @media (max-width:720px){
    .biz-demo-frame--pickup{ height:1320px; }
  }
</style>

## Technical Approach

### 1. State Detection with Multiple Sensors

We combine the optimal sensors for each asset's characteristics — weight, distance, acceleration, open/close, and more — to capture state changes at exactly the right granularity.

### 2. Status Estimation with HMM

Rather than simple threshold judgments on observed values, we use the Hidden Markov Model (HMM) to probabilistically estimate "which state the asset is currently in." This delivers operational decisions that are robust even against sensor noise and missing data.

### 3. Optimizing Remote Management

By combining the estimated state with operating costs and priorities, our algorithms automatically determine the optimal timing for collection, replenishment, and inspection.

---

## Case Studies & Inquiries

For questions about adoption or partnerships, please reach out via our [Contact page]({{ '/en/contact/' | relative_url }}).
