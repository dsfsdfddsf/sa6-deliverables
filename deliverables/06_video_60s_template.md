# 60s video script + storyboard — reusable template (Dework/Superteam video gigs)

Use: any open video-content gig (e.g. future "show us how you use X" listings). Filled instance for MozaikPay: ../mozaikpay/ (script_60s_es.md + storyboard.md).

## Script skeleton (60s, 10 beats, any product)
| Beat | 0:00-0:04 HOOK (pain, first person) | 0:04-0:09 SET (what I do about it) | 0:09-0:14 PRODUCT (real app screen 1) | 0:14-0:20 VALUE (concrete benefit #1) | 0:20-0:27 SOCIAL (friend/family use case) | 0:27-0:34 MECHANISM (how it works, 1 step) | 0:34-0:41 FLOW (second use case / cash-out) | 0:41-0:47 SCALE (geography/speed fact) | 0:47-0:53 CTA (logo + store badges) | 0:53-0:55 DISCLOSURE (#publicidad) |

## Storyboard table (fill per gig)
| Shot | Time | Asset type | Source | Prompt/notes |
| 1 | | creator B-roll | Higgsfield FREE image->video (escalate MAIN) | 9:16, candid, "smartphone-camera look, no text" |
| 2 | | creator B-roll | Higgsfield FREE | hand+phone close-up |
| 3-7 | | REAL app screens | submitter's device screen recording | required by most gigs ("shows your real account") |
| 8 | | map/animation | ffmpeg drawtext over still | city A -> city B, 1 line |
| 9 | | logo+badges | sponsor assets (listing JSON cloudinary URL) + official store badges | |
| 10 | | disclosure sticker | ffmpeg drawtext, last 2s | |

## ffmpeg assembly (9:16, captions burned)
    ffmpeg -i s1.mp4 -i s2.mp4 -i sc3.mp4 ... -filter_complex "[0:v]scale=1080:1920:force_original_aspect_ratio=increase,crop=1080:1920,setsar=1[v0]; ... [v0][v1]...concat=n=10:v=1:a=0[vc]; [vc]subtitles=captions.srt:force_style='FontSize=22,Outline=1,MarginV=120,Alignment=2'[vout]" -map "[vout]" -t 55 -r 30 -c:v libx264 -pix_fmt yuv420p out_v1.mp4
Verify: ffprobe out_v1.mp4 (duration 50-60s, 1080x1920, h264). Heavy encoding -> sait2 docker_run or PC ffmpeg (light enough for 55s vertical).

## Gig compliance checklist (generic)
- [ ] language/market of the gig
- [ ] duration within bounds
- [ ] real account on screen (human step)
- [ ] disclosure (#publicidad / paid-partnership)
- [ ] banned phrases per listing (e.g. no crypto/blockchain, no returns, no fee comparisons)
- [ ] posting platform + audience geography requirement
- [ ] submit fields (link, screenshots, username)
