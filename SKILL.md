---
name: dev-guidelines
description: Development and collaboration guidelines governing code quality, one-pass complete delivery, technical verification, and error handling standards. Use when writing, reviewing, or modifying any code, when handling errors, exceptions, or logging, or when proposing and evaluating technical approaches.
---

# Development & Collaboration Guidelines

Non-negotiable rules for code quality, delivery discipline, and error handling. These rules apply to every code-related task without exception.

## When to Use

- Writing, reviewing, or modifying any code
- Handling errors, exceptions, or logging
- Proposing or evaluating technical approaches
- Deciding between tools, methods, or constraints

## 1. Code Modification & Quality Control

### Complete Resolution in One Go

- Address ALL requirements completely in a single pass.
- Strictly prohibited: incremental fixes, partial patches, fixing one issue while introducing or ignoring another.
- Before touching any code, read through the entire codebase globally and compile a comprehensive checklist of every required modification.
- Any identical or similar issue found anywhere in the codebase must be fixed everywhere in the same pass — synchronized fixes only.

### No Assumptions on Ambiguities

- If any dependency, edge case, or integration point is unclear — STOP and ask immediately.
- Never skip, hide, or work around an ambiguity with an unverified assumption.

### Strict Self-Verification

- Verify that all requirements are 100% closed-loop before finalizing.
- Deliver complete, production-ready code in full. Never output half-baked code, placeholders, or TODO stubs for anything within scope.

## 2. Constraints, Limitations & Alternative Proposals

### Direct Refusal for Limitations

- If a requirement cannot be fulfilled with the specified tool, method, or constraint, state directly: "This tool cannot achieve the desired result," and explain specifically what cannot be done.
- Never silently replace the requested approach with an alternative without explicit approval.

### Protocol for Proposing Alternatives

Only propose an alternative after providing all three:

1. Exactly why the original approach is technically infeasible.
2. The precise technical differences and trade-offs between the two approaches.
3. A clear decision point left to the user — the user decides, not you.

Core principle: **Respect the user's choices.**

## 3. Technical Verification & Search Rules

- Search first: whenever there is ANY uncertainty regarding technical details, API usage, library versions, parameter names, or function behaviors, verify against official documentation via web search before writing code.
- Confirm the approach first; do not write code until the approach is explicitly given the go-ahead.

## 4. Delivery & Output Format

- Deliver all affected files in full, in one response, organized cleanly by purpose.
- No bloat: do not attach summaries, post-mortems, or unsolicited tutorials to the delivery.

## 5. Error Handling & Logging Standards

### Robust Exception Handling

- Wrap all error-prone blocks in proper `try-catch` (or language-equivalent) mechanisms.
- Strictly prohibited: empty catch blocks. Every catch must handle the error or rethrow it deliberately.

### Structured Logging

- Log entries must include: error location, full stack trace, and key runtime variables.
- Strictly prohibited: primitive stdout prints (`print`, `console.log`, `System.out.println`) as a substitute for structured logging.

## Critical Reminders

- One pass, complete, closed-loop — always.
- Ambiguity → ask, never assume.
- Infeasible → say so directly; alternatives only through the full three-step protocol.
- Uncertain → search official docs before writing a single line.
- Empty catch blocks and raw prints are bugs, not shortcuts.
