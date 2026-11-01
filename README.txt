WHAT IS IN THIS FOLDER
======================

This is the built output of the Arduino slide generator in ../ (the parent
folder). Nothing here is typed by hand: every .pptx and every .html in this
folder is produced by running

    python build.py

from the folder one level up. If a deck needs a change, change ../content.py
(or ../layouts.py, ../design.py) and rebuild. Editing a file in here is lost on
the next build.

The folder is self-contained. Copy it anywhere, zip it, drop it on a web server
or a GitHub repository, and it still works. There is no server-side code, no
build step in the browser and no external request: fonts and pictures are in
assets/, and every preview is a single HTML file.


WHAT IT IS FOR
--------------

16 lessons of a physical-computing / Arduino course for Years 7, 8 and 9.

    1 shared first lesson        L01  Introduction to Arduino
    5 Year 7 lessons             Y7-L02 .. Y7-L06
    5 Year 8 lessons             Y8-L02 .. Y8-L06
    5 Year 9 lessons             Y9-L02 .. Y9-L06

Year 7, 8 and 9 all sit the same first lesson, then split. So 1 + 5 + 5 + 5 =
16 decks, 158 slides.

Every deck is 10 slides in the same order, so a class learns the rhythm once:

    cover    the title, the promise
    hook     three pictures and a question
    idea     the one sentence that matters
    picture  a diagram that explains it
    steps    the Tinkercad build, numbered
    code     the code, decoded line by line
    mission  what to do in Tinkercad, with a goal you can check
    check    a question, with the answer hidden until you click
    close    wrap-up and the exit ticket

Each deck runs 10 minutes or less of talking. Speaker notes are inside each
.pptx, not in the HTML.


THE FILES
---------

index.html
    The chooser. Open this first. One card per lesson with a link to read it in
    the browser and a link to download the PowerPoint.

preview-L01-Introduction-to-Arduino.html
preview-Y7-L02-Press-a-button.html    ... and so on, one per deck
    A pixel-exact copy of the deck in the browser, one <section> per slide.
    This is the version to show in class if you do not want to open PowerPoint:
    it runs full screen, it is fast, and the answers hide and reveal exactly as
    they do in the .pptx.

    Presenting:  click the small "Present" pill in the bottom-right corner, or
    press Ctrl+Enter (Cmd+Enter on a Mac). Right arrow / space / click goes
    forward, left arrow goes back, Esc leaves. On a question slide the first
    press reveals the answer and the next press moves on. Arriving on a slide
    always clears it again, so the same deck can be run for a second class.

preview-all.html
    All 158 slides in one long page, in course order. Not for teaching: it is
    the proof-reading view, so every slide can be read top to bottom in one
    pass and any overflow or typo is easy to spot.

L01-Introduction-to-Arduino.pptx
Y7-L02-Press-a-button.pptx    ... and so on, one per deck
    The real deck, 16:9, with speaker notes. Opens in PowerPoint, Keynote,
    Google Slides. Fonts fall back if Fira Sans is not installed, so install
    the two woff2 files in assets/fonts first for an exact match (or just use
    the HTML preview, which carries the fonts with it).

assets/fonts/
    Five Fira Sans / Fira Sans Condensed woff2 files. The HTML previews load
    these, so the browser copy matches the PowerPoint with or without the fonts
    installed on the machine.

assets/img/
    91 pictures: the hook photographs, the board and component photographs,
    and the drawn diagrams (board layout, each circuit, the Tinkercad screens).
    The previews point at them by relative path, which is why the folder has to
    travel as a whole. The .pptx files have the same pictures embedded and do
    not need this folder.

_wordcount.txt
    Words per slide for every deck, next to the budget for that slide type.
    Housekeeping for the writing, not for teaching: a slide that overshoots its
    budget is a slide nobody can read from the back.

.nojekyll
    Empty on purpose. GitHub Pages runs Jekyll unless this file is present, and
    Jekyll refuses to serve any file whose name starts with an underscore,
    which would take _wordcount.txt (and nothing else) with it.


THE 16 DECKS
------------

    L01     Introduction to Arduino           Blink an LED. What the board is,
                                               and how code makes it act.      8
    Y7-L02  Press a Button                    A pin can listen. digitalRead.  10
    Y7-L03  Turn a Knob                       analogRead and analogWrite.     10
    Y7-L04  Sense the Light                   A sensor, a threshold, a number.10
    Y7-L05  Make a Sound                       tone() into a buzzer.           10
    Y7-L06  Eight Keys                         Eight inputs, one buzzer.       10
    Y8-L02  Colour from Three LEDs             Mixing light, not paint.        10
    Y8-L03  Seeing with Sound                  HC-SR04 and pulseIn().          10
    Y8-L04  A Voltage That Means Degrees       The TMP36.                      10
    Y8-L05  A Plant That Asks for Water        Calibration, soil moisture.     10
    Y8-L06  Measuring a Push                   Force-sensing resistor.         10
    Y9-L02  Motors Need a Driver               Transistor, current, PWM.       10
    Y9-L03  Servo Motors                       An angle, a pulse width.        10
    Y9-L04  Stepper Motor                      2048 steps, counted.            10
    Y9-L05  Two Rules                          Three zones, three lights.      10
    Y9-L06  Talking to the Network             A board with a radio, a page.   10


ONE THING TO KNOW
-----------------

The lesson names are the ones in the plan, but the order inside a year is not
sacred. Lessons 2 to 6 in each year assume only the first lesson and each other
in the order given; if you swap two, check the code slide of the second one.

No kit is required to read a deck. A kit is required to do the mission, and the
build is always in Tinkercad first, so a class can run the whole course on
laptops alone if the hardware has not arrived yet.
