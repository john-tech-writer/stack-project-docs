# Audio / video workflow

Output: overview and service videos for YouTube.

Software

  - Notepad ++
  - Guvcview - on laptop - profile: vintage-reels.gpfl
  - Shotcut - service guide template.mlt, to view export settings View > Export > Advanced, YT 1080p30 stack v2
  - Reaper - FX: VO - small speaker / phone tilt, Render > Presets > All settings > VO master WAV 44k 24bit - 15 LUFS / -1 dBTP
  - Mbox control - preset: 2 - recording VOs

Hardware

  - Logitec HD Pro C920 webcam
  - Mbox studio
  - Audio-technica MB 1K mic
  - Rode headphones (model?)

1. Write script for overview video. Based on overview .md file for the repo and on the overview skeleton, print to use on benchtop.

overview-skeleton.md > `[slug]-overview.md`
overview-script-skeleton.md  > `[slug]-overview-script.md`

2. (On laptop / benchtop) Record overview video with scratch audio, save .mkv file to micro card for transfer to workstation.

`[slug]-overview.mkv`

3. Create project in Shotcut, based on template (.mlt file) import video (.mkv file).

overview template.mlt > `[slug]-overview.mlt`

4. Edit project in Shotcut, adding stills and text from overview on repo, also from schematics and articles saved in the workspace, trimming, etc.

5. Create project in Reaper using fx preset, record VO, save, export as .wav using presets.

`[slug] overview audio.rpp`
`[slug] overview.wav`

6. Import audio to project in Shotcut, minor edits.

7. Export project as .mp4 file using YouTube preset, review locally, make sure Windows audio is playing correctly (no extra compression, etc. - check audio control panel).

`[slug]-overview.mp4`

8. Upload .mp4 to YouTube, write video title and description based on last YouTube upload, compare to local skeleton in workspace `youtube/skeletons-templates/`, and add to appropriate playlists. See in workspace `youtube/youtube-playlists.md`.

9. Add title and video link to the workspace `youtube/youtube-video-links.md`.

9. Go through the same sequence for service videos 1, 2, and any additional shorts. For steps 7 / 8, service videos will also have markers as chapters exported from Shotcut as a .txt file and pasted into the YouTube description.

`[slug]-service-[#]-of[#]-chapter-markers.txt`

10. After a video project is complete clean up the directories.

  - Delete the auto-saved mlt files Shotcut generates, identifiable by the date stamp e.g., `pflueger nobby service guide 1 of 2 2026-07-21T23-28-13.mlt`

  - Delete extra Reaper files:
  
    - Backups folder / .rpp-bak files

    - Media folder: Be careful, this contains real audio data. Run Reaper's built-in tool: Rather than deleting by hand, use File > Clean Current Project Directory — Reaper scans what's actually referenced by the project and only removes unreferenced media files.

      - `/media/peaks/` folder can be deleted

  - Delete any extras of the other video project file types:

    - txt: chapter markers exported from Shotcut
    - mp4: final audio / video output from Shotcut
    - wav: audio VO and fx files rendered from Reaper
    - mkv: raw video files from Guvcview
    
If there are issues with multiple rpp project files, etc., this can be generally be sorted out by opening each one, doing a Save As with the copy media box checked, play file to verify it works, then run the Clean dir command in Reaper.

## Notes on Shotcut backup files

This is a separate, configurable feature under Settings > Backup. When it runs, it duplicates your current project file into the same folder, appending the last-modified timestamp to the name — exactly the name yyyy-mm-ddThh-mm-ss.mlt pattern you're seeing. It can fire automatically (Manually / Hourly / Daily / Weekly — default is Daily, some builds default to Hourly) or on demand via File > Backup and Save (Shotcut User Guide, Shotcut configuration keys).
Purpose

It's a lightweight version-history safety net — if your main .mlt ever gets corrupted or you want to roll back to an earlier state, you (or Shotcut's File > Other Versions menu) can grab one of these timestamped snapshots instead of losing everything.
How to stop it from generating extras

Go to Settings > Backup and switch the frequency from Daily/Hourly to Manually. That stops Shotcut from auto-creating these timestamped copies — you'll only get one if you deliberately choose File > Backup and Save.
On deleting the extras

Since you already keep disciplined version control and file naming (per your GitHub-based workflow), it's safe to delete the timestamped extras once a project is finished and your primary .mlt is verified to open and play back correctly — they're redundant with your own backup practices. Just don't delete them mid-project before confirming the main file is intact.

## Notes on Reaper backup files

Backups folder / .rpp-bak files: These are just timestamped copies of the project file itself (not audio), generated on save so you can roll back to an earlier state if something breaks. Once you've confirmed the final .rpp opens and plays correctly, it's safe to delete this whole folder — some users even automate deleting anything older than N days, or archive finished projects by just wiping the backups subfolder entirely.

Media folder — different story, be more careful

This one actually holds your real audio data:

    .reapeaks files (waveform cache images) — always safe to delete. Reaper just regenerates them next time it opens the project.
