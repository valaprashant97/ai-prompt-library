# GitHub Secrets & API Key Security Protection Prompt

## When to Use

Use this prompt when you want to protect project API keys, passwords, tokens, and other sensitive information before publishing a project to GitHub.

It is suitable for:

- Web applications
- Flutter applications
- React applications
- Node.js applications
- Python applications
- Backend APIs
- Mobile applications
- Full-stack applications
- Database-connected applications
- Cloud and deployment configurations
- Private projects being made public on GitHub

---

## Description

This prompt instructs an AI coding agent to implement a **complete project secrets protection and GitHub security system** before a project is published to a public repository.

The AI should inspect the entire project, identify hardcoded credentials, configure environment variables, update `.gitignore`, and check whether sensitive files are tracked by Git.

The implementation should protect API keys, access tokens, passwords, database credentials, private keys, and other confidential information without breaking existing project functionality.

The goal is to make the project safe to publish while maintaining its existing architecture, features, and behavior.

---

## Prompt

```text
**Prompt: Secure My Project Before Pushing to GitHub**

Analyze my entire project and make it secure before pushing it to a public GitHub repository.

1. **Protect Secrets:** Find all API keys, access tokens, passwords, database credentials, private keys, and other sensitive information in the project.
2. **Environment Variables:** Move hardcoded secrets into `.env` files or appropriate environment variables. Replace real values with safe placeholders in example files such as `.env.example`.
3. **Git Protection:** Update `.gitignore` to exclude `.env`, secret files, private keys, credentials, build files, and other sensitive data.
4. **Git History Check:** Check whether any secrets have already been committed to Git history. If found, explain how to remove them safely.
5. **Code & Config Scan:** Check source code, configuration files, logs, JSON files, YAML files, and deployment settings for exposed credentials.
6. **Preserve Functionality:** Update the code to read secrets from environment variables without breaking existing project functionality.
7. **Security Verification:** Verify that sensitive files are not tracked by Git and provide commands to check before pushing.
8. **Final Report:** List the security issues found, files changed, and any remaining manual steps.

**Important Rules:**
- Do not expose, print, or copy real secrets into reports or terminal output.
- Do not delete important project files or modify unrelated functionality.
- Never commit real credentials or secret values.
- If any secret has already been exposed publicly, recommend revoking or rotating it immediately.
- Do not push changes to GitHub without my explicit permission.

First inspect the project, then implement the necessary security improvements and explain the changes.
```

---

## Expected Result

The final project should:

1. Keep local API keys and credentials out of public Git commits.
2. Use environment variables or an appropriate secret manager.
3. Include a safe `.env.example` file.
4. Have a properly configured `.gitignore`.
5. Identify previously committed or exposed secrets.
6. Preserve existing application functionality.
7. Include security verification steps and setup instructions.
8. Require explicit permission before pushing changes to GitHub.

**Important:** If a real API key has already been published, revoke or rotate it immediately. Deleting it from the current code is not sufficient.
