# Arduino - Software Development Fundamentals

This course introduces you to software development with a focus on Arduino as the environment - the language, IDE and platform.

# Course Topics

- Course Introduction - Arduino
    
    
    # Arduino Implementation
    
    <aside>
    ‼️ Be aware - The term "Arduino" can refer to either;
    
    1. The Arduino programming language,
    2. The Arduino IDE, or
    3. The Arduino board.
    </aside>
    
    ## Arduino Sketches
    
    <aside>
    ‼️ Arduino Code is referred to as Sketches.
    
    </aside>
    
    Each Arduino sketch needs to have the same basic structure.
    
    **At a minimum**, the sketch needs to have the setup() and loop() functions.
    
    ![Structure of an Arduino Sketch example with code.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Structure_of_an_Arduino_Sketch_example_with_code.png)
    
    # Practical Exercises
    
    In this initial stage, you'll be using [TinkerCAD](https://www.tinkercad.com/) to virtually program Arduino Uno board.
    
    ![Screen Shot 2021-12-14 at 11.55.20 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2021-12-14_at_11.55.20_pm.png)
    
    Click the link to join the Class for this subject.
    
    [Classroom login | Tinkercad](https://www.tinkercad.com/joinclass/QM5M8HWQJSG6)
    
    Sign into Tinkercad with Google, using your school credentials.
    
    ![SCR-20221205-g2b.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/SCR-20221205-g2b.png)
    
    Click on the first activity - “1 Blink”.
    
    Choose `Circuit` from the `Create new design` menu.
    
    ![SCR-20221205-gb8.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/SCR-20221205-gb8.png)
    
    Change the Basics components menu to Starters Arduino. Find `Blink` in that list.
    
    ![SCR-20221205-gco.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/SCR-20221205-gco.png)
    
    Drag the Blink module to the editing area
    
    ![SCR-20221205-ge8.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/SCR-20221205-ge8.png)
    
    Click on the Code button, and change the code type to Text.
    
    Here you will see the "Hello World" code for Arduino, also referred to as Blink. At this stage, don't worry too much about the specific code - you'll learn that later. Just notice how the code is written, the syntax and the functions used - `setup()` and `loop()`.
    
    ![Screen Shot 2021-12-15 at 12.00.54 am.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2021-12-15_at_12.00.54_am.png)
    
    You can start the code running by using the Start Simulation button.
    
    You should see the LED flashing on and off every second.
    
    Congratulations - you've (potentially) written your first Arduino Sketch!
    
    ![start simulation.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/start_simulation.gif)
    
    ## Extension
    
    1. Goal: Update the code to flash on and off every half a second. 
        
        What part of the code would you need to change? 
        
    2. Change the LED to be on pin 10. 
        
        What needs/needed to be changed?
        
    
    # Review
    
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
    
    [Key Terms](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Key%20Terms%20dd51e3cdbb39460293e6a0c2d98426cd.csv)
    
- Version Control - Arduino
    
    
    # Arduino Implementation
    
    ## TinkerCAD
    
    TinkerCAD stores code in the browser, and does not have inbuilt version control. Therefore, you will need to commit and publish your code through Github.
    
    ## Electronics Board Project Development
    
    When developing code for the Electronics Board project, you will start using the Arduino IDE and will then need to use a Version Control System to manage your code.
    
    TinkerCAD and the Arduino IDE do not have in-built functionality for Version Control, unfortunately. This means that you need to use [Github Desktop](https://desktop.github.com/) to manage access to the git system. 
    
    The information on this [Version Control System](https://www.notion.so/Version-Control-System-Github-527442170bf24bfba8cc3b4126d7493d) should aid you in configuring the environment.
    
    <aside>
    💡 It is recommended that you start by creating a new repository in Github Desktop first. Then create individual sketches inside the repository folder for each project.
    
    </aside>
    
    When appropriate (after moving away from TinkerCAD) create a new repository for the Electronics Board project.
    
    After completing the tasks shown in the video, your repository should look similar to this one:
    
    ![Screen Shot 2021-12-15 at 1.19.30 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2021-12-15_at_1.19.30_pm.png)
    
    [https://youtu.be/IyOwVwequD8](https://youtu.be/IyOwVwequD8)
    
    # Practical Exercises
    
    ## Create a Github Account
    
    1. Go to [https://github.com/join](https://github.com/join).
    2. Using your school email address (...@schoolsnet.act.edu.au) create a Github account.
    
    ## Creating a new Repository - Github
    
    Log into [Github](https://github.com/) (through the browser) and click New for a new repository.
    
    Your screen may look different to this - look for the green "New" button.
    
    ![Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/Screen_Shot_2021-07-20_at_9.29.27_am.png](Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/Screen_Shot_2021-07-20_at_9.29.27_am.png)
    
    Configure the repository settings.
    
    1. Give the repository an appropriate **name**
    2. Add a description
    3. Leave as **Public**
    4. **Add** a readme file
    5. Set the **.gitignore** settings to a setting appropriate for the project type.
        1. This will ignore files that are not needed to synchronise to Github for our project
    6. Set the license to MIT.
        
        ![Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/Create_a_New_Repository.png](Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/Create_a_New_Repository.png)
        
        Click Create Repository.
        
        ![Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/LTC-IT_FPS-Godot__Using_the_Godot_tutorial_for_learning_to_create_a_FPS_.png](Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/LTC-IT_FPS-Godot__Using_the_Godot_tutorial_for_learning_to_create_a_FPS_.png)
        
    
    ## Github Desktop - Cloning the Repository
    
    <aside>
    ‼️ Github desktop is the GUI interface to clone, commit, push etc repositories to and from Github that runs on your local computer.
    
    </aside>
    
    Now, open **Github Desktop** on your computer and click "Clone Repository" under the File menu.
    
    ![Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/Screen_Shot_2021-07-20_at_9.38.17_am.png](Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/Screen_Shot_2021-07-20_at_9.38.17_am.png)
    
    Select the new repository you just created.
    
    Choose the path where you want to save it. 
    
    <aside>
    ⁉️ The directory will need to be empty.
    
    </aside>
    
    Click Clone.
    
    ![Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/GitHub_Desktop.png](Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/GitHub_Desktop.png)
    
    After a short moment, it will then show you this page:
    
    ![Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/Screen_Shot_2021-07-20_at_9.40.18_am.png](Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/Screen_Shot_2021-07-20_at_9.40.18_am.png)
    
    Click on the Current Repository Download in the top left of the window. Right Click on the repository and choose to open it in the file explorer.
    
    ![Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/GitHub_Desktop2.png](Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/GitHub_Desktop2.png)
    
    ## Github Desktop - Commit and Sync
    
    You should see that it's detected the new files. As this is the first time you are committing to the repository, just type in "init" to the summary and detail boxes and then hit commit.
    
    <aside>
    ⁉️ When committing later, you'll need to put more details into these boxes. You'll need to explain what changes have been made.
    
    </aside>
    
    Finally, click "Push Origin" which will synchronise the repository to Github online.
    
    ![Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/20_7_21__9_58_am.png](Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/20_7_21__9_58_am.png)
    
    ![Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/20_7_21__9_59_am.png](Github%20-%20Master%20ad9076c7419d48498579ee23008406a7/20_7_21__9_59_am.png)
    
    # Review
    
    1. When do you push a project?
    2. When do you pull a project?
    3. Is Git a distributed or centralised system? Why?
    4. How does Version Control assist in software development?
    
    [Key Terms](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Key%20Terms%207c4bbd7fa0b54ed0b5abdf02f4ddf00c.csv)
    
- Computational Thinking - Arduino
    
    
    # Arduino Implementation
    
    None
    
    # Practical Exercises
    
    1. Consider the following problem. Decompose it into smaller problems.
        1. The ACT Government has given you a grant to protect the bike path / walkway around Lake Tuggeranong due to your robotics experience. You are tasked with building an autonomous robot to patrol the path and notify Transport Canberra and City Services of any obstacle or dangerous item.
    
    # Review
    
    [Key Terms](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Key%20Terms%20acf04116e9a14b9aa7ee72dbaf6df604.csv)
    
- Mathematical & Logic Operations- Arduino
    
    
    # Arduino Implementation
    
    Read and practice all topics under [Mathematical & Logic Operations](https://www.notion.so/Mathematical-Logic-Operations-fbb6dd5a5acf434799d572e3e70a4e02).
    
    # Practical Exercises
    
    Using [https://circuitverse.org/](https://circuitverse.org/) draw the following Logic Circuits, and then complete the truth tables for each. You can use Google Sheets to create the truth tables if needed.
    
    ## Logic Circuits and Truth Tables
    
    1. $(AB) + \overline{(AC)}$
    2. ${\overline{AB} + {\overline{BC}}}$
    3. ${\overline{\overline{AB} + {\overline{BC}}}}$
    4. $A. \overline{B} + C\overline{(A.B)}$
    5. $\overline{A}B\overline{C}$
    6. $\overline{\overline{A}.\overline{B}} + C$
    
    ### For Example
    
    $AB+C$
    
    ![Main.png](GDScript%20-%20Software%20Development%20Fundamentals%20c188b5273ab94c9696362483fccfa1d3/Main.png)
    
    ![Screen Shot 2021-12-16 at 12.51.18 pm.png](GDScript%20-%20Software%20Development%20Fundamentals%20c188b5273ab94c9696362483fccfa1d3/Screen_Shot_2021-12-16_at_12.51.18_pm.png)
    
    ### Sample Answer
    
    In this video, I show how to answer the first question listed above.
    
    [https://youtu.be/XQ1upSSMG_A](https://youtu.be/XQ1upSSMG_A)
    
    ## Simplification
    
    Simplify the following boolean equations. Show your working, and identity which rule you're using at each step.
    
    1. $AA + B$
    2. $C + \overline{BC}$
    
    Complete the Karnaugh Map process for each of the following equations:
    
    1. 
        
        ![commonality-of-boolean-variables-example-one.webp](GDScript%20-%20Software%20Development%20Fundamentals%20c188b5273ab94c9696362483fccfa1d3/commonality-of-boolean-variables-example-one.webp)
        
    2. 
        
        ![02834x01.webp](GDScript%20-%20Software%20Development%20Fundamentals%20c188b5273ab94c9696362483fccfa1d3/02834x01.webp)
        
        ![02834x02.webp](GDScript%20-%20Software%20Development%20Fundamentals%20c188b5273ab94c9696362483fccfa1d3/02834x02.webp)
        
    
    # Review
    
    Discussion: Why is logic important when learning software development?
    
    Discussion: What is the purpose of Karnaugh Maps and how does it assist us in developing solutions?
    
    1. Go to [https://learn.electronics-course.com](https://learn.electronics-course.com/) (sign in with your school Google Account to save your progress) and complete the following projects:
        1. NAND Gate
        2. Half Adder
        3. Care Safety Buzzer
    
    [Key Terms](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Key%20Terms%2073ebf4dcfc5a4a17af364cb9ef39c373.csv)
    
- Variables and Data Types - Arduino
    
    
    # Arduino Implementation
    
    In Arduino, variables **must** be declared before they can be used. If they are not declared, you will get a syntax error.
    
    Unlike some other languages, when programming in Arduino you must specify the data type of a variable using the specific keyword - `int`, `string` etc.
    
    Arduino is a statically typed language, meaning that once a variable has been declared as a certain data type, it cannot change throughout the execution of the code. This is different from some other languages (namely Python, GDScript, PHP etc) which are dynamically typed where the data type of a variable can be changed during the execution of code.
    
    ## Declaring variables
    
    When declaring variables in Arduino, you must indicate the data type prior to declaring the name and initial value (if any). A simple counter variable could be declared such as:
    
    ```arduino
    int sensorReadCounter;
    ```
    
    You can also set an initial value when declaring variables:
    
    ```arduino
    string loggedInUser = "None";
    ```
    
    ## Arduino Data Types
    
    In Arduino, there are a number of the standard primitive types. The syntax for each of these are:
    
    | Syntax | Data type | Description | Possible Values (on an Arduino Uno) |
    | --- | --- | --- | --- |
    | int | Integer | On the Arduino Uno an int stores a 16-bit (2-byte) value. | -32,768 to 32,767 |
    | bool | Boolean | Each bool variable occupies one byte of memory. | true or false.  |
    | char | Character | A data type used to store a character value - use single quotes for chars. Chars are stored as integers, meaning to can perform arithmetic. E.g. 'A' + 1 would equal 'B' | 'A', 'i' |
    | byte | Byte | A byte stores an 8-bit unsigned number | 0 to 255 |
    | float | Float | Numbers with decimal point values | 5.3
    0.1 |
    | String | String | Complex (non-primitive) data type. Comprised of a series of characters in an array. Use double quotes. An an array, Strings allow for more complex functionality, such as converting to integers, searching for substrings, converting to upper case etc. | "Lake Tuggeranong College"
    "32" |
    | long | Long | An integer data type which allocates and uses 32-bits (4 bytes). | 2,147,483,648 to 2,147,483,647 |
    
    This table describes some more of the data types available. 
    
    <aside>
    ‼️ The sizes and ranges shown are based on the Arduino Uno. Other languages and platforms may use different sizes, and therefore ranges.
    
    </aside>
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2047.png)
    
    ## Constants
    
    When declaring constants in Arduino, use the const keyword *before* the data type.
    
    ![Screen Shot 2021-12-15 at 9.20.40 am.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2021-12-15_at_9.20.40_am.png)
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll be updating the Bank Alarm Project to use more variables and constants.
    
    </aside>
    
    Open the Bank Alarm project on [Tinkercad](https://www.tinkercad.com/). 
    
    This code is the code at the conclusion of the Modularisation stage.
    
    You may recall that a few variables were used throughout this process - `potReading`, `brightness` etc.
    
    ```arduino
    void setup()
    {
      pinMode(A0, INPUT);
      pinMode(9, OUTPUT);
      Serial.begin(9600);
    }
    
    void loop()
    {
      int potReading = readPotentiometer();
      int brightness = map(potReading, 0, 1023, 0, 255);
      delay(250);
      setLEDBrightness(brightness);
    }
    
    int readPotentiometer() {
      int potValue = analogRead(A0);
      Serial.println(potValue);
      return potValue;
    }
    
    void setLEDBrightness(int LEDBrightness) {
      analogWrite(9, LEDBrightness);
    }
    ```
    
    Start updating the code by declaring a few constants to store the pins used by the LED and the potentiometer.
    
    <aside>
    ‼️ These have been declared as ******************constants****************** as there is no need for the contents to change throughout the execution of the code.
    
    </aside>
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2048.png)
    
    ```arduino
    const int pinLED = 9;
    const int pinPot = A0;
    ```
    
    Replace any reference to pins 9 or A0 with the corresponding constant.
    
    <aside>
    ‼️ You may have noticed that A0 has been defined as a integer, despite the A. This is because the Arduino language automatically converts this A0 ‘symbol’ into the number 14 for the Arduino Uno. 
    On the Arduino Uno, pin A0 can also be referred to as pin 14. Try updating the code and checking if it works!
    
    </aside>
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2049.png)
    
    This has the benefit of future maintainability - if the circuit needed to be changed and the devices must change pins, the ********only******** section of code you would need to change is the constants at the start of the code. The remainder of the code wouldn’t need to be changed.
    
    # Review
    
    1. How is data stored in memory?
    2. What’s the difference between primitive and non-primitive data types?
    3. What is type inference?
        1. Find three programming languages that use type inference.
    4. What is the opposite of type inference?
        1. Find three programming languages that don’t use type inference.
    5. What does strongly typed and weakly typed languages mean?
    
    Using tinkerCAD, create a circuit with just an Arduino Uno and write code to:
    
    1. Declare two variables, add them together (stored in a third variable) and output the result to the Serial Monitor.
        
        ![Screen Shot 2021-12-15 at 11.15.56 am.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2021-12-15_at_11.15.56_am.png)
        
    2. Read a name, as a String, from the Serial Monitor, store it in a variable and then output "Hello <name>" back to the Serial Monitor.
        
        ![2021-12-15 11-17-41.2021-12-15 11_19_21.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/2021-12-15_11-17-41.2021-12-15_11_19_21.gif)
        
    
    [Key Terms](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Key%20Terms%20a440bee715ff42408fda3d1fd0352e27.csv)
    
- Algorithm Design - Sequence - Arduino
    
    
    # Arduino Implementation
    
    Arduino is a subset of the C++ language. C++, invented in 1985, is an extension to C, which was invented in 1972. So, the basis for the language is quite old, in computer science terms. Luckily the Arduino language simplifies some aspects of C++ to suit the Arduino environment.
    
    Consider the code sample for `Blink`. 
    
    ## Brackets
    
    Notice the use of brackets - () and {} - these are very important in the Arduino language (as they are in C and C++). 
    
    <aside>
    💡 Each open bracket, whichever type, must have a corresponding close bracket.
    
    </aside>
    
    The standard brackets - or parentheses - indicate **conditions** and **parameters** and **arguments**. 
    
    The Curly Brackets - { and } - indicate the start and the end of a code block. This code block can be a **function** (as can be seen in the image with `setup()` and `loop()`) and also with **decisions** and **loops**. 
    
    ![Screen Shot 2021-12-16 at 1.23.37 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2021-12-16_at_1.23.37_pm.png)
    
    ## Semicolon
    
    The details of these topics will be discussed later in the course - just be aware of the different brackets and their uses at this stage.
    
    You may also notice that *almost* each line of code shown ends with a semi-colon. In C-based languages (Java, javascript, Arduino etc), the semi-colon identifies the end of a statement.
    
    ## Whitespace
    
    In programming, whitespace refers to the use of indentation (tabs), space characters new newline characters.
    
    In Arduino, the compiler generally ignores whitespace, meaning you can have as many blank lines in your code as you wish - the code will still compile.
    
    Indentation is also not critical, however it makes it easier to read code blocks if indented correctly.
    
    <aside>
    💡 CTRL+T is the shortcut to auto-format your code and fix up indentation.
    
    </aside>
    
    # Practical Exercises
    
    In a Google Doc write the sequence involved in you making toast.
    
    Update the blink code, to include a second (or third) LED, and code the LEDs to cycle through - e.g. RED, then GREEN, then RED, then GREEN etc.
    
    ![2021-12-16 13-55-55.2021-12-16 13_56_40.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/2021-12-16_13-55-55.2021-12-16_13_56_40.gif)
    
    Practical Demonstration - Robots!
    
    # Review
    
    1. Write the sequence of steps to make and eat toast.
    2. What the sequence of steps to 
        1. Read in individual lines of a text file (example shown)
        2. Calculate the GST
        3. Output the GST component to the user.
            
            ![Screen Shot 2022-01-27 at 9.44.53 pm.png](GDScript%20-%20Software%20Development%20Fundamentals%20c188b5273ab94c9696362483fccfa1d3/Screen_Shot_2022-01-27_at_9.44.53_pm.png)
            
        
        [Key Terms](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Key%20Terms%20850e99b40fa24ff8b2d73d627617580a.csv)
        
- Algorithm Design - Decisions - Arduino
    
    
    # Arduino Implementation
    
    ## IF..THEN..
    
    In Arduino, as with many other languages, the main decision block is the `IF..THEN..`. The syntax for this in Arduino is:
    
    ![Screen Shot 2021-12-16 at 2.07.37 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2021-12-16_at_2.07.37_pm.png)
    
    <aside>
    💡 Note the condition is enclosed in parenthesis.
    
    </aside>
    
    For the code block to execute, the condition needs to equate to **true**. If the condition equates to **false**, the code block is skipped.
    
    ### IF..THEN.. Example
    
    ```arduino
    if (x > 120) {
      digitalWrite(LEDpin1, HIGH);
      digitalWrite(LEDpin2, HIGH);
    }
    ```
    
    In this example, `x > 120` is the condition and `digitalWrite(LEDpin1, HIGH);
      digitalWrite(LEDpin2, HIGH);` is the code block that will run only if the condition is true at the time it is executed.
    
    ## IF..THEN.. ELSE..
    
    ![Screen Shot 2021-12-16 at 2.28.59 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2021-12-16_at_2.28.59_pm.png)
    
    The standard IF..THEN structure can be extended with an ELSE to allow a code block to run if the condition is false.
    
    ### IF..THEN..ELSE.. Example
    
    ```arduino
    if (x > 120) {
      digitalWrite(LEDpin1, HIGH);
      digitalWrite(LEDpin2, HIGH);
    } else {
    	digitalWrite(LEDpin1, LOW);
      digitalWrite(LEDpin2, LOW);
    }
    ```
    
    In this case, if x is greater than 120, then the LEDs will be turned on. If x is NOT greater than 120, the LEDs will turn off.
    
    ## Switch ... Case
    
    Switch cases are a different type of control structure to replace multiple, nested if..then statements. 
    
    Based on a given variable, Arduino code can have multiple cases or a catch-all state - default. They can be used to simplify code, but still provide multiple cases for variables.
    
    ### Syntax
    
    ```arduino
    switch (var) {
      case label1:
        // statements
        break;
      case label2:
        // statements
        break;
      default:
        // statements
        break;
    }
    ```
    
    ### Example
    
    ```arduino
    x = random(5);
    switch (x) {
          case 0: y = y + 1;
          case 1: y = y + 5;
          case 2: y = y + 2;
          case 3: y = y + 7;
          case 4: y = y + 3;
          default: y = 0;
        }
    
    // Compared to the equivalent IF statements:
    if (x == 0) y = y + 1;
        else if (x == 1) y = y + 5;
        else if (x == 2) y = y + 2;
        else if (x == 3) y = y + 7;
        else if (x == 4) y = y + 3;
        else y = 3;
    ```
    
    ## **Comparison Operators**
    
    The standard *comparison* operators in Arduino are shown here and can be used in `if` conditions.
    
    | Operator | Description |
    | --- | --- |
    | ! | Not |
    | x == y | x is equal to y |
    | x != y | x is not equal to y |
    | x < y | x is less than y |
    | x > y | x is greater than y |
    | x <= y | x is less than or equal to y |
    | x >= y | x is greater than or equal to y |
    
    ## Logical Operators
    
    | Operator | Description | Example |
    | --- | --- | --- |
    | && | AND  |  |
    | || | OR |  |
    | ! | NOT |  |
    
    # Practical Exercises
    
    <aside>
    ‼️ **********Goal**********
    
    In this task, you’ll be updating the Bank Alarm Project to :
    
    - include decision making, specifically to check if the potentiometer has reached a certain value (threshold) before the LED turns on.
    - You’ll then add additional components to build the final form of the Bank alarm which will operate under the following conditions:
        - 3 of the Sensors must be “triggered” for the alarm to go off (LED turn on)
    </aside>
    
    Open the Bank Alarm project on [Tinkercad](https://www.tinkercad.com/). Before implementing decisions specifically in the code, some code base changes need to be made to reorganise the code. 
    
    ## Modifying the Circuit
    
    In this stage, the code will not be changed, only the circuit itself. Close out of the Code view by clicking the code button in the tool bar.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2012.png)
    
    Change the component list to ********************************Components Basic******************************** in the dropdown list.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2013.png)
    
    Delete the ‘wires’ connecting the LED to the arduino and resistor. Select the wire and press delete.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2014.png)
    
    Add a ********************************Breadboard Small******************************** to the circuit by dragging the component to the circuit area.
    
    ![Jan-12-2023 15-05-35.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Jan-12-2023_15-05-35.gif)
    
    Move the resistor and LED over to the new breadboard. 
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2015.png)
    
    Connect a wire from the **********Anode********** pin (on the right) to the top of the resistor. Do this by clicking on the Anode and then clicking on the top terminal of the resistor.
    
    ![Jan-12-2023 15-12-07.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Jan-12-2023_15-12-07.gif)
    
    Connect the bottom terminal of the resistor to the breadboard.
    
    ![Jan-12-2023 15-13-15.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Jan-12-2023_15-13-15.gif)
    
    ### Breadboards
    
    A breadboard is a reusable platform used for building and prototyping electronic circuits. It allows you to easily connect and disconnect components, without having to solder them together. Breadboards consist of a grid of holes into which electronic components can be inserted. The holes are typically arranged in a pattern of interconnected vertical and horizontal rows. This allows for the connection of different components' leads, such as resistors, capacitors, and transistors, to be easily connected together to create a functioning circuit.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2016.png)
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2017.png)
    
    Connect the **********Cathode********** pin of the LED to the **********Black********** (- or ground) ********************rail of the breadboard.
    
    Using the toolbar, change the colour of the Ground wire to black. This is the standard for Ground wires in wiring diagrams.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2018.png)
    
    Next, connect the Ground rail on the breadboard to the GND pin on the Arduino. Then, connect the Positive (red) rail on the breadboard to the 5V pin.
    
    You can set corners in the wires by double clicking at the point you want to add a bend.
    
    ![gnd.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/gnd.gif)
    
    ![Jan-12-2023 15-25-29.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Jan-12-2023_15-25-29.gif)
    
    Finally, connect Pin 9 on the Arduino to the same row that your resistor is connected to.
    
    ![Jan-12-2023 15-29-27.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Jan-12-2023_15-29-27.gif)
    
    <aside>
    ‼️ Make sure the wire is connected to the correct row as your resistor.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2019.png)
    
    </aside>
    
    Run and test your code to ensure that the wiring is correct!
    
    Move the potentiometer and reconnect it through the breadboard.
    
    Also, connect the bottom 5V rail to the 5V pin, and the bottom GND (-) rail to the GND pin.
    
    <aside>
    ‼️ Remember that when rewiring the potentiometer, you’ll need to wire the potentiometer pins to the correct Arduino pins.
    
    | Pot Pin | Connect to | Description |
    | --- | --- | --- |
    | 1 | 5V | Positive Power |
    | 2 | A0 | Data or Signal |
    | 3 | GND | Negative (Ground) Power |
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2020.png)
    
    </aside>
    
    Your circuit should now appear similar to this. Not the Data pin connected through the breadboard - ensure that the wires are connected on the same row.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2021.png)
    
    ### Additional Sensors
    
    Add two more components to the circuit - the first is a ************Ultrasonic Distance************ (Sonar) sensor, and the second is a **Passive InfraRed** Sensor. 
    
    - A Ultrasonic Distance sensor can detect distance to objects but sending out a pulse signal and timing how long it takes for the signal to bounce back.
    - A Passive Infrared (PIR) sensor detects movement.
    
    Drag out the two components and wire them through the breadboard. Connect the 5V pins to the positive (red) rail, and the Ground pins to the negative (black) rail.
    
    <aside>
    ‼️ There are two ultrasonic sensors in the library. The one you want for this circuit is the one with ********four******** pins and has **************HC-SR04************** written on the image
    You may need to change the component listing to ********All******** to find the correct Ultrasonic sensor.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2022.png)
    
    </aside>
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2023.png)
    
    Connect the Signal pin of the PIR sensor to Pin 2 through the breadboard.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2024.png)
    
    Connecting the Sonar sensor requires connecting two wires to the Arduino. 
    
    - ********Trig******** pin for sending the pulse. Connect this to pin 3.
    - ********Echo******** for reading the response of the pulse. Connect this to pin 11.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2025.png)
    
    ## Code Reorganisation
    
    Create a new function to handle the functionality that is being implemented.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2026.png)
    
    ```arduino
    void determineLEDBrightness(int brightnessValue) {
      
    }
    ```
    
    Update `loop()` to call this function **************instead************** of `setLEDBrightness()`.
    
    <aside>
    ‼️ This new function is now going to act as intermediately between the main loop functionality and making the decision whether to turn the LED on or not, before setting the brightness.
    
    </aside>
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2027.png)
    
    Change the argument for calling  `determineLEDBrightness` to be `potReading` instead of `brightness`.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2028.png)
    
    Add `//` to the front of the line of code which maps the brightness variable.
    
    <aside>
    ‼️ This ****************comments**************** out the line of code, removing it from compilation and execution - essentially, the line of code is ignored by the computer.
    
    </aside>
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2029.png)
    
    ## Decision Making - LEDs
    
    Now the code has been reorganised, it’s time to focus on the new functionality - the LED is turned on until a particular potentiometer value is reached, then the brightness of the LED is determined by the remainder of the values.
    
    For simplicity, the threshold value of 511 is used here - half way between 0 and 1023. If the potentiometer reads under and including 511, the LED will remain off, over 511, the LED brightness will be scaled.
    
    Create a new variable inside `determineLEDBrightness()` to store the value that is determined.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2030.png)
    
    ```arduino
    int brightness;
    ```
    
    In `determineLEDBrightness()`, add an `if` statement to check `brightnessValue`.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2031.png)
    
    ```arduino
    if (brightnessValue <= 511) {
        
    }
    ```
    
    If the condition is ********true******** then the LED needs to be turned off. This is done by setting the value of `brightness` to 0.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2032.png)
    
    ```arduino
    brightness = 0;
    ```
    
    Add an `else` clause to handle any values greater than 511.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2033.png)
    
    Now, the mapping can be done. This is similar to how it was previously done in `loop()` however you don’t need to calculate for values 0-511 as these values have already been handled.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2034.png)
    
    ```arduino
    brightness = map(brightnessValue, 512, 1023, 0, 255);
    ```
    
    Finally, outside of the `if` block, write the `brightness` value to the LED pin by passing it to `setLEDBrightness()`.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2035.png)
    
    ```arduino
    setLEDBrightness(brightness);
    ```
    
    ## Test the functionality
    
    Start the simulation and you should see the new functionality in the circuit.
    
    ![Jan-12-2023 11-29-44.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Jan-12-2023_11-29-44.gif)
    
    ### Final Code
    
    ```arduino
    const int pinLED = 9;
    const int pinPot = A0;
    
    void setup()
    {
      pinMode(pinPot, INPUT);
      pinMode(pinLED, OUTPUT);
      Serial.begin(9600);
    }
    
    void loop()
    {
      int potReading = readPotentiometer();
      //int brightness = map(potReading, 0, 1023, 0, 255);
      determineLEDBrightness(potReading);
      delay(250);
    }
    
    int readPotentiometer() {
      int potValue = analogRead(pinPot);
      Serial.println(potValue);
      return potValue;
    }
    
    void determineLEDBrightness(int brightnessValue) {
      int brightness;
      if (brightnessValue <= 511) {
        brightness = 0;
      } else {
        brightness = map(brightnessValue, 512, 1023, 0, 255);
      }
      setLEDBrightness(brightness);
    }
    
    void setLEDBrightness(int LEDBrightness) {
      analogWrite(pinLED, LEDBrightness);
    }
    ```
    
    ## Decision Making - Multiple Inputs
    
    In this stage, the circuit will take inputs from multiple sensors ( Potentiometer, Sonar and PIR) and determine whether the LED should be on or not.
    
    Define constants for the pins being used. These are to be set at the start of the code.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2036.png)
    
    ```arduino
    const int trigPin = 3;
    const int echoPin = 11;
    const int pinPIR = 2;
    ```
    
    Add the code in `setup()` to configure the pins to be input or output.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2037.png)
    
    ```arduino
    pinMode(trigPin, OUTPUT); // Sets the trigPin as an OUTPUT
      pinMode(echoPin, INPUT); // Sets the echoPin as an INPUT
      pinMode(pinPIR, INPUT); // Sets the trigPin as an OUTPUT
    ```
    
    Add a function to read the response from the PIR.
    
    The PIR sensor responds with `true` if it detects movement, `false` otherwise.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2038.png)
    
    ```arduino
    boolean readPIR() {
     return digitalRead(pinPIR);
    }
    ```
    
    Add the following function to utilise the Sonar sensor.
    
    This function does all the specific low-level code to send the pulse and read the response from the sonar. 
    
    If the distance to the object is determined to be less than the threshold, then the function returns `true`, otherwise `false`.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2039.png)
    
    ```arduino
    boolean readDistance(int distanceThreshold) {
      long duration; // variable for the duration of sound wave travel
      int distance; // variable for the distance measurement
       // Clears the trigPin condition
      digitalWrite(trigPin, LOW);
      delayMicroseconds(2);
      // Sets the trigPin HIGH (ACTIVE) for 10 microseconds
      digitalWrite(trigPin, HIGH);
      delayMicroseconds(10);
      digitalWrite(trigPin, LOW);
      // Reads the echoPin, returns the sound wave travel time in microseconds
      duration = pulseIn(echoPin, HIGH);
      // Calculating the distance
      distance = duration * 0.034 / 2; // Speed of sound wave divided by 2 (go and back)
      // Displays the distance on the Serial Monitor
      Serial.print("Distance: ");
      Serial.print(distance);
      Serial.println(" cm");
      if (distance < distanceThreshold) {
        return true;
      } else {
       	return false; 
      }
    }
    ```
    
    To help the debugging process that may be required in the future, add a helper function which outputs all the values of the sensors. This will help you determine if and when there are any problems with the alarm triggering.
    
    <aside>
    ‼️ Adding this as a function will allow this to be easily turned on and off by removing the function call.
    
    </aside>
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2040.png)
    
    ```arduino
    void debugSensors(int potValue, boolean pirValue, boolean sonarValue) {
      Serial.print("The potentiometer value is :"); 
      Serial.print(potValue);
      Serial.print(". The PIR Reads:");
      Serial.print(pirValue);
      Serial.print(". The Sonar Reads:");
      Serial.println(sonarValue);
    }
    ```
    
    Create a function that will access and read the sensor values from the functions created previously.
    
    This function reads the responses from all the other functions and stores them locally.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2041.png)
    
    ```arduino
    void triggerAlarm() {
      int potTrigger = readPotentiometer();
      boolean pirTrigger = readPIR();
      boolean sonarTrigger = readDistance(100);
      debugSensors(potTrigger, pirTrigger, sonarTrigger);
    }
    ```
    
    Add an if statement to determine if all three trigger values are ‘correct’. “Correct” in this case means that they are enough to meet the requirements to trigger the alarm - the potentiometer value needs to be greater than 511. The PIR and Sonar values need to be `true`.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2042.png)
    
    ```arduino
    if (potTrigger > 511 && pirTrigger == true && sonarTrigger == true) {
        
    } else {
        
    }
    ```
    
    <aside>
    ‼️ ****************Compound**************** conditions, such as the one shown above, a logical expression that combines multiple individual conditions using logical operators such as "and" (&&) or "or" (||). These conditions are typically used in control flow statements such as "if-else" or "while" loops to determine the execution of certain code. For example, the expression "`x > 0 && x < 10`" is a compound condition that checks whether the variable "x" is greater than 0 and less than 10. If both conditions are true, the code within the corresponding control flow statement will be executed.
    
    In the code shown, ALL of the individual conditions (red, yellow and purple) must equate to `true` for the whole `if` statement to be evaluated as `true`.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2043.png)
    
    </aside>
    
    Add the appropriate code in the different if blocks to turn the LED on or off.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2044.png)
    
    ```arduino
    if (potTrigger > 511 && pirTrigger == true && sonarTrigger == true) {
        Serial.println("Alarm Triggered");
        determineLEDBrightness(potTrigger);
      } else {
        Serial.println("Alarm Off");
        determineLEDBrightness(false);
      }
    ```
    
    Finally, modify `loop()` to call `triggerAlarm()` instead of `determineLEDBrightness()`.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2045.png)
    
    ```arduino
    void loop()
    {
      int potReading = readPotentiometer();
      //determineLEDBrightness(potReading);
      triggerAlarm();
      delay(250);
    }
    ```
    
    ## Test the functionality
    
    Start the simulation and check to make sure that all three sensors need to have ‘correct’ values for the LED to be on.
    
    ![Jan-13-2023 10-59-19.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Jan-13-2023_10-59-19.gif)
    
    **Sonar**
    
    The highlighted value needs to be less than 100.
    
    ![SCR-20230113-f6h.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/SCR-20230113-f6h.png)
    
    **Potentiometer**
    
    The dial needs to be set to a value on the lefthand side (<511)
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2046.png)
    
    **PIR**
    
    This sensor requires movement, so click on it and move the circle around. You’ll notice that when the sensor detects movement, it highlights in red on the sensor.
    
    ![Jan-13-2023 10-54-17.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Jan-13-2023_10-54-17.gif)
    
    If the LED does not turn on as expected, check the Serial Monitor for the variable outputs to diagnose where the issue may reside.
    
    ![Jan-13-2023 11-00-07.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Jan-13-2023_11-00-07.gif)
    
    # Extension Exercises
    
    Using TinkerCAD, design the circuit and write code to:
    
    1. Have LED on while a button is being pressed.
    
    For this, you will need to identify the pins and set them to input or output in the `setup()` function. In the `loop()` function, read the value of the button using `digitalRead()`. If the button is pressed down, turn the LED on (digitalWrite HIGH). If the button is not being pressed, then turn the LED off (digitalWrite LOW).
    
    ![2021-12-16 14-45-01.2021-12-16 14_45_46.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/2021-12-16_14-45-01.2021-12-16_14_45_46.gif)
    
    1. When a button is pressed, turn the LED on for 1 second, and then off. (similar to Blink). 
    2. Using the same circuit design, when the button is pressed, the LED turns on, and when pressed again, it is turned off. Google “StateChangeDetection Arduino”. This will assist.
    
    1. Build this circuit. The sensor at the bottom is called a “potentiometer”, which is an analog input device. Use the code as a starting point. Continue writing the loop() function to complete the following logic:
    `If the input from the potentiometer is above the threshold value, then turn the LED on. If it’s below the threshold, then turn the LED off.`
    
    ![Screen Shot 2022-02-15 at 7.33.21 am.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-15_at_7.33.21_am.png)
    
    ```arduino
    // These constants won't change:
    const int analogPin = A0;    // pin that the sensor is attached to
    const int ledPin = 13;       // pin that the LED is attached to
    const int threshold = 400;   // an arbitrary threshold level that's in the range of the analog input
    
    void setup() {
      // initialize the LED pin as an output:
      pinMode(ledPin, OUTPUT);
      // initialize serial communications:
      Serial.begin(9600);
    }
    
    void loop() {
    // read the value of the potentiometer:
      int analogValue = analogRead(analogPin);
    }
    ```
    
    # Review
    
    1. Describe a decision in programming using plain language.
        1. Update the sentence with more technical language. 
    2. What’s a nested if statement?
    3. What’s the difference between a nested if block and a case switch?
    4. What logic gates or circuits can be found in the “StateChangeDetection Arduino” code?
    
    [Key Terms](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Key%20Terms%20f8417f78240c4791b0155ebdd0a87b3d.csv)
    
- Algorithm Design - Loops - Arduino
    
    
    # Arduino Implementation
    
    The Arduino language has the three loop structures identified on the General Learning Resource - `while`, `do..while` and `for`. As Arduino is a C-based language, the syntax for these are the same as with C, C++ etc.
    
    Here you can see the syntax and an example of each.
    
    ## While Loop
    
    ```arduino
    while (condition) {
      // statement(s)
    }
    ```
    
    ### Example
    
    ```arduino
    var = 0;
    while (var < 200) {
      // do something repetitive 200 times
      var++;
    }
    ```
    
    ## Do... While Loop
    
    ```arduino
    do {
      // statement block
    } while (condition);
    ```
    
    ### Example
    
    ```arduino
    int x = 0;
    do {
      delay(50);          // slight delay
      x = x + 1;          // add 1 to x.
    } while (x < 100);
    ```
    
    ## For Loop
    
    ```arduino
    for (initialization; condition; increment) {
      // statement(s);
    }
    ```
    
    ### Example
    
    ```arduino
    for (int i = 0; i <= 255; i++) {
        analogWrite(PWMpin, i);
        delay(10);
      }
    ```
    
    <aside>
    ‼️ Remember the *condition* has to equate to `true` or `false`.
    
    </aside>
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll be extending the Bank Alarm circuit by adding a number of additional LEDs to be used in a sequence. You will be using loops to access and cycle through the LEDs.
    
    </aside>
    
    Log into [Tinkercad](https://www.tinkercad.com/) and access the classroom used previously. Open the activity `Bank Alarm`.
    
    ## Modifying the Bank Alarm Circuit
    
    ### Add more LEDs
    
    Add four more LEDs and resistors, connecting them to pins 8, 7, 6 and 5.
    
    Change the colours of the cables to make it easier to read. 
    
    Each Ground wire should be black. 
    
    Set the resistance for each resistor to 220 Ω.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2050.png)
    
    At the end of the process, your wiring diagram should be similar to this.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2051.png)
    
    ## Adding functionality
    
    To add additional functionality, you’ll be using loops to configure the LED pins as output and then be using other loops to access each LED.
    
    Remove the `pinLED` constant and create an empty `for` loop in setup().
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2052.png)
    
    ```arduino
    for (int pinLED = 5; pinLED <= 9; pinLED++) {
       
    }
    ```
    
    Move the line `pinMode(pinLED, OUTPUT);` to be inside the for loop block.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2053.png)
    
    ```arduino
    pinMode(pinLED, OUTPUT);
    ```
    
    Update `setLEDBrightness()` to access the pins through a loop instead of writing to the individual pin. The `for` loop condition will be exactly the same as the one used in `setup()`.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2054.png)
    
    ```arduino
    for (int pinLED = 5; pinLED <= 9; pinLED++) {
        analogWrite(pinLED, LEDBrightness);
      }
    ```
    
    ## Test the Functionality
    
    Run the simulation and test to ensure that the functionality is as expected. 
    
    <aside>
    ‼️ You may notice there’s an issue with two of the LEDs - It’s got to do with something called ******Pulse Width Modulation******. Can you work out what the issue is?
    
    </aside>
    
    # Extension Exercises
    
    1. Using a for loop, set pins 2 to 5 as OUTPUT pins. Do this in setup(). 
        1. Attach LEDs to pins 2 to 5 (inclusive). Update loop(), using a for loop, to turn each each LED on, wait a second, and then turn them off in another for loop.
    
    [https://www.tinkercad.com/things/hyZxJA5vnY5](https://www.tinkercad.com/things/hyZxJA5vnY5)
    
    1. In a new Circuit, attach a button to pin 2 and a LED to pin 10. Using a while loop, code the circuit to turn the LED on when the button is pressed, and off when the button is not pressed.
    
    ## Answers
    
    This video shows how to approach and solve the first question, using For loops to access LEDs on different pins with efficient code.
    
    [https://youtu.be/_TbOxZKevcw](https://youtu.be/_TbOxZKevcw)
    
    # Review
    
    1. What is the difference between the available types of loops? Why choose one of the other/s?
    2. How many times can loops iterate?
    3. Write the steps in plain language, **using loops**, to 
        1. Read in individual lines of a text file (use the one shown)
        2. Calculate the GST
        3. Output the GST component to the user.
            
            ![Screen Shot 2022-01-27 at 9.44.53 pm.png](GDScript%20-%20Software%20Development%20Fundamentals%20c188b5273ab94c9696362483fccfa1d3/Screen_Shot_2022-01-27_at_9.44.53_pm.png)
            
        
        [Key Terms](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Key%20Terms%20dad3749844594d1fbab82a57f7b6a6e1.csv)
        
    
- Algorithm Design - Modularisation - Arduino
    
    
    # Arduino Implementation
    
    <aside>
    💡 `setup()` and `loop()` are functions that are required by the Arduino language.
    
    </aside>
    
    With Arduino, you will invariably be using some of the inbuilt functions as part of the language itself. For instance - `pinMode()`, `Serial.println()`, `digitalWrite()` etc. When you see brackets - () you are usually dealing with a function, or a condition.
    
    ## Custom Written Functions
    
    Organising your code with functions is an important skill to have when coding in any language.
    
    In Arduino, writing your own function requires the specific syntax of a C-based language. You can see in this example that the function declaration starts with the defining the return type, then the function name, and then any parameters.
    
    <aside>
    💡 If your function doesn’t return any data, the first keyword is void. Otherwise, you **must** declare the data type of the variable that will be returned.
    
    </aside>
    
    The curly brackets - `{}` - determine the start and the end of the function code block, which is run when the function is called.  
    
    ### Returning Data
    
    `return` is the keyword to end the function and “send” data back to where the function was called from.
    
    ![[https://docs.arduino.cc/learn/programming/functions](https://docs.arduino.cc/learn/programming/functions)](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/FuncAnatomy.png)
    
    [https://docs.arduino.cc/learn/programming/functions](https://docs.arduino.cc/learn/programming/functions)
    
    ### Returning Data Example 1
    
    Here is code to multiply two numbers together and return the result:
    
    ```arduino
    int myMultiplyFunction(int x, int y){
      int result;
      result = x * y;
      return result;
    }
    ```
    
    The function is called such as `myMultiplyFunction(10, 5);` but the result will need to be used once the function has been completed. You could store the result in a variable, or use it as part of another function call, such as printing it to the serial monitor. For example:
    
    ```arduino
    void setup() {
      // This block....
      int answer = myMultiplyFunction(10, 5);
      Serial.println(answer);
      
      // is functionally the same as this one
      Serial.println(myMultiplyFunction(10,5));
    }
    
    void loop() {
      // Nothing...
    }
    
    int myMultiplyFunction(int x, int y) {
      int result;
      result = x * y;
      return result;
    }
    ```
    
    [https://youtu.be/JPRBzRKqJ0I](https://youtu.be/JPRBzRKqJ0I)
    
    ### Returning Data Example 2
    
    It is possible, and often highly encouraged to have multiple return statements in a function. 
    
    Let’s say that you want a function to check to see if a sensor is reading a value over a set amount. This could be if a potentiometer is reading a value over 500. If the condition is correct (i.e. the value is over 100), the function will return `true`, otherwise it will return `false`. The function would be written as:
    
    ```arduino
    void loop()
    {
      isValid = validPotentiometerReading();
      if (isValid) {
        Serial.println("The sensor value is valid");
      } else {
        Serial.println("The sensor value is NOT valid");
      }
    }
    
    boolean validPotentiometerReading() {
      if (analogRead(A0) > 500) {
        return true;
      } else {
        return false;
      }
    }
    ```
    
    <aside>
    💡 The first return function executed will immediately end the function. I.e. only one return function will be executed for each function call.
    
    </aside>
    
    ![2022-01-06 22-52-19.2022-01-06 22_54_04.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/2022-01-06_22-52-19.2022-01-06_22_54_04.gif)
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll be programming an Arduino Uno to do the following:
    
    1. Set the brightness of the LED to be the value read by a variable input. In essence, you’re building a dimmable light switch.
    
    This task will involve writing and interfacing with two functions, the first to read the value set by the potentiometer, and the second to set the brightness of the LED.
    
    </aside>
    
    Log into [Tinkercad](https://www.tinkercad.com/) and access the classroom used previously. Open the activity `Bank Alarm`.
    
    <aside>
    ‼️ Remember to sign in with your school google account.
    
    </aside>
    
    With the Activity open, Under Shared with You, choose Copy and Tinker.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled.png)
    
    Open the Code tab to view the initial code.
    
    Currently, the code:
    
    - configures pin A0 to be INPUT
    - configures pin 9 to put OUTPUT, and
    - enables the Serial Monitor.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%201.png)
    
    <aside>
    ‼️ ********Explanation.********
    
    With the predefined circuit there are two components attached to the Arduino Uno
    
    1. an LED on Pin 9 which is a simple light bulb, and
    2. a Potentiometer on Pin A0, which provides the ability to read analog values that changes based on the position of the dial.
    
    The LED is an OUTPUT device and the Potentiometer is an INPUT device, hence the code configuring those pins as such. 
    
    </aside>
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%202.png)
    
    ## Reading the Potentiometer
    
    After `loop()` create a new function to read the value from the potentiometer.
    
    <aside>
    ‼️ The function header is made up of a number of sections:
    
    `int` indicates that this function will ******return****** a value as an **********integer********** (whole number).
    
    `readPotentiometer` is the name given to the function. Functions can be named ************almost************ anything, but they must not start with a number, and have no spaces. It is  advisable to name functions descriptively to indicate what their purpose is (more on that later in the project).
    
    `()` indicate what (if any) parameters are required by the function. As there are no parameters, the code requires just the open and close brackets.
    
    </aside>
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%203.png)
    
    ```arduino
    int readPotentiometer() {
      
    }
    ```
    
    Read the value of the potentiometer and store in a local variable. 
    
    <aside>
    ‼️ More on variables later in the project. Just think of the code temporarily storing the value to use later.
    
    </aside>
    
    ![SCR-20230111-lrj.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/SCR-20230111-lrj.png)
    
    ```arduino
    int potValue = analogRead(A0);
    ```
    
    Before making the code more complex, it’s advisable to check at regular intervals to ensure that smaller sections of code are working. In this case, you can print the value to the serial monitor to make sure the Potentiometer is reading correctly, and so you can see the range of values that are produced.
    
    Add code to output the value of the potentiometer, stored in `potValue` to the serial monitor.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%204.png)
    
    ```arduino
    Serial.println(potValue);
    ```
    
    The function is semi-complete, however it won’t execute the code contained within `readPotentiometer()` until you ********call******** the function, which is when you instruct the code when to execute (run) the code.
    
    Call the function in from `loop()` and then add a short delay into the code.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%205.png)
    
    ```arduino
    int potReading = readPotentiometer();
    delay(250);
    ```
    
    Press ********************************Start Simulation******************************** and expand the Serial Monitor tab.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%206.png)
    
    Change the position of the potentiometer and notice the output change.
    
    <aside>
    ‼️ Note how the values range from 0 to 1023. This will become important later.
    
    </aside>
    
    Stop the Simulation.
    
    ![Jan-11-2023 16-02-45.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Jan-11-2023_16-02-45.gif)
    
    The last modification needed for `readPotentometer()` is to ************return************ `potValue` back to where the function was called from.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%207.png)
    
    ```arduino
    return potValue;
    ```
    
    ## Rescaling the value
    
    As noted previously, the potentiometer provides values from 0-1023. The LED brightness can be set from 0-255, meaning that the value read by the potentiometer needs to be manipulated in some way for it to be useful and not cause unexpected behaviour.
    
    One possible solution to this issue is to use a prebuilt Arduino function called `map()`. This function takes a value and scales it from one range to another and keeps the position of the value the same.
    
    ![Pot -_ LED Mapping.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Pot_-__LED_Mapping.png)
    
    Update `loop()`to map the potentiometer values from 0-1023 to 0-255.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%208.png)
    
    ```arduino
    int brightness = map(potReading, 0, 1023, 0, 255);
    ```
    
    `brightness` is the value that will be used to set the brightness of the LED.
    
    ## Setting the LED brightness
    
    Create a new function to control the brightness of the LED - `setLEDBrightness(int LEDBrightness)`. 
    
    <aside>
    ‼️ This function does not need to return any data, so the keyword used is `void`.
    
    </aside>
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%209.png)
    
    ```arduino
    void setLEDBrightness(int LEDBrightness) {
      
    }
    ```
    
    Set the LED brightness using the built-in `analogWrite` function, passing it the Pin to output and the `LEDBrightness` variable.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2010.png)
    
    ```arduino
    analogWrite(9, LEDBrightness);
    ```
    
    Finally, call `setLEDBrightness()` from `loop()`, passing it `brightness`.
    
    ![Untitled](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Untitled%2011.png)
    
    ```arduino
    setLEDBrightness(brightness);
    ```
    
    ## Run the Circuit
    
    Run the simulation and you should see the LED brightness change depending on the value of the potentiometer.
    
    ![Jan-11-2023 16-48-38.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Jan-11-2023_16-48-38.gif)
    
    ### Final Code
    
    ```arduino
    void setup()
    {
      pinMode(A0, INPUT);
      pinMode(9, OUTPUT);
      Serial.begin(9600);
    }
    
    void loop()
    {
      int potReading = readPotentiometer();
      int brightness = map(potReading, 0, 1023, 0, 255);
      delay(250);
      setLEDBrightness(brightness);
    }
    
    int readPotentiometer() {
      int potValue = analogRead(A0);
      Serial.println(potValue);
      return potValue;
    }
    
    void setLEDBrightness(int LEDBrightness) {
      analogWrite(9, LEDBrightness);
    }
    ```
    
    # Review
    
    [Key Terms](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Key%20Terms%20e6dfea3e1c16479a8564bd55ef0f4ed1.csv)
    
- Style Guide - Arduino
    
    
    # Arduino Implementation
    
    ## Naming Conventions
    
    ********************Summary:******************** In Arduino, the conventions for naming items are:
    
    | Variables | lowerCamelCase |
    | --- | --- |
    | Constants | ALLCAPITALS |
    | Functions | lowerCamelCase |
    
    It is also standard convention to include comment blocks at the top of the code to explain the code, but also to include function header comments to explain the purpose of each function.
    
    Taken from : [https://www.arduino.cc/en/Reference/StyleGuide](https://www.arduino.cc/en/Reference/StyleGuide)
    
    ### Variables
    
    Avoid single letter variable names. Make them descriptive
    
    Avoid variable names like `val` or `pin`. Be more descriptive, like `buttonState` or `switchPin`
    
    If you want to define pin names and other quantities which won't change, use const ints. They're less messy than #defines, yet still give you a way to teach the difference between a variable and a constant.
    
    Use the wiring/Processing-style variable types, e.g. 
    
    - `boolean`,
    - `char`,
    - `byte`,
    - `int`,
    - `unsigned int`,
    - `long`,
    - `unsigned long`,
    - `float`,
    - `double`,
    - `string`,
    - `array`,
    - `void`
    
    when possible, rather than `uint8_t`, etc. The former are explained in the documentation, and less terse names.
    
    Avoid numbering schemes that confuse the user, e.g.:
    
    ```arduino
    pin1 = 2
    pin2 = 3
    etc.
    ```
    
    If you need to renumber pins, consider using an array, like this:
    
    ```arduino
    int myPins[] = { 2, 7, 6, 5, 4, 3 };
    ```
    
    This allows you to refer to the new pin numbers using the array elements, like this:
    
    ```arduino
      digitalWrite(myPins[1], HIGH);  // turns on pin 7
    
    ```
    
    It also allows you to turn all the pins on or off in the sequence you want, like this:
    
    ```arduino
    for (int thisPin = 0; thisPin < 6; thisPin++) {
       digitalWrite(myPins[thisPin], HIGH);
       delay(500);
       digitalWrite(myPins[thisPin], LOW);
       delay(500);
    }
    ```
    
    ## Example - Bad
    
    What does this code do?
    
    ```arduino
    void fc(float tt) {
      float c = ts.readTempC();
      m->setSpeed(100);
      if (c < tt) {
        fe = false;
      } else {
        fe = true;
      }
    }
    ```
    
    ## Example - Good
    
    ```arduino
    void waterPlant(int moistureValue) {
      /*
         Write a function which takes the moisture value,
         and if it's below a certain value, turns the pump on.
         The function is to be called waterPlant() which will
         take the moisture value as an argument, and return no value.
         @param moistureValue int measured from Moisture Sensor
         @return: void
      */
      if (moistureValue < 1000 ) {
        // motor/pump on
        myMotor->run(FORWARD); // May need to change to BACKWARD
        pumpIsRunning = true;
      } else {
        // motor/pump off
        myMotor->run(RELEASE);
        pumpIsRunning = false;
      }
    
    }
    
    ```
    
    More Information:
    
    [5.12. Arduino Coding Style Guide - 16-223 Introduction to Physical Computing](https://courses.ideate.cmu.edu/16-223/f2016/text/resrc/coding-style-guide.html)
    
    ## Commenting / Internal Documentation
    
    Each function needs a block comment to describe the purpose of the function. This block comment also should describe any arguments (inputs) and any return value (outputs).
    
    Consider the example shown previously.
    
    ```arduino
    void waterPlant(int moistureValue) {
      /*
         Write a function which takes the moisture value,
         and if it's below a certain value, turns the pump on.
         The function is to be called waterPlant() which will
         take the moisture value as an argument, and return no value.
         @param moistureValue int measured from Moisture Sensor
         @return: void
      */
      if (moistureValue < 1000 ) {
        // motor/pump on
        myMotor->run(FORWARD); // May need to change to BACKWARD
        pumpIsRunning = true;
      } else {
        // motor/pump off
        myMotor->run(RELEASE);
        pumpIsRunning = false;
      }
    }
    
    ```
    
    The block comment at the start of the function has three sections to it
    
    1. A description of the function and it’s goal, in plain language.
    2. A description of each of the parameters (`@param`).
    3. A description of the data that is returned (or **void** if none).
    
    [https://youtu.be/2MZAC6HL-J8](https://youtu.be/2MZAC6HL-J8)
    
    ## Good vs Bad Comments
    
    [Coding Rules: the Power of Correct Names, Good and Bad Comments](https://codegym.cc/groups/posts/369-coding-rules-the-power-of-correct-names-good-and-bad-comments)
    
    # Practical Exercises
    
    1. Update all existing code to match naming conventions & function header comments.
    
    # Review
    
    [Key Terms](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Key%20Terms%200b3cb6d11b6d4d32962e50e8924bd363.csv)
    
- Data Structures - Arduino
    
    
    # Arduino Implementation
    
    ## Arrays
    
    Arrays in Arduino are treated as standard variables, made up of other types. It’s important to note that in Arduino, the arrays are declared with a single data type, meaning that you cannot mix data types within the elements.
    
    <aside>
    💡 In Arduino, Array indexes start at 0. If your array has 5 elements, the maximum index is 4.
    
    </aside>
    
    ### Declaring Arrays
    
    Declaring arrays can be declared in a number of approaches in Arduino, much like other C-based languages. 
    
    Here are the options you have:
    
    ```arduino
    int myInts[6];                          // 6 Element array, with null as each element. 5 is maximum index. 
    int myPins[] = {2, 4, 8, 3, 6};         // 5 Element array, initialised with indicated values
    int mySensVals[5] = {2, 4, -8, 3, 2};   // Mixture of the two previous options.
    char message[6] = "hello";              // An array of chars, similar to a string.
    ```
    
    If you know how many elements you will need, you can declare an empty array of *n* elements. When an array is declared without the initial values, each element is `null`.
    
    ### Accessing Array Elements
    
    After declaring arrays, you can access individual elements by indicating the array by using its name, and then indicating the index within square brackets - `[]`. For example: `myInts[0] = 5;`
    
    ### Array Example
    
    ```arduino
    int arrayExample[10];
    
    void setup() {
      Serial.begin(9600);
      delay(100);
      for (int index = 0; index < 10; index++) {
        arrayExample[index] = index * 10;           // populates the array with 0, 10, 20, 30 etc.
      }
      delay(100);
    
      for (int index = 0; index < 10; index++) {
        Serial.println(arrayExample[index]);
      }
    }
    
    void loop() {
      // Nothing to see here...
      return;
    }
    ```
    
    ![Screen Shot 2022-01-08 at 10.15.29 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-01-08_at_10.15.29_pm.png)
    
    ## Key Value Pair
    
    Unlike C++, Arduino does not have the native ability to implement dictionaries. C++ refers to these structures as *maps*, although they are the same thing. This is due to the processing power and memory requirements for this structure, and the Arduino board does not have enough resources.
    
    # Practical Exercises
    
    # Extension Exercises
    
    ## LED Arrays
    
    <aside>
    💁 **Problem:** Create an Array of integers, representing pins 2-12. Attach LEDs to each of these pins. In your loop(), write a loop (`for`/`while`) to iterate over each pin, generating a random number between 0-255, and then set that as the brightness/strength of the LED.
    
    Use [`random()`](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870.md) to generate the random number. Hint: You will need to generate a new “seed” for each time you generate a random number. 
    
    </aside>
    
    ![2022-01-08 09-00-35.2022-01-08 09_01_23.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/2022-01-08_09-00-35.2022-01-08_09_01_23.gif)
    
    ### Copy Starting Project
    
    Open this project, and click on Copy and Tinker. This will give you the circuit to build from.
    
    [Tinkercad | From mind to design in minutes](https://www.tinkercad.com/things/4zdB1jGJSFy-led-array/editel)
    
    ![Screen Shot 2022-02-26 at 9.16.31 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_9.16.31_pm.png)
    
    <aside>
    💁 This project could be done without using an array. The code could create 11 different variables for each pin, however it can be more efficient to use arrays and loops to iterate over the pins. As always, this is only one approach to solve this problem.
    
    </aside>
    
    Replace the default code with this bare bones code base.
    
    ```arduino
    void setup()
    {
    
    }
    
    void loop()
    {
    
    }
    ```
    
    ### Define the Array
    
    Prior to the `setup()`, the global variables need to be defined. As the array of pin numbers is going to be used throughout the code, this means that the array needs to be defined outside of any function. 
    
    <aside>
    💁 See Variable Scope for more details.
    
    </aside>
    
    Add the array definition before `setup()`.
    
    ![Screen Shot 2022-02-26 at 9.25.04 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_9.25.04_pm.png)
    
    - Code
        
        ```arduino
        int ledPins[] = {2,3,4,5,6,7,8,9,10,11,12};
        ```
        
    
    Before the array can be iterated over, the size of the array needs to be stored. 
    
    It may seem obvious, however the code doesn’t automatically know how many elements are in the array, so it needs to be calculated.
    
    Inside setup() define a new array called `arraySize` and calculate the length of the array by calculating the amount of bytes the array takes up in memory and dividing it by the size of an individual integer variable.
    
    `arraySize` can be printed to the Serial Monitor to confirm that the value is correct.
    
    <aside>
    💁 Calculating the size of the array and storing it in a variable in code is future-proofing your code. If the number of pins changes (for instance only using pins 2-10) only the ledPins definition needs to be updated then the remainder of the code remains unchanged.
    
    </aside>
    
    ![Screen Shot 2022-02-26 at 9.43.42 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_9.43.42_pm.png)
    
    - Code
        
        ```arduino
        Serial.begin(9600);
        int arraySize = sizeof(ledPins) / sizeof(int);
        	Serial.println(arraySize);
        ```
        
    
    ### Configure the pins for Output
    
    This is where arrays can be used efficiently with loops. 
    
    Using a for loop, iterate over each pin (from 2 to 13 inclusive) and set each pin to output.
    
    First, inside `setup()`, define the for loop to iterate over the correct pins.
    
    ![Screen Shot 2022-02-26 at 9.44.16 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_9.44.16_pm.png)
    
    - Code
        
        ```arduino
        for (int individualPin=2; individualPin < arraySize; individualPin++) {
            
        }
        ```
        
    
    Inside the for loop, set each pin to OUTPUT by utilising the `ledPins` array and `individualPins` Loop Control Variable which updates each iteration.
    
    ![Screen Shot 2022-02-26 at 9.44.22 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_9.44.22_pm.png)
    
    - Code
        
        ```arduino
        pinMode(ledPins[individualPin], OUTPUT);
        ```
        
    
    That’s all that’s needed for configuration and setup. Now it’s time to write the code for the main loop.
    
    ### Coding `loop()`
    
    Inside `loop()`, create another for loop, exactly the same configuration as the one in `setup()`.
    
    ![Screen Shot 2022-02-26 at 9.48.10 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_9.48.10_pm.png)
    
    - Code
        
        ```arduino
        for (int individualPin=2; individualPin < arraySize; individualPin++) {
            
        }
        ```
        
    
    Generate a random number. This number will be generated between 0 and 255 to correlate with the possible strengths of the LEDs.
    
    <aside>
    💁 `[random(255)](https://www.arduino.cc/reference/en/language/functions/random-numbers/random/)` generates a Pseudo Random Number between 0 and 255;
    
    </aside>
    
    ![Screen Shot 2022-02-26 at 9.49.59 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_9.49.59_pm.png)
    
    - Code
        
        ```arduino
        int randomStrength = random(255);
        ```
        
    
    Using the number generated, write the randomStrength value to the pin using analogWrite. Additionally, put a short delay so it’s possible to see the LEDs before they change too quickly.
    
    ![Screen Shot 2022-02-26 at 9.54.11 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_9.54.11_pm.png)
    
    - Code
        
        ```arduino
        analogWrite(ledPins[individualPin], randStrength);
        delay(50);
        ```
        
    
    ### AnalogWrite and Pulse Width Modulation
    
    This code uses `[analogWrite()](https://www.arduino.cc/reference/en/language/functions/analog-io/analogwrite/)` which writes an analog value to a pin, using Pulse Width Modulation (PWM). This is a fantastic tutorial on the details of PWM.
    
    The short version of PWM is that the Arduino, whilst a digital device, can simulate analog data. Instead of writing simply `HIGH` or `LOW` , analogWrite can write values between 0 and 255. In this case, 0 would be the equivalent of `LOW` and 255 would be the equivalent of `HIGH`.
    
    [Pulse Width Modulation](https://learn.sparkfun.com/tutorials/pulse-width-modulation/all)
    
    ### Run the Code
    
    Run the simulation and watch the randomness unfold.
    
    ![2022-02-26 22-00-05.2022-02-26 22_00_13.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/2022-02-26_22-00-05.2022-02-26_22_00_13.gif)
    
    ## Sensor Input Storage
    
    <aside>
    💁 Problem: Create and code a circuit which reads 5 sensor values from separate potentiometers and stores them in an array. Each loop(), output the raw values and then the average. For instance: `45, 565, 23, 54, 1. Average: 137.6`
    
    </aside>
    
    Open this Circuit which has the wiring completed for the potentiometers.
    
    Click the Copy and Tinker button to open your own version.
    
    [Circuit design Sensor Input Storage Starter | Tinkercad](https://www.tinkercad.com/things/crk5oZw4Pv0-sensor-input-storage-starter)
    
    ![Spectacular Krunk-Bombul.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Spectacular_Krunk-Bombul.png)
    
    ### Configure the global variables
    
    Similar to the previous project, configure an array with the pins being used - A0 to A4. Additionally calculate and store the size of the array to be used later in loops.
    
    ![Screen Shot 2022-02-26 at 11.03.25 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_11.03.25_pm.png)
    
    - Code
        
        ```arduino
        int potPins[] = {A0, A1, A2, A3, A4};
        int arraySize = sizeof(potPins) / sizeof(int);
        ```
        
    
    Declare another array to store the values read for each potentiometer. At the beginning of the code, the values are unknown, and therefore shouldn’t be set. Arduino can declare an array of a specific size without any values.
    
    ![Screen Shot 2022-02-26 at 11.07.59 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_11.07.59_pm.png)
    
    - Code
        
        ```arduino
        int potValues[5];
        ```
        
    
    ### Configure the pins as inputs
    
    As before, define all the pins used as input pins. As the pins are stored in `potPins`, a for loop can be used to iterate over the pins and configure each to INPUT.
    
    Also configure the Serial monitor by running the `begin()` function.
    
    The configuration is now complete. It’s time to focus on `loop()`.
    
    ![Screen Shot 2022-02-26 at 11.14.31 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_11.14.31_pm.png)
    
    - Code
        
        ```arduino
        Serial.begin(9600);
        
        for (int individualPot = 0; individualPot < arraySize; individualPot++) {
          pinMode(individualPot, INPUT);
        }
        ```
        
    
    ### Read values from Each Potentiometer
    
    The code will read each value, store them in an array, print out each element in the array and then show the average. To start this, declare an integer variable called total which will store the addition of all the values read from the sensors.
    
    <aside>
    💁 The `total` variable is reset to 0 each time the loop function runs so as to not carry any values over from the previous loop.
    
    </aside>
    
    ![Screen Shot 2022-02-26 at 11.20.08 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_11.20.08_pm.png)
    
    - Code
        
        ```arduino
        int total = 0;
        ```
        
    
    Create a for loop which iterates over each analog pin.
    
    This is done in a very similar way to done previously. 
    
    <aside>
    💁 Note: `individualPot` is just an integer, which will go from 0 to 4. This will be used to access the pins that the potentiometers are attached to, and also the index of the `potValues` array to store the values in.
    
    </aside>
    
    ![Screen Shot 2022-02-26 at 11.21.37 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_11.21.37_pm.png)
    
    - Code
        
        ```arduino
        for (int individualPot = 0; individualPot < arraySize; individualPot++) {
            
        }
        ```
        
    
    Read the values for the pin and store the value in the correct index in potValues.
    
    This may seem a complex line of code, so let’s break it down a bit, starting with the right-hand side of the `=`. 
    
    `analogRead(potPins[individualPot])` . This part of the code runs `analogRead()` which reads the value sent to the Arduino from the sensor. The data in between the `()` refers to the particular pin. 
    
    In this case, the pin being referenced is `potPins[individualPot]`. The first time the loop runs, individualPot will be 0. `potPins[0]` is A0. 
    
    Therefore the first time the loop runs, this will read the value of the sensor attached to A0.
    
    The left-hand side of the = is `potValues[individualPot]`. On the first iteration of the loop, `individualPot` is 0 (as it is above), which will write the value to `potValues[0]`.
    
    ![Screen Shot 2022-02-26 at 11.25.05 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_11.25.05_pm.png)
    
    - Code
        
        ```arduino
        potValues[individualPot] = analogRead(potPins[individualPot]);
        ```
        
    
    ### Outputting the values
    
    The values have been stored, now it’s time to output.
    
    Create another for loop with the same configuration as previously done.
    
    ![Screen Shot 2022-02-26 at 11.33.34 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_11.33.34_pm.png)
    
    - Code
        
        ```arduino
        for (int individualPot = 0; individualPot < arraySize; individualPot++) {
            
          }
        ```
        
    
    Inside the new loop, calculate the total value of the individual potentiometers. This will be used later to calculate the average.
    
    ![Screen Shot 2022-02-26 at 11.35.06 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_11.35.06_pm.png)
    
    - Code
        
        ```arduino
        total = total + potValues[individualPot];
        ```
        
    
    Output the element of `potValues` for this iteration. The index used is `individualPot`.
    
    Also output a comma to the Serial Monitor to separate the values to make it more readable.
    
    ![Screen Shot 2022-02-26 at 11.37.19 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_11.37.19_pm.png)
    
    - Code
        
        ```arduino
        Serial.print(potValues[individualPot]);
        Serial.print(",");
        ```
        
    
    <aside>
    💁 Notice the use of `Serial.print()` instead of `Serial.println()` used elsewhere. Serial.print() still outputs to the Serial Monitor, however does **not** add a return or new line character at the end of the print command. `Serial.println()` will output the data and follow it automatically with a newline character.
    
    </aside>
    
    ### Calculate and output the Average
    
    After the total has been calculated and the values outputted, its time to calculate the average and output that value.
    
    After the second for loop, calculate the average using the following equation.
    
    In this code, this can be calculated as `average = total / arraySize`.
    
    $$
    average = \frac{total sum}{number of items in set}
    $$
    
    As the average will most likely be a decimal point value, this average variable will need to be declared as a `float` rather than an `int`.
    
    ![Screen Shot 2022-02-26 at 11.47.18 pm.png](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Screen_Shot_2022-02-26_at_11.47.18_pm.png)
    
    - Code
        
        ```arduino
        Serial.print("The average is : ");
        float average = total / arraySize;
        Serial.println(average);
        delay(100);
        ```
        
    
    ### Run the Simulation
    
    Start the Simulation and change the values of the Potentiometers. Make sure to expand the Serial Monitor to see the output.
    
    ![2022-02-26 23-48-59.2022-02-26 23_49_21.gif](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/2022-02-26_23-48-59.2022-02-26_23_49_21.gif)
    
    # Review
    
    1. What are the main differences between an Array and a Key Value Pair.
    2. **Practical** - Update the Sensor Input Storage code to include 5 LEDs attached to Digital Pins. Add additional functionality to the code by using the potentiometer values to power the brightness of the LEDS. 
        1. Note that the potentiometers input values from 0 to 1023, and the LEDs can accept PWM values from 0 to 255. You will need to research the `map()` command for Arduino to convert between the two number ranges.
        
        [Key Terms](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Key%20Terms%2008272f0c754445778368101e88bf47dc.csv)
        
    
- Technical Reports - Arduino
    
    
    # Arduino Implementation
    
    None
    
    # Practical Exercises
    
    # Review
    
    1. 
    
    [Key Terms](Arduino%20-%20Software%20Development%20Fundamentals%20cc4eab9811e94d60a4e3a154d8e47870/Key%20Terms%20f26ad0e9a39542a6a3a3c4c5b9ef1ff7.csv)
    
- Flowcharts - Arduino
    
    
    # Practical Exercises
    
    In your Github repository for the project, create a new file called `logic.md`.
    
    Open the file with Visual Studio Code. 
    
    <aside>
    ‼️ If it’s not installed, install the extension called “****Markdown Preview Mermaid Support”****. This allows you to render Markdown files, including mermaid in Visual Studio code. You can activate the preview by pressing this button.
    
    ![Untitled](GDScript%20-%20Software%20Development%20Fundamentals%20c188b5273ab94c9696362483fccfa1d3/Untitled.png)
    
    </aside>
    
    Using Mermaid, write the flowchart for the bank alarm code as it is at this stage.