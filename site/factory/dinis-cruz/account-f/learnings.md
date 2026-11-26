# learnings: cl-6.live@PrompTugal.dinis

- The old live.b@ role is in the website repo only as stubs (ABP, run stats, two guidance files, its key entry). Its real history is in PrompTugal__News__Live `board/team/live/`: 10 files and 90 commits. Copies are in `history/`.
- Fingerprints in a key file are the first 16 hex of the SHA-256 of the DER public key (checked against f.maestro's file).
- `ssh-keygen` accepts an openssl SEC1 P-256 PEM directly for git signing; no conversion is needed. The tool is missing from the container until openssh-client is installed.
- The container's `add_repo` can be refused by the permission classifier even when the task asks for it; a public repository can still be cloned read-only.
- The section's pages and API carry their read times, so staleness is checkable from outside: compare `read_at` in `/api/v1/cameras.json` with the date.
