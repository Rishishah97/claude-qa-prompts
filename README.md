# 🤖 claude-qa-prompts

> Claude AI prompts to help QA teams test smarter and faster.

A curated library of ready-to-use Claude AI prompts for software quality assurance engineers and testers. Whether you're writing test cases, reporting bugs, testing APIs, or building automation — this repo has a prompt for that.

---

## 📁 Folder Structure

```
claude-qa-prompts/
├── README.md
├── prompts/
│   ├── test-case-generation.md
│   ├── bug-reporting.md
│   ├── api-testing.md
│   ├── performance-testing.md
│   ├── security-testing.md
│   ├── mobile-testing.md
│   ├── accessibility-testing.md
│   ├── test-automation.md
│   ├── exploratory-testing.md
│   ├── database-testing.md
│   └── ui-visual-testing.md
└── examples/
    └── sample-outputs.md
```

---

## 🚀 How to Use

1. Browse the `prompts/` folder and pick a prompt that fits your need.
2. Copy the prompt into [Claude.ai](https://claude.ai) or via the Anthropic API.
3. Fill in the `[placeholders]` with your specific context.
4. Review and iterate on Claude's output as needed.

> 💡 **Tip:** The more context you give Claude, the better the output. Include your tech stack, user stories, or acceptance criteria wherever possible.

---

## 📋 Prompt Categories

### 🧪 [Test Case Generation](./prompts/test-case-generation.md)
Generate thorough test cases from user stories, requirements, or feature descriptions. Covers happy paths, edge cases, and negative scenarios.

### 🐛 [Bug Reporting](./prompts/bug-reporting.md)
Write clear, structured, and developer-friendly bug reports with steps to reproduce, expected vs actual behaviour, and severity classification.

### 🔌 [API Testing](./prompts/api-testing.md)
Generate API test scenarios, validate request/response contracts, and identify edge cases for REST and GraphQL endpoints.

### ⚡ [Performance & Load Testing](./prompts/performance-testing.md)
Design performance test plans, write k6/JMeter scripts, analyse results, and define SLAs.

### 🔐 [Security Testing](./prompts/security-testing.md)
Generate OWASP Top 10 test cases, threat models, auth test cases, and security checklists.

### 📱 [Mobile Testing](./prompts/mobile-testing.md)
Cover device compatibility, OS versions, gestures, network conditions, and mobile performance.

### ♿ [Accessibility Testing](./prompts/accessibility-testing.md)
Generate WCAG 2.1 AA test cases, screen reader test scripts, and accessibility audit guidance.

### 🤖 [Test Automation & Code Review](./prompts/test-automation.md)
Write Playwright/Cypress/Selenium scripts, review test code quality, generate POMs, and fix flaky tests.

### 🔍 [Exploratory Testing](./prompts/exploratory-testing.md)
Create session charters, apply testing heuristics, write session reports, and build risk-based test plans.

### 🗄️ [Database Testing](./prompts/database-testing.md)
Validate data integrity, test migrations, write SQL test queries, and test stored procedures.

### 🎨 [UI / Visual Testing](./prompts/ui-visual-testing.md)
Generate UI test cases, cross-browser plans, form validation tests, and visual regression strategies.

---

## 🛠 Tips for Better Results

- **Be specific**: Include feature names, user roles, and acceptance criteria.
- **Provide examples**: Paste in a sample request/response or user story.
- **Iterate**: Ask Claude to refine, extend, or reformat its output.
- **Chain prompts**: Use the output of one prompt as input for the next.

---

## 🤝 Contributing

Contributions are welcome! If you have a prompt that's saved you time, please open a PR.

1. Fork the repo
2. Add your prompt to the relevant file in `prompts/`
3. Follow the existing format (prompt title, description, prompt block)
4. Open a pull request with a short description

---

## 📄 License

MIT License — free to use, modify, and share.

---

## ⭐ Star This Repo

If these prompts save you time, give the repo a star — it helps others find it!
