# FlipCart_PlaywrightJS
# 🎭 Playwright Automation Framework – Flipkart E2E Testing

A **real-world Playwright automation framework** built using **JavaScript** to validate a critical e-commerce user journey on **Flipkart**.

This project focuses on **how automation frameworks are structured in real teams** — with clear separation of concerns, reusable utilities, and readable test flows — rather than just writing test scripts.

---

## 🧪 Automated Test Scenario

The following end-to-end user flow has been automated to simulate a real customer journey:

1. Launch the Flipkart application
2. Search for a mobile phone
3. Capture and print all displayed search results
4. Apply filters on the search results
5. Select and validate the first product displayed after filtering

This scenario validates **search functionality, filtering behavior, and result consistency**, making it suitable for smoke and regression testing.

---

## 🧩 Tech Stack

* **Playwright** (JavaScript)
* **Node.js**
* **Playwright Test Runner**
* **Page Object Model (POM)**
* **Git & GitHub**

---

## 🏗️ Project Structure

```
FLIPKARTJS/
│
├── .github/                # GitHub workflows & configs
│
├── Base/                   # Core base-level utilities
│   └── Library.js          # Common reusable base methods
│
├── components/             # UI component-level abstractions
│
├── constants/              # Application constants & static values
│
├── fixtures/               # Test data & custom fixtures
│
├── hooks/                  # Test hooks (before/after logic)
│
├── pages/                  # Page Object Model (POM)
│   ├── SearchPage.js
│   └── SearchResultPage.js
│
├── tests/                  # Test specifications
│   ├── smoke/              # Smoke test suite
│   │   └── SearchTest.spec.js
│   ├── regression/         # Regression test suite
│   └── e2e/                # End-to-end test suite
│
├── utils/                  # Reusable utilities
│   ├── ElementAction.js    # Wrapper methods for element interactions
│   ├── WaitUtils.js        # Centralized wait handling
│   ├── FrameUtils.js       # Frame-related helpers
│   ├── ExcelUtility.js     # Data handling from Excel
│   └── ReusableUtils.js    # Generic helper methods
│
├── playwright-report/      # Playwright HTML reports
├── reports/                # Custom reports (if any)
├── test-results/           # Screenshots, videos & traces
│
├── playwright.config.js    # Playwright configuration
├── package.json
├── package-lock.json
└── README.md
```

---

## ✨ Framework Highlights

* Page Object Model (POM) for clean UI abstraction
* Separate test suites for **smoke, regression, and e2e** testing
* Reusable utilities for element actions, waits, and frames
* Clean, readable test cases focused on business flows
* Playwright HTML reporting with screenshots and traces on failure
* CI/CD friendly project structure

---

## 🧪 Sample Test Flow

```js
test('Search mobile and apply filters', async ({ page }) => {
  const searchPage = new SearchPage(page);
  const searchResultPage = new SearchResultPage(page);

  await searchPage.searchForProduct('Mobile');
  await searchResultPage.printAllResults();
  await searchResultPage.applyFilters();
  await searchResultPage.selectFirstProduct();
});
```

The test remains **business-readable**, while implementation details are handled inside page objects and utilities.

---

## ▶️ How to Run the Tests

### 1️⃣ Clone the repository

```bash

```

### 2️⃣ Install dependencies

```bash
npm install
```

### 3️⃣ Run all tests

```bash
npx playwright test
```

### 4️⃣ Run tests in UI mode

```bash
npx playwright test --ui
```

---

## 📊 Test Reports

After execution, open the Playwright HTML report:

```bash
npx playwright show-report
```

The report includes:

* Test execution summary
* Screenshots on failure
* Video recordings
* Trace files for debugging

---

## 🧠 Design Principles Followed

* No hard-coded waits — Playwright auto-waiting is used
* Assertions kept within tests, not page objects
* Reusable logic extracted into utilities
* Tests written to reflect real user behavior
* Framework structured for easy scalability

---

## 🚀 Future Enhancements

* GitHub Actions CI pipeline
* Environment-based execution (QA / Staging / Prod)
* API + UI integrated flows
* Dockerized test execution
* Advanced reporting integration

---

## 👩‍💻 Author

**Thirupathi** – QA Automation Engineer

* Experience with Playwright, Selenium, and API automation
* Strong focus on framework design and test reliability
* Passionate about writing clean, maintainable automation code

---

⭐ If this repository helped you understand my approach to automation, feel free to star the repo or connect with me on LinkedIn.

