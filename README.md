# Time_Driven_Access_Control_System
Project Title: The Time-Driven Access Control System is an embedded security solution that regulates access based on predefined time schedules.

OBJECTIVE:

Display RTC information (date, time and day) on an LCD.
Allow users to modify RTC information via a 4x4 matrix keypad.
Allow users to modify the system access time via 4x4 matrix keypad.
Grant the access based on the correct password entry with in the scheduled time.

BLOCK DIAGRAM: 

![image](https://github.com/user-attachments/assets/82ee7bbe-917b-40d7-b703-67832111b128)

Hardware Requirements:

LPC2148, 
16x2 and 20x4 LCD, 
4x4 matrix keypad, 
Buzzer/LED, 
Switches, 
USB-UART converter / DB-9 cable

Software Requirements:

Keil uVision 
Flash Magic 
Proteus 

Hardare Connection:

Keypad Connection:

![image](https://github.com/user-attachments/assets/2ed23ff2-34b7-44b8-9fcf-0a91c1899b82)

Lcd Connections:

![image](https://github.com/user-attachments/assets/9c798445-ede7-4804-8a0a-9747ff862131)


Switches and Led Connection:

switch 1----> LPC2148 P0.0

switch 2----> LPC2148 P0.1

Led --------> LPC2148 P0.5

Software Flow:

Initialize system: RTC, LCD, Keypad, and Buzzer/Led.

Display current time, date and day on LCD.
Allow user to enter the password based on switch1 press.
After switch1 is pressed, user has to enter the password from the 4x4 matrix keypad. If the password is matched with the current/updated password, then check the scheduled time. If correct/updated password is entered with in the scheduled time, then give the access for the security system.
If user want to edit the RTC information and schedule time, then need to generate the interrupt by pressing switch2. Based on the interrupt request below mentioned menu will display.

Edit RTC Info
Edit Schedule Time
Exit
Editing process need to follow as per the user requirement.
After editing, again application program will start running from step2.

Software Simulation:

![image](https://github.com/user-attachments/assets/de17e332-035f-4106-81f2-6fb5fa1a04f2)
