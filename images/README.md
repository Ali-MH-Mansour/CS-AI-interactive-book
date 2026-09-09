# Instructor photo

The book's index cover (`index.html`) shows a small round instructor portrait
near the byline. It loads from this folder:

    images/instructor.png

**Present:** `instructor.png` — the instructor's photo, displayed at 96×96 px,
rounded to a circle. If the file is ever missing, the `<img>` hides itself
automatically (`onerror` handler), so the cover stays clean with no
broken-image icon.

To replace it, drop a new square/portrait crop here as `instructor.png`
(or use `.jpg` and update the `src="images/instructor.png"` reference in
`index.html` to match).

— placed for activity 260831-001 (cs-ai-course), chunk C04; photo wired C01 serial 024
