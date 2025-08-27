---
layout: post
title: OpenBIMRL – Rule-Based Validation for IFC Models
date: 2024-10-01
tags:
  - BIM
  - rule-engine
  - webtool
  - Java
  - Kotlin
  - C++
---

## Overview

**OpenBIMRL** is a collaborative research-driven initiative maintained by Ruhr-University Bochum’s Chair of Computing in Engineering, now updated and maintained by me. 
The project builds an open, modular ecosystem for creating and executing rule-based validations on **IFC** building models—bridging digital model standards with compliance verification in construction.

## Project Components & Tech Stack

The OpenBIMRL initiative includes multiple interconnected repositories, each serving a distinct purpose:

- **OpenBIMRL-Engine** – A Kotlin-powered engine (originally Java) that executes rule checking on IFC models.
- **OpenBIMRL-Engine-REST** – A RESTful backend interface providing clean endpoints for rule execution workflows.
- **OpenBIMRL-Engine-Native** – A C++ implementation accessing IFCOpenShell for Rules that rely on parsing IFC data and 3D geometry.
- **OpenBIMRL-CreatorTool** – A Vue + TypeScript web application enabling visual rule authoring and intuitive rule graph editing.

All components are open source under the **MIT License**, ensuring flexibility and extensibility for diverse BIM workflows.

## Research Foundation & Design Goals

This project is grounded in academic research, including my publication with Daniel Napps at the 2024 Forum Bauinformatik, showcasing a container-based, modular rule engine accessible via RESTful APIs.

Key design highlights:

- **Separation of concerns**: Rule engine, REST API, and frontend tools are decoupled for easier integration and modular extension.
- **Containerization**: Enables seamless, OS-agnostic deployment and consistent runtime environments.
- **Graph-based DSL**: Allows non-programmers to define rules visually using nodes that extract data from IFC models and apply logical operations.

One example: validating German ASR A1.2 workplace regulations by fetching IFC spaces, retrieving properties (like floor area and number of workspaces), performing calculations, and aggregating results using logical operators such as AND.

## What Headway We've Made

- Enabled **rule creation by non-technical users** via an approachable graph-based interface.
- Enhanced **debugging** and transparency through node-level JSON responses and direct IFC visualization.
- Created a **modular system** that can easily plug into existing BIM pipelines or tools.

## Looking Forward

The project continues to evolve—planned improvements include:

- **Groupable graph nodes** or "macros" (similar to Unreal Engine’s Blueprint clusters) to simplify complex rule logic.
- **Dynamic or scriptable code nodes** for greater flexibility, sandboxed to ensure security without altering core code.

## Why This Matters for My Portfolio

OpenBIMRL reflects my strengths in:

- **Architecting modular software systems**, cleanly decoupling UI, API, and engine layers.  
- **Bridging academic research with practical tooling**, turning prototypes into usable solutions.  
- **Working across diverse tech stacks**: Kotlin, Java, REST APIs, C++, Vue, and TypeScript.  
- **Designing for usability**, enabling non-technical domain experts to interact with model compliance tools directly.

---

**Explore the codebase and contribute:** [OpenBIMRL on GitHub](https://github.com/OpenBimRL)