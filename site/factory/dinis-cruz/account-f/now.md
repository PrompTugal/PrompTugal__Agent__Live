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
