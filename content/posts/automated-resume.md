+++
title = "Automating My Professional Identity: A CI/CD Workflow"
date = "2026-02-17T23:26:03+01:00"
draft = false
tags = ["DevOps", "GitHub Actions", "Automation", "Python"]
categories = ["Engineering"]
description = "How I built a self-updating resume and portfolio using Markdown and GitHub Actions."
showTableOfContents = true
+++

## The Concept
As a Software Engineer with nearly a decade of experience, I’ve realized that a CV is more than a document—it’s a data structure. 

I decided to treat my professional identity like a software project. Here is how I built a self-updating resume pipeline.

Over the years, I’ve used different types of software, including Word, and LaTeX. While LaTeX provides beautiful typography, it lacks the "Developer Experience" (DX).

I wanted a system where a single `git push` updated my website and generated a recruiter-ready PDF simultaneously.

I also wanted: version control, easy editing, and automated distribution.

## The Architecture of a Resume
The goal was simple: **Update a single Markdown file and have it automatically reflected on my website and as a downloadable PDF.**

### 1. The Source of Truth (Markdown)
Markdown is the ultimate format for version control. It’s readable, lightweight, and plays perfectly with Git. I structured my repository to keep my content (`resume.md`) separate from my styling (`style.css`).

### 2. The Visual Identity (Nord Aesthetic)
I’ve always been a fan of the **Nord palette**—an arctic-inspired, clean color scheme. By using a custom CSS file for the PDF generation, I ensured my resume wasn't just another black-and-white sheet. It signals a modern, tech-forward aesthetic that aligns with the Cloud/DevOps ecosystem I work in.

### 3. The Automation Engine (GitHub Actions)
I implemented a GitHub Action that triggers every time I push a change to the `resume.md` file.

> The GitHub Action is defined in the `.github/workflows/resume.yml` file the repository. At the end of this post, I'll share GitHub repository link.

## Why Bother?
You might ask: “Olcay, why not just export a PDF from Google Docs?”

For an Engineer, the answer is Scalability and Consistency.

- Zero Drift: My website’s "About" section stays 100% in sync with the PDF recruiters see.
- Version History: I can see exactly when I added a new skill or project over the last 9 years.
- Efficiency: I can apply for a job, realize I have a typo, fix it on my phone via the GitHub app, and have a fresh PDF ready in 60 seconds.

## Conclusion
Automating your resume is a small project, but it mirrors how we should handle enterprise software: **Source Control**, **Automated Builds**, and **Consistent Deployment**. If you're interested in the specific CSS or the workflow YAML, check out my repository at [molcay/molcay.github.io](https://github.com/molcay/molcay.github.io).
