# Finding & Transporting Cargo — Companion

A single-page, self-paced coding companion for the VEX AIM **Unit 6: Finding and
Transporting Cargo** lesson (9th/10th grade). Students code the robot to use its
**AI Vision Sensor** to find sports balls — whose positions change every round —
and kick them through a goal marked by AprilTag 0.

Built on the TETC Stadium Rover Companion template, with the lesson arc adapted
for vision: instead of measuring fixed distances and hard-coding them, each level
teaches the robot to *look* (detect → turn toward → drive in → kick).

## The arc

- **Level 1 — Blocks.** Use the AI Vision blocks to find one ball, line up the goal, and kick it in.
- **Level 2 — Switch.** Convert blocks to Python and read how the vision values (`.exists`, `.bearing`) steer the robot.
- **Level 3 — Python.** Type it from scratch — and make the robot search until it actually sees a ball.
- **Bonus — Loops & variables.** One `for` loop that scores both balls. (Locked until Level 3 is complete.)

## Files

- `index.html` — the companion (single file; inline CSS, one JS IIFE; no build step)
- `field.html` — field reference: layout, bearing, and what the AI Vision Sensor reports
- `logo-tetc.png` — TETC logo

## Run it

Open `index.html` in any modern browser. Progress (path, completed levels,
hint state, and notes) is saved to `localStorage` under
`tetc_finding_transporting_cargo_companion_v1`. Use **Reset my progress** in the
sidebar when a new student starts on a shared Chromebook.

## VEXcode AIM commands used

- Vision: `robot.vision.get_data(SPORTS_BALL)`, `robot.vision.get_data(TAG0)`, `robot.vision.tag_detection(True)`
- What it sees: `ball[0].exists`, `ball[0].bearing`, `ball[0].centerX`
- Move: `robot.turn_for(LEFT|RIGHT, degrees)`, `robot.move_for(mm, 0)`
- Kick: `robot.kicker.kick(SOFT|MEDIUM|HARD)`

Live URL: https://tetc-edu.github.io/Transporting-Cargo_Ai-Vision/
