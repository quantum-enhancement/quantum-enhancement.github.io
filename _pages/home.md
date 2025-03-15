---
layout: splash
permalink: /
hidden: true
header:
  #overlay_color: "#5e616c"
  overlay_image: /assets/images/ai_gen3.jpg
  overlay_filter: 0.4 # same as adding an opacity of 0.5 to a black background
  # actions:
  #  - label: "<i class='fas fa-download'></i> Install now"
  #    url: "/docs/quick-start-guide/"
excerpt: >
    Technologies by quantum science and security from physics !  <br />
    We develop the necessary solutions with spooky action at a distance.
intro: 
  - excerpt: ''
feature_row:
  - image_path: /assets/images/sensitive_fast_safe.png
    alt: "Q-Computing"
    title: "Q-Computing"
    excerpt: "Quantum Algorithm for Large Scale Quantum System Simulation"
    url: "/docs/q_computing/"
    btn_class: "btn--primary"
    btn_label: "Learn more"
  - image_path: /assets/images/security1.png
    alt: "Q-Security"
    title: "Q-Security"
    excerpt: "Efficient QKD Post Processing using Word Masking technique"
    url: "/docs/q_security/"
    btn_class: "btn--primary"
    btn_label: "Learn more"
  - image_path: /assets/images/degenerate_fwm.png
    alt: "Q-Entanglement"
    title: "Q-Entanglement"
    excerpt: "Long distance entanglement distribution in frequency domain"
    url: "/docs/q_entanglement/"
    btn_class: "btn--primary"
    btn_label: "Learn more"      
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}
