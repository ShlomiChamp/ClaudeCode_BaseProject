# MCP Integration Decisions

**Date:** 2025-11-04
**Project:** Mortgage Simulator (Full-Stack Web Application)

---

## Project Context

**Application Type:** Mortgage Simulator with interactive UI
**Architecture:**
- Backend: Calculation engine + API endpoints
- Frontend: Interactive charts, visualizations, scenario comparisons
- Database: User workspaces, saved scenarios, history
- Focus: Real-time calculations, dynamic UX, financial accuracy

---

## MCP Evaluation Summary

### ✅ **Approved: Playwright MCP**

**Status:** Recommended for installation
**Priority:** HIGH

**Reasoning:**
- Building web application with complex UI
- Financial calculations require accuracy validation
- Heavy use of charts and visualizations (core UX)
- Multi-step workflows (create → calculate → save → compare)
- Need E2E testing for frontend-backend integration

**Use Cases:**
- End-to-end testing of calculation flows
- Visual regression testing for charts/graphs
- Automated scenario comparison workflows
- Frontend-backend integration validation
- Cross-browser compatibility testing
- Screenshot debugging for UI issues

**When to Install:** Early in development phase (before frontend work begins)

**Installation:**
```bash
npm install -D @playwright/test
npx playwright install chromium
npm install @executeautomation/playwright-mcp-server
```

---

### ⏸️ **Deferred: Sequential Thinking MCP**

**Status:** Not installing now
**Priority:** MEDIUM (revisit later if needed)

**Reasoning:**
- Claude Code's TodoWrite tool handles task breakdown
- Built-in planning mode sufficient for current complexity
- Prefer to avoid redundant tooling
- Can add later if complex workflows become unmanageable

**Revisit When:**
- Complex multi-step calculations with missed steps
- Need auditable reasoning chains for financial logic
- Planning large refactoring projects

---

### ⏸️ **Deferred: mcp-language-server**

**Status:** Not installing now
**Priority:** MEDIUM (revisit for TypeScript backend)

**Reasoning:**
- Claude Code has strong built-in code understanding
- May add value for TypeScript/strongly-typed backend
- Wait to see if built-in capabilities are sufficient

**Revisit When:**
- Large TypeScript codebase with complex types
- Need precise type information for refactoring
- Working with heavy dependency trees

---

### ❌ **Rejected: Context7 MCP**

**Status:** Not installing
**Priority:** LOW

**Reasoning:**
- Memory/ folder provides structured context
- Claude Code's Explore agents handle context retrieval
- No external documentation sources to integrate
- Would add redundancy without clear value

**Alternative:** Continue using memory/ folder system

---

## Decision Philosophy

**Approach:** Start lean, add tools when specific needs emerge
**Criteria:**
- Avoid premature optimization
- Reduce configuration overhead
- Minimize token usage in context window
- Add MCPs only when clear value demonstrated

**Review Cadence:** Reassess MCP needs as project evolves

---

## Current MCP Status

**Installed:** None (base Claude Code capabilities only)
**Next Action:** Install Playwright MCP when frontend development begins
**Monitoring:** Track pain points that might justify additional MCPs

---

## Notes for Future AI Agents

- This project requires web UI testing → Playwright is essential
- Financial calculations demand accuracy → automated testing critical
- Charts/visualizations are core UX → visual regression needed
- Keep MCP stack minimal unless specific needs identified
- Document any new MCP decisions in this file
