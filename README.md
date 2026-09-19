# CMP_SCI-4500-Intro-to-Software-Profession-SG3-Group-project-CSV

Small Group 3 Software Development Project for CS 4500, Spring 2025 4 or 5 person teams
Small Group 3 (SG3) is the semester’s third and last CS 4500 group software development project. You
will be in a group of 4 or 5 developers. You should log all the time you spend on this project in the time
log described in the syllabus. In addition to working on your time log during this project, you will also be
spending quite a bit of time communicating with other team members, and documenting that
communication.
You should find that your SG3 tasks are closely related to the SG1 and SG2 tasks. This means that the SG1
and SG2 code, designs, and tests that your teammates and you previously developed should be of great
benefit to the SG3 project. However, you need to decide in your SG3 group what programming language
you will use, and which, if any, of the SG1 and SG2 programs brought into your SG3 group should be used
as a basis for the SG3 project. Software reuse is a major issue in software engineering, and you are going
to get some experience with that practice in CS 4500.
You’ll find that a big emphasis in SG3 is documentation for two audiences: a user (not a software
engineer), and someone maintaining your code in the future (certainly a programmer, and probably a
software engineer). There will be some programming challenges, but not as many as usual.
You must communicate with other members of your team each weekday during the assignment, and
you must document that communication.
You are REQUIRED to communicate with your teammates EVERY WEEKDAY from when this specification
appears in the schedule to when your group submits the assignment. This can be a phone call, an email, a
Zoom session, a post on Discord, a face-to-face meeting, or any other means of communication your team
decides is appropriate. You are allowed to communicate on the weekend, and you are not limited to one
communication per weekday. But it is part of this assignment to communicate with your teammates at
least once every weekday. No exceptions. If you don’t, your semester grade will be lowered.
Please only send me ONE notification of communicating with your team each weekday. You can
communicate with your teammates as often as you’d like, but only notify me once a day during the week.
You can (and I hope you will) communicate with teammates during the weekends (Saturday and Sunday),
but don’t send me any notifications on Saturday or Sunday.
In order to enforce the communication requirement, you are required to notify me of at least one
communication with your group each weekday. Although the communication between team members
can take many forms, the notification to me must be via email. Do NOT use my usual UMSL email address
for this notification. If you use my UMSL email for this notification, the notification will be ignored, and
you will not get credit for the notification. Instead use this email for the notification:
CS4500instructor@yahoo.com
The subject heading should be “notification” without the quotes. The message in each notification email
to me must be in this form:
X communicated with Y via Z
…where X is your name, Y is either a single name or a list of names, and Z describes how you
communicated. Each name should have a first name and a last name, as they appear on our Canvas
website. Here are three examples of legal notification messages, assuming that the named people were
really in your small group:
Fred Zilphath communicated with Ethyl Mermen via email
Angie Doyle communicated with Larry Robin, Marie Koster, and Edna Lumbar via Discord
Mary Boyd communicated with Bonnie McNight via a face-to-face meeting
The notification shouldn’t include a date because the notification should be sent on the day of the
interaction. If the notification does not include the phrase “communicated with” or the word “via,” it is
not a valid notification. If you spell either of those words incorrectly, it is not a valid notification. If the
message does not include your first name and last name, it is not a valid notification. If it does not include
at least one of your team members’ names, then it is not a valid notification. You only get credit for valid
notifications. As you might guess, I am being picky about the format of these notifications because the
notifications will be tabulated automatically, and the strict format facilitates that process. You only get
credit for one notification per weekday, so don’t bother to send multiples on the same day. Also, if you
forget to send a notification, you may NOT make it up by sending the notification the next day.
I’m not going to lie to you; this notification system is a pain. Yes, it is a pain for you, but it is an even
bigger pain for me. (There are 50 students or so in this class, so you can imagine how many of these
notifications I’ll be dealing with.) However, there is a reason for all this pain. The number one most
annoying thing about being in a student group project is having a team member who disappears during
the project. Students HATE that, and I don’t blame them. This notification system is my latest method of
trying to enforce the idea that group members MUST communicate with each other daily (during the
week) while they are on a team. In CS 4500, you will communicate with your team, or your grade will
suffer. And you will document that communication using valid notifications (as detailed above), or your
grade will suffer.
WHAT YOUR SG3 PROGRAM SHOULD DO
Your program (also known as SG3 in this specification) should begin by printing to the screen a short
explanation of what the program will do. The explanation should take up one screen or less.
Next, SG3 should ask the user for the name of a file. The file should be a CSV file. If you forget the details
of a CSV file, check the SG1 specification.
SG3 should check to make sure that the file name the user enters ends in .CSV. (I will use upper case only,
but the user doesn’t need to worry about upper or lower case, and SG2 should accept any mixture of
upper and lower case for the CSV at the end of the filename. If the name that the user enters does not end
in .CSV (or .csv or .CsV, or…), then SG3 should give an appropriate error message and reprompt for the
filename. This goes on forever, or until the user finally gives a good file name, whichever comes first.
Once the user has entered a valid filename, SG3 should attempt to open the named file for reading. The
named file should reside in the same directory as where SG3 resides. If the file does not exist in the
directory where SG3 resides, then SG3 should give the user an appropriate error message, and reprompt
for another valid file name. This should continue until SG3 successfully opens a .CSV file designated by the
user. I will call that file F in this specification, even though the name could not be F. (Yes, it could be
F.CSV, but it is so much easier to just use F in this specification.)
Once SG3 has successfully opened F, it should read the file, line by line. The file should include the
following information:
Line 1 of F should begin with a comma, indicated a null string, followed by comma separated character
strings. Each of these strings I will refer to as a “species.” A species name can contain English letters,
periods, numbers, blanks, and underscores. A species name cannot include a comma. Your program
should count how many species are in F’s first line. I’ll call that number N.
There should be at least one more line in F. For SG3, you should make sure that there is at least one more
line in the file, and that there are not more than 999 lines in the file. If either of those constraints are not
met, SG3 should give an appropriate error message, wait for the user to push ENTER, and then halt.
For the rest of this specification, we will assume that there is at least one more line in the file, and no
more than 999 more lines in F. Each line after the first line should be in the following form:
Each line in F after its first line will start with a date in the format MM/DD/YYYY where MM is a two digit
number from 01 to 12, DD is a two digit number given a day of that month, and YYYY is a four digit year.
Leading zeros, where appropriate, are allowed, but not required. Therefore, 01/04/2020 is a legal date,
and 1/04/2020 and 1/4/2020 are also legal. However, 1/4/20 is illegal. SG3 must validate the dates to
make sure each date is legal. If a date in the file is illegal, SG3 should give an error message, identifying
which line the illegal date was in, including a copy of the illegal date, and an explanation of why the date
is illegal. Then SG3 should prompt the user to press ENTER to end the program. We assume for the rest
of the specification that all the dates found were legal.
After the date, each line should have N numbers, separated by commas. The numbers must be
nonnegative. A number can be an integer, or a real number given with a decimal. Here are some numbers
that are legal in SG3: 0, 4.2, 0.563, 7, and 42. Here are numbers that are not legal in SG3: -4, 2/3, and -.09.
SG3 will have to verify that there is the right number of numbers in each line (should be N), and that each
of the numbers is legal. If any line does NOT have the right number of numbers, or if any of the numbers
is illegal, SG3 should give an error message that identifies the line where the problem occurred, prints out
the entire line, and then explains what went wrong, including which number was illegal and why. SG3
only has to discover the first illegal number, it need not find them all if there are more than one. Then SG3
should prompt the user to press ENTER to end the program. We assume for the rest of the specification
that all the numbers found were legal and the correct number of numbers appeared on each line.
SG3 will read in these lines that contain one date and N numbers, keeping track of how many such lines
are in F. Let’s say that D is the number of lines containing a date and N numbers. After the D lines are read
in, SG3 should close F.
Here is an example of what a valid file for F might contain. For this file, N=3 and D=7.
,Organism A1,Organism B12,Organism_D4
01/05/1999,56,0,3
02/17/1999,12,4,0
03/05/1999,11,1,3
02/22/2000,0,4,3
06/11/2000,5,10,25
10/13/2001,14,50,29
11/12/2001,0,6,22
If you open that file as a .CSV file using your favorite spreadsheet program, you will get something like the
following. (Some details may be different, depending on what spreadsheet you use. For example, the
dates may or may not retain the leading zeros.) You would be wise to populate a data structure to hold
this information in a way that is organized around the columns and rows shown here.
Organism A1 Organism B12 Organism_D4
01/05/1999 56 0 3
02/17/1999 12 4 0
03/05/1999 11 1 3
02/22/2000 0 4 3
06/11/2000 5 10 25
10/13/2001 14 50 29
11/12/2001 0 6 22
We will refer to the numbers as “abundance counts.” The dates are still called “dates.”
SG3 should output a message to the screen announcing how many different species (names) were found
in the file, and how many different dates were found. The user should be prompted to push ENTER to
continue the program.
SG3 should next open two files for writing: Species.txt and DatedData.txt. The files should reside in the
same directory as SG3. If the files already exist in that directory, overwrite them. Into Species.txt, SG3
should write the names that were on the first line of F, one name per line, in the same order as they were
given in F. Then SG3 should close Species.txt. Next, SG3 should write to DatedData.txt all the dates that
were found in F, in the same order in which the dates appeared in F. Write one date per line in
DatedData.txt. When all the dates in F are written to DatedData.txt, close DatedData.txt.
Next, SG3 should open a file called PresentAbsent.txt in the same directory. If such a file already exists in
that directory, overwrite it. While you create the data for that file, make a data structure, which I will call
PA, that holds exactly the same information you put into the file. PA could be an array, a list of lists, or any
other data structure you and your group find convenient.
The first line of PresentAbsent.txt and the appropriate first row of PA should be identical to the first line
of F, including a blank and all the species names.
At this point, each of the remaining D lines that were in F should contain a date and N abundance counts.
For each line, do the following:
Copy the date into PresentAbsent.txt and into your PA datastructure.
For each abundance count X, determine if X is a 0 or a positive number. If X is a 0, write a 0 to
PresentAbsent.txt. If X is a positive number, write a 1 to PresentAbsent.txt. When this line runs out of
numbers, go to the next line in PresentAbsent.txt. Numbers that you write to PresentAbsent.txt should be
separated by commas. When you have processed all D lines in F, close PresentAbsent.txt.
Note that PresentAbsent.txt could be a .CSV file, but that this specification requires the name given. If
given the example file shown above, SG3 should make this PresentAbsent.txt file:
,Organism A1,Organism B12,Organism_D4
01/05/1999,1,0,1
02/17/1999,1,1,0
03/05/1999,1,1,1
02/22/2000,0,1,1
06/11/2000,1,1,1
10/13/2001,1,1,1
11/12/2001,0,1,1
PA should hold this same information in the same order.
Next, SG3 should print out to the screen a report that lists each date in the data, the maximum abundance
that was measured on that date, and all the species that had that abundance count. (There may be only
one, but there might be more.)
Finally, SG3 should print out to the screen a report that lists all the dates that have exactly the same
presence/absence vector. Notice that there may be multiple different lists in this report. For our example
above, there would be two lists:
1,1,1 occurs three times: 03/05/1999, 06/11/2000, and 10/13/2001.
0,1,1 occurs two times: 02/22/2000, and 11/12/2001.
Format and order the lists in your report in a way that you see as logical and readable. Make sure that
your report is grammatically correct.
Next, SG3 should make a “heat map” of the abundance counts. SG3 should find the highest and lowest
abundance values for each species over all the dates. (NOTE: not the presence / absence numbers, the
abundance numbers.) For each species, use the high and low values to calculate three separate ranges:
low to A, A to B, and B to high; where A and B are calculated so that each of the three has the same size of
range. For example, if the highest abundance of a species S is 90, and the lowest abundance of S is 0, then
A should be 60, and B should be 30. (You are allowed to round fractions when making this split.) Next,
designate each date for S as H, M, or L (for high, medium, and low). If I were you, I’d make this a new data
structure, but that is not required. After you have determined H, M, or L for each date of each species,
print to the screen a “heat map” of all the dates.
One way (which I think is pretty cool) to do a heat map is to use three colors, chosen to communicate
High (or hot), Medium, or Low (or cold). You are not required to use colors, but I hope you and your team
will be up to that challenge. If not, use “type writer graphics,” and assign a visually small character
(perhaps a minus sign) for Low values, a character with a bit more ink for medium (perhaps as small
letter oh, not zero), and a bigger character still for High values (maybe an upper case X). You and your
group may decide on something else, perhaps using ASCI characters that show up well on the screen.
SG3 should open a file called HeatMap.txt for writing. If it already exists, overwrite it.
Whatever you do to make the heat map communicate clearly, print it to the screen, one date per line. Also
print to HeatMap.txt a line that starts with the date, and then alternates blanks and letters. The letter
should be L, M, or H, depending on the abundance count for that species (column) on that date (row).
When all the dates are processed, close the file HeatMap.txt.
Finally, SG3 should look for any species that share EXACTLY the same H, M, and L values for all the dates.
If no species share exactly the same HML values for all the dates, SG3 should print that information to the
screen. If any species DO share exactly the same HML values for all the dates, SG3 should print out that
information to the screen, giving the HML values they share, and the names of all the species that share
those HML values. There may be only one group of such species, or there may be many.
When SG3 has done all these tasks, it should write a polite message to the screen inviting the user to push
ENTER to finish the program. When the user pushes ENTER, the program should halt.
MORE INSTRUCTIONS ABOUT WHAT TO SUBMIT
This assignment is designed for a group of 4 or 5 people. Each group should submit one zipped file. Only
one member of the group should submit the file. The zipped file should include three files:
1. Functioning code that implements the specification in one of the three required languages. More
requirements for your code will be given below. Your code must be contained in a single file, not
multiple files.
2. A separate design document that has a title page that lists the name of our class, the number of
your group, and the people in your group. The document should have page numbers. There should
be a list of any major revisions (or the date of first design, if there were no revisions). Starting on a
new page, there should be a pseudo code design of the program. It should be at a high level of
abstraction so that it fits on one page, single spaced. If you have never done a pseudocode design,
or you would like a reminder of what it is exactly, please see https://www.geeksforgeeks.org/what-is-
pseudocode-a-complete-tutorial/ . That website will be used as the grading standard for your
pseudo-code design. Starting on a separate page, include a second design (some might call it a
description more than a design, but it can function as a design) that is a call graph of your
program. Before you write code, a call graph can help you plan how to structure your code. After
you write code, a call graph can show you that structure. There are tools that analyze code and
produce a call graph. Read about call graphs here: https://en.wikipedia.org/wiki/Call_graph. You
may use an automated call graph generator, or you may build your own call graph. However, hand
drawn call graphs are not acceptable; you must use some sort of drawing tool and uniform shapes
for your call graph.
3. A separate test plan document that has a title page that lists the name of our class, the number of
your group, and the people working on this program. There should be a list of any major revisions
(or the date of first test plan, if there were no revisions.). Starting on a new page, there should be a
list of tests that you planned and then executed before turning in your assignment. Each test
should include, well-marked, the precise input that the test will use, and the precise behavior you
expect to occur after that input. (NOTE: try to NOT just describe the input and output; specify it
EXACTLY. For example, don’t say “test with a positive integer;” instead, say “test with a 12.” There
should also be a record of when the test was done, and what the result was. If the program does
NOT produce the expected output, that failure should be recorded. If multiple tests executions are
required before success, each should be recorded, including who did the test, when, and the result.
The document should have page numbers. For this program, inputs will be either user responses
to prompts, or a file that will be processed by SG3. When specifying a file in a test plan, it is NOT
permitted to merely vaguely describe the file; instead, you must include everything in the file, item
by item, line by line.
4. A user manual written for a biologist who knows nothing of computer programming. Assume that
someone has compiled your program and installed it in a directory for the biologist. Assume that
the biologist is sitting at the keyboard in the proper directory. Now instruct the biologist how to
run your program, what it will do, and where she should look for outputs in the directory when
the program is finished. Be as clear as possible in your explanations. Include screen shots, and
perhaps diagrams showing data structures. The user manual should conform to the title page,
table of contents, and page numbering established for the other documents.
The group should cooperate on such things as a common format for cover pages, pseudocode design, and
for test plans. They should help each other to get everything submitted on time and in working order,
because a part of everyone’s grade depends on the whole group’s accomplishments.
MORE ABOUT THE DOCUMENTATION IN YOUR SOURCE CODE
No matter what programming language you eventually use, start the source code for your program with
an extensive opening comment. The first line of that opening comment must describe which
programming language you are using. You should also mention what development system (or IDE) you
used.
The opening comment in your code must include a section that describes how to compile, build, and
execute your program. These instructions must be sufficiently detailed and clear so that a reader will be
able to compile, build, and execute your program.
The rest of the opening comment must include the names of all the team members working on the
program, the date of submission (or the date you started the program, and major revision dates), the
name and number of our class, an explanation of what the program is designed to do, a description of the
central data structure or structures in your program, and an explanation of any external files used.
Every subprogram in your code (function, procedure, or the like) should include a short opening
comment. That comment should include what the subprogram accomplishes, any global variables it uses,
what each parameter is and does, and what, if anything, the subprogram returns to the caller.
If you use any outside resources to develop your program, for example looking up programming language
details on the Web, then your opening comment should explicitly list those sources, and give at least a
little information about what you found at each resource. If you don’t use ANY outside resources during
development (and that would greatly surprise me), then indicate that no outside resources were used.
Remember, even looking up a syntax detail, or checking out a debug problem in StackOverflow, are
examples of using an outside resource. There is absolutely nothing wrong with doing that, but you must
document it. Give credit where credit is due. Also, if you adapt or adopt a function or code segment from
the Web or perhaps from a previous program you wrote, document it twice: once in your opening
comment, and again in an internal comment wherever the borrowed code appears in your program.
Documentation is a central concern when developing high quality software. I am convinced that the best
software engineering professionals document their work in excruciating detail. That’s exactly what I
want you to do for any assignments in CS 4500.
This documentation is going to be particularly important to you and your teammates in CS 4500. There
are three phases to the SG programs, and they build on each other. You will be in three different teams,
one for each phase of the project. When you move from your first team to your second team (and from
your second team to your third team) you will take your source code and other deliverables with you.
These will prove vital in building the next phase of the project, and any documentation you do in Phase X
is likely to help you in adapting the software to Phase X+1.
In addition to the extensive opening comment, internal comments should explain important data
structures where they are declared and/or used, delineate large sections of code (“paragraphing
comments”), and clarify anything clever or hard to understand in your code. We grade documentation
critically, so I recommend that you spend some time on your opening and internal comments.
PEER EVALUATIONS ARE SUBMITTED SEPARATELY USING A DROPBOX IN CANVAS
After SG3 has been submitted, each member of your team will send me a confidential assessment of the
other team members’ contributions to the project. These are peer evaluations. A team member does not
assess him or herself. The assessments are straightforward. Each team member will submit, via Canvas, a
list of the names of the other team members, giving each member a rank of either 1, 2, or -1. If you only
know about the contributions of one other member of the team, then only evaluate that one person. Here
are what the three possible peer evaluation ratings mean:
• 1 will indicate that the team member made a good faith effort to contribute to the project. We
expect that most of the time, most team members will get a 1 from the rest of the team.
• 2 will indicate that, in your opinion, this particular team member made an extraordinary effort to
contribute to the project. You can only award one 2 in each of your peer assessments, and you are
not required to award any 2 ranking.
• -1 will indicate that, in your opinion, a team member did NOT make a good faith contribution to
the group project.
I hope that there will be very few -1 rankings. But if someone does not make a good faith effort to
contribute to the group effort, then I want to know.
If you or your team have questions about the SG3 project, or about anything else in CS 4500, please email
me at millerkei@umsl.edu.
Take care, and best of luck on SG3.
Keith
