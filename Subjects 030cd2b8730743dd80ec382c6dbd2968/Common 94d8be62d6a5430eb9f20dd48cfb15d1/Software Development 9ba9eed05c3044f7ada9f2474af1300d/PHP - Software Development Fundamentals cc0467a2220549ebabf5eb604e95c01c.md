# PHP - Software Development Fundamentals

- Course Introduction - PHP
    
    
    # Website Development Overview
    
    Front-end website development refers to the client-side of web development, which deals with the design and user experience of a website. This includes technologies such as HTML, CSS, and JavaScript, which are used to build the layout, look and feel, and interactivity of a website.
    
    Back-end website development, on the other hand, deals with the server-side of web development, which is responsible for the functionality of a website. This includes technologies such as PHP, Ruby, Python, and JavaScript, as well as databases like MySQL and MongoDB. Back-end developers are responsible for building and maintaining the code that runs on the server and powers the functionality of a website, such as data storage, processing, and retrieval.
    
    In this course, the focus will be on the back-end functionality, with **PHP** being the main language for this. The course will also show how to interface with a database using **SQL**. Whilst building the site, you will also be learning some front-end technologies as well - HTML, CSS and Javascript.
    
    ![web front and back end technologies.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/web_front_and_back_end_technologies.png)
    
    The code that will be written for this course will be executed in a number of different places - front end code (HTML, CSS and Javascript) are rendered and executed in the browser on the client device. The back-end code is executed on the web server, and this acts as an Intermediary between the client device and the database.
    
    ![PHP process explained.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/PHP_process_explained.png)
    
    # PHP Implementation
    
    PHP is a **server side** scripting language. This means that PHP code runs on the server (not the client/browser) and delivers the necessary code to the client to display. 
    
    For example, the server loads user information from the database and checks the username and password. If the password is correct, the browser is to display a message “login successful”. 
    
    PHP co-exists with HTML and other Web Technologies. Unlike standard HTML, PHP requires a server to be running to process the PHP code.
    
    PHP was created in 1994, so in terms of Programming Languages it is quite old, but it is very powerful and widespread.
    
    PHP is used by itself but is also the main language in many other frameworks available, such as Wordpress and Laravel.
    
    ![PHP mixed in with HTML.](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screen_Shot_2022-08-30_at_9.05.41_pm.png)
    
    PHP mixed in with HTML.
    
    ![PHPDevelopment_53c5061d67f82_w1500.jpeg](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/PHPDevelopment_53c5061d67f82_w1500.jpeg)
    
    # Project Overview
    
    Over this course of this term, you will develop a website which will allow the users to order products through a simple shopping cart system. The site will save these orders into a text file, and then allow users to load invoices for the orders.
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll be creating the accounts and installing the software you’ll be using for this course.
    
    </aside>
    
    Create a Jetbrains Educational Account.
    
    <aside>
    ‼️ Log in using Google, and use your school account!
    
    </aside>
    
    [Free Educational Licenses - Community Support](https://www.jetbrains.com/community/education/#students)
    
    ## Install PHPStorm (if not already installed)
    
    Using the Jetbrains toolbox, Install PHPStorm. 
    
    You can follow the video, here, but install PHPStorm instead.
    
    [2020 07 19 - Install Pycharm Final.mp4](https://drive.google.com/file/d/1-2Z0MS-TXCvL807bcc8l4oCGx6GzIKd6/view?usp=drivesdk)
    
    ## Install XAMPP
    
    > XAMPP is a completely free, easy to install Apache distribution containing MariaDB, PHP, and Perl.
    > 
    
    This allows you to run PHP code on a web server (Apache) that is running on your local machine.
    
    Download the installer. Choose the latest version for your OS. At the time of writing, the latest version was `8.1.12`.
    
    `Note, if you’re on macOS, choose the Installer version (not the VM).`
    
    [Download](https://www.apachefriends.org/download.html)
    
    Install XAMPP on your machine.
    
    On Windows, leave the installation directory as the default - C:\xampp.
    
    ![Screenshot 2022-11-21 at 11.44.25 am.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-21_at_11.44.25_am.png)
    
    After installation, run XAMPP, click on the Manage Servers tab and start `Apache Web Server` and `MySQL Database` are running.
    
    ![Screenshot 2022-11-21 at 12.08.11 pm.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-21_at_12.08.11_pm.png)
    
    ## PHPMyAdmin
    
    After the XAMPP installation, test to ensure that it’s all working by access PHPMyAdmin on your local machine.
    
    [](http://127.0.0.1/phpmyadmin/)
    
    ![Screenshot 2022-11-21 at 12.11.19 pm.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-21_at_12.11.19_pm.png)
    
    ## Create a Github Account
    
    <aside>
    ‼️ If you already have a github account, you can skip this step.
    
    </aside>
    
    1. Go to [https://github.com/join](https://github.com/join).
    2. Using your school email address (...@schoolsnet.act.edu.au) create a Github account.
    
    ## Duplicate Project
    
    Open the link to view the template project on Github for this project. 
    
    [https://github.com/Lake-Tuggeranong-College/Software-Development-Fundamentals-PHP-Template](https://github.com/Lake-Tuggeranong-College/Software-Development-Fundamentals-PHP-Template)
    
    Click on the **Use This Template** Button.
    
    ![SCR-20221212-han-2.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/SCR-20221212-han-2.png)
    
    Click **Create New Repository** to make a copy of the project into your account.
    
    ![SCR-20221212-hd2-2.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/SCR-20221212-hd2-2.png)
    
    Give the project a name, such as `Software-Development-Fundamentals-PHP` and then click **************************************************************Create Repository from Template**************************************************************. 
    
    This will create a new repository in your account.
    
    ![SCR-20221212-heq-2.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/SCR-20221212-heq-2.png)
    
    Once that’s completed, open PHPStorm and choose ************************Get from VCS.************************
    
    ![SCR-20221212-hh6-2.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/SCR-20221212-hh6-2.png)
    
    Select **Github** in the menu on the left, find the project you just created and click **Clone**.
    
    ![SCR-20221212-hhx-2.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/SCR-20221212-hhx-2.png)
    
    The project will now open. If PHPstorm asks you if you trust the project, click Trust. 
    
    Double click on `hello.php`. Click the popup to view the rendered page in the PHPStorm internal browser.
    
    ![Screen Shot 2022-12-12 at 12.41.13 pm.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screen_Shot_2022-12-12_at_12.41.13_pm.png)
    
    When you first open the project, you will receive a ******************************502 Bad Gateway****************************** error. This is due to PHPStorm not knowing where PHP is installed on your computer. Click on ****************************Configure PHP Interpreter**************************** in the notification.
    
    If PHPStorm shows the other notification, click **Don’t Ask Again**.
    
    ![SCR-20221212-hnw-2.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/SCR-20221212-hnw-2.png)
    
    To configure the PHP Interpreter, click on the `...` button.
    
    ![SCR-20221212-hp8-2.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/SCR-20221212-hp8-2.png)
    
    Click the `+` to add a new interpreter.
    
    ![SCR-20221212-hpk-2.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/SCR-20221212-hpk-2.png)
    
    In the `+` menu that appears, if the PHP is not automatically detected, you’ll need to browse to where PHP is installed (c:\XAMPP), and then under `bin/php`. This is the file you wish to choose.
    
    Click Ok and then Ok again.
    
    ![SCR-20221212-hq1-2.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/SCR-20221212-hq1-2.png)
    
    Using Kubuntu in 6118, when configuring the PHP Interpreter in PHPStorm, set the PHP Executable to `/opt/lampp/bin/php`. This should detect it as PHP Version 8.2.0
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2018.png)
    
    Close the preview window and then reopen it and you’ll see `Hello World` appear. This means that the project and PHP is configured correctly.
    
    ![SCR-20221212-hqd.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/SCR-20221212-hqd.png)
    
    ## Publish Project to Github
    
    Open the PHP project in PHP.
    
    ![Screenshot 2022-11-21 at 1.17.28 pm.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-21_at_1.17.28_pm.png)
    
    Choose VCS→ Enable Version Control Integration.
    
    ![Screenshot 2022-11-21 at 1.14.11 pm.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-21_at_1.14.11_pm.png)
    
    Choose Git and click Ok.
    
    ![Screenshot 2022-11-21 at 1.14.58 pm.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-21_at_1.14.58_pm.png)
    
    Open Settings (File → Settings). Under Version Control Click Githhub and then click the + button to add a new Github account. Choose Login Via Github.
    
    Log in to Github with your browser and authorise the connection.
    
    ![Screenshot 2022-11-21 at 1.12.28 pm.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-21_at_1.12.28_pm.png)
    
    # Review
    
    1. What was PHP original developed for?
    2. Where did the name "bug" originate?
    3. What is this "Hello World" you speak of?
    4. In plain language, What is the difference between interpreted and compiled code?
        1. Expand on your explanation by adding technical details.
    5. Is PHP compiled or interpreted? 
    6. What is the best programming language to learn? Why?
- Version Control - PHP
    
    
    # PHP Implementation
    
    N/A
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll be learning:
    
    - what Git and Github is,
    - How Version control is important in software development.
    - What a **commit** is and how to perform one.
    - How to **push** and **pull** changes to repositories.
    </aside>
    
    ## Github Courses
    
    To practice the use of Git and Github, complete the following course:
    
    ### Introduction to Github
    
    [https://github.com/skills/introduction-to-github](https://github.com/skills/introduction-to-github)
    
    ### Communicate with Markdown
    
    [https://github.com/skills/communicate-using-markdown](https://github.com/skills/communicate-using-markdown)
    
    ## Software Development Project
    
    Open your `Software-Development Fundamentals-PHP` project in PHPStorm.
    
    Update `[README.md](http://README.md)` with information about you and your project.
    
    Commit and Push changes to Github.
    
    # Review
    
    1. When do you push a project?
    2. When do you pull a project?
    3. Is Git a distributed or centralised system? Why?
    4. How does Version Control assist in software development?
    
    [Key Terms](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Key%20Terms%20d612866e40984da4bc6ecbd4bfce80d2.csv)
    
- Computational Thinking - PHP
    
    
    # PHP Implementation
    
    N/A
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll be looking at large problems and considering how to tackle them.
    
    </aside>
    
    1. Consider the following problem. Decompose it into smaller problems.
        1. The ACT Government has given you a grant to protect the bike path / walkway around Lake Tuggeranong due to your robotics experience. You are tasked with building an autonomous robot to patrol the path and notify Transport Canberra and City Services of any obstacle or dangerous item.
    
    # Review
    
    [Key Terms](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Key%20Terms%204edbf8d2e6b94fcf8b10d93fd8a39acd.csv)
    
- Mathematical & Logic Operations- PHP
    
    
    # PHP Implementation
    
    N/A
    
    # Practical Exercises
    
    # Review
    
- Variables and Data Types - PHP
    
    
    # PHP Implementation
    
    In PHP, all user defined variables **********must********** start with `$`. 
    
    For example:
    
    `$username = **"Obiwan Kenobi"**;`
    
    In this case `username` is the variable name.
    
    > Rules for PHP variables:
    A variable starts with the `$` sign, followed by the name of the variable
    A variable name must start with a letter or the underscore character
    A variable name cannot start with a number
    A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
    Variable names are case-sensitive (`$age` and `$AGE` are two different variables)
    [https://www.w3schools.com/php/php_variables.asp](https://www.w3schools.com/php/php_variables.asp)
    > 
    
    ## Declaring Variables
    
    PHP is a Loosely Typed Language (alternatively called Weakly Typed) meaning the rules for what data can be stored in variables is lax. For example, you do not need to declare the data type of variables when you first use them, unlike other some other languages (most notably C-based languages (Arduino, Java etc). 
    
    ```php
    $radius = 5;
    $area = pi() * $radius * $radius;
    echo "The area is ", $area;
    ```
    
    More complex example:
    
    ```php
    $numberInput = $_GET["age"];
    ```
    
    ## Using Variables
    
    After the variable has been declared and data stored within it, the data can be used at a later stage of the code. When the code executes, the value stored within the variable name is used instead:
    
    This example will calculate the area of a circle with a radius of 5.
    
    The output will be :
    
    ![Screenshot 2022-11-21 at 2.52.24 pm.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-21_at_2.52.24_pm.png)
    
    ```php
    $radius = 5;
    $area = pi() * $radius * $radius;
    echo "The area is ", $area;
    
    ```
    
    ```php
    $numberInput = $_GET["age"];
    echo "The square of ".$numberInput." is ".squareNumber($numberInput)."<br>";
    echo "The square root of ".$numberInput." is ".squareRootNumber($numberInput)."<br>";
    echo "<br>";
    ```
    
    ## PHP Data Types
    
    PHP Supports these data types.
    
    | Data type | Description | Possible Values |
    | --- | --- | --- |
    | Integer | Whole number value. | Range between -2,147,483,648 and 2,147,483,647 |
    | Boolean | Value either true or false (1 or 0). | true or false.  |
    | Float | Numbers with decimal point values | 5.3
    0.1 |
    | String | Complex (non-primitive) data type. Comprised of a series of characters in an array. Use double quotes. An an array, Strings allow for more complex functionality, such as converting to integers, searching for substrings, converting to upper case etc. | "Lake Tuggeranong College"
    "32" |
    
    ## Constants
    
    Constants are variables where the channel cannot be changed once it’s been defined.
    
    ```php
    define("school", "Lake Tuggeranong College");
    ```
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll learn:
    
    - How to create a simple HTML form,
    - The PHP code to collect the data the user entered in the form, and
    - How to output variables onto a HTML page.
    </aside>
    
    Open your `Software-Development Fundamentals-PHP` project. In this stage of the project, you will be creating a simple contact form, which will collect data from the user and then display it back to them to confirm. 
    
    ## Contact Page
    
    Right click on the Project name in the Project Explorer and choose New→PHP file. 
    
    ![Screenshot 2022-11-21 at 2.11.30 pm.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-21_at_2.11.30_pm.png)
    
    Enter `contact` for the filename. This will create the contact.php file.
    
    ![Screenshot 2022-11-21 at 2.13.41 pm.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-21_at_2.13.41_pm.png)
    
    PHPStorm may ask you if you wish to add this to the Git Repository. Click `Don’t Ask Again`, and then click Add.
    
    ![Screenshot 2022-11-21 at 2.13.50 pm.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-21_at_2.13.50_pm.png)
    
    Replace the contents of the the file with the standard ‘template’ for HTML files for this project.
    
    [https://gist.github.com/RyanCather/7af6a1df2bc62ec750d137ea9a77d336](https://gist.github.com/RyanCather/7af6a1df2bc62ec750d137ea9a77d336)
    
    After the heading copy the code for a simple HTML form.
    
    This may look complex, however much of the code is Bootstrap code to display the form in a certain way. 
    
    At this stage, the important aspects to note is the `name` attributes of each of the `input` fields - `inputEmail` and `inputMessage`. These will be referred to later in PHP code.
    
    ![Screenshot 2022-11-22 at 9.49.12 am.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-22_at_9.49.12_am.png)
    
    ```html
    <div class="container-fluid">
        <form action="contact.php" method="post">
            <div class="mb-3">
                <label for="inputEmail" class="form-label">Email address</label>
                <input type="email" class="form-control" id="inputEmail" name="inputEmail" aria-describedby="emailHelp">
                <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
            </div>
            <div class="mb-3">
                <label for="inputMessage" class="form-label">Message</label>
                <input type="text" class="form-control" id="inputMessage" name="inputMessage">
            </div>
            <button type="submit" class="btn btn-primary">Submit</button>
        </form>
    </div>
    ```
    
    At this stage, the page simple shows the form but doesn’t do anything with the data when the user presses submit. That’s where PHP is introduced.
    
    ![Screenshot 2022-11-22 at 9.50.51 am.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-22_at_9.50.51_am.png)
    
    After the form add PHP code to detect if the form has been submitted. This is done through the `$_SERVER["REQUEST_METHOD"] == "POST"` check. 
    
    `POST` is a standard webserver protocol, and is linked with the `<form action="contact.php" method="post">` code created earlier. When the user presses the submit button on the form, the form is `post`ed back to the server. The PHP code added detects that `post` and can respond accordingly.
    
    ![Screenshot 2022-11-22 at 9.52.34 am.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-22_at_9.52.34_am.png)
    
    ```php
    <?php
    if ($_SERVER["REQUEST_METHOD"] == "POST") {
    
    }
    ?>
    ```
    
    If the PHP code detects the post (meaning the user presses the submit button), the code will then access and store the data the user entered into the form field.
    
    `$_POST['inputEmail'];` refers to the field with the name `inputEmail` created earlier. Likewise for `inputMessage`.
    
    <aside>
    ‼️ `$emailAddress` and `$messageSubmitted` are two variables to store the data entered into the form. What data type would they be?
    
    </aside>
    
    ![Screenshot 2022-11-22 at 9.55.38 am.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-22_at_9.55.38_am.png)
    
    ```php
    $emailAddress = $_POST['inputEmail'];
    $messageSubmitted = $_POST['inputMessage'];
    ```
    
    The last step is then to output the values stored in the two variables. This can be done simply by using the `echo` command to output the values onto the webpage itself.
    
    ![Screenshot 2022-11-22 at 9.57.10 am.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Screenshot_2022-11-22_at_9.57.10_am.png)
    
    ```php
    echo $emailAddress;
    echo "<p>";
    echo $messageSubmitted;
    ```
    
    Test the form by entering data and pressing submit. The data entered should be displayed on screen.
    
    ![2022-11-22 09-59-41.2022-11-22 10_00_25.gif](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/2022-11-22_09-59-41.2022-11-22_10_00_25.gif)
    
    Update the Heading on the page to the Contact page.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2019.png)
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2020.png)
    
    In this Contact form, a standard programming process has been developed - Input → Processing → Output. The data gets inputted into the system, it is processed and then outputted.
    
    $* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 
    
    # Review
    
    1. How is data stored in memory?
    2. What’s the difference between primitive and non-primitive data types?
    3. What is type inference?
        1. Find three programming languages that use type inference.
    4. What is the opposite of type inference?
        1. Find three programming languages that don’t use type inference.
    5. What does strongly typed and weakly typed languages mean?
    
    [Key Terms](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Key%20Terms%209c4a88c2e20f4199916605f56090161d.csv)
    
- Algorithm Design - Sequence - PHP
    
    
    # PHP Implementation
    
    PHP can co-exist with HTML in the source file, meaning it can be challenging to read a single file as there could be a number of languages in a single file.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2021.png)
    
    <aside>
    ‼️ PHP code can be included with HTML as many time as needed in a single file.
    
    </aside>
    
    To start a PHP block, you can either use `<?php` or simple `<?` and end the PHP block with `?>`. 
    
    This code collects data from a HTML form (`$_GET['username']`) and then outputs it in the rendered HTML page.
    
    `echo` outputs information to the rendered page.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2022.png)
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2023.png)
    
     
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll 
    
    </aside>
    
    # Review
    
- Algorithm Design - Decisions - PHP
    
    
    # PHP Implementation
    
    PHP `if` blocks are similar to C (and other languages) in their syntax.
    
    An example of a PHP `if` is:
    
    ```php
    <?php
    $subtotal = 24.5;       // Subtotal of the bill
    $discount = 0.1;        // discount is applied if subtotal is over $50
    $total = 0;
    
    if ($subtotal >= 50) {
        $total = $subtotal - ($subtotal * $discount);
    } else {
        $total = $subtotal;
    }
    
    echo "Total = $" . $total;
    
    ?>
    ```
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll be implementing a simple error checker by updating the Contact Us page to include some feedback in case the user leaves a field empty.
    
    </aside>
    
    Open `contact.php` created in Variables and Data Types.
    
    Find the code which tests if the form has been submitted.
    
    ![SCR-20230120-tl7.png](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/SCR-20230120-tl7.png)
    
    The logic of what needs to be done is shown in this flowchart
    
    ```mermaid
    flowchart TD
    terminalStart([Previous code])
    terminalEnd([Continue remainder of code])
    ifFormSubmit{Has form been submitted?}
    ifEmailEmpty{Is Email Field empty?}
    ifMessageEmpty{Is Message Field empty?}
    setEmailErrorFlag[formError = true]
    setMessageErrorFlag[formError = true]
    outputEmailError[Please enter a valid email address]
    outputMessageEmpty[Please enter a message]
    ifError{if formError}
    setEmailAddress["emailAddress <- Email field data"]
    setMessage["messageSubmitted <- Message field data"]
    echoEmail[output email address]
    echoMesssage[output message]
    
    terminalStart-->ifFormSubmit-->ifEmailEmpty-->|True|setEmailErrorFlag-->outputEmailError-->ifMessageEmpty
    ifEmailEmpty-->|False|ifMessageEmpty-->|True|setMessageErrorFlag-->outputMessageEmpty-->ifError
    ifMessageEmpty-->|False|ifError-->setEmailAddress-->setMessage-->echoEmail-->echoMesssage-->terminalEnd
    ```
    
    To implement this logic, first set the value of `$formError` to be `false`.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled.png)
    
    ```php
    $formError = false;
    ```
    
    Next implement the code to check each field and whether it is empty.
    
    PHP has a helper function called `empty()` which returns `true` if the variable or object is empty and `false` if there is some data stored. If the user does not enter an email address, `$_POST['inputEmail'])` will be empty and therefore return `true` which will then run the code in the `if` block.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%201.png)
    
    ```php
    if (empty($_POST['inputEmail'])) {
        $formError = true;
        echo "Enter an email address.";
    }
    if (empty($_POST['inputMessage'])) {
        $formError = true;
        echo "Enter a message to submit.";
    }
    ```
    
    The remainder of the existing code which collects and then displays the email address and message entered can remain the same, although be placed in an `if` block to check if the `formError` variable has been set to `true`.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%202.png)
    
    ```php
    if ($formError == false) {
            ...
    }
    ```
    
    Test the changes made. Check the functionality by testing all combinations of data (✅) and no data (❌).
    
    | Attempt | Email Address | Message |
    | --- | --- | --- |
    | 1 | ❌ | ❌ |
    | 2 | ❌ | ✅ |
    | 3 | ✅ | ❌ |
    | 4 | ✅ | ✅ |
    
    $* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 
    
    # Review
    
- Algorithm Design - Loops - PHP
    
    
    # PHP Implementation
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll 
    
    </aside>
    
    # Review
    
- Algorithm Design - Modularisation - PHP
    
    
    # PHP Implementation
    
    In PHP, functions are identified with the `function` keyword. 
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%203.png)
    
    PHP functions can be called from other PHP blocks.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%204.png)
    
    ## PHP Arguments
    
    Functions can accept data through Arguments. Arguments are declared in the function declaration as with many other programming languages. 
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%205.png)
    
    ## PHP Return Data
    
    PHP does not **************require************** the declaration of return data when declaring functions. Arguably it is recommended to do so if known, however not strictly required.
    
    When declaring functions, identify the return data type after the `()` with `: <data type>`.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%206.png)
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll be creating code functions that will be used multiple times throughout the site. 
    
    </aside>
    
    The site being developed requires a number of forms on various pages, and on those pages will have a number of fields that need to be completed.
    
    ## Template Page
    
    Open your `Software-Development Fundamentals-PHP` project. Open Create a new PHP file called `template.php`. Add the file to Git if required.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%207.png)
    
    $* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 
    
    ## Footer Code
    
    A simple example of implementing functions at this stage is to create a function to have a standardised footer on all pages across the site.
    
    Open `template.php`.
    
    Create a new function called `footer()`. This function doesn’t need any parameters as it will simply dynamically generate the HTML code for the footer and return it to where it was called from.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%208.png)
    
    Add the code to generate a string which includes the last date and time that the file was saved.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%209.png)
    
    ```php
    $filename = basename($_SERVER["SCRIPT_FILENAME"]);
    $footer = "This page was last modified: " . date("F d Y H:i:s.", filemtime($filename));
    return $footer;
    ```
    
    Create `index.php` if there is not already one created. Replace the contents of the file with the default code.
    
    ```php
    <!doctype html>
    <html lang="en">
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <title>PHP Template</title>
        <link href="css/bootstrap.min.css" rel="stylesheet">
    </head>
    <body>
    <h1>Heading</h1>
    
    </body>
    <script src="js/bootstrap.bundle.min.js" ></script>
    </html>
    ```
    
    Add the PHP code to load another file into the current file for the server to process.
    
    <aside>
    ‼️ Including other files can save you a lot of development time, as you can write the code once and access it many times. Having a central location for this shared code can also make it quicker to update code, as there is only one place to update code, not spread out through other files.
    
    </aside>
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2010.png)
    
    ```php
    <?php include "template.php"?>
    ```
    
    Execute and output the result from `footer()` near the bottom of the page - just before `</body>`. 
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2011.png)
    
    ```php
    <?php echo footer() ?>
    ```
    
    Open the page in the browser and you should see the footer output.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2012.png)
    
    One of the issues with the output is that the time is not correct, specifically, it is in GMT. Edit `template.php` to first set the timezone correctly before generating the time the file was modified. 
    
    Save the file.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2013.png)
    
    ```php
    date_default_timezone_set('Australia/Canberra');
    ```
    
    Open `index.php` in the browser again and the time should be accurate.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2014.png)
    
    $* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 
    
    ## Sanitising Data
    
    Open `template.php`.
    
    One of the biggest issues, outside the actual website development, that need to be considered throughout the process, is the security of site itself. Whenever websites accept data through forms, it is possible that malicious users could attempt to cause issues by including code in the form.
    
    This is known as Cross Site Scripting (XSS).
    
    [https://www.youtube.com/watch?v=EhOcAZJp81s](https://www.youtube.com/watch?v=EhOcAZJp81s)
    
    [https://www.youtube.com/watch?v=M_nIIcKTxGk](https://www.youtube.com/watch?v=M_nIIcKTxGk)
    
    As there is many fields for data to be submitted, instead of individually sanitising each field, a function can be written to sanitise the data and when the forms are submitted, the function is called for each field.
    
    Declare a new function called `sanitiseData` which accepts a variable which will be the unsanitised data.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2015.png)
    
    ```php
    function sanitiseData($unsanitisedData)
    {
    
    }
    ```
    
    This function, at this stage, will manipulate `unsanitisedData` in three ways.
    
    First, the string is `trim`ed which removes white space (spaces/tabs) from the beginning of the string.
    
    E.g.           `data` becomes `data`.
    
    Then `stripslashes` is run on the trimmed string which removes any `\` from the string which can be used to indicate a string with quotes within it.
    
    E.g. `stripslashes("Who\'re you?")` would return `Who're you?`
    
    Finally, `htmlspecialchars` is run which convert certain characters (&, “,. ‘, < and >) into the HTML code version. This removes the possibility that the string will have HTML code included.
    
    E.g. `echo("This is some <b>bold</b> text.");` will be converted to `This is some &lt;b&gt;bold&lt;/b&gt; text.` . The browser then renders (displays) this as normal, however it couldn’t run it as code.
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2016.png)
    
    ```php
    $unsanitisedData = trim($unsanitisedData);
    $unsanitisedData = stripslashes($unsanitisedData);
    $sanitisedData = htmlspecialchars($unsanitisedData);
    return $sanitisedData;
    ```
    
    This function will be used in the future whenever data is uploaded through a HTML form.
    
    $* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 
    
    ![Untitled](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Untitled%2017.png)
    
    ## Contact Page
    
    Create a new file `contact.php` and copy the contents of index into it.
    
    Add code to create the HTML form below the H1 tag and about the footer() output.
    
    ```php
    <div class="container-fluid">
        <h1 class="text-primary">Please Send us a Message</h1>
        <form action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]); ?>" method="post">
            <div class="mb-3">
                <label for="contactEmail" class="form-label">Email address</label>
                <input type="email" class="form-control" id="contactEmail" name="contactEmail"
                       placeholder="name@example.com">
            </div>
            <div class="mb-3">
                <label for="contactMessage" class="form-label">Message</label>
                <textarea class="form-control" id="contactMessage" name="contactMessage" rows="3"></textarea>
            </div>
            <button type="submit" name="formSubmit" class="btn btn-primary">Submit</button>
        </form>
    </div>
    ```
    
    # Review
    
- Style Guide - PHP
    
    
    # PHP Implementation
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll 
    
    </aside>
    
    # Review
    
- Data Structures - PHP
    
    
    # PHP Implementation
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll 
    
    </aside>
    
    # Review
    
- Technical Reports - PHP
    
    
    # PHP Implementation
    
    # Practical Exercises
    
    <aside>
    🏁 **********Goal**********
    
    In this task, you’ll 
    
    </aside>
    
    # Review
    
    [Key Terms](PHP%20-%20Software%20Development%20Fundamentals%20cc0467a2220549ebabf5eb604e95c01c/Key%20Terms%20b5e729d7226e407ab9311cb0ef9823e0.csv)