## YouTube-DL

> [🧳 Download Suitcase](https://github.com/Impedimenta/Suitcase/releases)

```bash
% Suitcase --name="Download YouTube" \
  --window-floating \
  --control-title="Drop Your URLs Here!" --control-type="dropped-urls-label" \
  --control-title="Download" \
    --control-type="button" \
    --control-action="/usr/local/bin/youtube-dl" \
    --control-action-parameter="-o,~/Downloads/downloaded-video.mp4,SUITCASE_DROPPED_URLS"
```