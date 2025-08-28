---
layout: post
title: "Bachelor Thesis – Automated SBoM Generation and Evaluation for Open-Source Projects"
date: 2025-02-01
tags:
  - bachelor-thesis
  - sbom
  - open-source
  - security
  - rust
---

## Thesis Overview

For my bachelor’s thesis at Ruhr-Universität Bochum, I researched and implemented a system for **automated generation and evaluation of Software Bills of Materials (SBoMs)** in open-source projects. The work focused on the growing importance of **software supply chain security**, particularly in the context of vulnerabilities in dependencies.

My solution combined:

- Large-scale data collection from GitHub repositories  
- Automated SBoM creation and vulnerability checking using multiple databases  
- A scalable, containerized architecture developed in **Rust** with **GraphQL**, **MariaDB**, and **OWASP Dependency-Track**  

The results showed that more than half of the analyzed projects contained at least one medium- or high-severity vulnerability, with some persisting for years. This demonstrated both the urgency of the issue and the effectiveness of automated analysis.

## Key Outcomes

- Designed and implemented a Rust-based data collection and analysis tool
- Successfully analyzed **714 GitHub repositories** and over **423,000 dependencies**  
- Delivered actionable insights into the state of security in open-source ecosystems
- Contributed to the discussion of responsible disclosure and vulnerability management

---

## Achievement

The thesis was graded **very good**, reflecting the strong technical implementation, depth of research, and contribution to the field of software supply chain security.

---

Full codebase: [GitLab Repository](https://gitlab.ruhr-uni-bochum.de/florianb/bachelorarbeit-code)  
Full thesis (PDF): Available on request
