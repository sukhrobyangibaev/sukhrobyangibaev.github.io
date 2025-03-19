---
layout: post
title: "Project | Thesis Generator"
description: Automatically analyze source code files and generate a structured thesis document.
date: 2025-01-24 00:30:00 +0500
categories: [blog,project]
image: assets/images/2025-01-24-thesis-generator/thesis-generator.png
image_alt: "thesis-generator"
---

![](/assets/images/2025-01-24-thesis-generator/thesis-generator.png)

This project provides a tool designed to automatically analyze source code files and generate a structured thesis document. It uses Large Language Models (LLMs) through API integration to accomplish this. The system is intended to assist in creating a first draft of a thesis.

## Key Features

*   Analyzes provided source code to understand the project.
*   Generates a complete thesis structure, including introduction, analysis, development, conclusion, references, and appendix.
*   Offers optional translation into Russian and Uzbek.
*   Integrates with LLMs via API (compatible with OpenAI, Google, and Anthropic).

## Example Use Case

The tool can process the core source code files that are placed inside the `project_files` directory. The thesis structure and outline are generated in `draft/EN/THESIS_PLAN_EN.txt`. The complete thesis content is generated in `draft/EN/THESIS_MAIN_TEXT_EN.txt`. If translation is enabled, additional files are also generated.

## Getting Started
To install, the repository can be cloned, the dependencies can be installed and the `.env` file needs to be configured.

To learn more, the full readme is available here: [https://github.com/sukhrobyangibaev/bmi_first_draft](https://github.com/sukhrobyangibaev/bmi_first_draft)