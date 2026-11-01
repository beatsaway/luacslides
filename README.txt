ELECTRONICS · YEARS 7, 8 AND 9
A static site. No build step, no server, no dependencies.

  index.html        the chooser
  v2027/            the current course: 15 lessons, 12 slides each
  v2026/            the previous course, kept for reference
  v2025/            the first version, kept for reference

Published at https://luacslides.netlify.app/ . Open index.html in a browser,
or that address, and everything else is linked from there.

WHAT IS IN v2027
  15 PowerPoint decks, a self-contained HTML preview of each, one page with
  all 180 slides, a chooser, the course on paper (CURRICULUM.txt), and the
  notes for using the folder (README.txt). Each lesson is one inquiry. The
  pictures are photographs in assets/img/v27.

HOW TO PRESENT
  From the HTML: open a lesson, press the Present button at the bottom right
  (or Ctrl+Enter). Right arrow for the next slide, left for back, Esc to leave.
  Where a slide has a hidden answer, the first click shows it and the second
  moves on. A slide always starts with its answer hidden, so going back to it
  re-hides the answer for the next class.

  From PowerPoint: open the .pptx and start the slide show. The answers are
  click-to-reveal animations, one click each. Speaker notes are on every slide.

SOURCE
  v2027 is generated from newyeardraft3/gslides/v27/ by `python -m v27.build`.
  v2026 is generated from v26/ by `python -m v26.build`. Edits inside a version
  folder are overwritten by the next build of that version. This page is not.

TYPE
  Fira Sans, by Carrois Type Design, SIL Open Font License. The font files are
  in each version's assets/fonts.
