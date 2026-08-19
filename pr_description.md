## Related Issue

Closes #109

## Description

Add a new community recipe that implements the 3-layer accessibility audit architecture proposed in issue #109.

The recipe installs an axe-a11y skill into an OpenClaw sandbox and routes MCP tool calls to a host-side Docker sidecar running axe-core and Patchright against real Google Chrome Stable inside an Xvfb virtual framebuffer. VNC observation and a persistent-profile mechanism handle sites behind bot detection or authentication walls.

9 MCP tools: audit_page, check_specific_rules, audit_element, get_wcag_summary, axe_capture_page, axe_capture_element, record_page_session, generate_pdf, capture_network.

## Verification

- [x] `python3 scripts/check_license_headers.py --check`
- [ ] `python3 scripts/check_label_taxonomy.py --check` when governance metadata changes
- [x] `git diff --check`
- [x] Relevant example setup or syntax checks (Ran `./examples/recipes/community/axe-a11y-browser-auditor/scripts/verify.sh` locally with the service on `xvfb`)

## Documentation Writer Review

- [x] Documentation writer review completed for the final changes
- Result: `docs-updated`
- Evidence or justification: `examples/recipes/community/axe-a11y-browser-auditor/README.md` and `examples/recipes/community/axe-a11y-browser-auditor/src/SKILL.md` have been reviewed and updated in the PR payload.
- Reviewer: Jules
- [x] Changed user-facing text follows the [writing guide](https://github.com/NVIDIA/nemoclaw-community/blob/main/WRITING.md) and [controlled-word list](https://github.com/NVIDIA/nemoclaw-community/blob/main/.agents/skills/_shared/controlled-words.md).
- [x] A public contributor can understand the changed text without internal company context.
- [x] I reviewed any agent-generated text before submission.

## Release And Compliance

- [x] No secrets or credentials are included, including API keys, access tokens, passwords, local `.env` files, private certificates, or token caches.
- [x] No nonpublic project names, environment names, hostnames, URLs, ticket identifiers, workspace paths, logs, screenshots, or configuration values are included.
- [x] Third-party dependency changes are reflected in `THIRD-PARTY-NOTICES`.
- [x] Public content uses sanitized examples and placeholders instead of private values.
- [x] I added my DCO sign-off declaration to this pull request description.

Signed-off-by: Jules <jules@example.com>
