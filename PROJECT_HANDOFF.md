# NAGA Content Review — AI Collaboration Handoff

## Project identity
- Existing application: **NAGA Content Review**.
- GitHub repository: `muayyadabughazaleh/naga-content-review`.
- Production hosting: Netlify (verify the linked site and production branch in Netlify before merging).
- Current repository entry point: `index.html` on `main`.
- **Do not rebuild the application.** Iterate on the existing UI, content, features and workflows.

## Core rules for Claude, ChatGPT, and Codex
1. **Sync first:** Read the latest `main` and this file before changing anything. Verify the uploaded/deployed version matches the expected baseline.
2. **Protect production:** Never push experiments directly to `main`. Use a new branch and open a pull request. Do not merge or publish without the owner's review.
3. **Preserve data and behavior:** Do not delete or reset existing posts, captions, stories, calendar entries, project content, approvals, accounts, configurations, or saved user data. Test state persistence and identify its storage mechanism before changing it.
4. **Small scoped changes:** Modify only the requested screens/features, avoid unrelated redesigns, and keep the existing NAGA visual identity, color palette and information architecture.
5. **Avoid duplicate UI:** Consolidate redundant widgets and actions while keeping the workflow easy and fast.
6. **Check existing features:** Before modifying, document what already works, what is a placeholder, and any dependencies or issues.
7. **Do not expose secrets:** Never commit credentials, tokens or private content. Treat internal company assets and user data as confidential.
8. **Always hand off:** After each work session update the status below (what changed, files, verification, limitations and next steps).
9. **Deploy safely:** If Netlify is connected to `main`, use preview deploys for pull requests and obtain approval before merging.

## Application areas to retain
Content Review / Calendar / Strategy / Upcoming / Dashboard / Reports / People & Access / Team Chat / Notifications / Activity / Archive.

## Important technical note
A standalone HTML exported from Claude can be a **bundled deployment artifact**, with code/assets embedded inside the file. This is not the same as the maintainable original source project. If Claude has source components, export them into a separate source structure *without replacing the deployed artifact* until independently verified. Do not assume that a successful HTML preview means persistence or cloud integrations work.

## Handoff log

### 2026-11-04 — Collaboration setup
- GitHub connection to ChatGPT confirmed.
- Repository metadata confirmed: default branch `main`; repository currently **public**; a standalone `index.html` is on `main`.
- User supplied a more recent `index.html` export in the conversation. The uploaded artifact contains an embedded asset manifest/template. **Its contents have not been deployed or committed by this setup.**
- Set up collaboration workflow on a separate branch; leave production code unchanged.
- Next: compare the latest user-supplied export against the currently deployed site and `main`, check sensitive content/history, then stage any verified update through a dedicated pull request.

## Session handoff template
- **Date / actor:**
- **Task / user request:**
- **Branch / PR:**
- **Files changed:**
- **Existing features preserved / regression check:**
- **Tests / preview URL:**
- **Known limitations:**
- **Next recommended action:**
