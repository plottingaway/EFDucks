[README.md](https://github.com/user-attachments/files/27298326/README.md)
# Semester River

Semester River is a single-page, static HTML app for turning a semester syllabus into a visual planning map.

The map represents a 16-week term as angular geometric shards. Assignments appear as ducks, with larger Mama Ducks for major assignments and smaller ducklings for planned subtasks. Course difficulty is shown with static textures, and Calm Waters mark protected planning or recovery blocks.

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
- Syllabus paste box with basic date and assignment parsing
- Subject-colored ducks:
  - Clinicals: bright yellow
  - Theory: crisp white
  - Pharmacology: pale electric lime
  - Skills Lab: light cyan
- Mama Duck planning interaction
- Ducklings placed upstream in earlier weeks
- Poof animation when a major assignment is planned
- Static difficulty textures
- Calm Waters blocks

## Files

- `index.html` - main GitHub Pages entry point
- `semester_river.html` - same app, kept as a named working copy
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
