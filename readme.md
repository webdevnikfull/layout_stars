# 🧪 QA Portfolio: Interactive Star Rating & Visual Testing

> **About this repository:** This project features an interactive star rating component accompanied by a robust QA setup. It showcases expertise in **Visual Regression Testing** for dynamic UI components and strict architectural enforcement using BEM and CSS linters.

![Visual Testing](https://img.shields.io/badge/-Visual_Regression-FF4081?style=for-the-badge&logo=applitools&logoColor=white)
![CSS3 & BEM](https://img.shields.io/badge/-BEM_Methodology-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![ESLint](https://img.shields.io/badge/-Static_Analysis-4B32C3?style=for-the-badge&logo=eslint&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/-CI/CD-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)

## 🎯 Project Overview

The core application is a dynamic star-rating widget (`src/index.html`, `src/images/`). However, the primary focus of this repository is its **Quality Assurance automation pipeline**. 

As a **QA Automation Engineer**, my objective here is to validate that interactive UI elements render correctly across viewports and remain visually stable through automated regression testing.

## 🛠️ QA Tech Stack & Tools

* **Visual Regression Testing:** BackstopJS (`backstopConfig.js`)
* **UI Architecture Validation:** BEM Linter (`.bemlintrc.json`)
* **Static Code Analysis (Shift-Left QA):** Stylelint, LintHTML, ESLint
* **CI/CD Pipeline:** GitHub Actions

## 📊 Test Strategy & Coverage

The testing framework targets potential frontend vulnerabilities:

### 1. Visual Regression Validation (BackstopJS)
Using `backstopConfig.js`, the test suite captures baseline snapshots of the star rating component in various states (default, hovered, active/selected). Any unintended shifting or styling bugs introduced during code modifications are caught automatically.

### 2. Architectural & Code Quality Gates
The repository enforces strict standards via continuous integration (`.github/workflows/test.yml`):
* **BEM Compliance:** Ensures CSS classes follow the Block Element Modifier convention for high scalability.
* **Linters:** Automatically checks HTML, CSS, and JS files for syntax, formatting, and structural errors before merge.

## 🚀 How to Run the Tests Locally

To evaluate the visual tests and code quality tools on your local machine, follow these steps:

### 1. Environment Setup
Clone the repository and install the dependencies:
```bash
npm install
