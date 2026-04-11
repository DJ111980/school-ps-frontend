# Frontend - School PS

Welcome to the School PS Frontend repository. This is a clearance management system for schools to track student accounts and payment status. This document outlines our development standards and conventions to maintain consistency and clarity across the project.

## 🚀 Project Overview

This is the frontend application for the School PS clearance system. We follow strict naming conventions, commit standards, and branch protection rules to ensure maintainability, stability, and secure collaboration.

---

## 📋 Naming Conventions

### **⚠️ IMPORTANT: Team Members - Follow These Standards from Day One**

To maintain a clean and organized repository, all team members **MUST** adhere to the following naming conventions:

### 1. **Branch Names**

Use descriptive branch names with the following format:

```
{type}/{kebab-case-description}
```

**Examples:**

- `feature/student-clearance-system`
- `feature/payment-status-dashboard`
- `fix/clearance-calculation-error`
- `fix/student-balance-display`
- `hotfix/payment-processing-timeout`
- `refactor/clearance-validation-logic`
- `docs/clearance-api-documentation`
- `test/payment-verification-tests`

**Types:**

- `feature/` - New features or functionality
- `fix/` - Bug fixes
- `hotfix/` - Urgent fixes for production
- `refactor/` - Code refactoring without changing functionality
- `docs/` - Documentation updates
- `test/` - Test additions or improvements

---

### 2. **Pull Request Titles**

Use the following format for PR titles:

```
{type}: {imperative-tense-description}
```

**Examples:**

- `feat: add student clearance verification system`
- `feat: implement payment status dashboard`
- `fix: correct clearance calculation for partial payments`
- `fix: resolve student balance display error`
- `refactor: simplify payment validation logic`
- `docs: update clearance workflow documentation`
- `test: add unit tests for payment processing`

**Accepted Types:**

- `feat:` - New feature
- `fix:` - Bug fix
- `refactor:` - Code refactoring
- `docs:` - Documentation
- `test:` - Test additions or modifications
- `chore:` - Maintenance tasks
- `style:` - Code style changes (formatting, missing semicolons, etc.)

---

### 2.5 **Pull Request Template**

The PR template is managed in `.github/pull_request_template.md`. When you create a new PR, the template will be automatically populated with the required sections:

- **Description** - Explain what this PR does and why
- **Type of Change** - Select the appropriate change type
- **Related Issues** - Reference any related issues (e.g., `Fixes #123`)
- **Testing** - Describe how you tested your changes
- **Screenshots** - Add UI screenshots before/after (if applicable for UI changes)
- **Checklist** - Verify all items before requesting review

---

### 3. **Commit Messages**

Commits should be concise and follow this format:

```
{type}: {short description}
```

**Examples:**

- `feat: add JWT authentication for student portal`
- `fix: correct clearance status validation`
- `refactor: optimize payment verification component`
- `docs: add student dashboard documentation`
- `test: add integration tests for clearance module`
- `chore: update dependencies`
- `style: format code with prettier`

**Rules:**

- Keep the description under 50 characters when possible
- Use imperative mood (add, fix, update, not adds, fixed, updated)
- Capitalize the first letter after the type
- No period at the end

---

## 🔐 Branch Protection & PR Workflow

### **Critical Rules for All Developers**

⚠️ **ALL PULL REQUESTS MUST:**

1. **Target the `develop` branch only**
   - PRs to `main`, `master`, or other branches will be rejected
   - The `develop` branch is the integration branch for all changes
   - Only authorized team leads can merge to `main`

2. **Pass all required checks before merging:**
   - ✅ All CI/CD tests must pass
   - ✅ Code coverage requirements must be met
   - ✅ Linting and formatting checks must pass
   - ✅ At least 2 code review approvals required
   - ✅ No merge conflicts allowed
   - ✅ All branch conversations must be resolved

3. **Protected Branches:**
   - `main` - Production branch (protected, no direct commits)
   - `develop` - Integration branch (protected, requires PR and approvals)
   - All `feature/*` branches are protected
   - All `fix/*` branches are protected
   - All `hotfix/*` branches are protected

---

## 📚 Best Practices

1. **Atomic Commits**: Each commit should represent a single logical change
2. **Frequent Commits**: Commit often, push regularly
3. **Meaningful Messages**: Write clear, descriptive messages that explain the "why"
4. **Link Issues**: Reference issue numbers when applicable (e.g., `fix: resolve #123`)
5. **Code Review**: All PRs must be reviewed by at least 2 team members before merging
6. **Keep PRs Small**: Smaller PRs are easier to review and merge faster

---

## 🔄 Workflow Example

```bash
# 1. Create a feature branch from develop
git checkout develop
git pull origin develop
git checkout -b feature/add-payment-notifications

# 2. Make changes and commit with proper messages
git commit -m "feat: add payment notification system"
git commit -m "feat: implement email notifications for payments"
git commit -m "test: add tests for notification service"

# 3. Push to remote
git push origin feature/add-payment-notifications

# 4. Create PR to develop branch with title:
#    "feat: add payment notification system"
#    Include description, related issues, testing info

# 5. Wait for all checks to pass and get 2+ approvals

# 6. Merge the PR (will be auto-deleted after merge)

# 7. Delete local branch
git branch -d feature/add-payment-notifications
```

---

## 🛠️ Getting Started

### Prerequisites

- Node.js (v22 or higher)
- npm or yarn
- Git

### Installation

```bash
# Clone the repository
git clone <respository-url> frontend
cd frontend

# Install dependencies
npm install

```

### Development

```bash
# Start development server
npm run dev
```

### Build

```bash
npm run build
```

### Testing

```bash
npm run test
npm run test:coverage
```

### Linting & Formatting

```bash
npm run lint
npm run format
```

---

## 📋 PR Checklist Before Submitting

Before creating a pull request, ensure:

- [ ] Your branch is based on the latest `develop`
- [ ] All tests pass locally: `npm run test`
- [ ] Linting passes: `npm run lint`
- [ ] Code is formatted: `npm run format`
- [ ] Commits follow conventional format
- [ ] PR title follows naming conventions
- [ ] PR description is clear and references issues
- [ ] No merge conflicts
- [ ] No breaking changes (or documented if necessary)
- [ ] Screenshots/videos included (if UI changes)

---

## 🚫 What NOT to Do

❌ **DON'T:**

- Commit directly to `main` or `develop`
- Create PRs to branches other than `develop`
- Skip the code review process
- Merge your own PR without approvals
- Force push to protected branches
- Create commits with unclear messages
- Mix unrelated changes in one PR
- Ignore failing tests or CI checks

---

## 🔒 Protected Branches Explanation

All branches in this repository are protected to ensure code quality and prevent accidental overwrites:

| Branch      | Protection Level | Who Can Merge              |
| ----------- | ---------------- | -------------------------- |
| `main`      | Maximum          | Project Lead Only          |
| `develop`   | High             | Lead Dev + 2 Approvals     |
| `feature/*` | Standard         | Lead Dev + 2 Approvals     |
| `fix/*`     | Standard         | Lead Dev + 2 Approvals     |
| `hotfix/*`  | Maximum          | Project Lead + 2 Approvals |

---

## 📝 Notes for Team Members

- **Consistency is key**: These conventions apply to **ALL** branches, PRs, and commits
- **No exceptions**: Even small fixes must follow these standards
- **Always use develop**: Your PRs **MUST** target the `develop` branch
- **Passing checks required**: No PR will be merged if checks fail
- **Ask questions**: If unsure about naming or workflow, ask the team lead before pushing

---

## 🔍 Code Review Expectations

When reviewing PRs:

1. Check branch and commit naming conventions
2. Verify all checks pass
3. Review code quality and functionality
4. Ask questions if unclear
5. Approve or request changes
6. Do not approve your own PR

---

## 👥 Team Internal Rules

**These are human rules that complement GitHub's technical protections. GitHub enforces what it can, but team discipline ensures what it can't.**

### Core Team Agreements:

1. **🚫 No one commits directly to `main`**
   - This is absolute. Even if you think you're a maintainer, use a PR
   - Direct commits to `main` may be rejected or reverted

2. **👥 No self-merges - Peer review is mandatory**
   - You **CANNOT** approve and merge your own PR
   - Your PR must be approved by at least one other team member
   - If your team agrees on mandatory cross-review, then EVERYONE needs approval from someone else
   - This ensures fresh eyes on every change

3. **🎫 Every change must come from an issue or task**
   - Before creating a branch, verify there's a corresponding issue/ticket
   - Reference it in your PR title or description: `fix: resolve #45`
   - This maintains traceability and context for future developers

4. **📦 Every PR should be small and focused**
   - One logical intention per PR
   - Easier to review, test, and revert if needed
   - Target: Keep PRs under 400 lines of code changes

5. **🔪 If a PR exceeds the size limit, split it**
   - Large PRs take longer to review and are harder to understand
   - Split into multiple smaller PRs targeting logical features
   - Example: Instead of "feat: complete payment system", split into:
     - `feat: add payment models`
     - `feat: add payment validation logic`
     - `feat: add payment endpoints`

6. **⚔️ If there are conflicts, the PR author resolves them**
   - It's the author's responsibility to keep their branch updated
   - Before requesting merge, update your branch with `develop`
   - Fix conflicts yourself before asking for review
   - This prevents bottlenecks and keeps the process flowing

7. **👀 Reviewers must actually validate the code**
   - **Don't approve "blindly"** - this defeats the purpose of code review
   - Reviewers should:
     - ✅ Read and understand the code
     - ✅ Run tests locally (when possible)
     - ✅ Verify the changes work as intended
     - ✅ Check for security issues
     - ✅ Ask questions if anything is unclear
   - Approval is a professional commitment, not a checkbox

---

## 🤝 Conflict Prevention & Resolution

**Conflicts are reduced dramatically with discipline and coordination. Here's how to minimize and handle them:**

### Prevention Strategy:

**1. Keep branches short-lived**

- Features should be completed and merged within 1-3 days
- The longer a branch exists, the more likely conflicts arise
- Quick, frequent merges to `develop` reduce integration problems

**2. Always work from the latest `develop`**

- Before starting a branch: `git pull origin develop`
- Before requesting merge: `git pull origin develop` (again)
- Before merging: Ensure your branch is up-to-date
- GitHub can enforce this rule, but manual discipline helps too

**3. Don't leave branches open for days**

- Abandoned branches cause stale PRs
- If you need to pause, communicate it in the PR
- Other developers shouldn't have to wait for your branch

**4. Coordinate if working on related modules**

- If two team members will work on the same file/module, discuss it first via an issue
- Assign tasks clearly in your issue tracker
- Prevent overlapping work before it happens
- Example:
  - Dev A: "I'm doing payment validation logic"
  - Dev B: "I'll do payment endpoint routing"
  - Agreed: Coordinate via PR before merge

### GitHub's Enforcement:

- ✅ **Require branches to be up-to-date before merge** - GitHub setting enabled
- ✅ **This automatically detects conflicts** before entering `develop`
- ✅ **Force push disabled** - Prevents accidental history rewrites

### Handling Conflicts When They Occur:

1. **Author receives a conflict notification**

   ```bash
   # Update your branch
   git fetch origin
   git merge origin/develop

   # Manually resolve conflicts (editor will show them)
   # Then commit the merge
   git add .
   git commit -m "merge: resolve conflicts with develop"
   git push origin feature/your-feature
   ```

2. **Review the conflict carefully**
   - Don't just delete code blindly
   - Understand what changed in `develop` vs your branch
   - Test after resolving to ensure nothing broke

3. **Re-request review**
   - Add a comment: "Conflicts resolved, ready for re-review"
   - Wait for approval again if needed

### Quick Conflict Prevention Checklist:

Before pushing your code:

- [ ] My branch is based on the **latest `develop`**
- [ ] I've pulled `develop` today: `git pull origin develop`
- [ ] No one else is working on my same files (coordinated)
- [ ] My branch is less than 3 days old
- [ ] My PR is small and focused (< 400 lines)
- [ ] I've resolved any local merge conflicts
- [ ] I'm not trying to merge directly to `main`
- [ ] Someone else will review this (not self-merge)
- [ ] There's an issue/task backing this change

---

## 📞 Support

For questions or clarifications about these conventions or the branch protection rules, please reach out to the project lead or team.

---

**Last Updated:** 2026
**Repository:** School PS Frontend
**Status:** Production
