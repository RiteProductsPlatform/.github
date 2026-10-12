## PR Summary — Merge to SIT

**Application / Module:** <!-- e.g., TimeRite, CrewRite, OnboardRite, EquipRite, PraRite -->
**Ticket / Story ID(s):** <!-- link -->
**Developer:** 
**Target Branch:** sit
**Type of Change:** ☐ Feature ☐ Bug Fix ☐ Enhancement ☐ Hotfix ☐ Config Only ☐ Refactor

### 1. What changed and why
<!-- 2–4 lines: business purpose + technical summary -->

### 2. Components impacted
| Layer | Object / File | Change (New / Modified / Deleted) |
|---|---|---|
| DB (Tables / Packages / Views) | | |
| ORDS (Modules / Handlers) | | |
| VBCS (Pages / Flows / Service Connections) | | |
| OIC / Fusion Integration | | |
| Config / Metadata | | |
| Security / Roles | | |

### 3. Deployment notes
- [ ] DB scripts are attached, in run order, and re-runnable (idempotent)
- [ ] Rollback script is included
- [ ] No hard-coded environment values (URLs, credentials, instance names)
- [ ] Environment-specific config for SIT is listed below
- [ ] Dependencies on other PRs or deployments: <!-- list or "None" -->

**SIT config / manual steps:**
<!-- e.g., lookup values, profile options, role mappings -->

---

## Self-Review Checklist

### Code quality
- [ ] Code follows team naming and coding standards
- [ ] No commented-out or dead code, and no debug logs / console.log left behind
- [ ] Error handling and logging are in place (DB exceptions, REST error responses)
- [ ] No duplicate logic; reusable components and framework patterns are used
- [ ] Merge conflicts resolved, and the branch is rebased on the latest `sit`

### Functional testing (done in DEV)
- [ ] Unit-tested every scenario in the ticket
- [ ] Positive, negative, and edge cases tested
- [ ] Existing functionality still works (regression check on impacted areas)
- [ ] UI checked for validations, messages, and responsiveness (VBCS)
- [ ] Tested with the correct user roles / personas

### Security & compliance
- [ ] No secrets, passwords, or tokens in code or config
- [ ] Authorization enforced (Fusion roles / app roles); no bypass of access checks
- [ ] Input validated; SQL uses bind variables (no dynamic SQL concatenation)
- [ ] PII / sensitive data is not logged or exposed in REST responses
- [ ] Audit columns (CREATED_BY, LAST_UPDATED_BY, dates) populated where applicable

### Performance
- [ ] Queries reviewed for indexes / full table scans on large tables
- [ ] Pagination used for list APIs / tables
- [ ] No unnecessary REST calls on page load

### Documentation
- [ ] Ticket updated with technical notes
- [ ] API contract / data model changes documented
- [ ] Release notes entry added

---

## Test Evidence
<!-- Attach screenshots, Postman results, or a short recording -->
| Scenario | Expected | Actual | Result |
|---|---|---|---|
| | | | ☐ Pass ☐ Fail |

## Known Issues / Risks
<!-- Anything reviewers or QA should know. Write "None" if none. -->

---

## Self-Approval Declaration
I confirm that:
- I have reviewed my own code against the checklist above,
- all applicable items are checked, and any unchecked item is explained below,
- the changes have been tested in DEV and are ready for SIT,
- I understand that this PR may be rejected if the checklist is incomplete or inaccurate.

**Unchecked items / justification:** 
**Developer Name:** 
**Date:** 

---

## Reviewer / Lead Approval *(filled by reviewer)*
- [ ] Self-review checklist verified
- [ ] Deployment and rollback steps are clear
- **Decision:** ☐ Approved for SIT ☐ Changes Requested
- **Reviewer:** 
- **Date:** 
- **Comments:** 
