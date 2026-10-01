# Pursuit Rotor Test

A free, browser-based classroom simulation of the **pursuit rotor**, a classic apparatus for studying motor learning. A target moves around a circular path, and the participant tries to keep their cursor (or finger) on it for as long as possible. The tool records time on target and accuracy across repeated trials and draws a learning curve.

**Live version:** https://sarahqureshipsych-cmd.github.io/pursuitrotor/

**Related project:** [Digital Memory Drum Simulator](https://sarahqureshipsych-cmd.github.io/memorydrum/)

> **Note:** This is a classroom demonstration. Using a mouse or finger on a screen differs from a stylus on a physical rotor, and screen and input delay can add error. Results are for teaching and demonstration only and are not lab-grade measurements.

---

## Features

- Target moving clockwise around a dashed circular path, starting from the top of the circle at the start of each trial
- Works with **mouse, touch and pen** input (pointer events)
- Responsive canvas that scales to the screen, with pointer positions mapped to the internal 400 x 400 drawing area
- Live display of the current trial, time on target, and time remaining
- Results panel at the end of each trial showing **time on target** and **accuracy**
- Multi-trial sessions with a "Session Complete" message
- Results table and a **learning curve chart** of accuracy by trial
- **CSV export** of all trial data
- No installation, no accounts, no external libraries (a single HTML file)

## How to use

1. Open the page in a browser on a computer, phone or tablet.
2. Adjust the settings (optional).
3. Press **Start Session**.
4. Keep your cursor or finger inside the moving circular target until the trial ends.
5. Read your results and repeat for the remaining trials. Press **Export CSV** to download your data, or **Reset Data** to clear everything and start again.

## Settings

| Setting | Range | Default | What it does |
|---|---|---|---|
| Trials per Session | 1 to 20 | 5 | Number of trials before the session ends |
| RPM (Speed) | 1 to 60 | 30 | Rotation speed of the target in revolutions per minute |
| Target Size | 10 to 50 | 15 | Radius of the target in pixels (smaller is harder) |
| Duration (s) | 5 to 60 | 15 | Length of each trial in seconds |
| Rest Interval (s) | 0 to 60 | 10 | Rest between trials (see below) |

Settings are locked while a session is running. Press **Reset Data** to change them again.

### Massed and spaced practice

- **Rest Interval above 0:** after each trial a countdown runs, and the next trial starts automatically (spaced practice).
- **Rest Interval of 0:** the next trial waits for you to press **Start Next Trial** (massed practice).

This lets students compare practice schedules and see how speed and target size affect performance.

## How scoring works

- **Score (time on target):** the total time, in seconds, that the pointer was inside the target circle during the trial.
- **Accuracy (%):** `time on target / trial duration x 100`, shown to one decimal place.
- Time on target is capped at the trial duration, so accuracy cannot exceed 100%.
- To avoid large jumps if the browser tab is hidden mid-trial, each animation frame is limited to a maximum of 0.1 seconds.
- If the pointer leaves the play area, it counts as being off target.

## Exported data

The CSV file is named `pursuit_rotor_results.csv` and has one row per trial with these columns:

`Trial, RPM, Target Radius, Duration (s), Score (s), Accuracy (%)`

## Limitations

- Data is stored only in the page's memory. Reloading or closing the page clears it, so export your CSV first.
- A single target and a circular path only.
- Timing depends on the device's screen refresh rate and input latency.
- Not validated against physical pursuit rotor apparatus.

## Technical notes

- Built with HTML, CSS and JavaScript in one file, using the HTML canvas
- No dependencies and no data sent to any server
- To host on GitHub Pages, name the file `index.html` and enable Pages for the repository

## License

Copyright (c) 2026 Sarah Qureshi. All rights reserved.

This software is free to use for personal, educational and non-commercial purposes, including use in classrooms and linking to it from other sites.

You may not copy, redistribute, modify, sell or create derivative works of the source code without prior written permission from the copyright holder.

The software is provided "as is", without warranty of any kind.

Contact: sarahqureshipsych@gmail.com

## Author

Created by Sarah Qureshi, undergraduate psychology student, Government College for Women, M.A. Road, Srinagar.
