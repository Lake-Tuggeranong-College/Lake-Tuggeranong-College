# Software Development Fundamentals Course Theory

# Course Contents

- Overview
    
    
    # Course Overview
    
    <aside>
    ‼️ This course uses the generic, language agnostic "Software Development Fundamentals" course as a base. The Fundamentals course will introduce the topics / concepts for each stage, and this page has the language / platform specific implementation.
    
    </aside>
    
    <aside>
    💁‍♀️ In short - read and understand the theory, code the practical.
    
    </aside>
    
    This will be general skills for programming. Not dependant on language, just the concepts.
    Specific implementations of these topics, in specific languages and software will be demonstrated in the necessary courses.
    
    Some of the languages you may code in are:
    
    - Arduino
    - GDscript
    - C#
    - Python
    - PHP
    
    ![General Programming Skills.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/General_Programming_Skills.png)
    
    ## What is programming?
    
    > Programming is the process of giving a computer or device a set of instructions to complete a task.
    > 
    
    ![DE3905E0-7D18-4473-98B8-1E60725FF556.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/DE3905E0-7D18-4473-98B8-1E60725FF556.png)
    
    Essentially, programming (or software development) is problem-solving. Aside from learning syntax, and your programming languages’ additional functionality and libraries, one of the skills you will want to enhance is your problem-solving skills.
    
    ## History of Programming languages
    
    ### First Generation
    
    ![Untitled](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Untitled%201.png)
    
    **Machine code**
    
    - all 0’s and 1’s.
    
    Programmers had to design all code away from the computer and then use punch cards.
    
    If there was a mistake, the programmer would have to re-design and rewrite everything.
    
    ### Second Generation
    
    ![Untitled](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Untitled%202.png)
    
    **Assembly Code**
    
    - Low-level
    - More resembles English than machine code.
    
    Code can only be written for a particular type of CPU
    
    Extremely fast code
    
    Still used today to optimise code (games, Operating Systems etc)
    
    ### Third Generation
    
    ![Untitled](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Untitled%203.png)
    
    **High-Level language**
    
    - More English-like
    - Modern Languages
    
    Source Code ****written is converted into Assembly for the particular computer
    
    Done by the **compiler** or **interpreter**
    
    Introduces more programming structures:
    
    - Loops
    - Conditions
    - etc
    
    ### Fourth Generation
    
    ![Untitled](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Untitled%204.png)
    
    **Higher abstraction**
    
    Aims to run faster code than 3GL and with fewer lines
    
    Database focus
    
    - SQL
    
    Platform independent (mostly)
    
    ### Fifth Generation
    
    ![Untitled](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Untitled.gif)
    
    **Artificial Intelligence**
    
    - Designed for the computer to solve the problem without the programmer.
    
    The data and constraints are specified
    
    - How the solution should look
    
    Not successful. Yet….. or maybe???
    
    ## Programming languages
    
    Programming languages are the languages that are used to code the computer. Similar to different human languages, each have their own set of words and symbols - referred to as the **syntax**.
    
    ![9BC26002-A4B8-4499-A531-08DA5A799C7A.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/9BC26002-A4B8-4499-A531-08DA5A799C7A.jpeg)
    
    *Most* languages can achieve the same outcome, but use different syntax to achieve the same goal.
    
    Compare the following code snippets which produce the text “Hello World” on a console/terminal or browser.
    
    They all achieve the same output, but using different syntax, and the place they output is different.
    
    ### Python 3
    
    ```python
    print("Hello World")
    ```
    
    ### Javascript
    
    ```jsx
    console.log("Hello World");
    ```
    
    ### Arduino
    
    ```arduino
    Serial.println("Hello World");
    ```
    
    ### PHP
    
    ```php
    <?php
    echo "Hello World!";
    ?>
    ```
    
    ### A**ssembly**
    
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
    
    ## Executing Code
    
    Once you write the code, you've got have the computer execute (run) it. Depending on the language and environment, there are two broad approaches to executing code - **interpreted** and **compiled**.
    
    **Interpreted**
    
    I**nterpreted** code is executed line by line by the *interpreter.*
    
    This means that the interpreter takes the first line of code that it can execute, performs that function and then moves to the next line.
    
    **Compiled**
    
    The *compiler* analyses the entire code and then checks to make sure that it there are no syntax, or other, errors and then produces an executable (.exe on windows)
    
    <aside>
    ‼️ While some languages are designed to be interpreted or compiled, some languages can be configured to do both.
    
    </aside>
    
    ### Which is better?
    
    Neither is *better*, it depends on the circumstances. Compiling code can take time to compile the entire code base before it can execute, but once the code is running, it is generally faster.
    
    Interpreted languages can allow for more flexible programming, however tend to execute slower than compiled languages.
    
    <aside>
    ‼️ These are broad pros and cons and not representative of all languages.
    
    </aside>
    
    ## Input, Processing, Output
    
    All code you’ll write (at least at this stage of your career) will fall into this simple structure- your code will take some input, process it in some fashion, and output a result. 
    
    ### Input
    
    This could be a number, a user's name mouse click, a hyperlink, or a combination of a few items.
    
    ### Processing
    
    This is generally where the majority of the logic of your code will fall. The question or problem you’re trying to solve is how to manipulate the input into a useful output.
    
    ### Output
    
    This could be a result of a calculation used in another part of the code or writing to a database, a file, or a number of other parts types of output. 
    
    ### IPO Chart Example
    
    ![6F444F51-80BC-4F3E-BFE8-E1869D084D5D.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/6F444F51-80BC-4F3E-BFE8-E1869D084D5D.jpeg)
    
    ### IPO Chart Template
    
    Here is a template you can use to create your IPO Charts.
    
    [IPO Chart Template](https://docs.google.com/document/d/15Z3BKzqbFT7EnutHYzFpX6Hff8vbE91ow20xJkksAIc/edit?usp=drivesdk)
    
    # Key Terms
    
    [Key Terms](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Key%20Terms%20516ac2874fc14203b9518d8f14f1d66d.csv)
    
- Version Control System / Github
    
    
    # Version Control System / Github
    
    ## What does Git do?
    
    - Manage projects with **Repositories**
    - **Clone** a project to work on a local copy
    - Control and track changes with **Staging** and **Committing**
    - **Branch** and **Merge** to allow for work on different parts and versions of a project
    - **Pull** the latest version of the project to a local copy
    - **Push** local updates to the main project
    
    [https://www.w3schools.com/git/git_intro.asp](https://www.w3schools.com/git/git_intro.asp)
    
    ## What is Git?
    
    [https://www.youtube.com/watch?v=2ReR1YJrNOM](https://www.youtube.com/watch?v=2ReR1YJrNOM)
    
    ![A304378B-A96E-41D4-8E47-FC9E173BF4D3.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/A304378B-A96E-41D4-8E47-FC9E173BF4D3.jpeg)
    
    ### Github Account
    
    Create a Github Account [here](https://github.com/signup). Use your schoolsnet email address when it asks for your email address.
    
    ## How to use Git
    
    Depending on the setup, you may use Github in different methods. Choose the option below that best suits your environment.
    
- Computational Thinking
    
    
    # **What is Computational Thinking?**
    
    [https://www.bbc.com/bitesize/guides/zp92mp3/revision/1](https://www.google.com/url?q=https%3A%2F%2Fwww.bbc.com%2Fbitesize%2Fguides%2Fzp92mp3%2Frevision%2F1&sa=D&sntz=1&usg=AFQjCNFLFykzM1LBBM1Ie3VSRI-JuGUp0w)
    
    Computers can be used to help us solve problems. However, before a problem can be tackled, the problem itself and the ways in which it could be solved need to be understood.
    
    Computational thinking allows us to do this.
    
    Computational thinking allows us to take a complex problem, understand what the problem is and develop possible solutions. We can then present these solutions in a way that a computer, a human, or both, can understand.
    
    ![EmbeddedImage.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/EmbeddedImage.jpeg)
    
    [https://youtu.be/mUXo-S7gzds](https://youtu.be/mUXo-S7gzds)
    
    # **The four cornerstones of computational thinking**
    
    There are four key techniques (cornerstones) to computational thinking:
    
    - **decomposition** - breaking down a complex problem or system into smaller, more manageable parts
    - **pattern recognition** – looking for similarities among and within problems
    - **abstraction** – focusing on the important information only, ignoring irrelevant detail
    - **algorithms** - developing a step-by-step solution to the problem, or the rules to follow to solve the problem
    
    Each cornerstone is as important as the others. They are like legs on a table - if one leg is missing, the table will probably collapse. Correctly applying all four techniques will help when programming a computer.
    
    ![EmbeddedImage.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/EmbeddedImage.png)
    
    # **Computational thinking in practice**
    
    A complex problem is one that, at first glance, we don't know how to solve easily.
    
    Computational thinking involves taking that complex problem and breaking it down into a series of small, more manageable problems (**decomposition**). Each of these smaller problems can then be looked at individually, considering how similar problems have been solved previously (**pattern recognition**) and focusing only on the important details while ignoring irrelevant information (**abstraction**). Next, simple steps or rules to solve each of the smaller problems can be designed (**algorithms**).
    
    Finally, these simple steps or rules are used to **program** a computer to help solve complex problems in the best way.
    
    # Decomposition
    
    Decomposition is one of the four cornerstones of Computer Science. It **involves breaking down a complex problem or system into smaller parts** that are more manageable and easier to understand. The smaller parts can then be examined and solved, or designed individually, as they are simpler to work with.
    
    [https://www.youtube.com/watch?v=rxsYpP2-omg](https://www.youtube.com/watch?v=rxsYpP2-omg)
    
    # Problem Solving Approaches
    
    ## Top-Down Approach
    
    <aside>
    ❗ The main problem is broken into smaller subsystems.
    
    </aside>
    
    Starting with the overall problem, and break it into stages, or areas, which are smaller more manageable tasks. Continue this process until the "problems" are small, easy to solve tasks.
    
    For instance: **Making Pancakes.** Initially, this may be daunting (especially if you haven't made pancakes before).
    
    Break the task into smaller manageable tasks:
    
    1. Buy Ingredients
    2. Make Pancakes
    3. Eat Delicious Pancakes.
    
    [https://www.youtube.com/watch?v=0NdThGHhX8M](https://www.youtube.com/watch?v=0NdThGHhX8M)
    
    Then approach each individual task separately. For example.
    
    ![top-down 1.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/top-down_1.png)
    
    ![top-down 2.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/top-down_2.png)
    
    ![I really want pancakes.](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/top-down_3.png)
    
    I really want pancakes.
    
    ## Bottom-Up Approach
    
    <aside>
    ❗ Solve small manageable tasks, integrating them together until an overall solution is reached.
    
    </aside>
    
    This approach starts by creating a list of all outstanding issues or considering the system as a whole, and categorise them into similar jobs, and then solving those smaller, more specific jobs first. Once the parts of the system are solved, then work is begun to integrate them.
    
    An example of this approach could be designing a library system using Object Oriented Programming (an advanced Programming topic) approach. In this approach, the designers of the system would first identify individual objects that the system would need - book, magazine, staff member, etc - and then model them in code. Once the individual objects are coded, then a "controller" piece of code would focus on having the individual objects interact as needed.
    
    # Algorithm Design
    
    [https://www.youtube.com/watch?v=6hfOvs8pY1k](https://www.youtube.com/watch?v=6hfOvs8pY1k)
    
    # Key Terms
    
    [Key Terms](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Key%20Terms%20565f6287272d4e3b8f00143510e73b65.csv)
    
- Mathematical & Logic Operations
    
    
    # Mathematical & Logic Operations
    
    # Mathematical Operations
    
    When programming in any language, you can perform the usual set of mathematical equations; adding, subtracting, division and multiplication. 
    
    You can also perform many more equations and complex processes using either built into the language or by using an external library. 
    
    <aside>
    💡 In *most* programming situations, you need to follow the standard structure of the assignment statement. 
    
    $variable = expression$
    
    For instance to calculate the year the user was born:
    
    $bornInYear = currentYear - getAgeFromUser()$
    
    </aside>
    
    ![12781063064_95c9c66c96_c.jpg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/12781063064_95c9c66c96_c.jpg)
    
    # Logic operations
    
    ## Logic Gates & Truth Tables
    
    Logic gates are used to display and understand the logic in a circuit or piece of code.
    
    Logic gates process signals which represent **true** or **false**. Normally the positive supply voltage +Vs represents true and 0V represents false. Other terms used for the true and false states are shown in the table, it is best to be familiar with them all.
    
    Gates are identified by their function: NOT, AND, NAND, OR, NOR, EX-OR and EX-NOR. Capital letters are normally used to make it clear that the term refers to a logic gate.
    
    ![https_lh3.googleusercontent.com-NX18QZQHZK4XfFw6ohJ2fIAAAAAAAAe1gXISU-9E8oBkcMUlyd9_3SwjKS2fstkYCwCLkCGAYYCws0Screen2BShot2B2019-12-122Bat2B9.42.312Bam.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/https_lh3.googleusercontent.com-NX18QZQHZK4XfFw6ohJ2fIAAAAAAAAe1gXISU-9E8oBkcMUlyd9_3SwjKS2fstkYCwCLkCGAYYCws0Screen2BShot2B2019-12-122Bat2B9.42.312Bam.png)
    
    [https://www.youtube.com/watch?v=kbXwFWMl6WA&ab_channel=MrPowell%27sComputerScienceChannel](https://www.youtube.com/watch?v=kbXwFWMl6WA&ab_channel=MrPowell%27sComputerScienceChannel)
    
    There are a number of fundamental logic gates that you need to be aware of.
    
    ## **NOT Gate**
    
    A NOT gate takes one input and produces a single output. The NOT gate simply "flips" the input, so TRUE becomes FALSE, and FALSE becomes TRUE.
    
    ![Truth Table - NOT.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Truth_Table_-_NOT.png)
    
    [https://circuitverse.org/simulator/embed/42660](https://circuitverse.org/simulator/embed/42660)
    
    ## **AND Gate**
    
    An AND gate takes two inputs and produces a single output. For the output to be TRUE, then **both** of the inputs have to be TRUE.
    
    ![Truth Table - AND.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Truth_Table_-_AND.png)
    
    [https://circuitverse.org/simulator/embed/42653](https://circuitverse.org/simulator/embed/42653)
    
    ## **OR Gate**
    
    An OR gate takes two inputs and produces a single output. For the output to be TRUE, then **either one or both** of the inputs have to be TRUE.
    
    ![Truth Table - OR.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Truth_Table_-_OR.png)
    
    [https://circuitverse.org/simulator/embed/42658](https://circuitverse.org/simulator/embed/42658)
    
    ## **NAND Gate**
    
    A NAND gate takes two inputs and produces a single output and is the combination of an AND gate with a NOT gate, so it is the opposite of an AND gate. For the output to be TRUE, then **either or both** of the inputs have to the FALSE.
    
    ![Truth Table - NAND.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Truth_Table_-_NAND.png)
    
    [https://circuitverse.org/simulator/embed/42661](https://circuitverse.org/simulator/embed/42661)
    
    ## **NOR Gate**
    
    A NOR gate takes two inputs and produces a single output and is the combination of an OR gate with a NOT gate, so it is the opposite of an OR gate. For the output to be TRUE, then **both** of the inputs have to the FALSE.
    
    ![Truth Table - NOR.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Truth_Table_-_NOR.png)
    
    [https://circuitverse.org/simulator/embed/42662](https://circuitverse.org/simulator/embed/42662)
    
    ## **XOR and XNOR**
    
    The final two gates are **eXclusive** OR and NOR. In this case, Exclusive means the output is TRUE **only if either inputs are true, not both**.
    
    ![Truth Table - XOR and XNOR.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Truth_Table_-_XOR_and_XNOR.png)
    
    [https://circuitverse.org/simulator/embed/42663](https://circuitverse.org/simulator/embed/42663)
    
    ---
    
    ### Logic Game Symbols
    
    Here is a summary of the Logic Gate Symbols that are standards.
    
    These images are used to define the logic circuits.
    
    <aside>
    ❗ Notice how the NOR and NAND gates incorporate the small circle on the right of the symbol to indicate the NOT aspect.
    
    </aside>
    
    ![https_lh3.googleusercontent.com-5osQKHoHQKEXfBNWp8tv5IAAAAAAAAevwb3etvLzqrqYUrE45PFO1m5p-XURBqzyOgCLkCGAYYCws0NV_0501_Byers_Large.jpg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/https_lh3.googleusercontent.com-5osQKHoHQKEXfBNWp8tv5IAAAAAAAAevwb3etvLzqrqYUrE45PFO1m5p-XURBqzyOgCLkCGAYYCws0NV_0501_Byers_Large.jpg)
    
    Aaannd now for the humour:
    
    ![icnl6sxtugp81.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/icnl6sxtugp81.jpeg)
    
    # Logic Circuits
    
    Logic Gates can be combined to make logic circuits. The output from each of the logic gates determine the input for the subsequent logic gate in the sequence
    
    ## **Simple Memory Circuit**
    
    With a simple logic gate circuit you can design the logic of a single bit of memory.
    
    [https://circuitverse.org/simulator/embed/memory-circuit-fd73493e-2499-45f7-ad76-d385094093f0](https://circuitverse.org/simulator/embed/memory-circuit-fd73493e-2499-45f7-ad76-d385094093f0)
    
    # Boolean Algebra
    
    Boolean algebra is the written, mathematical form of logic games and circuits.
    
    Each of the logic gates described above can be written as a mathematical equation, and perform some standard, and not so standard, algebraic functions to them.
    
    For instance, an AND gate, is written as a multiplication. Assuming you have two inputs into the AND gate, the mathematical equation would be $A.B$ or just $AB$.
    
    ## Symbols Summary
    
    A NOT gate has a line over the top, such as:
    
    $$
    { \overline A}
    $$
    
    An OR gate is an addition:
    
    $$
    A + B
    $$
    
    A NOR gate is a combination of the NOT gate and the OR gate - an addition with a line over the equation:
    
    $$
    {\overline{A+B}}
    $$
    
    Similarly, the NAND gate is a combination of the NOT and AND gates:
    
    $$
    {\overline{AB}}
    $$
    
    The XOR symbol is the following: ${\bigoplus}$, so an XOR statement would appear as:
    
    $$
    {A\bigoplus B}
    $$
    
    And XNOR is, again the combination of the XOR and NOT gates
    
    $$
    { \overline{ A\bigoplus B}}
    $$
    
    ## Examples
    
    Consider the boolean equation: $((AB) + (AC))$ `(A AND B) OR (A AND C)`. This would be represented by the following logic circuit:
    
    [https://circuitverse.org/simulator/embed/boolean-logic-exercise-1](https://circuitverse.org/simulator/embed/boolean-logic-exercise-1)
    
    This equation - $A {\overline{B}} + C(AB)$ `(A AND NOT B) OR (C AND(A AND B))`. 
    
    [https://circuitverse.org/simulator/embed/a-and-not-b-or-c-and-a-and-b](https://circuitverse.org/simulator/embed/a-and-not-b-or-c-and-a-and-b)
    
    ## Simplification
    
    You can simplify Boolean algebra as with "normal" algebra.
    
    ### Example
    
    [Boolean Algebra Simplification Example 1.MP4](https://drive.google.com/file/d/1MIKxPdLqM5ZAwEtlnMSewu17UZ9HO4cV/view?usp=drivesdk)
    
    ![C Or Nand(ab)-1.jpg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/C_Or_Nand(ab)-1.jpg)
    
    <aside>
    ❗ Why Simplify? Because it can make logic easier when coding logic into your system.
    
    </aside>
    
    ![[https://www.allaboutcircuits.com/technical-articles/boolean-identities/](https://www.allaboutcircuits.com/technical-articles/boolean-identities/)](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2021-11-25_at_1.00.59_pm.png)
    
    [https://www.allaboutcircuits.com/technical-articles/boolean-identities/](https://www.allaboutcircuits.com/technical-articles/boolean-identities/)
    
    ### Example
    
    ![boolean-mathematics-factoring2.webp](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/boolean-mathematics-factoring2.webp)
    
    # Karnaugh Maps
    
    Karnaugh Maps are a useful process and tool to simplify complex boolean expression. They offer similar benefits to the simplification process in mathematical equations.
    
    [https://www.youtube.com/watch?v=A0XupfXiKIo](https://www.youtube.com/watch?v=A0XupfXiKIo)
    
    [https://www.youtube.com/watch?v=QK8uPfZESh4](https://www.youtube.com/watch?v=QK8uPfZESh4)
    
    [https://www.youtube.com/watch?v=7jI0Hv9h2t8](https://www.youtube.com/watch?v=7jI0Hv9h2t8)
    
    # Review
    
    1. Go to [https://learn.electronics-course.com](https://learn.electronics-course.com/) (sign in with your school Google Account to save your progress) and complete the following projects:
        1. NAND Gate
        2. Half Adder
        3. Care Safety Buzzer
    
    # Key Terms
    
    [Key Terms](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Key%20Terms%202f74fb99dbaa4cb1a2ddff10f7e2dac7.csv)
    
- Variables and Variables
    
    
    # Variables and Data Types
    
    # Variables
    
    <aside>
    ❗ Variables are a way of storing data in a computer program.
    
    </aside>
    
    Regardless of the language you’re programming in, you will at some stage need to store some data in memory (RAM)
    
    To consider what variables are, You can think of memory in a computer as a series of boxes. 
    
    ![3C4D29DD-EDEE-4ADB-AE9E-A69642C08EC2.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/3C4D29DD-EDEE-4ADB-AE9E-A69642C08EC2.jpeg)
    
    Each one of these boxes can be given a unique name.
    
    ![A8E47C84-4E7D-46E1-BE98-2B3FEE53E655.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/A8E47C84-4E7D-46E1-BE98-2B3FEE53E655.jpeg)
    
    Variables can be named *almost* anything. Generally, they cannot start with a number. 
    
    <aside>
    ❗ The way you name variables is called the **naming convention.** Each programming language has its own standard naming convention. This is discussed in [Style Guide](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735.md)
    
    </aside>
    
    Now that variables have been named, you can store data in the box. For instance, you may set the following data to the four variables in the example:
    
    ```
    HighScore is set to 25.
    ButtonValue is set to HIGH.
    Username is set to “administrator"
    Password is set to “securePassword”
    ```
    
     
    
    ![BAB793D5-1D31-4578-AB81-6685D172FDCA.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/BAB793D5-1D31-4578-AB81-6685D172FDCA.jpeg)
    
    Once the values have been stored, you can retrieve the values by using the name of the box (variable name). For instance HighScore = HighScore + 5, would set the HighScore to 30.
    
    Memory in the device (desktop, laptop, phone, tablet, microcontroller etc) is sandboxed to the application, and sub-divided into various sections, one being set aside for variables. That section is then used as the application needs, allocating specific memory addresses for particular variables. The number and structure of the memory addresses is dependant on many things, one of which is the **data type** of the variable.
    
    # Data types
    
    The type of data being stored in variables is important, and must be considered when using variables. 
    
    Data Types can be divided up into different categories, initially into `Primitives` and `Non-Primitives`.
    
    Primitives are the most simplest types of data, which can be used to create more complex, non-primitive data structures.
    
    This is just an example of the breakdown of the data types - each programming language can implement variables and data types in their own manner.
    
    <aside>
    ⁉️ Characters may appear to be in the incorrect position, under Numeric, however this is due to the fact that Characters are stored in memory as the equivalent [ASCII character number](https://www.asciitable.com/). For instance, 'A' would be stored as `01000001`
    
    </aside>
    
    ![Data Type Tree.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Data_Type_Tree.png)
    
    ## Primitive data types
    
    Primitives are the base types of data, including booleans, integers, characters etc. 
    
    <aside>
    ❗ Primitives may differ between programming languages.
    
    </aside>
    
    Primitives are the most basic versions of data types - whole numbers, decimal point numbers, Booleans (true or false), individual characters, etc.
    
    The types of data that can be stored in each of these are:
    
    ![data types examples.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/data_types_examples.png)
    
    ## Non-Primitive Data Types
    
    These data types offer more complexity, but need to be understood and managed in more detail. 
    
    Some examples of non-primitive data types are : Arrays, Lists, Dictionaries, but the most common one you'll deal with when starting out is a `String`.
    
    A string is a collection of characters in a sequence. In a string, each character can be considered an individual (primitive) character. In the example here, each letter is a character.
    
    ![Data Types - Strings example.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Data_Types_-_Strings_example.png)
    
    Strings are useful non-primitive data types because you can manipulate the individual letters to perform certain actions, such as changing to upper or lower case, combining strings, removing unwanted characters, and many others.
    
    # Assignment statements
    
    Assignment statements are very important in any programming language. 
    
    > Assignment statements are where the code assigns a value to a variable.
    > 
    
    In the majority of modern, high-level languages an assignment statement follows this general convention:
    
    $$
    variable = expression
    $$
    
    The expression (one the right-hand side of the equals) is calculated and the “answer” or result is stored in the variable (one the left hand side).
    
    Some examples:
    
    | Example | Explanation |
    | --- | --- |
    | Age = 42 | Sets the Age variable to the integer 42 |
    | Name = “Anakin Skywalker” | Assigns “Anakin Skywalker” to the variable Name. |
    | Answer = value1 + value2 | Calculates the addition of the contents of value1 and value2 and stores the result in the variable Answer. |
    
    The right hand side of the assignment statement can be incredibly complex, but the left hand side will (almost) always a single variable. But there’s always exceptions to the rule.
    
    # Review
    
    1. How is data stored in memory?
    2. What’s the difference between primitive and non-primitve data types?
    3. What is type inference?
        1. Find three programming languages that use type inference.
    4. What is the opposite of type inference?
        1. Find three programming languages that don’t use type inference.
    5. What does strongly typed and weakly typed languages mean?
    
    [Key Terms](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Key%20Terms%208605e6bc93f744649dc0f2a266858da7.csv)
    
- Algorithm Design - Sequence
    
    
    # Algorithm Design - Sequence
    
    # Summary
    
    If a set of instructions are executed in the order that they appear (from the top to the bottom), then this is a sequence.
    
    ![maxresdefault.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/maxresdefault%202.jpeg)
    
    # Explanation
    
    In programming, a sequence is a series of steps that occur in a particular order and each step must be complete before the next begins. So, `step1` is completed and then `step2` is run and when complete `step3` starts and so on.
    
    For instance, think about your morning routine.
    
    1. Get out of bed
    2. Shower
    3. Get dressed
    4. Eat breakfast
    5. Brush teeth
    6. Leave house
    7. Etc.
    
    Now, your *actual* routine may differ from this, however each step must be complete before the next starts, and many of them can’t easily be done out of order.
    
    Another example of Sequencing is in recipes. Once you have the ingredients, the actual making of the food item is a sequence of steps, which is the basis for an *algorithm.*
    
    ![639B9496-3368-48A1-816D-ED9154FF142F.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/639B9496-3368-48A1-816D-ED9154FF142F.jpeg)
    
    # Flowchart Example
    
    ```mermaid
    flowchart TD;
        A[Place All Ingredients in a food processor fitting with a steel blade]-->B[Cover and process until pureed];
        B-->C[Serve with pita chips, warm pitas, or veggies];
    		C-->D[Store remaining hummus in an airtight container in the fridge for up to 10 days]
    
    ```
    
    [Key Terms](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Key%20Terms%20526c5687e0e14693a4e92d2205733e19.csv)
    
- Algorithm Design - Decisions
    
    
    # Algorithm Design - Decisions
    
    # Summary
    
    Decisions, or *selection*, is a programming structure where different steps can take place depending on particular *conditions.*
    
    ![maxresdefault.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/maxresdefault%201.jpeg)
    
    # Explanation
    
    Making decisions in software development is critical as it allows the code to perform a different set of tasks depending on the current state of certain variables when the code is executed (or run).
    
    The basic structure of the syntax to a decision in code will in one of two forms:
    
    ## if...then
    
    The standard syntax structure for this is: 
    
    `IF <condition>` 
    
    `THEN` 
    
    `<THEN block statement/s>` 
    
    This works by checking the condition and if the condition is true, then the statements in the THEN block are executed.
    
    ## if...then...else
    
    The standard syntax structure for this is the same as the IF...THEN, but includes an optional ELSE clause: 
    
    `IF <condition>` 
    
    `THEN` 
    
    `<THEN block statement/s>` 
    
    `ELSE` 
    
    `<ELSE block statement/s>` 
    
    This is executed in the same manner as the standard IF...THEN structure, however if the condition is false, the ELSE block statement/s will be executed.
    
    One of the critical parts of the decision is the *condition.*
    
    ## Condition
    
    The **condition** is the part of the decision which determines which path is taken after the decision is made.
    
    As an example, consider the end of the day of school or work: You look at time - if it's after 3:30pm, you go home. In more programming terms, this could be written as `if time>3:30pm, then go home.` In this case, `time>3:30pm` is the condition.
    
    # Example One - Temperature
    
    ## Overview
    
    You're given the task to write a simple thermometer alert. The system is to output the temperature on an LCD screen. The instructions are:
    
    `If the temperature is above 30℃, the temperature is shown in red.` 
    `If the temperature is less than 30℃ display the temperature in blue.`
    
    ## Data
    
    | Temperature | Output Colour |
    | --- | --- |
    | > 30 | Red |
    | < 30 | Blue |
    
    ## Algorithm
    
    This flowchart shows the coding **logic** required to complete the specifications of the system.
    
    ```mermaid
    flowchart TD
      terminalStart([Start])
    	decision1[/Get temperature from sensor/]
    	q1{Temperature > 30}
    	terminalEnd([end])
    	
    	terminalStart-->decision1
    	decision1-->q1
    	q1--> |Yes| outputTrue[/Display temperature on LCD in RED/]
    	q1--> |No| outputFalse[/Display temperature on LCD in BLUE/]
    	outputTrue --> terminalEnd
    	outputFalse --> terminalEnd
    
    	
    ```
    
    # Example Two - Grades
    
    ## Overview
    
    Let's say you're writing a grade sorting algorithm for an exam. Grades in this algorithm are determined by the score the student receives on the exam, according to this table shown.
    
    The code would need to be written to read the score for each student and output the correct grade. 
    
    This would require a decision (or number of) to behave similar to:
    
    `If the score is above 90, then output A.`
    
    `If the score is greater than or equal to 75 AND the score is  less than or equal to 89, then output B.`
    
    `If the score is greater than or equal to 55 AND the score is  less than or equal to 74, then output C.`
    
    `If the score is greater than or equal to 45 AND the score is  less than or equal to 54, then output D.`
    
    `If the output is less than 44, then output E.`
    
    ## Data
    
    | Score | Grade |
    | --- | --- |
    | >90 | A |
    | 75-89 | B |
    | 55-74 | C |
    | 45-54 | D |
    | <44 | E |
    
    ## Algorithm
    
    ```mermaid
    flowchart TB
      terminalStart([Start])
    	input1[/Get Student Store/]
    	case1{Score > 90}
    	case2{Score &#8805 75 AND Score &#8804 89}
    	case3{Score &#8805 55 AND Score &#8804 74}
    	case4{Score &#8805 45 AND Score &#8804 54}
    	case5{Score &#8804 44}
    	grade1[/Grade = A/]
    	grade2[/Grade = B/]
    	grade3[/Grade = C/]
    	grade4[/Grade = D/]
    	grade5[/Grade = E/]
    	terminalEnd([end])
    	
    	terminalStart --> input1
    	input1 --> case1
    	case1 -->|No|case2
    	case1 -->|Yes|grade1
    	case2 -->|No|case3
    	case2 -->|Yes|grade2
    	case3 -->|No|case4
    	case3 -->|Yes|grade3
    	case4 -->|No|case5
    	case4 -->|Yes|grade4
    	case5 -->|Yes|grade5
    	grade1 --> terminalEnd
    	grade2 --> terminalEnd
    	grade3 --> terminalEnd
    	grade4 --> terminalEnd
    	grade5 --> terminalEnd
    
    ```
    
    [Key Terms](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Key%20Terms%2042443e59040d4f69befed71c2e7626eb.csv)
    
- Algorithm Design - Loops
    
    
    # Algorithm Design - Loops
    
    # Explanation
    
    ![maxresdefault.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/maxresdefault%201.jpeg)
    
    ## Video
    
    [https://youtu.be/2e0HmKTSq2k](https://youtu.be/2e0HmKTSq2k)
    
    ## Notes
    
    [Presentation - Loops.pdf](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Presentation_-_Loops.pdf)
    
    # Summary
    
    Loops are a programming structure that allows the code to repeat blocks of code multiple times. 
    
    This saves you coding all possible situations.
    
    # Explanation
    
    Computers are really good at repetitive tasks, whereas humans are, *well human*, and make mistakes. So, software development relies on loops (or repetition) to achieve goals that require the same, or similar, steps to be completed.
    
    A loop structure allows us to code a block of code which will execute any number of times, including zero. 
    
    <aside>
    ❗ Loops, similar to decisions, rely heavily on [conditions](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735.md) as part of their structure.
    
    </aside>
    
    There are a number of general loop structures that are available in (almost) all languages.
    
    ## Important Term
    
    There are a few keywords that are important with loops:
    
    ## While Loop
    
    This loop is a block of code that is repeated *while* the condition is true.
    
    However the condition is only tested once the loop has completed the iteration.
    
    <aside>
    ❗ The condition is at the **top** of the loop.
    
    </aside>
    
    ### Flowchart Example
    
    ```mermaid
    flowchart TD
      terminalStart([Start])
    	bread[Put Bread in Toaster]
    	watch[Watch Toaster]
    	toast[Eat delicious toast]
    	isToastReady{Toast Ready?}
    	terminalEnd([End])
    
    	terminalStart-->bread
    	bread-->isToastReady
    	isToastReady-->|No|watch
    	watch-->isToastReady
    	isToastReady-->|Yes|toast
    	toast --> terminalEnd
    ```
    
    ## Do... While Loop
    
    Extremely similar to a while loop, however the block of code in a do... while loop is repeated *at least once* before the condition is checked.
    
    <aside>
    ❗ The condition is at the **bottom** of the loop.
    
    </aside>
    
    ### Flowchart Example
    
    ```mermaid
    flowchart TD
      terminalStart([Start])
    	bread[Put Bread in Toaster]
    	watch[Watch Toaster]
    	toast[Eat delicious toast]
    	isToastReady{Toast Ready?}
    	terminalEnd([End])
    
    	terminalStart-->bread
    	bread-->watch
    	watch-->isToastReady
    	isToastReady-->|No|watch
    	isToastReady-->|Yes|toast
    	toast --> terminalEnd
    ```
    
    ## For Loop
    
    For loops are a more structured loop than either of the while loops. For loops include a **Loop Control Variable** which determine how many times the loop is run.
    
    ### Flowchart Example
    
    ```mermaid
    flowchart TD
      terminalStart([Start])
    	loopControlVariable[Loop Control Variable Installation]
    	body[Body of Loop]
    	update[Update Loop Control Variable]
    	isReady{Has End  Condition been met?}
    	terminalEnd([End])
    
    	terminalStart-->loopControlVariable
    	loopControlVariable-->isReady
    	isReady---->|Yes| terminalEnd
    	isReady-->|No| body
    	body-->update
    	update-->isReady
    ```
    
    # Review
    
    [Key Terms](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Key%20Terms%200191da6bf21f4eddb85c67c833c79c87.csv)
    
- Algorithm Design - Modularisation
    
    
    # Algorithm Design - Modularisation
    
    # Explanation
    
    Modular programming is a software design technique that involves separating the functionality of a program into independent, interchangeable modules that can be used in different combinations to create multiple applications.
    
    ![1_TxDhmsq9LG0p4au_RULnVA.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/1_TxDhmsq9LG0p4au_RULnVA.png)
    
    ## Video
    
    [https://youtu.be/TU3JzrwS2as](https://youtu.be/TU3JzrwS2as)
    
    ## Notes
    
    [Presentation - Modularisation.pdf](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Presentation_-_Modularisation.pdf)
    
    # Summary
    
    Modularisation is the process of splitting a large computer program into smaller, more manageable blocks of code. At this stage, the main structure for this process is called a **function.**
    
    A function is a small subset of code which can be run (called) at different times during the execution of a program. The use of functions allow you to modularise your code to solve different, smaller problems in order to solve the overall problem.
    
    # Functions
    
    Functions are used to break the larger program into smaller, more manageable sections. This allows you, the developer, to focus on different parts of the program in different sections at different times.
    
    Additionally, it can allow multiple developers to work on the same code base, but focusing on different functionality minimising interference. 
    
    Functions allow you to reuse your functions in different parts of your code (and avoid repeating blocks of code), or in other programs, as well as provide you with a level of abstraction. 
    
    <aside>
    ❗ Functions can have many names. Depending on the context, they can be called **methods, modules, procedures** and many others.  They are all *functionally* the same, pun intended.
    
    </aside>
    
    ## Abstraction Example
    
    Using the [top-down approach](https://www.notion.so/Computational-Thinking-16248ba104c84a14858882259cafe2f0), instead of writing down all the steps required for a task to be completed, you could focus on the higher level logic of the code, and identify the sections of the code to "farm out" to a function.
    
    For instance, using the pancake analogy, you would first identify the higher level logic:
    
    1. Buy ingredients
    2. Cook Pancakes
    3. Eat Pancakes
    
    The implementation of (the details on how to complete) each of these stages would be a function. This is known as **abstraction.** 
    
    > Abstraction is the process of identifying the overall logic (e.g. "buy ingredients") and ignoring the details (for now) of what that entails.
    > 
    
    [https://www.youtube.com/watch?v=L1-zCdrx8Lk](https://www.youtube.com/watch?v=L1-zCdrx8Lk)
    
    Another example of abstraction
    
    ## DRY vs WET
    
    ![7339BA26-AAF2-4F12-A216-704700EF5063.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/7339BA26-AAF2-4F12-A216-704700EF5063.png)
    
    Functions are one approach to reducing repeated code. Repeated code is undesirable in code as it can be harder to maintain (I.e. update and fix in the future) as the developer will have to change multiple parts of the code to solve one problem.
    
    [https://www.youtube.com/watch?v=-P-jMG6zVPA](https://www.youtube.com/watch?v=-P-jMG6zVPA)
    
    ## Function Parameters / Arguments
    
    Functions have three main parts to it (discussed later in [IPO Charts](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735.md)), which can be simplified into Input, Processing, and Output. Some functions don't require any input to run, such as a function which loads a set file each time the program starts. However some functions require some form of input in order to start, such as a function to find the average of three numbers - the function requires the three numbers before it can calculate the result.
    
    <aside>
    💡 Functions **do not** require input as a rule, but they all require processing and some form of output.
    
    </aside>
    
    <aside>
    💡 Occasionally developers can use **parameters** and **arguments** interchangeably, but they are different. When the function is running, the variables defined in the function heading are called **parameters**. In the part of the code that calls the function, the data that is "sent" to the function is referred to as an **argument**.
    
    </aside>
    
    ### Parameter Example
    
    ```mermaid
    flowchart TD
    subgraph calculateGST
    terminalStartCalculateGST(["calculateGST(productPrice)"])
    terminalEndCalculateGST(["End"])
    gstComponent["GSTComponent = productPrice / 11"]
    displayResult[The GST Component of productPrice is GSTComponent]
    
    terminalStartCalculateGST-->gstComponent
    gstComponent-->displayResult
    displayResult-->terminalEndCalculateGST
    end
    subgraph Main
    terminalStart([Start])
    terminalEnd([End])
    getPrice1[/productPrice=get price from user/]
    getPrice2[/productPrice=get price from user/]
    callGST1[["calculateGST(productPrice)"]]
    callGST2[["calculateGST(productPrice)"]]
    
    terminalStart-->getPrice1
    getPrice1-->callGST1
    callGST1-->getPrice2
    getPrice2-->callGST2
    callGST2-->terminalEnd
    end
    
    ```
    
    This program calculates the GST component of the price of a product being sold.
    
    The overall logic of the code is: 
    
    - *Get the price of a product from the user, divide that price by 11, and tell the user the GST component of that price.*
    
    The flowchart here shows that being done twice, and uses a function to calculate the GST and output it to the user.
    
    You can see the flow of the logic here:
    
    ![RPReplay_Final1639017678.2021-12-09 13_45_38.gif](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/RPReplay_Final1639017678.2021-12-09_13_45_38.gif)
    
    ## Return Data
    
    Generally, data that is modified within a function is lost when the function completes - it goes out of scope. This is not *always* true, if you're using Global variables, however this should be minimised as much as possible. More accurately, any variables that are declared within a function are "forgotten" by the program when the function completes.
    
    Fitting with the Input...Process...Output structure, functions **return** data, which is the output stage.
    
    Functions *generally* need to specify the data type of the data being returned from the function. This can be referred to as the **return type**, or the **methods type.**
    
    If a function doesn't return anything, the return type is **void** meaning nothing.
    
    ```mermaid
    flowchart TD
    subgraph calculateGST
    terminalStartCalculateGST(["calculateGST(productPrice)"])
    terminalEndCalculateGST(["Return GSTComponent"])
    gstComponent["GSTComponent = productPrice / 11"]
    
    terminalStartCalculateGST-->gstComponent
    gstComponent-->terminalEndCalculateGST
    end
    subgraph Main
    terminalStart([Start])
    terminalEnd([End])
    getPrice1[/productPrice=get price from user/]
    getPrice2[/productPrice=get price from user/]
    displayResult1[The GST Component of productPrice is GSTComponent]
    displayResult2[The GST Component of productPrice is GSTComponent]
    callGST1[["calculateGST(productPrice)"]]
    callGST2[["calculateGST(productPrice)"]]
    
    terminalStart-->getPrice1
    getPrice1-->callGST1
    callGST1-->displayResult1
    displayResult1-->getPrice2
    getPrice2-->callGST2
    callGST2-->displayResult2
    displayResult2-->terminalEnd
    end
    
    ```
    
    # Functions Design
    
    These topics describe how you could/should consider when designing your functions.
    
    ## IPO Charts
    
    One method to start designing function is to determine and document their Inputs (if any), what processing needs to occur and then what Outputs are needed (if any).
    
    This can be done using an IPO (Input Process Output) Chart.
    
    ![maxresdefault.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/maxresdefault.jpeg)
    
    ## Implementation Hiding
    
    The concept of Implementation Hiding is used when deciding when and how functions are used. Importantly as well, is that the concept revolves around the remainder of the program not knowing, and not needing to know, how the implementation of the function is achieved. 
    
    [https://www.youtube.com/watch?v=zaqiMBoGFO4](https://www.youtube.com/watch?v=zaqiMBoGFO4)
    
    <aside>
    ‼️ Implementation Hiding is the concept of the low level details are "hidden" from the remainder of the program through a function call.
    
    </aside>
    
    Example:
    
    Let's say you have an application developed which reads and writes data to a database. In testing, the application is written for SQLite (which is easier for a single user), however when the system is to be deployed in the wild, the database needs to be changed/upgraded to MySQL (much more robust and scalable). This is not necessarily an easy task.
    
    If the application has been written well, the access to the database is only done in a certain number of functions, which would be easier to change the implementation of to the new database system. 
    
    The remainder of the application code wouldn't need to change, and just use the functions to request or write data from/to the database, whereas the functions deal with the specific details of how to access the new/different database.
    
    ## Cohesion & Coupling
    
    <aside>
    💡 You should strive to increasing cohesion.
    You should strive to reduce coupling.
    
    </aside>
    
    ### Cohesion
    
    Cohesion is the concept of how each function should solve one job (and one job only). 
    
    If a function is completing two tasks, it's referred to a **low cohesion** and you you should strongly consider splitting it into more functions so each solve a smaller part of the task.
    
    Why? It's so you can reuse the function in different stages of the code without causing expected outcomes (by it completing an unintended task).
    
    ### Coupling
    
    Coupling is the measure of the strength of connection between two functions - as in how much information is exchanged between the two functions.
    
    **Tight coupling** is where two functions exchange a lot of information
    
    **Loose coupling** is where functions do not rely on each other at all, or very minimal.
    
    ![Screen Shot 2021-12-10 at 12.30.35 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2021-12-10_at_12.30.35_pm.png)
    
    [https://www.youtube.com/watch?v=e25ZjHaiSlE](https://www.youtube.com/watch?v=e25ZjHaiSlE)
    
    This video focuses on classes and object oriented programming, however the concepts are similar to function design.
    
    ## Variable Scope
    
    Variables, constants etc that are declared within a function, are only accessible from within that variable. When the function completes, the data for those variables is “lost” in memory.
    
    # Review
    
    1. In plain language, describe a function.
        1. Update the plain language description using technical language. 
    2. What’s the difference between a parameter and argument?
    
    [Key Terms](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Key%20Terms%20dfcafff9cdb34f799c51fa3446ce1181.csv)
    
- Flowcharts
    
    
    # Flowcharts
    
    ## Flowcharts Overview
    
    Flowcharts show the *****logic***** of an algorithm without specific code syntax.
    
    [https://www.youtube.com/watch?v=kxZJv56BxU8](https://www.youtube.com/watch?v=kxZJv56BxU8)
    
    ![a1e0e7936.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/a1e0e7936.jpeg)
    
    ## **Flowchart Writing Tips**
    
    This page is a tutorial on how to write/make tutorials: [https://www.lucidchart.com/pages/what-is-a-flowchart-tutorial](https://www.google.com/url?q=https%3A%2F%2Fwww.lucidchart.com%2Fpages%2Fwhat-is-a-flowchart-tutorial&sa=D&sntz=1&usg=AFQjCNHWnPrmDeScQr3b3ceOtgWZWRPl7g)
    
    [https://www.youtube.com/watch?v=AjoSfSd-5Nw](https://www.youtube.com/watch?v=AjoSfSd-5Nw)
    
    ![Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/https_lh3.google.comu0pAF1QipMz36NJBUiv4FIOlZNfo9vWrePgJAfwwTGW3ADHw1008-h1344.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/https_lh3.google.comu0pAF1QipMz36NJBUiv4FIOlZNfo9vWrePgJAfwwTGW3ADHw1008-h1344.png)
    
    ## Mermaid
    
    [Mermaid](https://mermaid.js.org/) is a text-based language for creating diagrams, and specifically Flowcharts.
    
    There are similar languages (PlantUML for one) however mermaid has the ability to be rendered on Github when it’s included in a markdown file.
    
    This site contains a comprehensive list of the options available using Mermaid.
    
    [Basic overview of creating flowcharts using Mermaid](https://ckeditor.com/blog/basic-overview-of-creating-flowcharts-using-mermaid/)
    
    As an example, in a Markdown file, you can include a block such as the one shown below and when viewing the Markdown file on Github, the flowchart is rendered as shown.
    
    ```
    ```mermaid
    flowchart TD
        terminalStart([Start])
        %% Comment
        terminalEnd([End])
        thresholdSet(distanceThreshold = 30)
        setPiezoPin(piezoPin = 2)
        currentDistanceReading(distanceRead = response from Sonar)
        activatePiezo(write HIGH to piezoPin)
        deactivatePiezo(write LOW to piezoPin)
    
        ifDistanceLessThanThreshold{distanceRead < distanceThreshold}
    
        terminalStart --> thresholdSet
        thresholdSet --> setPiezoPin
        setPiezoPin --> currentDistanceReading
        currentDistanceReading --> ifDistanceLessThanThreshold
        ifDistanceLessThanThreshold --> |True| activatePiezo
        ifDistanceLessThanThreshold --> |False| deactivatePiezo
        deactivatePiezo --> terminalEnd
        activatePiezo --> terminalEnd
    ```
    ```
    
    ![SCR-20230120-sfb-2.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/SCR-20230120-sfb-2.png)
    
    <aside>
    ‼️ **If** you’re developing in a Jetbrains tool, you can enable Mermaid rendering in the IDE. Go to Settings, then Languages & Frameworks → Markdown and tick Mermaid. You may need to install first.
    
    ![Untitled](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Untitled.png)
    
    </aside>
    
    ## Creating Flowcharts - Mermaid
    
    ### Mermaid Symbols and Syntax
    
    This cheat sheet demonstrates the nodes available and the associated syntax.
    
    ![[https://jojozhuang.github.io/tutorial/mermaid-cheat-sheet/](https://jojozhuang.github.io/tutorial/mermaid-cheat-sheet/)](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-05-05_at_9.16.28_am.png)
    
    [https://jojozhuang.github.io/tutorial/mermaid-cheat-sheet/](https://jojozhuang.github.io/tutorial/mermaid-cheat-sheet/)
    
    ### Create a Markdown File
    
    Open Visual Studio Code, or any text editor, Create a new file and immediately save it as `logic.md` into the directory identified above. ****
    
    <aside>
    ❓ .md indicates it is a Markdown file. Markdown is a simplified language which can add formatting styles to plain text documents.
    
    </aside>
    
    ![Screen Shot 2022-04-29 at 10.02.00 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_10.02.00_pm.png)
    
    To make sure the workflow is configured correctly, go back into GitHub Desktop and it should show that the file has been created. 
    
    $* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 
    
    ![Screen Shot 2022-04-29 at 10.06.19 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_10.06.19_pm.png)
    
    ### Flowchart Structure
    
    In the text editor, create the start to the mermaid flowchart, by adding the following at the top of the file - `flowchart TD`
    
    The ````mermaid` and ````` on lines 1 and 3 inform Github to display the text as Mermaid diagrams. You can add headings and other standard text before and after the mermaid charts.
    
    This indicates that the diagram will be a flowchart, and that it will be **T**op **D**own.
    
    <aside>
    ❓ [Possible FlowChart orientations are](https://mermaid-js.github.io/mermaid/#/./flowchart?id=flowchart-orientation):
    
    TB - top to bottom
    TD - top-down/ same as top to bottom
    BT - bottom to top
    RL - right to left
    LR - left to right
    
    </aside>
    
    ![Screen Shot 2022-04-29 at 10.16.25 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_10.16.25_pm.png)
    
    Create the two basic nodes first - the start and the end.
    
    `terminalStart([Start])`
    `terminalEnd([End])`
    
    <aside>
    ❓ The order of the nodes and connections in mermaid is irrelevant. The flowchart will be displayed (rendered) after reading in the whole diagram.
    
    </aside>
    
    <aside>
    ❓ The indentation shown is not important, and not required in Mermaid. It may make it easier to read, particularly when there are multiple flowcharts listed in one file.
    
    </aside>
    
    ![Screen Shot 2022-04-29 at 10.16.29 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_10.16.29_pm.png)
    
    ### Preview Flowchart in Visual Studio Code (Optional)
    
    If you’re using Visual Studio Code, you can install an extension to preview the mermaid flowcharts without having to commit and push to Github.
    
    To do so, click on the Extensions button, search for Mermaid and then install the "Markdown Preview Mermaid Support” extension.
    
    ![Screen Shot 2022-05-16 at 9.50.29 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-05-16_at_9.50.29_pm.png)
    
    Once that’s installed, you can open the preview of the file, with rendered flowchart by using the following key command:
    
    | Windows | CTRL K + V |
    | --- | --- |
    | Mac | ⌘ K + V |
    | Linux | CTRL K + V |
    
    Alternatively, you can press the Preview button in the top right of the window.
    
    ![Screen Shot 2022-05-16 at 10.04.08 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-05-16_at_10.04.08_pm.png)
    
    This splits the window with the original file on the left, and the rendered version on the right.
    
    ![Screen Shot 2022-05-16 at 10.05.27 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-05-16_at_10.05.27_pm.png)
    
    ### View the file on Github
    
    In the browser, navigate to the Github repository, or click View on Github in Github Desktop, and click on [logic.md](http://logic.md/). The file should display as shown.
    
    ![Screen Shot 2022-04-29 at 10.18.38 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_10.18.38_pm.png)
    
    ### Create Nodes and Connections
    
    Determine the first steps required in the logic for each individual behaviour.
    
    The first behaviour in the sample project (shown above) is: `When a person gets too close (**sonar**) to the house, an alarm is sounded (**piezo)**.`
    
    To break this down, first the distance value would need to be read from the sonar sensor. **If** this value is below a certain threshold, then activate the piezo. This would require a number of nodes to achieve:
    
    1. Set the threshold variable to a value. Let’s say 50cm.
    2. Set piezoPin to pin connected to piezo.
    3. Read the distance value from the sensor
    4. If distance value < 50
        1. activate piezo
    
    Create the sequence (default) nodes first.These are points 1, 2 3, and 4a above.
    
    - Name the nodes appropriately using **lowerCamelCase**. Same with variables.
        
        ![camel-case.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/camel-case.png)
        
    
    ![Screen Shot 2022-04-29 at 10.39.02 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_10.39.02_pm.png)
    
    ```mermaid
    thresholdSet(distanceThreshold = 50)
    setPiezoPin(piezoPin = 22)
    currentDistanceReading(distanceRead = response from Sonar)
    activatePiezo(write HIGH to piezoPin)
    ```
    
    The last node to create is the if statement (point 4 above). This uses slightly different syntax. Instead of standard brackets, `{` and `}` are used to indicate a  decision symbol.
    
    ![Screen Shot 2022-04-29 at 10.41.35 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_10.41.35_pm.png)
    
    ```mermaid
    ifDistanceLessThanThreshold{distanceRead < distanceThreshold>}
    ```
    
    Refresh or view the document on [Github.com](http://Github.com) to see the individual nodes.
    
    ![Screen Shot 2022-04-29 at 10.47.59 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_10.47.59_pm.png)
    
    ### Build Connections
    
    Now that all the individual nodes are created, it’s time to join them together to create the flowchart, showing the algorithm steps in order.
    
    The general syntax for creating a connection with an arrow between two nodes is shown here.
    
    The `A` and `B` in this example are the **ids** of each node.
    
    ```mermaid
    A-->B
    ```
    
    In the Smart House Example, to create the connection between terminalStart and thresholdSet, the code is as follows.
    
    ```mermaid
    terminalStart --> thresholdSet
    ```
    
    ![Screen Shot 2022-04-29 at 10.56.51 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_10.56.51_pm.png)
    
    Create all of the other connections as required.
    
    ```mermaid
    terminalStart --> thresholdSet
    thresholdSet --> setPiezoPin
    setPiezoPin --> currentDistanceReading
    currentDistanceReading --> ifDistanceLessThanThreshold
    ```
    
    ![Screen Shot 2022-04-29 at 11.01.42 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_11.01.42_pm.png)
    
    The decision connections is a little more complicated as there are two output from the decision - whether the condition is true or false. Luckily, mermaid gives you the ability to add text to the connection line. In this example the connection is made and `True` is displayed on the line in the diagram. 
    
    ```mermaid
    ifDistanceLessThanThreshold --> |True| activatePiezo
    ```
    
    ![Screen Shot 2022-04-29 at 11.04.35 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_11.04.35_pm.png)
    
    Complete the output from the decision if it is false, and also the the next step after activatePiezo. At this stage, these are connecting to the same node - terminalEnd.
    
    ```mermaid
    ifDistanceLessThanThreshold --> |False| terminalEnd
    activatePiezo --> terminalEnd
    ```
    
    ![Screen Shot 2022-04-29 at 11.07.08 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_11.07.08_pm.png)
    
    ### View the Completed Flowchart
    
    Open/Refresh the file in [github.com](http://github.com/) and see the final version.
    
    ![Screen Shot 2022-04-29 at 11.11.38 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_11.11.38_pm.png)
    
    ### Continue Development
    
    One flowchart has been completed, however there are more behaviours.
    
    Add in a heading above the mermaid block indicating the behaviour being attempted.
    
    ![Screen Shot 2022-04-29 at 11.17.01 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_11.17.01_pm.png)
    
    After the end of the first flowchart, add a heading in for the next behaviour algorithm, and start the mermaid block.
    
    ![Screen Shot 2022-04-29 at 11.18.15 pm.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-04-29_at_11.18.15_pm.png)
    
    **Continue developing the diagrams as required.** See the link in the resources section above for more details on other possible nodes and connections.
    
    ## **Tips**
    
    ### **"Wait for <event>"**
    
    If you're writing your flowchart and you have a section which has to wait for an event, such as waiting for a button to press, you can include it in a flowchart by using a simple loop. For example:
    
    [](https://lucid.app/documents/embeddedchart/36da5ebd-ad4d-4023-bf42-296accd848bd)
    
- Style Guide
    
    
    # Style Guide
    
    A style guide is a document in an organisation or programming environment which describes how programmers should (amongst other things) name their variables, and organise and comment their code.
    
    ![Naming-Conventions-1366x768.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Naming-Conventions-1366x768.png)
    
    # Clean code
    
    You should strive for **clean code**. This is where your code is readable by other humans, not just executable by the computer. There are a number of considerations that fall under Clean Code - first of which is the naming conventions described above.
    
    Some rules for writing clean code:
    
    1. Following existing naming conventions (either project, organisation or programming language)
    2. Keep is Simple!
    3. Be consistent
        1. If you do things one way in the code already, keep doing them the same way
    4. Avoid negative conditions
    5. Functions:
        1. Do **one** thing
        2. Should be kept small
        3. Minimise arguments as much as possible
        4. Have no side effects
    6. Comments
        1. Always explain yourself
        2. Don't be redundant
        3. Explain the purpose of the block of code
        4. Clarify the block of code
    7. Indent code appropriately
    
    [Clean Code: A Handbook of Agile Software Craftsmanship | 1st edition | Pearson](https://www.pearson.com/store/p/clean-code-a-handbook-of-agile-software-craftsmanship/P100002065712/9780132350884)
    
    Clean Code, by Robert Martin, is considered one of the best resources for how to write clean cod
    
    # Naming Conventions
    
    Naming Conventions is a programming topic that focuses on naming variables, functions and other structures in a standardised format. There are a number of standard formats used throughout programming:
    
    [Key Terms](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Key%20Terms%20fe42f388bd314579acdca3429c9b3aff.csv)
    
    Variable and function names generally have to start with a letter, and then can include numbers or another other character, and therefore you can generally name variables whatever you want. However, it is a Good Idea™  to name your variables and functions with useful or descriptive names.
    
    # Naming Guidelines
    
    Now that you know the structure needed, here are some rules on how to name your variables/functions etc.
    
    <aside>
    💡 These guidelines can be a hot topic amongst developers - these are **not** hard and fast rules, and they will change depending on the organisation or project you're working on.
    
    </aside>
    
    ## Meaningful Names
    
    Name your variables and functions with descriptive names that indicate what the data or purpose of it is. And avoid abbreviations.
    
    For instance, if your variable is to store the moisture value read from a sensor, you could use the name `moistureValue`. If you, or another person, is reading the code, they will immediately understand what the variable is used for.
    
    If your focus on brevity, and use a name similar to `mVal`, there is immediate ambiguity as to what the variable is used for.
    
    ## Avoid Generic / Temporary Names
    
    Use names that are specific to the variable or function, and don't use temporary names. 
    
    <aside>
    💡 **Don't** use names like `a`, `i`, `temp`, `tmp`, `variable1` etc.
    
    </aside>
    
    ## Function Names
    
    Along with the previous guidelines, functions have an additional guideline:
    
    **When naming functions, use verbs (doing words).** 
    
    Function names should describe the action being performed - `loadFile()`, `saveData()`, `readSensor()`, `sanitiseData()`, `addNumbers()` etc.
    
    If the function is returning some data, you can use "get" as the prefix - `getButtonData()`.
    
    ---
    
    # Code Commenting
    
    <aside>
    ‼️ Also known as **internal documentation**.
    
    </aside>
    
    Comments are messages written in plain language to explain your code. They are used for documentation, and do not form part of the program logic.
    
    ## Block Comments
    
    Block comments are multi-line comments at the beginning of a code file, which explain the purpose of the code, the author and date, and any other information that is relevant.
    
    For example:
    
    ```jsx
    // This code demonstrates the loading and saving of text files to the SD card.
    // Written by Ryan Cather
    // Last Modified : Semester 2, 2021
    ```
    
    ## Inline comments
    
    Inline comments are short, usually single line comments which explain the purpose and logic of line/s of code. For example:
    
    ```jsx
    // Calculate the interest.
    Set interest = balance * INTEREST_RATE
    // Add the interest to the balance.
    Set balance = balance + interest
    ```
    
    Inline comments can also be placed after the program code, to minimise the length of code file:
    
    ```jsx
    Set interest = balance * INTEREST_RATE // Calculate the interest.
    Set balance = balance + interest // Add the interest to the balance.
    ```
    
    ## Function Header Comments
    
    Each function should have a comment explaining the purpose of the function, the arguments (if any) and the data type and description of the return value (if any).
    
    <aside>
    ‼️ Also known as **docstrings** and other names in different languages.
    
    </aside>
    
- Data Structures
    
    
    # Data Structures
    
    # Data Structures Overview
    
    ## Video
    
    [https://youtu.be/XW9GCUo6-E0](https://youtu.be/XW9GCUo6-E0)
    
    ## Notes
    
    [Data Structures.pdf](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Data_Structures.pdf)
    
    # Array
    
    An array is a collection of variables in an organised manner. 
    
    <aside>
    💡 The benefit of organising your code in such a manner becomes more clear with more data that is related. Additionally, sometimes you're not aware of how many values you will need to store when the code is written, and the data is collected when the program is running.
    
    </aside>
    
    Arrays are a list of items that are related in some way - Student Scores, Student Names, Movie Release Dates, Book Titles etc.
    
    [https://www.youtube.com/watch?v=kbv3N4-h6iA](https://www.youtube.com/watch?v=kbv3N4-h6iA)
    
    In many languages the data stored in the array has to be the same type - strings, integers etc.
    
    ## Array Example 1 - Days Of The Week
    
    A simple example of array usage is keeping track of the days of the week.  Instead of creating 7 different variables to hold the name of the day, you could create one array called `daysOfWeek` with a structure like this:
    
    | Index | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
    | --- | --- | --- | --- | --- | --- | --- | --- |
    | Element | Sunday | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday |
    
    There are a number of additional benefits to structuring the data in an array such as this. For instance, assume that you were writing code to store the day of the week in a text file or a database. It is much more efficient to store an integer rather than a string. 
    
    If you were to write code to randomly generate a day of the week, rather than creating some complex code, you could simply perform the logic shown here.
    
    Using the randomly generated integer (from 0 to 6), you could use that as the index for the data that you wish to print.
    
    This can be used in many different situations - months for example.
    
    ```mermaid
    flowchart TD
    	terminalStart(Start)
    	terminalEnd(End)
    	generateRandom[randomDay = Generate a random number between 0 and 6 respectively]
    	printDay["Print dayOfWeek[randomDay]"]
    
    	terminalStart --> generateRandom
    	generateRandom--> printDay
    	printDay --> terminalEnd
    ```
    
    ## Array Example 2 - Birthday Counter
    
    You are tasked with this problem:
    
    `Imagine a line with an infinite number of people in it. How many people would you need to check before you found a birthday for every day of the year?` 
    
    How would you approach this? You could do trial and error - which *could* work, however it would most like be inaccurate.
    
    Or, you could use arrays to try and solve this problem.
    
    ```mermaid
    flowchart TD
    	terminalStart(Start)
    	terminalEnd(End)
    	initialiseArray["birthdaysFound = array of 365 boolean"]
    	initialiseVariables1["numberOfBirthdaysFound = 0"]
    	initialiseVariables2["birthdayIndex = 0"]
    	initialiseVariables3["peopleCounter = 0"]
    	generateRandom[birthdayIndex = Generate a random number between 0 and 365 respectively]
    	setTrue["dayOfYear[randomDay] = true"]
    	conditionWhile{"numberOfBirthdaysFound<365"}
    	ifFalse{"birthdaysFound[birthdayIndex]==false"}
    	increaseBirthdaysFound["numberOfBirthdaysFound++"]
    	increasePeopleCounter["peopleCounter++"]
    	outputTotal["It took {peopleCounter} number of people to find ALL birthdays"]
    	
    
    	terminalStart --> initialiseArray
    	initialiseArray-->initialiseVariables1
    	initialiseVariables1-->initialiseVariables2
    	initialiseVariables2-->initialiseVariables3
    	initialiseVariables3-->conditionWhile
    	conditionWhile-->|true|generateRandom
    	generateRandom--> ifFalse
    	ifFalse-->|true|setTrue
    	ifFalse-->|false|increasePeopleCounter
    	setTrue-->increaseBirthdaysFound
    increaseBirthdaysFound-->increasePeopleCounter
    increasePeopleCounter-->conditionWhile
    	
    	conditionWhile -->|false| outputTotal
    outputTotal-->terminalEnd
    ```
    
    ### Java Implementation
    
    Here’s the code to implement this in Java, which would be similar in other C-based languages. 
    
    ![Screen Shot 2022-02-22 at 8.55.53 am.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Screen_Shot_2022-02-22_at_8.55.53_am.png)
    
    [Key Terms](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Key%20Terms%205a2ab83c59a043038527390d43deaaa5.csv)
    
    # Key Value Pair
    
    <aside>
    ‼️ Depending on the language, this may also be referred to as : hash, hashmap, associated array. They are functionally the same.
    
    </aside>
    
    A Key Value Pair is another collection of data, where the data is organised with a *key* and a *value*.
    
    Key Value Pair may appear to be similar, however differs from an array in that the data is not ordered, and can’t be accessed through an index value.
    
    When considering Key Value Pair in programming, you can think about a standard book dictionary - each entry has a key (the word) and then the value (the definition). Key Value Pair in code have the same structure, although you the developer can decide what the key and values are.
    
    To access (read or write) the value the code would use the key: `studentScores("Ryan") = 25` would find the key "Ryan" and set the value to be 25.
    
    ![14264475338_ca40835497_b.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/14264475338_ca40835497_b.jpeg)
    
    ![1_oNuaSOlSozUchdxiOE1ieQ.jpeg](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/1_oNuaSOlSozUchdxiOE1ieQ.jpeg)
    
    <aside>
    💁 Key Value Pairs could be used in situations where you would need to store (in memory or on disk) settings for your application, such as high scores, user names etc.
    
    </aside>
    
    ## Key Value Pair Example - Movie Ratings
    
    For instance, you might want to store the ratings of Star Wars movies from IMDB. Instead of creating variables for each of the Awesome Star Wars movies - A New Hope, The Last Jedi, Caravan of Courage etc - *which is possible* (but not ideal), you can create a Key Value Pair which stores the values in a list of items. 
    
    The values (59% etc) could be stored in a Key Value Pair and accessed in code as (for example) `starWarsMovieRatings.`
    
    ![Array - Star Wars movies.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Array_-_Star_Wars_movies.png)
    
    # Review
    
    [Key Terms](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Key%20Terms%20448590a67e014fff96acdb2aae0c2774.csv)
    
- Debugging
    
    
    # Debugging
    
    ![debugging.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/debugging.png)
    
    # Error Messages
    
    <aside>
    ‼️ Debugging code and projects is just as important as being able to code in the first place!
    
    </aside>
    
    # Rubber Duck Debugging
    
    ![programming-duck-debug.png](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/programming-duck-debug.png)
    
    [https://www.youtube.com/watch?v=huOPVqztPdc](https://www.youtube.com/watch?v=huOPVqztPdc)
    
- Technical Reports
    
    
    # Technical Report
    
    ## Example Design Document
    
    [High Level Design for Advanced Workspace Report](https://docs.google.com/document/d/1DxFAaFNCgF09B0XQcA0ysZ9jn6SKooa3NudKMQ1yxKY/edit?usp=drivesdk)
    
    ## Example: Documentation Analysis
    
    ### Format Template
    
    For each entry in the rubric, you can follow this basic template for a response-
    
    ```mermaid
    graph LR;
    Introduction-->Evidence-->Analysis;
    Analysis-->crit["Critical Analysis"];
    ```
    
    So this *could* equate to 
    
    1. Include a screenshot of code
    2. Explaining how it works (Analysis), using technical language and linking it to other code or resources (research). You may also delve into explaining the technical details involved (again, research)
    3. Critical Analysis (or Evaluation). Look at what you have submitted, and then evaluate it whether it solves the problem that was required or what you were attempting to solve. Compare and contrast to other options for solving the same problem. 
    
    ### Example - “Design Process of Each Item - Design Process”
    
    > This is an entry in the rubric.
    > 
    
    <aside>
    ‼️ “Each Item” in this case means the individual component and the accompanying code.
    This example covers the SD Card.
    
    </aside>
    
    ---
    
    ### Micro SD Card Module.
    
    The Micro SD Card module in this project (below) is Serial Peripheral Interface (SPI) module which enables an Arduino, and other Microcontrollers, to read and write data to micro SD cards.
    
    ![Micro-SD-TF-Card-Module-Pinout-SPI.png](../Assessment%20Examples%20ba9ee48cf95a4ca78c4a3653b16831a0/Micro-SD-TF-Card-Module-Pinout-SPI.png)
    
    ### Wiring
    
    Different from the other components in this project, this device communicates over SPI, which is a specific communications protocol requiring specific pins to be used on the Arduino. The SPI pins for the Arduino Uno and Mega are shown here.
    
    | Pin | Uno | Mega |
    | --- | --- | --- |
    | MISO | 12 | 50 |
    | MOSI | 11 | 51 |
    | SCK | 13 | 52 |
    | CS | 10 | 53 |
    
    Therefore the *logical* wiring diagram for this module is:
    
    ![Screen Shot 2022-06-13 at 9.45.57 pm.png](../Assessment%20Examples%20ba9ee48cf95a4ca78c4a3653b16831a0/Screen_Shot_2022-06-13_at_9.45.57_pm.png)
    
    ### Code
    
    The Arduino code required to enable this module is:
    
    Configuration
    
    ```arduino
    // SD Card Module
    #include <SPI.h>
    #include <SD.h>
    // SD Card
    #define SDpin 10
    
    // Real Time Clock (RTC)
    #include "RTClib.h"
    RTC_Millis rtc;     // Software Real Time Clock (RTC)
    DateTime rightNow;  // used to store the current time.
    ```
    
    `Setup()`
    
    ```arduino
    // SD Card initialisation
      Serial.print("Initializing SD card...");
      if (!SD.begin(SDpin)) {
        Serial.println("initialization failed!");
        while (1);
      }
    
      // Real Time Clock (RTC)
      rtc.begin(DateTime(F(__DATE__), F(__TIME__)));
    
      logEvent("System Initialisation Start");
    ```
    
    `logEvent()`
    
    ```arduino
    void logEvent(String dataToLog) {
      /*
         Log entries to a file on an SD card.
      */
      // Get the updated/current time
      DateTime rightNow = rtc.now();
    
      // Open the log file
      File logFile = SD.open("events.csv", FILE_WRITE);
      if (!logFile) {
        Serial.print("Couldn't create log file");
        abort();
      }
    
      // Log the event with the date, time and data
      logFile.print(rightNow.year(), DEC);
      logFile.print(",");
      logFile.print(rightNow.month(), DEC);
      logFile.print(",");
      logFile.print(rightNow.day(), DEC);
      logFile.print(",");
      logFile.print(rightNow.hour(), DEC);
      logFile.print(",");
      logFile.print(rightNow.minute(), DEC);
      logFile.print(",");
      logFile.print(rightNow.second(), DEC);
      logFile.print(",");
      logFile.print(dataToLog);
    
      // End the line with a return character.
      logFile.println();
      logFile.close();
      Serial.print("Event Logged: ");
      Serial.print(rightNow.year(), DEC);
      Serial.print(",");
      Serial.print(rightNow.month(), DEC);
      Serial.print(",");
      Serial.print(rightNow.day(), DEC);
      Serial.print(",");
      Serial.print(rightNow.hour(), DEC);
      Serial.print(",");
      Serial.print(rightNow.minute(), DEC);
      Serial.print(",");
      Serial.print(rightNow.second(), DEC);
      Serial.print(",");
      Serial.println(dataToLog);
    }
    ```
    
    ### Analysis
    
    In these three snippets of code, you can see that the required libraries are included in the sketch and the Cable Select (CS) pin is set to 10. This is set as a variable to be used in the `setup()` function code - `SD.begin(SDpin)` - so that the code can be easily modified to use a different pin. This is useful if the project had to be modified to use a different microcontroller board, such as the Arduino Mega.
    
    The configuration also utilises the Real Time Clock (RTC) library. While this is not strictly required for the SD card module to function, this allows the code to timestamp the events with the correct time. This project does not have a hardware RTC module, therefore the RTC is a software simulated version, where the time is set when the code is compiled and uploaded to the Arduino. 
    
    The `setup()` function attempts to interface with the SD card module on the indicated pin. If there is no SD card module detected, the sketch stops executing and doesn’t proceed. If an SD card is detected, the setup() function continues executing.
    
    The software RTC is achieved through this line of code -`rtc.begin(DateTime(F(__DATE__), F(__TIME__)));`
    
    The `logEvent()` function is used throughout the code to write timestamped events to the SD card. For debugging, it also outputs to the Serial Monitor, however this can easily be disabled to improve execution speed or to free resources. 
    
    Each event is logged in the following format:
    
    `YYYY,MM,DD,HH,MM,SS,Event`
    
    This format is compatible with the Comma Separated Values (CSV) format which can be opened in any spreadsheet application for analysis.
    
    ![Screen Shot 2022-06-14 at 8.10.38 pm.png](../Assessment%20Examples%20ba9ee48cf95a4ca78c4a3653b16831a0/Screen_Shot_2022-06-14_at_8.10.38_pm.png)
    
    As can be seen from the CSV output, the events are logged and can be used in an audit, or for forensic analysis for security issues.
    
    ### Critical Analysis / Evaluation
    
    <aside>
    ‼️ This would require more research and detail.
    
    </aside>
    
    The project works and achieves the goals set up - log each event in the system as required. In this project, the log is written to a local SD card, making this system airgapped with no internet connectivity.
    
    One improvement to the system could be connecting the microcontroller to the internet and upload the events to an external server. This would require a few changes and considerations. First the project as it stands cannot connect to the internet as the Arduino Uno does not have this functionality. A wifi Shield or module could be added to the project, such as this one:
    
    [https://docs.arduino.cc/retired/getting-started-guides/ArduinoWiFiShield](https://docs.arduino.cc/retired/getting-started-guides/ArduinoWiFiShield)
    
    This may require rewiring of the modules, and may not be possible if other pins are required. An Arduino Mega could be used to allow for this, but testing would need to be done.
    
    Another option is change to a platform that has internet connectivity built in, such as the Adafruit ESP32 Feather, or Raspberry Pi.
    
    One of the biggest issues with the SD card module that it appears to cause conflicts with other SPI module connected to the board, specifically in the case of the provided Bluetooth module - the nrf8001 module. According to research, the MicroSD card module used is not 100% compatible with the SPI protocol. In effect, when the SD card module is wired into the circuit, the bluetooth module does not broadcast. Other SPI modules may have similar issues, but further testing is required.
    
    ## References
    
    [https://www.tutorialspoint.com/spi-in-arduino-uno#:~:text=ArduinoSoftware %26 CodingHardware,that uses SPI for communication](https://www.tutorialspoint.com/spi-in-arduino-uno#:~:text=ArduinoSoftware%20%26%20CodingHardware,that%20uses%20SPI%20for%20communication).
    
    [https://tronixstuff.com/2011/05/13/tutorial-arduino-and-the-spi-bus/](https://tronixstuff.com/2011/05/13/tutorial-arduino-and-the-spi-bus/)
    
    [http://elm-chan.org/docs/mmc/mmc_e.html](http://elm-chan.org/docs/mmc/mmc_e.html)
    
    # Structure of Technical Report
    
    The Analysis is to be written as a technical report and should be structured as such.
    
    Here are some resources to assist you.
    
    At a minimum, your document should have the following sections:
    
    - Title page
    - Table of Contents
    - Introduction
    - Summary
    - Body
        
        <aside>
        ‼️ This section can be split into different sections depending on the purpose of the report.
        
        </aside>
        
    - Conclusion
    
    [Technical report writing](https://students.unimelb.edu.au/academic-skills/explore-our-resources/report-writing/technical-report-writing)
    
    [How to Write Technical Report](https://medium.com/technical-writing-is-easy/how-to-write-technical-report-e935210002c9)
    
    [https://www.youtube.com/watch?v=QJ3bZeF1AKg](https://www.youtube.com/watch?v=QJ3bZeF1AKg)
    
    # Diagrams
    
    Your technical report will need some diagrams to explain the system to the readers.
    
    For the assessment task, you are required to include Use Case Diagrams to explain the functionalities, and Webpage Wireframes to show examples of the interfaces that the users will have access to.
    
    ## Use Case Diagrams
    
    > The purpose of a use case diagram in UML is to demonstrate the different ways that a user might interact with a system.
    [https://www.lucidchart.com/pages/uml-use-case-diagram](https://www.lucidchart.com/pages/uml-use-case-diagram)
    > 
    
    > Use case diagrams are used to gather the requirements of a system including internal and external influences.
    [https://www.tutorialspoint.com/uml/uml_use_case_diagram.htm](https://www.tutorialspoint.com/uml/uml_use_case_diagram.htm)
    > 
    
    > “…the purposes of use case diagrams can be said to be as follows −
    - Used to gather the requirements of a system.
    - Used to get an outside view of a system.
    - Identify the external and internal factors influencing the system.
    - Show the interaction among the requirements are actors.”
    > 
    
    ### Examples
    
    ![Slide1.png](../Technical%20Report%20Writing%20664e018c758445829486a708594d2938/Slide1.png)
    
    ![Slide2.png](../Technical%20Report%20Writing%20664e018c758445829486a708594d2938/Slide2.png)
    
    ### How to Create your own Use Case Diagrams
    
    Using [diagrams.net](http://diagrams.net) or a similar app, create a Use Case Diagram for the proposed system.
    
    ### **How to Draw a Use Case Diagram?**
    
    [https://online.visual-paradigm.com/diagrams/tutorials/use-case-diagram-tutorial/](https://online.visual-paradigm.com/diagrams/tutorials/use-case-diagram-tutorial/)
    
    A Use Case model can be developed by following the steps below.
    
    1. Identify the Actors (role of users) of the system.
    2. For each category of users, identify all roles played by the users relevant to the system.
    3. Identify what are the users required the system to be performed to achieve these goals.
    4. Create use cases for every goal.
    5. Structure the use cases.
    6. Prioritize, review, estimate and validate the users.
    
    ### Resources
    
    [Use Case Diagram Tutorial ( Guide with Examples ) - Creately Blog](https://creately.com/blog/diagrams/use-case-diagram-tutorial/)
    
    [https://www.youtube.com/watch?v=quS39HW_bVg](https://www.youtube.com/watch?v=quS39HW_bVg)
    
    ## Webpage Wireframes
    
    Sketch the interfaces for:
    
    1. Monitors view and access
    2. Guests view and access
    3. Other’s as required.
    
    These sketches can be done on paper, or digitally through [diagrams.net](https://app.diagrams.net) or similar.
    
    More Information here: [Website Wireframes](../Design%206dd970530a3f4a668fb5adcecdfac517/Website%20Wireframes%20c6e8595356884137a4719d62dfd9ebb9.md) 
    

[Key Terms](Software%20Development%20Fundamentals%20Course%20Theory%20d7b47926fb2a42dc85c32b286f178735/Key%20Terms%2079307cb75c804c53a601b612cbb7c313.csv)