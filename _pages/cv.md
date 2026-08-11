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
* Coursework in Computer Science & Artificial Intelligence, KTH Royal Institute of Technology, Aug 2023 – June 2024
* B.Tech in Electronics & Telecommunication Engineering (Honours: AI & Data Analytics), Vishwakarma Institute of Technology (affiliated with University of Pune), Aug 2019 – May 2023

Experience
======
* **Master's Thesis Researcher, PostNord** (Jan 2026 – Present)
  * Reframed parcel dwell-time prediction as a survival-analysis problem across a network of ~6,000+ parcel lockers handling ~12M+ annual deliveries.
  * Built an end-to-end modelling pipeline — feature engineering, model benchmarking, and hyperparameter optimization.
  * Evaluated feature importance to support a target of increasing locker utilization from 1.25x to 2.25x, continuing to collaborate with PostNord toward real-time production deployment.

* **AI Intern, TCS Sverige AB** (Jul 2025 – Jun 2026)
  * Translated business workflows across 5 departments into 4 Copilot agents automating repetitive tasks, improving cross-functional productivity by an estimated 10%.
  * Co-designed an AI maturity assessment framework across 7 business domains, defining evaluation criteria to identify high-value AI opportunities.
  * Deployed an AI-assisted SDLC framework, demonstrating AI-driven software engineering workflows for client engagements — including rapid PoC prototyping with Claude Code at TCS Pace Studio.
  * Built a reusable camera calibration pipeline for vision-guided robotic automation on a robotic arm at TCS Pace Studio (Stockholm).
  * Shipped an internal sales-enablement web app via AI-assisted prototyping, wiring REST APIs to local storage.

* **Computer Vision Engineer, LiU Formula Student** (Sep 2024 – Jun 2025)
  * Designed a 90%+ accurate perception pipeline for YOLO-based cone detection on the team's autonomous race car.
  * Led integration of the perception module (Camera + LiDAR) for the driverless vehicle, improving vehicle state estimation by 70% via ZED-camera pose estimates.
  * Provided vehicle position information for downstream navigation, supporting successful camera-based autonomous vehicle testing.
  * Collaborated cross-functionally on continual perception-stack improvements.

* **Computer Vision Intern, PostNord** (Jul 2022 – May 2023)
  * R&D on correct-parcel-drop detection at PostNord terminals — compared keypoint tracking (MediaPipe), optical flow, and YOLO object detection.
  * Built and deployed a background-subtraction solution (90% detection accuracy) as the backbone of a real-time parcel-drop detection pipeline on operational camera feeds.
  * Trained a custom YOLOv8 model for cage detection and implemented GDPR-compliant person-masking on top of distortion correction for reliable tracking.
  * Designed a fisheye-feed orientation-correction method from terminal cameras.

* **ADCS Engineer, Trident Labs (SATLAB)** (Jul 2021 – Aug 2022)
  * Developed the core mathematics library for satellite Attitude Determination & Control Systems (ADCS).
  * Collaborated cross-functionally on payload selection.

Skills
======
* **Programming Languages**: Python, R, C++, SQL
* **Machine Learning**: PyTorch, TensorFlow, scikit-learn, OpenCV, Deep Learning, NLP
* **LLM & Agentic AI**: LangChain, LangGraph, Retrieval-Augmented Generation (RAG — Naïve, Reranking), Prompt & Context Engineering, MCP
* **Cloud & Deployment**: GCP, AWS, Docker, Google Cloud Run
* **Data**: Pandas, NumPy, PySpark, Vector Databases (Qdrant, ChromaDB)
* **Web**: FastAPI, Node.js, React, REST APIs
* ROS

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
