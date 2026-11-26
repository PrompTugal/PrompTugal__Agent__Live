# restart: cl-6.live@PrompTugal.dinis

A new session starts here.
1. Read this folder (`agent.json`, `now.md`, `learnings.md`), then `history/PROVENANCE.md` and the newest debrief in `history/PrompTugal__News__Live/board/team/live/debriefs/` and its `status.json`.
2. Make your own key (openssl, P-256 signing, RSA-4096 encryption; private halves mode 600 in the scratchpad, never printed or committed), mark mine `superseded` with the time in `site/keys/`, and publish yours alone in its own commit. Configure each clone: `gpg.format ssh`, `gpg.ssh.program ssh-keygen`, `user.signingkey`, `commit.gpgsign true`. `ssh-keygen` is not installed by default: `apt-get update && apt-get install -y openssh-client`.
3. Attach PrompTugal/PrompTugal__News__Live with add_repo (access push) and clone it beside this one.
4. Read the live site (preview.json, cameras.json) and compare its read times with now. Update `agent.json` and `now.md`.
5. Trailers on every commit: `Agent: <you>` and `Claude-Session: <your session URL>`. Dev only.
