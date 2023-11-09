# Remote Learning, ICT Unit 1 Course Content

1. Build network
2. Program ESP32s
3. ...
4. Profit

## Software Requirements {id="Remote-1-SoftwareRequirements"}

There are no requirement to install software for this semester.

You are required to create an account on [TinkerCAD](https://www.tinkercad.com/). 

When logging in, choose Students and then Sign in with Google. Use your schoolsnet email address to sign in.

![TinkerCADLogin.png](tinkerCADLogin.png)

## Subject Overview {id="Remote-1-SubjectOverview"}

This course introduces you to software development with a focus on Arduino as the environment - the language, IDE and platform.

## Course Introduction {id="Remote-1-CourseOverview"}

This will be general skills for programming. Not dependant on language, just the concepts.
Specific implementations of these topics, in specific languages and software will be demonstrated in the necessary courses.

Some of the languages you may code in are:

- Arduino
- GDscript
- C#
- Python
- PHP

![General Programming Skills](generalProgrammingSkills.png)

### What is programming?

> Programming is the process of giving a computer or device a set of instructions to complete a task.
> 

![Programming Languages Generations](programmingLanguagesGenerations.png)

Essentially, programming (or software development) is problem-solving. Aside from learning syntax, and your programming languages’ additional functionality and libraries, one of the skills you will want to enhance is your problem-solving skills.

### History of Programming languages

#### First Generation: Machine code

![Punch Card](punchCard.png)

- all 0’s and 1’s.

Programmers had to design all code away from the computer and then use punch cards.

If there was a mistake, the programmer would have to re-design and rewrite everything.

#### Second Generation: Assembly Code

![Assembler Language](assembly.png)

- Low-level
- More resembles English than machine code.

Code can only be written for a particular type of CPU

Extremely fast code

Still used today to optimise code (games, Operating Systems etc)

#### Third Generation: High-Level language

![High Level Languages](highLevelLanguage.png)

- More English-like
- Modern Languages

Source Code written in high-level languages is converted into Assembly for the particular computer

Done by the **compiler** or **interpreter**

Introduces more programming structures:

- Loops
- Conditions
- etc

#### Fourth Generation: Higher Abstraction

![SQL Example](sql.png)


Aims to run faster code than 3GL and with fewer lines

Database focus

- SQL

Platform independent (mostly)

#### Fifth Generation: Artificial Intelligence**

![Artificial Intelligence](robotsAI.gif)

- Designed for the computer to solve the problem without the programmer.

The data and constraints are specified

- How the solution should look

Not successful. Yet….. or maybe???

### Programming languages

Programming languages are the languages that are used to code the computer. Similar to different human languages, each have their own set of words and symbols - referred to as the **syntax**.

![Hello World Example](helloWorld.jpeg)

*Most* languages can achieve the same outcome, but use different syntax to achieve the same goal.

Compare the following code snippets which produce the text “Hello World” on a console/terminal or browser.

They all achieve the same output, but using different syntax, and the place they output is different.

#### Python 3

```python
print("Hello World")
```

#### Javascript

```Javascript
console.log("Hello World");
```

#### Arduino

```C++
Serial.println("Hello World");
```

#### PHP

```php
<?php
echo "Hello World!";
?>
```

#### Assembly

```
; x86 32 bit Mac OSX
; to run file, compile and run with the following command
; nasm -f macho hello_world32.asm && ld -macosx_version_min 10.7.0 -o hello_world32 hello_world32.o && ./hello_world32

global start

section .text
start:
    push    dword msg.len
    push    dword msg
    push    dword 1
    mov     eax, 4
    sub     esp, 4
    int     0x80
    add     esp, 16

    push    dword 0
    mov     eax, 1
    sub     esp, 12
    int     0x80

section .data

msg:    db      "Hello, world!", 10
.len:   equ     $ - msg
```

### Executing Code

Once you write the code, you've got have the computer execute (run) it. Depending on the language and environment, there are two broad approaches to executing code - **interpreted** and **compiled**.

**Interpreted**

**Interpreted** code is executed line-by-line by the *interpreter*.

This means that the interpreter takes the first line of code that it can execute, performs that function and then moves to the next line.

**Compiled**

The *compiler* analyses the entire code and then checks to make sure that it there are no syntax, or other, errors and then produces an executable (.exe on windows)

- While some languages are designed to be interpreted or compiled, some languages can be configured to do both.

#### Which is better?

Neither is *better*, it depends on the circumstances. Compiling code can take time to compile the entire code base before it can execute, but once the code is running, it is generally faster.

Interpreted languages can allow for more flexible programming, however tend to execute slower than compiled languages.

> These are broad pros and cons and not representative of all languages.
> 
{style="note"}

### Input, Processing, Output

All code you’ll write (at least at this stage of your career) will fall into this simple structure- your code will take some input, process it in some fashion, and output a result. 

#### Input

This could be a number, a user's name mouse click, a hyperlink, or a combination of a few items.

#### Processing

This is generally where the majority of the logic of your code will fall. The question or problem you’re trying to solve is how to manipulate the input into a useful output.

#### Output

This could be a result of a calculation used in another part of the code or writing to a database, a file, or a number of other parts types of output. 

#### IPO Chart Example

![Completed IPO Chart](chartIPO.jpeg)

#### IPO Chart Template

Here is a template you can use to create your IPO Charts.

[IPO Chart Template](https://docs.google.com/document/d/15Z3BKzqbFT7EnutHYzFpX6Hff8vbE91ow20xJkksAIc/edit?usp=drivesdk)

### Arduino Implementation

> Be aware - The term "Arduino" can refer to either;
> 1. The Arduino programming language, 
> 2. The Arduino IDE, or 
> 3. The Arduino board.
>
{style="note"}
    
### Arduino Sketches

> Arduino Code is referred to as Sketches.
>
{style="note"}

Each Arduino sketch needs to have the same basic structure.

**At a minimum**, the sketch needs to have the setup() and loop() functions.

![Structure of an Arduino Sketch example with code](Structure_of_an_Arduino_Sketch_example_with_code.png)

### Practical Exercises

In this initial stage, you'll be using [TinkerCAD](https://www.tinkercad.com/) to virtually program Arduino Uno board.

![TinkerCAD Front Page](tinkerCADFrontPage.png)

Click the link to join the Class for this subject.

[Classroom login | Tinkercad](https://www.tinkercad.com/joinclass/QM5M8HWQJSG6)

Sign into Tinkercad with Google, using your school credentials.

![Join The Classroom](tinkerCADJoinClassroom.png)

Click on the first activity - “1 Blink”.

Choose `Circuit` from the `Create new design` menu.

![Select Circuits](tinkerCADSelectCircuit.png)

Change the Basics components menu to Starters Arduino. Find `Blink` in that list.

![TinkerCAD Blink Example](tinkerCADBlink.png)

Drag the Blink module to the editing area

![TinkerCAD Blink Circuit](tinkerCADBlinkCircuit.png)

Click on the Code button, and change the code type to Text.

Here you will see the "Hello World" code for Arduino, also referred to as Blink. At this stage, don't worry too much about the specific code - you'll learn that later. Just notice how the code is written, the syntax and the functions used - `setup()` and `loop()`.

![Code View](tinkerCADCode.png)

You can start the code running by using the Start Simulation button.

You should see the LED flashing on and off every second.

Congratulations - you've (potentially) written your first Arduino Sketch!

![Start Simulation](tinkerCADStartSimulation.gif)

### Extension

1. Goal: Update the code to flash on and off every half a second. 
    
    What part of the code would you need to change? 
    
2. Change the LED to be on pin 10. 
    
    What needs/needed to be changed?
    

### Review

1. How were the first computers programmed?
2. Where did the name "bug" originate?
3. What is this "Hello World" you speak of?
4. In plain language, What is the difference between interpreted and compiled code?
    1. Expand on your explanation by adding technical details.
5. What is the best programming language to learn? Why?
6. What does the term “Arduino” refer to?
7. How does the Arduino communicate between the computer and itself?
8. What do you use to display data sent from the Arduino?
9. What types of pins does an Arduino Uno have?
