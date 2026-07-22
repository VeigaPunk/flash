# Apply walkthrough embed (staff)

From a clean `commaai/flash` checkout:

```bash
curl -sL https://raw.githubusercontent.com/VeigaPunk/flash-bounty-128-package/main/walkthrough-embed.patch | git apply
# or: git apply walkthrough-embed.patch
```

Then set deploy env `VITE_WALKTHROUGH_YOUTUBE_ID=<real-device-youtube-id>` and ship.

Demo UI: https://veigapunk.github.io/flash-bounty-128-package/  
Handoff: STAFF-HANDOFF-128.md  
Gist: https://gist.github.com/VeigaPunk/095daab661527435e0c920cbc218b331
