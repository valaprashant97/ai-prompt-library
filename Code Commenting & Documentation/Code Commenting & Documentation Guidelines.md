📝 Clean Code & Documentation Standard : 

Core Rule: Code should explain what it does; comments should explain why it does it. Clean code always comes before comments.

💡 1. When to Write Comments :
💡 Explain the 'Why', Not the 'What': Clarify the business reasoning, architectural decisions, or intent behind the code.
🧠 Complex Business Logic: Document intricate domain rules, non-obvious calculations, and multi-step algorithms.
🛡️ Edge Cases & Guardrails: Highlight critical boundary conditions, potential race conditions, or specific fail-safes.
🔧 Framework & Platform Workarounds: Document temporary hacks or workarounds required due to browser, API, or third-party library limitations (include issue link if possible).
📑 Public APIs & Shared Modules: Provide clear JSDoc / Docstrings for exposed classes, utilities, and reusable components.

🚫 2. When NOT to Write Comments :
🙅‍♂️ Self-Explanatory Code: Never state the obvious. If variable and function names are descriptive, skip the comment.
🧹 Bad Code Cover-up: Don't use comments to explain messy code. Refactor the code first.
🔊 Code Noise: Avoid over-commenting every single line; excessive text bloat reduces overall readability.
🧪 Leftover Debugging: Remove temporary console.log, print, or debug comments before raising a Pull Request.

🔄 3. Maintenance & Best Practices :
⚡ Keep Comments Fresh: Always update the associated comments when refactoring or modifying logic. Outdated comments are worse than no comments.
🎯 Be Concise: Keep explanations brief, clear, and straight to the point.
🏷️ Clean Up Technical Debt: Track actionable tasks using standard markers (TODO:, FIXME:) with context, but clean them up before hitting production.
🎨 Consistent Formatting: Stick to standard commenting formats across the repository (e.g., JSDoc, Docstrings, or standardized single-line headers).

🔍 Quick Examples (Do vs Don't) :

❌ BAD (Redundant & Obvious) :
javascript
// Check if user age is 18 or above
if (user.age >= 18) { // Set isAdult to true
    isAdult = true; 
}

✅ GOOD (Clear Intent & Context) :
javascript
// Region-specific compliance: Users under 18 in EU require parental approval 
// due to GDPR Article 8 restrictions.
const requiresParentalConsent = user.isEU && user.age < 18;

🎯 Summary Checklist for PR Reviews :
[ ] Can the code be simplified to eliminate the need for this comment?
[ ] Does this comment explain why this approach was taken?
[ ] Are public functions/APIs documented with parameters and return types?
[ ] Have all temporary debug statements been removed?

THAT'S IT!
