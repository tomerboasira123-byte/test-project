---
workflow: general-video
flow: automation
storyboard: no
message: "Recut of Tomer's gym talking-head clip, trimmed to speech, with captions/overlays/animation in his established reel style"
destination: instagram-reel
aspect: 1080x1920
language: he
length: ~47s
angle: talking-head recut
---

## Intent

Existing single-take gym talking-head footage of Tomer (@tomer_boasira), speaking
directly to camera, sitting on a bench in a gym, gesturing while talking. Task:
trim the dead air at the start/end down to the exact speech bounds, then dress
the clip with dynamic captions, overlays, and animation matching his established
Instagram Reels style (see `/tomer-editing-style`): white bold captions on a
lower-third band synced tightly to speech, direct hard cuts, natural look with
no heavy color grade, closing on a clear CTA if the transcript has one.

## Assets

- assets/source.mp4 — the user's raw footage (54.4s, 464x832 h264/aac, vertical).
  Trim window confirmed by cross-checking silencedetect (-30dB and -40dB) against
  visual frames: 0-11.6s is setup/chair movement (not speech, despite some of it
  registering as "sound" at looser thresholds); real speech runs 11.6s -> 52.85s
  (41.25s kept). He reaches for the camera right after the last word.

## Customizations

- Dynamic word/phrase-synced captions (white bold, lower-third-center, per the
  house style's default pattern).
- Overlays/animations "where needed" — left to editorial judgment on this pass:
  entrance/exit motion, light punch-ins keyed to emphasis, and a numbered-list
  treatment if the transcript turns out to be a listicle.

## Notes

- Automated Hebrew speech-to-text is unavailable in this session: the sandbox's
  network egress policy blocks huggingface.co (whisper model download) and the
  OpenAI/Groq Whisper APIs. Per the user's choice, the Hebrew transcript is being
  supplied directly by the user and manually time-aligned to the speech segments
  found via ffmpeg silencedetect, instead of word-level STT timestamps.
- No color grade / filter — keep the natural gym lighting look per house style.
