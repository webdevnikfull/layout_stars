# 🖥️ QA & UI Layout: Rating Stars Component - Pixel-Perfect Validation

> ### A frontend layout project focusing on state-based UI testing, strict BEM architecture, and component isolation.

This repository demonstrates the ability to translate strict UI/UX design specifications into semantic, production-ready HTML/CSS. 

More importantly from a Quality Assurance perspective, it showcases how to build DOM structures using scalable naming conventions (BEM) that are highly predictable and optimized for automated End-to-End (E2E) testing frameworks.

---

## 🌐 Live Demo & QA Reports

- **[Live Application Demo](https://webdevnikfull.github.io/layout_stars/)**
- **[Automated Test HTML Report](https://webdevnikfull.github.io/layout_stars/report/html_report/)**

---

## 🧪 QA Focus: Design for Testability

Writing testable UI code is a critical skill for modern automation. This component was developed with specific constraints to ensure stability in headless browser testing environments:

### 1. State-Driven Test Locators (BEM Modifiers)
Relying on complex CSS selectors for automation leads to flaky tests. To ensure robust E2E test scripts, the component states are strictly controlled by BEM modifiers (`stars--0` through `stars--5`).
- **QA Advantage:** A test script can easily validate the correct rendering of a 3-star rating by simply asserting `expect(element).toHaveClass('stars--3')`, without needing to count individual child nodes.

### 2. Test Runner Compatibility Constraints
Modern CSS features sometimes conflict with older or specific headless test runners. 
- **Constraint Handled:** The CSS Flexbox `gap` property was intentionally avoided for spacing the stars, as it lacks support in certain automated testing pipelines. Standard margins/paddings within flex containers were strategically used instead to ensure 100% test compatibility.

### 3. Visual Regression & Component Isolation
The UI component was coded to exactly match the Figma design (Pixel-Perfect), providing a strict baseline for Visual Regression Testing tools. Each BEM block is isolated in its own file, ensuring that layout adjustments do not cause regressions in global styles.

---

## 🎯 UI / UX Specifications (System Under Test)

The stars component adheres to the following strict layout and styling rules:

- **Component States:** Implements 6 distinct instances of the rating block, displaying scores from 0 to 5.
- **Strict Modifier Logic:** The dynamic highlighting of active (yellow) stars is handled purely via CSS parent modifiers combined with pseudo-selectors, keeping the DOM extremely clean and free of unnecessary utility classes.
- **Asset Handling:** Stars are rendered using CSS `background-image` rather than inline `<img>` or `<svg>` tags, separating content from decorative layout elements.
- **Flexible Layout:** Built with `display: flex` to resolve inline-block spacing anomalies, ensuring pixel-perfect alignment according to Figma specifications.
- **Reset Standards:** Browser default margins were completely reset to ensure consistent cross-browser rendering during automated tests.

---

## 🧰 Tech Stack

- **Markup:** Semantic HTML5
- **Styling:** CSS3 (Flexbox, BEM Methodology, Background-Images)
- **Design Source:** Figma Mockups
- **Testing Approach:** Pixel-Perfect Validation, Automated DOM Testing compatibility

---

## ⚙️ Local Development

1. Clone the repository:
   ```bash
   git clone [https://github.com/webdevnikfull/layout_stars.git](https://github.com/webdevnikfull/layout_stars.git)
