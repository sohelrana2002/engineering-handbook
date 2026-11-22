# Git & Version Control

A comprehensive guide to Git, GitHub, version control workflows, branching strategies, pull requests, code reviews, and collaboration best practices.

This section documents practical Git commands, team collaboration workflows, and recommended practices for maintaining clean, consistent, and maintainable project histories.

## Table of Contents

### 1. Git Fundamentals

- [Git Basics](fundamentals/git-basics.md)
- [Git Commands](fundamentals/git-commands.md)
- [Git Configuration](fundamentals/git-configuration.md)

### 2. Branching Strategy

- [Branching Strategy](branching/branching-strategy.md)
- [Branch Naming Convention](branching/branch-naming-convention.md)
- [Branch Protection Rules](branching/branch-protection-rules.md)
- [Branching Workflow](branching/branching-workflow.md)

### 3. Pull Requests & Code Reviews

- [Pull Request Guidelines](pull-requests/pull-request-guidelines.md)
- [Code Review Guidelines](pull-requests/code-review-guidelines.md)
- [Merge Strategies](pull-requests/merge-strategies.md)

### 4. Git Workflows

- [Feature Workflow](workflows/feature-workflow.md)
- [Bugfix Workflow](workflows/bugfix-workflow.md)
- [Hotfix Workflow](workflows/hotfix-workflow.md)

## Core Principles

- Use meaningful and consistent branch names.
- Keep commits small, focused, and descriptive.
- Never push directly to protected production branches.
- Use Pull Requests for code integration.
- Require code reviews before merging.
- Keep branches synchronized with their base branches.
- Resolve merge conflicts carefully.
- Maintain a clean and understandable Git history.

## Recommended Workflow

The recommended development workflow follows this integration process:

1. Create a feature or bugfix branch from `development`.
2. Implement changes and commit regularly.
3. Push the branch to the remote repository.
4. Open a Pull Request targeting `development`.
5. Review, test, and approve the changes.
6. Merge the Pull Request into `development`.
7. Once development is ready for release, open a Pull Request targeting `main`.
8. Complete the final review and merge into `main`.

## Documentation Goals

This documentation aims to:

- Establish consistent Git practices.
- Standardize team collaboration workflows.
- Improve code review and integration processes.
- Reduce unnecessary merge conflicts.
- Maintain a reliable and traceable project history.

---

**Parent Documentation:** [Engineering Handbook](../README.md)
