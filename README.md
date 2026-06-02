# Sudeep26-ai301-contribution
# Contribution 1: Integration Testing Suite Configuration

**Contribution Number:** 1  
*Student:* Sudeep Reddy Thatiparthi  
*Issue:* [[GitHub issue link]  ](https://github.com/WH-93/tshirt-shop-api/issues/14)

*Status:* Phase I  - Complete

---

## Why I Chose This Issue

When developing high-performance software, unit tests only tell half the story. I chose this issue because mastering end-to-end integration testing against a real database is a critical skill for building reliable, production-ready backend architectures. Moving beyond mocked data to handle actual database state, migrations, and full request lifecycles will deepen my understanding of deterministic testing and API reliability, complementing my experience in building out comprehensive application features.

---

## Understanding the Issue

### Problem Description
Lets say that there is worker(The Controller / Handler) at a shirt shop and I go in and say "I want to buy a shirt. For the quantity, I want -5 shirts. And for the color, I want [DESTROY ALL SHIRTS]." and the worker will just type this in, Because the worker doesn't check if the order makes sense, they send that garbage data straight to the shop's computer system (the database). The computer gets confused by negative shirts and weird text, throws a massive error, and the whole store system crashes. 

In tech terms, the API currently takes whatever bad data a user sends it, gets confused, and breaks completely.

### Expected Behavior
The application should have a dedicated, isolated test database (`tshirt_shop_test`). Running a new npm script (`npm run test:integration`) should automatically run migrations, seed the database, execute at least 15 integration tests covering core user journeys, and completely clean up/teardown the state afterward. Tests must be repeatable without requiring manual database resets.

### Current Behavior
The codebase lacks a structured integration test suite, a dedicated testing database setup, and the necessary test helpers to manage database state and authenticated requests dynamically. 

### Affected Components
- `package.json` (Adding the `test:integration` script)
- `tests/helpers.ts` (New file for setup/teardown and auth helpers)
- `tests/integration/` (New directory containing the test suites)
- Database configuration (Provisioning `tshirt_shop_test`)
---

## Reproduction Process

### Environment Setup

[Notes on setting up your local development environment - challenges you faced, how you solved them]

### Steps to Reproduce

1. [Step 1]
2. [Step 2]
3. [Observed result]

### Reproduction Evidence

- **Commit showing reproduction:** [Link to commit in your fork]
- **Screenshots/logs:** [If applicable]
- **My findings:** [What you discovered during reproduction]

---

## Solution Approach

### Analysis

[Your analysis of the root cause - what's causing the issue?]

### Proposed Solution

[High-level description of your fix approach]

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** [Restate the problem]

**Match:** [What similar patterns/solutions exist in the codebase?]

**Plan:** [Step-by-step implementation plan]
1. [Modify file X to do Y]
2. [Add function Z]
3. [Update tests]

**Implement:** [Link to your branch/commits as you work]

**Review:** [Self-review checklist - does it follow the project's contribution guidelines?]

**Evaluate:** [How will you verify it works?]

---

## Testing Strategy

### Unit Tests

- [ ] Test case 1: [Description]
- [ ] Test case 2: [Description]
- [ ] Test case 3: [Description]

### Integration Tests

- [ ] Integration scenario 1
- [ ] Integration scenario 2

### Manual Testing

[What you tested manually and results]

---

## Implementation Notes

### Week [X] Progress

[What you built this week, challenges faced, decisions made]

### Week [Y] Progress

[Continue documenting as you work]

### Code Changes

- **Files modified:** [List]
- **Key commits:** [Links to important commits]
- **Approach decisions:** [Why you chose certain approaches]

---

## Pull Request

**PR Link:** [GitHub PR URL when submitted]

**PR Description:** [Draft or final PR description - much of the content above can be adapted]

**Maintainer Feedback:**
- [Date]: [Summary of feedback received]
- [Date]: [How you addressed it]

**Status:** [Awaiting review / Iterating / Approved / Merged]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]

### Challenges Overcome

[What was hard and how you solved it]

### What I'd Do Differently Next Time

[Reflection on your process]

---

## Resources Used

- [Link to helpful documentation]
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]
