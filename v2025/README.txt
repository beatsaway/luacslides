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

An Arduino course for Years 7, 8 and 9: 16 lessons, 158 slides.

    1 first lesson, shared      L01  Introduction to Arduino
    5 Year 7 lessons            Y7-L02 .. Y7-L06
    5 Year 8 lessons            Y8-L02 .. Y8-L06
    5 Year 9 lessons            Y9-L02 .. Y9-L06

All three years start on the same first lesson, then split their own way.
That is 1 + 5 + 5 + 5 = 16 lessons.

Every lesson is ten slides in the same order, so a class only has to learn the
pattern once:

     1  title        name of the lesson and one line saying what it is
     2  hook         three pictures and one question to open the lesson
     3  one idea     the single sentence the lesson is built on
     4  hardware     a diagram of the part and how it connects
     5  setup        the build in four numbered steps
     6  code         the program, explained line by line
     7  mission 1    first thing to do in Tinkercad, with a goal to check
     8  mission 2    the same again, one step harder
     9  check        one question, answer hidden until you click
    10  exit ticket  what to write down before logging off

That is where "two missions" comes from: slides 7 and 8 are the two things the
class builds, one after the other.

Each lesson is about 10 minutes of talking. The words to say in class are in
the speaker notes of the .pptx, not on the slide.


THE FILES
---------

index.html
    The chooser. Open this one first. One card per lesson, with a link to read
    it in the browser and a link to download the PowerPoint.

preview-L01-Introduction-to-Arduino.html
preview-Y7-L02-Press-a-button.html    ... and one more per lesson
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
    All 158 slides on one long page, in course order. Not for teaching: it is
    there to read the whole course straight through, so a mistake or a crowded
    slide is easy to spot.

L01-Introduction-to-Arduino.pptx
Y7-L02-Press-a-button.pptx    ... and one more per lesson
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
