# Documentation Structure Example

## Format Template

For each entry in the rubric, you can follow this basic template for a response

```mermaid
graph LR;
Introduction-->Evidence-->Analysis;
Analysis-->crit["Critical Analysis"];
```

So this *could* equate to 

1. Include a screenshot of code.
2. Explaining ‘how it works’ (Analysis), using technical language and linking it to other code or resources (research). You may also delve into explaining the technical details involved (again, research)
3. Critical Analysis (or Evaluation). Look at what you have submitted/discussed, and then evaluate it whether it solves the problem that was required or what you were attempting to solve. Compare and contrast to other options for solving the same problem.  

## Analysis Examples

### Robotics - Micro SD Card Module"
The Micro SD Card module in this project (below) is Serial Peripheral Interface (SPI) module which enables an Arduino, and other Microcontrollers, to read and write data to micro SD cards.

![Micro-SD-TF-Card-Module-Pinout-SPI.png](Micro-SD-TF-Card-Module-Pinout-SPI.png)

### Wiring

Different from the other components in this project, this device communicates over SPI, which is a specific communications protocol requiring specific pins to be used on the Arduino. The SPI pins for the Arduino Uno and Mega are shown here.

| Pin | Uno | Mega |
| --- | --- | --- |
| MISO | 12 | 50 |
| MOSI | 11 | 51 |
| SCK | 13 | 52 |
| CS | 10 | 53 |

Therefore, the *logical* wiring diagram for this module is:

![Screen Shot 2022-06-13 at 9.45.57 pm.png](Screen_Shot_2022-06-13_at_9.45.57_pm.png)

### Code

The Arduino code required to enable this module is:

Configuration

```
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

```
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

```
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

![Screen Shot 2022-06-14 at 8.10.38 pm.png](Screen_Shot_2022-06-14_at_8.10.38_pm.png)

As can be seen from the CSV output, the events are logged and can be used in an audit, or for forensic analysis for security issues.

### Critical Analysis / Evaluation

> This would require more research and detail.
{style="note"}

The project works and achieves the goals set up - log each event in the system as required. In this project, the log is written to a local SD card, making this system airgapped with no internet connectivity.

One improvement to the system could be connecting the microcontroller to the internet and upload the events to an external server. This would require a few changes and considerations. First the project as it stands cannot connect to the internet as the Arduino Uno does not have this functionality. A wifi Shield or module could be added to the project, such as this one:

[https://docs.arduino.cc/retired/getting-started-guides/ArduinoWiFiShield](https://docs.arduino.cc/retired/getting-started-guides/ArduinoWiFiShield)

This may require rewiring of the modules, and may not be possible if other pins are required. An Arduino Mega could be used to allow for this, but testing would need to be done.

Another option is change to a platform that has internet connectivity built in, such as the Adafruit ESP32 Feather, or Raspberry Pi.

One of the biggest issues with the SD card module that it appears to cause conflicts with other SPI module connected to the board, specifically in the case of the provided Bluetooth module - the nrf8001 module. According to research, the MicroSD card module used is not 100% compatible with the SPI protocol. In effect, when the SD card module is wired into the circuit, the bluetooth module does not broadcast. Other SPI modules may have similar issues, but further testing is required.

### References

[https://www.tutorialspoint.com/spi-in-arduino-uno#:~:text=ArduinoSoftware %26 CodingHardware,that uses SPI for communication](https://www.tutorialspoint.com/spi-in-arduino-uno#:~:text=ArduinoSoftware%20%26%20CodingHardware,that%20uses%20SPI%20for%20communication).

[https://tronixstuff.com/2011/05/13/tutorial-arduino-and-the-spi-bus/](https://tronixstuff.com/2011/05/13/tutorial-arduino-and-the-spi-bus/)

[http://elm-chan.org/docs/mmc/mmc_e.html](http://elm-chan.org/docs/mmc/mmc_e.html)

### Robotics - Arduino Route"

The default `/dashboard.html` route is:

![Screen Shot 2022-09-13 at 9.42.17 am.png](Screen_Shot_2022-09-13_at_9.42.17_am.png)

This contains a lot of information in the few short lines. Let’s analyse it.

First this route will execute (run) if the user attempts to access `dashboard.html`.

The first code that is executed is to check to see if the user has not authenticated yet.

The authentication is based on username and password, which are defined by the `http_username` and `http_password` variables defined in `sensitiveInformation`.

If the user hasn’t been authenticated with `http_username` and `http_password`, the server will send a message to the browser to collect that information.

Once authenticated, the system logs the event by running logEvent()

The server then sends `dashboard.html` to the browser.

False here indicates the the file is **not** set to download. If you wish the file to prompt to download (such as with the log file), this would be set to `true`.

Finally, processor is a function that will be run before the file (dashboard.html) is sent back to the browser.

### "Website Development"

#### Website Functionality

The website developed - Ngunnawal Country - has been written in Python, using the Flask framework and heavily utilises the common Bootstrap library.

![Untitled](Untitled.png)

The screenshot shows only some of the functionality through it’s navigation bar. The implemented functionality includes:

| Unregistered Users | Registered Users (includes all Unregistered Users functionality) | Administrators (includes all Registered Users functionality) |
|--------------------|------------------------------------------------------------------|--------------------------------------------------------------|
| Home               | Reset Their Password                                             | View All Contact Messages                                    |
| History            |                                                                  | List All Users                                               |
| Contact Us         |                                                                  | Reset other users account                                    |
| Gallery            |                                                                  | Enable / Disable Users                                       |
| Registration       |                                                                  |                                                              |
| Login              |                                                                  |                                                              |

##### User Management

One of the more complex modules of the website is the User Management system. This includes:

- User Registation
- User Login
- User Logout
- Password Reset
- User Level

These functions are supported by the User table in the database, as is visualised here.

![User.png](User.png)

The fields shown contain all the information for each user to be able to perform any of the User Management functions.

As with Flask’s approach to database connections, a model **is defined in code to match the database table. The model implemented in this project appears as:

![Untitled](UserClass.png)

Not only does the class contain variables to store the relevant fields in the database, but helper functions have been developed to assist the main code (app.py) to perform common functions regarding the user. For instance, `set_password` and `check_password` functions are used registering and logging in, to standardise the process of hashing the password before storing or checking what the user entered. This process is explained in the “Password Hashing” section.

#### Password Hash

From a security aspect, the password hash is the most important field in the table as it securely stores the users password. If an unauthorised person gained access to the database, they wouldn’t be able to read the password.

This project utilises the [werkzeug.security](http://werkzeug.securityhttps://werkzeug.palletsprojects.com/en/2.3.x/utils/) library which is best-practice for Flask projects, providing the `generate_password_hash()` and `check_password_hash()` functions. By default, the one-way algorithm used to generate and check password hashes is `scrypt`.

### Interactive Software Development
TBA
