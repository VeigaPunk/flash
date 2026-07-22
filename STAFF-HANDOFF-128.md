# Staff handoff — flash.comma.ai walkthrough (issue #128)

**Author:** [VeigaPunk](https://github.com/VeigaPunk)  
**Issue:** https://github.com/commaai/flash/issues/128  
**Date:** 2026-07-22

## Why this package (not a PR)

VeigaPunk is **GitHub-blocked** from interacting with `commaai/*` (fork POST 403, issue comments 403 `"Blocked"`). A normal fork → PR under this account is currently impossible. This repo is a **non-fork mirror** with the embed ready for staff cherry-pick / credit.

## Maintainer bar (from @adeebshihadeh, 2026-05-08 on #128)

> the deliverable is essentially just a YouTube upload, like the videos I originally linked. also note how the linked videos show an **actual device** going through the whole process.

Rejected class: screen-recording / TTS-only (see closed PR #201 discussion).

## What is ready (code)

| Item | Detail |
|------|--------|
| Embed | Landing “Watch walkthrough” → modal → `youtube-nocookie` iframe |
| Gate | `VITE_WALKTHROUGH_YOUTUBE_ID` — button hidden until real YT id is set |
| Branch | `veigapunk/walkthrough-yt` / commit with `feat: embed YouTube walkthrough` |
| Mirror | https://github.com/VeigaPunk/flash |
| Package | https://github.com/VeigaPunk/flash-bounty-128 |
| Gist | https://gist.github.com/VeigaPunk/095daab661527435e0c920cbc218b331 |

Cherry-pick path (once a real-device YouTube id exists):

```bash
# from commaai/flash
git remote add veigapunk https://github.com/VeigaPunk/flash.git
git fetch veigapunk
git cherry-pick <embed-commit-sha>
# set VITE_WALKTHROUGH_YOUTUBE_ID in deploy env (or bake at build time)
```

## What is NOT ready (honest)

| Gap | Why |
|-----|-----|
| Real-device footage | No comma three/3X/four + camera on this host |
| Public YouTube id | No channel OAuth; no device video to upload |
| Upstream PR from VeigaPunk | Account blocked on commaai org |

Storyboard-only MP4s in orch workspaces are **not** claimable under the real-device bar.

## Minimum acceptable capture spec (for whoever films)

1. Full device in frame for the whole flash (not only browser UI).
2. USB cable path visible; QDL entry (buttons) visible on device.
3. Browser URL bar shows `flash.comma.ai` (or staging) during the flow.
4. Continuous take preferred: connect → QDL → select device → flash → done.
5. Upload public (or unlisted) YouTube; set `VITE_WALKTHROUGH_YOUTUBE_ID=<id>`.
6. Reference quality: https://www.youtube.com/watch?v=NAz5NGnaDKs and https://www.youtube.com/watch?v=gNnRmEyVSVQ

## Unblock checklist

1. Comma / GitHub: remove VeigaPunk block on commaai → fork → PR closes #128.
2. Or staff cherry-pick embed + assign bounty credit when real-device YT is live.
3. Hardware: obtain device + film per spec above.

## Contact

- GitHub: VeigaPunk (cannot comment on commaai issues while blocked)
- Package maintainer email via GitHub profile if needed

