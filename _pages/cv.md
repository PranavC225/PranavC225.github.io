---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<div class="cv-download-links">
  <a href="{{ base_path }}/files/Pranav_Chandode.pdf" class="btn btn--primary">Download CV as PDF</a>
</div>

Education
======
* M.S. in Statistics & Machine Learning, Linköping University, Aug 2024 – June 2026
* Bachelor's degree in Electronics & Telecommunication Engineering (Honours: AI & Data Analytics)

Experience
======
* **Master's Thesis Student, PostNord** (Jan 2026 – Jun 2026)
  * Designed an interpretable statistical baseline for parcel dwell-time forecasting and built the evaluation harness used as the project benchmark.
  * Benchmarked ML models against that baseline to drive data-driven model-selection decisions.
  * Continuing to collaborate with PostNord beyond the thesis — refining the model and moving it toward real-time production deployment.

* **AI Intern, Tata Consultancy Services** (Jul 2025 – Jun 2026)
  * Built rapid AI prototypes (PoCs) for client-facing demos at TCS Pace Studio, including agentic coding workflows with Claude Code.
  * Calibrated the camera on a robotic arm at TCS Pace Studio (Stockholm), preparing the rig for downstream robotics use cases.
  * Shipped an internal sales-enablement web app via AI-assisted prototyping, wiring REST APIs to local storage.
  * Engineered M365 Copilot custom agents that improved cross-functional productivity by an estimated 10%.

* **Software Engineer, Driverless, LiU Formula Student** (Sep 2024 – Jun 2025)
  * Led integration of the perception module (Camera + LiDAR) for the driverless vehicle.
  * Improved vehicle state estimation by 70% via ZED-camera pose estimates.
  * Collaborated cross-functionally on continual perception-stack improvements.

* **Computer Vision Intern, PostNord** (Jul 2022 – May 2023)
  * R&D on correct-parcel-drop detection at PostNord terminals — compared keypoint tracking (MediaPipe), optical flow, and YOLO object detection.
  * Built a background-subtraction solution (90% accuracy) as the backbone of the detection pipeline.
  * Engineered a custom YOLOv8 cage-detection model with person-masking for GDPR compliance.
  * Designed a fisheye-feed orientation-correction method from terminal cameras.

* **ADCS Engineer, Trident Labs (SATLAB)** (Jul 2021 – Aug 2022)
  * Developed the core mathematics library for satellite Attitude Determination & Control Systems (ADCS).
  * Collaborated cross-functionally on payload selection.

Skills
======
* Python, Machine Learning, Large Language Models (LLM), Computer Vision
* LangChain, LangGraph, Retrieval-Augmented Generation (RAG)
* PyTorch, scikit-learn, OpenCV, Deep Learning, NLP
* FastAPI, Docker, SQL, PySpark, Google Cloud Run
* ROS

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
