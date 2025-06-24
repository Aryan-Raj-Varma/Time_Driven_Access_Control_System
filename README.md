**Project Title:**
Time-Driven Access Control System

**Overview:**
The Time-Driven Access Control System is an embedded security solution that regulates access based on predefined time schedules. It integrates real-time clock functionality with user authentication to enhance security in time-sensitive applications.

---

**Objective:**

* Display Real-Time Clock (RTC) information (Date, Time, and Day) on an LCD.
* Allow users to modify RTC information via a 4x4 matrix keypad.
* Permit editing of access schedules using the keypad.
* Provide access based on correct password entry within the scheduled time slot.

---

**Block Diagram:**

![image](https://github.com/user-attachments/assets/5efd13be-c15b-43f7-93ff-cf361382e3c2)

---

**Hardware Requirements:**

* LPC2148 ARM7 Microcontroller
* 16x2 or 20x4 Alphanumeric LCD
* 4x4 Matrix Keypad
* Buzzer and/or LED Indicator
* Push Button Switches (Switch1 and Switch2)
* USB-UART Converter or DB-9 Serial Cable

---

**Software Requirements:**

* Keil uVision (IDE for ARM Development)
* Flash Magic (Programming Tool)
* Proteus Design Suite (For Simulation)

---

**Hardware Connections:**

**Keypad Connections:**

![image](https://github.com/user-attachments/assets/7f69f84c-fa0d-4eb7-8e2a-87f763ff9096)


**LCD Connections:**

![image](https://github.com/user-attachments/assets/7c525aae-8d4d-43df-b01b-031867b20698)


**Switches and LED Connections:**

* Switch1 → LPC2148 Pin P0.0 (for Access Request)
* Switch2 → LPC2148 Pin P0.1 (for Edit Menu)
* LED       → LPC2148 Pin P0.5 (indicates access granted)

---

**Software Flow:**

1. **Initialization**

   * Initialize RTC, LCD, Keypad, Switches, and Buzzer/LED.

2. **Display RTC Info**

   * Continuously display current Date, Time, and Day on the LCD.

3. **Access Request Handling (Switch1)**

   * On pressing Switch1:

     * Prompt user to enter password via keypad.
     * Validate password.
     * If correct, compare current time with access schedule.
     * If within scheduled time, grant access (activate LED/Buzzer).
     * Else, deny access and optionally sound alert.

4. **Editing RTC or Schedule (Switch2)**

   * On pressing Switch2:

     * Display menu:

       * Edit RTC Info
       * Edit Schedule Time
       * Exit
     * Based on user selection, allow modification using the keypad.

5. **Resume Monitoring**

   * After editing, return to RTC display and monitoring loop.

Software Simulation:

![image](https://github.com/user-attachments/assets/3767c433-9ef4-4430-a75a-c638297275fe)


---

**Conclusion:**
This project demonstrates an effective approach to combining real-time clock management and access control using LPC2148 and basic input/output peripherals. It is suitable for labs, lockers, or restricted area control systems that require timed access with security authentication.

