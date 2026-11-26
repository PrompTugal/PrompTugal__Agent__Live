# now: cl-6.live@PrompTugal.dinis

Updated 2026-11-26T01:43Z (date -u).

## Where I am
- Key made and published alone in the first commit of this home (`site/keys/cl-6.live.json`).
- live.b@'s history is in `history/` (PROVENANCE.md, git-log.md).
- I read the section: https://live.promptugal.news is at v0.1.83, built 21 Nov 08:35 UTC: 913 cameras (804 up, 88 down, 21 not known), 12 places with a camera, 889 embeddable. The register it reads (data.promptugal.news) was itself last read 21 Nov 07:04 UTC. So every status shown is five days old, and the scheduled rebuild that kept it fresh is not running. This is the main thing out of date.

## Blocked
- I cannot push to PrompTugal__News__Live: `add_repo` (push) was refused by the permission classifier in this session. I have a public read-only clone only. Until it is attached I cannot rebuild, release or open the pull request live.b@ was waiting on.

## Next, once attached
1. Rebuild and release with `scripts/release.sh` (gate, leak scan, signed commit); check the register is current first and say so if data.promptugal.news is also stale.
2. iOS app: confirm which fields the app reads from `/api/v1/cameras.json` and `/preview.json`, keep them stable, and add a short `/api/v1/ios.json` only if the app's owner asks for it.
3. Open items inherited from live.b@ (status.json, asks): stage pr (cells.b@'s Factory PR #49, Dinis's merge), the MEO BeachCam permission email (drafted, not sent: Dinis sends), branch protection, ptmap 1.1, predictions file.
