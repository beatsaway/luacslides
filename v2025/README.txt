WHAT IS IN THIS FOLDER
======================

This is the output of the Arduino slide builder in the folder one level up.
Nothing here is written by hand. Every .pptx and every .html comes from
running

    python build.py

To change a lesson, change the content or the layout up there and build again.
Anything edited in here is overwritten by the next build.

The folder stands on its own. Zip it, copy it to a USB stick, put it on a web
server or a GitHub repository and it still works. There is no server code, no
setup in the browser and nothing loaded from the internet: the fonts and the
pictures are in assets/, and each preview is one HTML file.


WHAT IT IS FOR
--------------

An Arduino course for Years 7, 8 and 9: 18 lessons, six in each year.
The wording is ordinary classroom English. The ideas are the key points from
the course notes, not a separate topic list.

    Year 7   the board, a button, a sensor number, a knob,
             loops and functions, variables and decisions
    Year 8   voltage current and resistance, three colours, a screen,
             temperature and humidity, movement, distance
    Year 9   a buzzer, a DC motor, a servo, a stepper,
             a board with Wi-Fi, a solar cell

A lesson is a question, the idea, the build, the code, one thing to try,
and a check. The check answer stays hidden until you click.

The words to say in class are in the speaker notes of the .pptx, not on the slide.


THE FILES
---------

index.html
    The chooser. Open this one first. One card per lesson, with a link to read
    it in the browser and a link to download the PowerPoint.

preview-Y7-1-Meet-the-board.html
    ... and one more per lesson
    The lesson as a web page: the same slides, the same fonts, the same
    pictures, one after another. Use this in class instead of PowerPoint if you
    like. It goes full screen, it opens instantly, and questions hide their
    answers the way the .pptx does.

    To run it:  click the small "Present" button in the bottom-right corner, or
    press Ctrl+Enter (Cmd+Enter on a Mac). Right arrow, space or a click moves
    forward, left arrow goes back, Esc comes out. On a question slide the first
    press shows the answer and the next press moves on. Going back to a slide
    always hides it again, so a second class can use the same file.

preview-all.html
    Every slide on one long page, in course order. Not for teaching: it is
    there to read the whole course straight through, so a mistake or a crowded
    slide is easy to spot.

Y7-1-Meet-the-board.pptx
    ... and one more per lesson
    The lesson as a real deck, 16:9, with speaker notes. Opens in PowerPoint,
    Keynote or Google Slides. It uses Fira Sans; if that font is not installed
    the deck still reads fine but the spacing shifts a little. Installing the
    five files in assets/fonts fixes that, or just teach from the HTML preview,
    which has the fonts already in it.

assets/fonts/
    Fira Sans and Fira Sans Condensed, five files. The web previews load these,
    so the browser copy looks the same on a machine with none of it installed.

assets/img/
    91 pictures: the opening photographs, the board and component photos, and
    the drawn diagrams (board layout, each circuit, the Tinkercad screens). The
    previews reach them by relative path, which is why this folder travels with
    them. The .pptx files have the same pictures inside and do not need them.

_wordcount.txt
    How many words are on each slide, next to the number that slide is meant to
    stay under. This is for whoever writes the lessons, not for teaching: it
    catches the slide that quietly grew into a paragraph nobody can read from
    the back of the room.

.nojekyll
    Empty on purpose. GitHub Pages turns on Jekyll unless this file exists, and
    Jekyll refuses to serve any file whose name starts with an underscore. It
    would only lose _wordcount.txt, but an empty file is cheap.


THE 16 LESSONS
--------------

    L01     Introduction to Arduino       Blink an LED, and what the board is.  8
    Y7-L02  Press a Button                A pin can listen. digitalRead.        10
    Y7-L03  Turn a Knob                   analogRead and analogWrite.           10
    Y7-L04  Sense the Light               A sensor, a threshold, a number.      10
    Y7-L05  Make a Sound                  tone() into a buzzer.                 10
    Y7-L06  Eight Keys                    Eight inputs, one buzzer.             10
    Y8-L02  Colour from Three LEDs        Mixing light, not paint.              10
    Y8-L03  Seeing with Sound             HC-SR04 and pulseIn().                10
    Y8-L04  A Voltage That Means Degrees  The TMP36.                            10
    Y8-L05  A Plant That Asks for Water   Calibration, soil moisture.           10
    Y8-L06  Measuring a Push              Force-sensing resistor.               10
    Y9-L02  Motors Need a Driver          Transistor, current, PWM.             10
    Y9-L03  Servo Motors                  An angle, a pulse width.              10
    Y9-L04  Stepper Motor                 2048 steps, counted.                  10
    Y9-L05  Two Rules                     Three zones, three lights.            10
    Y9-L06  Talking to the Network        A board with a radio, a page.         10

The last column is the number of slides.


TWO THINGS TO KNOW
------------------

The lessons inside a year are written in the order given, and each one assumes
the lesson before it. Swapping two is fine as long as the code slide of the
later one still makes sense; check that slide before you change the order.

No kit is needed to read a lesson, or to do the build. Every build happens in
Tinkercad first, so a class can do the whole course on laptops even if the
hardware has not arrived.
