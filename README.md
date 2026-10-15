# SRA Robotics: Sample Robot Dataset Audit

**I check robot training datasets (LeRobot / Hugging Face) for problems before you train on them**, so you don't lose GPU time and weeks to bad data. Automated checks on every episode, plus a real person watching the videos that get flagged.

Independent, solo-run, based in the Bay Area.

## See a real sample

**[Read the sample audit report (PDF)](sample_audit_report_maxt90.pdf)**: an audit of the public dataset `MaxT90/so101-pick-place` (SO-101 arm, 50 episodes, 22,771 frames, 30 fps, 2 cameras), audited Oct 11, 2026.

| Headline | Result |
|---|---|
| Usable episodes | **49 of 50 (98%)**, passes the 85/15 rule (at least 85% usable) |
| Findings | **0 Critical, 1 Major, 2 Minor** |
| Verdict | **PASS after 1 fix** |
| Major | Episode 0: robot completely still for the first ~16 s (dead start). Fix: trim it, no re-recording |
| Minor | No calibration file in the dataset; gripper left open at the end of episode 45 |

This is a sample on a public dataset. It is not a statement about the dataset owner's work as a whole.

## What I offer

- **Free check:** I check 10 episodes from your dataset and send a short summary of what I found and recommend.
- **Full audit:** automated checks on every episode, a PDF report with Critical/Major/Minor findings, a list of unusable episodes, and fix advice. Turnaround 3-5 days.
- **Monthly plan:** I audit each new batch as you collect it, with a report within 2 business days and a monthly trend note.
- **Pricing:** on request.


## How it works
1. Send me a Hugging Face dataset link (LeRobot v3 format).
2. I run the automated checks (open source: see [robot-dataset-audit](https://github.com/sraentertainment17-code/robot-dataset-audit)) and watch the episodes that get flagged.
3. You get a PDF with the verdict, findings, unusable episodes, and a fix list.

## Honest limits
- LeRobot **v3** datasets only for now.
- Automated checks can't catch wrong labels or a frozen-but-decodable camera picture. Those only get caught by human video review, which is sampled, not every episode, unless we agree otherwise.
- The sample report has human review on 2 of 50 episodes and no coverage score; the paid audit adds more.
- I don't promise your robot will train well. I promise you'll know what's in your data.

## Contact
Email: founder@sra-robotics.com
Website: [FILL IN]
LinkedIn: [FILL IN]

Free check: just send a Hugging Face link and I'll reply with what I find in 10 episodes.
