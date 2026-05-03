# Semester Space Path

Semester Space Path is a single-page, static HTML app for turning a semester syllabus into a visual planning map.

The map represents a 16-week term as a meandering cosmic path. Assignments appear as planet milestones, with larger planets for major assignments and smaller planets for planned subtasks. Course difficulty is shown with static textures, and Rest Orbit markers protect planning or recovery blocks.

## Open the App

Open `index.html` in a browser.

If your browser blocks local files, run `Start Semester River.cmd` on Windows and then open:

```text
http://127.0.0.1:8765/
```

## Main Features

- 16 angular, asymmetrical week shards
- Semester start date picker
- Automatic week date ranges
- Today marker
- PDF/text syllabus upload with basic date and assignment parsing
- Class-colored planet milestones:
  - Class 1: bright yellow
  - Class 2: crisp white
  - Class 3: pale electric lime
  - Class 4: light cyan
  - Class 5: soft rose
- Editable course names that relabel the difficulty sliders and legend
- Major milestone planning interaction
- Smaller milestone steps placed in earlier weeks
- Completion launch animation when a task is finished
- Static difficulty textures
- Rest Orbit blocks
- Transparent PNG planet assets for Earth, Jupiter, Saturn, Mars, and Neptune

## Files

- `index.html` - main GitHub Pages entry point
- `semester_river.html` - same app, kept as a named working copy
- `assets/planets/ef_planet_assets/` - transparent PNG planet milestone assets
- `extract_syllabus_assignments.py` - optional PDF syllabus parser
- `add_upstream_echo.py` - optional helper for adding Boulder notifications to JSON
- `requirements.txt` - optional Python dependencies

## GitHub Pages

This app can be hosted directly with GitHub Pages:

1. Create a new GitHub repository.
2. Upload the files in this folder.
3. In GitHub, go to `Settings` -> `Pages`.
4. Set the source to the main branch and root folder.
5. Open the published Pages URL.

No build step is required.

## Optional Python Parser

Install dependencies:

```bash
pip install -r requirements.txt
```

Extract assignments from a syllabus PDF:

```bash
python extract_syllabus_assignments.py syllabus.pdf -o assignments.json --course-name "Course Name"
```

Add Upstream Echo reminders to an existing JSON file:

```bash
python add_upstream_echo.py assignments.json -o assignments_with_echo.json --year 2026
```
