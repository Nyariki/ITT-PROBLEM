# ITT-PROBLEM

This is a problem I was to provide a solution for, as part of a coding interview. It is translated from pdf, so formatting is a little bit off. 

## INTERVIEW PRACTICAL QUESTION

**Task: event tracker system**

**Goal:** Design and implement a program that logs when tasks should be carried out as explained herein.

**Problem:**

xxxxxx supervisor monitors when the team members should carry out tasks as they fall due.
To achieve this, the supervisor requires a task tracker that logs when a task should be carried
out. Supervisor also requires a report of all the tasks that should have been done prior to the
time of generating the report.

Each task has a predetermined interval in which it should repeatedly be performed as well as
the order of precedence in case tasks coincide, as summarized below:

```
Task Interval (Seconds) Precedence
START 30 1
STOP 40 2
REPORT 50 3
```
***Task description:**

START – a team member should start N servers every 30 seconds, where N is a random integer
value between 10 and 20 inclusive.

STOP – a team member should stop n servers every 40 seconds, where n is a random integer
value between 5 and K inclusive (K is the total number of servers running at any particular point in time).

REPORT – every 50 seconds, a team member should report K servers running, where K is the
total number of servers running at the time of reporting.

**Required:**

i. Using tools (framework, language and database) of your choice, design and implement a mobile application to solve the problem.^
ii. The program should have two parts: User Interface (UI) - to capture input and display output, and a BACKEND API – to perform all the necessary computations based on the input and feeding the UI with the output. (Further details provided below)
iii. UI
a. Should comprise of a 12-hour wall clock hanging on a masonry wall of a color of your choice.
b. For every START task log, change the color of the wall to the new wall color obtained from the API.
c. For every STOP task log, change the color of the clock’s face to the new face color obtained from the API.
d. For every REPORT task log, change the color of the hour labels to the new hour labels color obtained from the API.
e. The clock MUST simulate a real clock, with all the three hands (hour, minute and second hands).
f. The clock hands should all be set at 12:00 o’clock whenever the program starts and time simulation runs independent of the host system time.
g. Place a display area below the wall clock to be used for showing the most recent ask(s). Every new due task overwrites any task displayed.
h. Periodically post current time and colors of the three UI sections (refer (iii) b, (iii) c and (iii) d above) to the API to query if an event is happening at that particular time. For every task due retrieved from the API, print the returned message on the display area and update the associated section color.
i. Strategically, place a report button that when clicked, retrieves a detailed report from the API of every event logged since the program was started (sample report given below).
j. The UI shall NOT directly access the data storage, but depend on the API to retrieve the current task(s) and the logged tasks’ report.

iv. BACKEND API 
a. Logs actual time the program was started (sample provided below)
b. Accepts current time and the current colors of the three sections (refer (iii) b, (iii) c and (iii) d above) from the wall clock.
c. If some given task(s) should be carried out at the received time,^
i. Log the program-based task(s) time, task(s) type, task(s) message, actual time (sample provided below)
ii. Respond with a display message of the current due task(s) with respect to he time received from the wall clock. (sample provided)
iii. For each task, generate and respond with new color(s) for the appropriate section(s) as noted in (iii) b, (iii) c and (iii) d above. The new color MUST be different from the previous color.


