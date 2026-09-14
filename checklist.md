# Project Checklist

## 1. Project Context

- Personal-use fitness tracking web application.
- Planned areas may include workout planning, logging, progression, body data, nutrition and analytics.
- Xunji integration is intended.
- Official Xunji plans are read-only through the available interface.
- Agent templates and training/body/food records may only be changed through preview and explicit user-confirmation workflows.
- The project uses separate Reviewer and Implement Agent roles.
- Hosting and application implementation are not part of the current task.

## 2. Current Milestone

Complete the move to `/Users/nateguo/Documents/projects/fitness-tracker`, commit the privacy-safe public documentation, and verify the private GitHub repository.

## 3. Source of Truth

1. Latest user or Reviewer requirement.
2. Existing project architecture and conventions.
3. This checklist for durable requirement, decision, issue and handoff context.
4. `健身计划.md` remains a local private reference and is not committed.

## 4. Privacy Boundaries

- Never record authentication values, API keys, complete authorization headers, `.env` values or client secrets here.
- Never copy detailed workout history, body measurements, food records or private content from `健身计划.md` here.
- Xunji Skill files and personal fitness data are local-only and ignored by Git.
- Keep verification output to filenames, statuses and summaries; never print secret values.

## 5. Requirements Ledger

### REQ-001 — Documentation and privacy-safe repository initialisation

- **Summary:** Organise documentation and initialise a privacy-safe private GitHub repository.
- **Status:** IN_PROGRESS
- **Acceptance criteria:** AC-01 through AC-12 in the implementation task.
- **Implementation summary:** Removed four verified root-level duplicate Markdown copies; added privacy-safe README, checklist, and Git ignore rules; amended Reviewer and Implementer checklist responsibilities. The complete project was moved to `/Users/nateguo/Documents/projects/fitness-tracker`, where `main` tracks the intended `origin/main`; the five public project documents still need to be committed and pushed from the new repository.
- **Review status:** CHANGES REQUIRED — correction in progress after the project-directory move explained the apparent missing-file findings.
- **Relevant files:** `README.md`, `checklist.md`, `reviewer.md`, `implementer.md`, `.gitignore`, four `xunji-*` Skill directories, `健身计划.md`.
- **Next action:** Commit the five privacy-safe public documents in the new repository, verify repository privacy and ignored files, push `main`, then perform independent review.

## 6. Active Task Checklist

- [x] Re-read `implementer.md` and apply Ponytail full constraints.
- [x] Verify all four duplicate pairs byte-for-byte.
- [x] Remove only verified root-level duplicate Markdown files.
- [x] Create privacy-safe `README.md`, `checklist.md`, and `.gitignore`.
- [x] Amend `reviewer.md` with checklist responsibilities.
- [x] Amend `implementer.md` with checklist responsibilities.
- [x] Initialise Git with `main`.
- [x] Stage only intended public files.
- [x] Verify ignored and untracked private paths.
- [x] Scan staged content for credential indicators without printing matches.
- [x] Commit with the required message.
- [x] Move the complete project to `/Users/nateguo/Documents/projects/fitness-tracker`.
- [x] Confirm the intended `fitness-tracker` remote and `origin/main` upstream in the new repository.
- [x] Confirm the four Xunji Skills and `健身计划.md` are present and ignored in the new repository.
- [ ] Commit the five public project documents in the new repository.
- [ ] Verify private GitHub visibility and push `main`.

## 7. Decision Log

| ID | Decision | Reason | Date |
| --- | --- | --- | --- |
| DEC-001 | Canonical Xunji copies remain under the four `xunji-*` directories. | These are the required skill locations; root Markdown copies are exact duplicates. | 2026-09-14 |
| DEC-002 | `健身计划.md` and all Xunji Skill directories remain local-only. | They contain private fitness information and/or credentials. | 2026-09-14 |
| DEC-003 | The GitHub repository name is `fitness-tracker` and visibility must be private. | Explicit project requirement. | 2026-09-14 |
| DEC-004 | `/Users/nateguo/Documents/projects/fitness-tracker` is the canonical project working directory. | The user moved the complete project there; future work must not use the old Downloads path. | 2026-09-14 |

## 8. Discovered Issues

| ID | Status | Description | Impact / next action |
| --- | --- | --- | --- |
| ISS-001 | OPEN | GitHub CLI is not installed, but the new repository has the intended GitHub remote and upstream through another workflow. | Verify repository visibility through an authenticated or independently reliable method before closing. |
| ISS-002 | RESOLVED | The independent review temporarily observed missing private files after they were moved out of the old Downloads directory. | All four Xunji Skills and `健身计划.md` were found in the canonical Documents project directory with the previously observed sizes. |
| ISS-003 | RESOLVED | The independent review temporarily observed deleted tracked documentation in the old Git working tree. | All five public project documents were found in the canonical Documents project directory and match the original commit blobs exactly. |
| ISS-004 | RESOLVED | The old Downloads Git directory contained an unexpected remote. | The canonical Documents repository uses the intended `Player0124/fitness-tracker` remote; the old directory will not be used or pushed. |

## 9. Verification Log

| Check | Result | Evidence |
| --- | --- | --- |
| Duplicate comparisons | PASS | All four specified pairs were byte-for-byte identical before deletion. |
| Duplicate deletion | PASS | Only `训练.md`, `身体.md`, `饮食.md`, and `模板.md` were removed. |
| Remaining Skill files | PASS | Four canonical paths and hashes recorded before commit; `健身计划.md` hash also recorded. |
| Git privacy and credential scan | PASS | All private paths ignored/untracked; staged credential scan returned no filenames; whitespace check passed after cleanup. |
| Local Git initialisation and staging | PASS | `main` initialised and five intended public files staged. |
| GitHub CLI/authentication | BLOCKED | `gh` is not installed; remote operation stopped before any mutation. |
| Local commit | PASS | Created with message `chore: organize project documentation`. |
| Git status and branch | PASS | Clean working tree on `main` after the local commit. |
| GitHub visibility and upstream | BLOCKED | No remote or upstream exists because the authenticated GitHub workflow is unavailable. |
| Project-directory migration | PASS | All public and private project files are present in the canonical Documents directory; public files match their original commit blobs. |
| Canonical repository remote | PASS | New repository `main` tracks `origin/main` at the intended `fitness-tracker` remote. |
| New repository public-file credential scan | PASS | The public documentation and Git configuration files returned no credential-pattern filenames. |

## 10. Deferred / Optional Work

- Implementing the web application.
- Hosting or deployment.
- Installing the local Skill directories globally for other projects.
- Adding `.env.example` (not needed until an application configuration exists).

## 11. Handoff / Next Action

The Documents project directory is now canonical and contains all required files. Commit the five public documents, verify the repository is private, push `main`, and then have the Reviewer independently re-run AC-01 through AC-12. Do not use or push the old Downloads Git directory.
