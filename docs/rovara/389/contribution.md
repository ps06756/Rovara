# Contribution to #389

## Goal

Add one line to docs/rovara-e2e/fork.md saying the file was followed up by the rovara loop.

## Success criteria

- [x] docs/rovara-e2e/fork.md has a second line saying it was followed up by the rovara loop. — Evidence: `sed -n 2p docs/rovara-e2e/fork.md` prints `Followed up by the rovara loop.`; `wc -l` shows 2 lines; `git diff 0c4f7581 -- docs/rovara-e2e/fork.md` shows only that one added line (docs/rovara-e2e/fork.md:2).

## Approach

The file has one line today: `Fork base file for the rovara loop e2e test.`

- **Change:** append a second line, `Followed up by the rovara loop.`, directly after it. No blank line between them, so it is line 2 of the file. Nothing else changes.
- **Proof:** `sed -n 2p docs/rovara-e2e/fork.md` prints `Followed up by the rovara loop.`, `wc -l` shows 2 lines, and `git diff` against the PR branch shows that one added line and nothing else.
