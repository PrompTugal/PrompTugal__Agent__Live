# now: cl-6.live@PrompTugal.dinis

Updated 2026-11-26T01:43Z (date -u).

## Where I am
- Key made and published alone in the first commit of this home (`site/keys/cl-6.live.json`).
- live.b@'s history is in `history/` (PROVENANCE.md, git-log.md).
- I read the section: https://live.promptugal.news is at v0.1.83, built 21 Nov 08:35 UTC: 913 cameras (804 up, 88 down, 21 not known), 12 places with a camera, 889 embeddable. The register it reads (data.promptugal.news) was itself last read 21 Nov 07:04 UTC. So every status shown is five days old, and the scheduled rebuild that kept it fresh is not running. This is the main thing out of date.

## Blocked
- PrompTugal__News__Live is attached with push and cloned (dev at 6334ebd). I have pushed nothing, because its gate would refuse my commits: `scripts/check-signatures.mjs` takes keys only from the parent commit's `team/keys.json`, only Ed25519, and the only key there is live.b@'s (its session ended). My key is P-256 and not listed, and the commit that lists it would itself need a listed key. The gate also refuses shallow clones. I will not weaken a check; Dinis or security@ decides how a cl-6 key gets in.

## Next, once attached
1. Rebuild and release with `scripts/release.sh` (gate, leak scan, signed commit); check the register is current first and say so if data.promptugal.news is also stale.
2. iOS app: confirm which fields the app reads from `/api/v1/cameras.json` and `/preview.json`, keep them stable, and add a short `/api/v1/ios.json` only if the app's owner asks for it.
3. Open items inherited from live.b@ (status.json, asks): stage pr (cells.b@'s Factory PR #49, Dinis's merge), the MEO BeachCam permission email (drafted, not sent: Dinis sends), branch protection, ptmap 1.1, predictions file.

## Pass of 2026-11-26T02:36Z (everything in the area up to date as of 26 Nov 2026)
- The section is not stale because of this repository: a local build of News__Live `dev` works and reads 913 cameras with none skipped. It is stale because its source, data.promptugal.news's camera register, was last read on 21 Nov at 07:04 UTC (its `read_at`). A release now would only re-stamp the same 21 Nov data, so I have not prepared one. Data agent: please refresh the register; then one release here updates the site.
- I added nothing from other sources: I may not invent a camera status, and the register is the only source the section reads.
- Blocked and unchanged: signing in News__Live (see above); I will ship the rebuild the moment a key route exists, after cl-6.security has seen it.

## Key PR (2026-11-26T02:38Z)
- ssh-ed25519 key made; its public line is `ssh_ed25519` in `site/keys/cl-6.live.json` (db9e55c).
- The key PR is committed locally, signed with that key, on branch `key/cl-6.live` in the News__Live clone (22 added, 2 removed lines in `team/keys.json`: my entry, and live.b@'s marked superseded). The leak scan passes. It is not pushed: pushing a branch is outside dev-only until the process is live, and the exact `pages.yml` block is in IaC's `policy/key-bootstrap.json`, which is not merged yet (404 at 2026-11-26T02:38Z).
- When it is: add that block byte for byte, push the branch, open the PR, send the link to cl-6.security.
