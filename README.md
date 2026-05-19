<h1 align="center"> Digital Design and Fabrication Portfolio
</h1>
<p align="center">
  <b>Tugce Saroglu</b>
</p>
<h2>Week 01 - Electrical Circuits 🔌</h2>
 <details>
  <summary><b>Task 1 </b></summary>
 
  <b>Task 1.1</b>
  <img width="260" height="462" alt="task1 1 circuit" src="https://github.com/user-attachments/assets/285de816-cecf-4fb6-9458-a9c49c4a8d11" />
  Task 1.1 Circuit<br>
  <br/>
  This task was the most fundamental task in the series. When measuring voltages across various resistors, it was clearly visible to observe changes in LED’s brightness even with the naked eye. Observed measurements for each given resistors are presented in the table below:<br><br/>

  | R1 (Ω)  | Measured V1 (V)  | Measured VLED (V) |
| :--- | :--- | :--- |
| 220 | 2.20 | 2.73 |
| 1000 | 2.18 | 2.73 |
| 4700 | 2.70 | 2.28 |

To varify the approximate values, a total voltage around 5V in total (the sum of V1 and VLED) was expected and all the measurements fulfilled this condition. <img width="120" height="160" alt="task1 1  measurement" src="https://github.com/user-attachments/assets/e58a246a-4227-455e-9986-b0548eb1d490" />
Measurement of the LED<br>
  <br/>
The most obvious observation was that the dimming of the LED as the resistance of R1 was increased.  Although V1 remained relatively constant for the first two resistors, a sudden increase in V1 suddenly was observed when R1 was switched from 1000 ohm to 4700 ohm. Simultaneously, a sharp decrease in VLED was recorded. This significant change was probably caused by the surpassing the threshold of the LED. 

<b>Task 1.2</b>
<img width="462" height="260" alt="task1 2 circuit" src="https://github.com/user-attachments/assets/db0328a0-5a4d-478d-8ec6-58b510438fc3" />
Task 1.2 Circuit<br>
  <br/>

This circuit was the identical to the first one, only difference was addition of a switch. The LED was illuminated only when the switch was in the 'on' position. No changes were observed in the circuit's behavior when the orientation of the switch was reversed. The reason for this, switch elements don’t have polar properties, so it doesn’t affect the circuit differently based on orientation, unlike the LED which is a polar component. 

<b>Task 1.3</b>

<img width="462" height="260" alt="task 1 3  circuit" src="https://github.com/user-attachments/assets/a6b57605-3810-4f97-8035-0328ad89bb95" />
Task 1.3 Circuit<br>
  <br/>
With the addition of potentiometer, complexity of the circuit is a bit increased and became more difficult to understand as a beginner in circuits. Measurements were recorded at various potentiometer positions, as detailed in the table below:

| R1 (Ω)  | VLED (V)  | V2 (V) |
| :--- | :--- | :--- |
| a) full brightness | 2.90 | 1.99 |
| b) dimmed | 2.20 | 0.480 |
| c) OFF | 0.05 | 0.476 |

As the potentiometer’s resistance was increased, a progressive dimming of the LED was observed. Due to this increase, the LED could not receive enough voltage to remain lit and eventually turned off. Similarly, both VLED and V2 decreased acording to the potentiometer’s behavior. For example, when the potentiometer’s resistance is maximum (when the LED is off) the voltages of both measurements dramatically decreased. Some tiny voltage values were still observed because the circuit is not perfect, which prevents it from reaching zero completely. The operation of potentiometer is also added below to describe the dimmer behavior more clearly.


https://github.com/user-attachments/assets/3646ca49-c53c-432c-9c50-f6096ce94be6


https://github.com/user-attachments/assets/aaeed968-a6bc-4dd1-8e00-e58007c28597
</details>


<details>
 <summary><b>Task 2 </b></summary>
  In this task, HW193 USB adapter was used by plug it in directly to the breadboard.<br>
    <br/>
<b>Task 2.1</b>
<img width="462" height="260" alt="task 2 1 circuit" src="https://github.com/user-attachments/assets/cd627e76-bc87-4ef3-b994-68869757016d" />
Task 2.1 Circuit<br>
  <br/>
In this circuit, the main voltage flow is controlled by the switch although the 12V is on. This means that if the switch is turned off, the LED strip also turns off. On the other hand, the transistor has some different roles for the circuit. Firstly, it seperates 12V and 5V. Due to its semiconductor properties, the transistor’s gate acts as a bridge, preventing these two voltages from mixing. When the main switch is off, any remaining voltage is directed to the ground through the S leg. This ensures the 12V supply feeds the LED strip (consists of many LED connected in parallel) without interference from the 100 ohm and 10k ohm resistors. Especially the switch’s duty can be observed the video below.<br>
    <br/>



https://github.com/user-attachments/assets/8a69ec50-e5f9-4f1d-adc1-27949a68f5b1

<b>Task 2.2</b>

<img width="260" height="353" alt="task 2 2  circuit" src="https://github.com/user-attachments/assets/bfd20563-a027-4943-a0ef-22b9abf518fa" />
Task 2.2 Circuit<br>
  <br/>

  In the first part of the observation, the LED strip became brighter as the duty cycle percentage was increased, behaving similarly to the dimmable LED circuit. While the behavior seemed similar to the previous dimmable LED circuit, the underlying mechanism is quite different. Instead of changing the resistance like a potentiometer, the duty cycle controls the transistor's operation time within a specific period. For this specific case, the period was around 11 miliseconds due to the 90 Hz frequency. Within this cycle, the duty cycle defines how long the transistor remains active; for example, a 2% duty cycle means the transistor operates for only 2% of that 11 ms window. Since the human eye cannot perceive such high speeds, lower duty cycle values are perceived as dimmer. Although the visual effect is similar to the potentiometer circuit, the technical operation is fundamentally different. <br>
  <br/>

https://github.com/user-attachments/assets/73beaa96-9cfe-45e1-8816-088c86175c3f

  In the second part of the observation, the transistor was set to a 0.5 duty cycle. Consequently, the LED remained active for exactly half of each cycle. At lower frequencies, this resulted in a visible blinking pattern. As the frequency increased, the blinking rate accelerated accordingly. Because the LED deactivates precisely at the midpoint of each cycle and resumes at the start of the next, the human eye perceives this rapid switching as a continuous blinking effect. <br>
  <br/>

  

https://github.com/user-attachments/assets/69f1f1c0-2ba4-4a51-9fb0-8a82c692cd37

</details>



<h2>Week 02 - Arduino Alarm Clock ⏰</h2>

  This task was significantly more challenging compared to the first week’s objective because the exact circuit schematics for the alarm clock were not provided this week.
  <details>
  <summary><b>Sub-Circuits</b></summary>
  <br/>
    
  - **Sub-Circuit 1**
  
    Initially, the development process began by integrating only a buzzer into the circuit. The most notable observation from the buzzer test was that increasing the delay times directly extended the duration of the pauses by altering the duty cycle and periodic frequency of the beep sound.

    <img width="260" height="462" alt="IMG20260507114104" src="https://github.com/user-attachments/assets/209f26a2-e2c3-4452-b1cf-04e2c99dfcb1" />

    Sub-circuit 1 on operation:

https://github.com/user-attachments/assets/7710a893-73f2-4ed0-ae2a-1c16f3103c23
  
- **Sub-circuits 2&3**
  
    Following the integration of the RTC and LCD modules, three distinct I2C addresses were detected during the scanner test. The specific address for the LCD was added into the source code to establish the communication  between the computer and the LCD screen. This phase had the most challenging aspect of the project due to its highly complex wiring. As an entry-level practitioner in Arduino, this setup required an extended development period and further trial and errors outside the laboratory environment. Multiple faulty wiring attempts occurred, which were identified by the initial failure of the I2C scanner to detect the device addresses. 

Sub-circuit 3: 

<img width="462" height="260" alt="IMG20260508003118" src="https://github.com/user-attachments/assets/634a3d3c-ee9e-445d-a6bf-a7fd9017923a" />
    
Detailed wiring of the sub-circuit 3:

<img width="462" height="260" alt="IMG20260508003024" src="https://github.com/user-attachments/assets/618a8d76-73de-49a1-82ab-bcbbbf7dd14f" />

Addresses of the LCD and RTC:

<img width="462" height="260" alt="IMG20260508002957" src="https://github.com/user-attachments/assets/5c13ff51-06e4-4b38-a74c-644e09b6494a" />




- **Sub-Circuit 4**

Subsequently, the four control buttons specified in the manual were integrated into the circuit. This step completed the hardware section of the alarm clock circuit.

Detailed wiring of the sub-circuit 4:

<img width="462" height="260" alt="IMG20260515153153" src="https://github.com/user-attachments/assets/f220e7ba-1b7a-4dbc-bab8-1ebe51a9e579" />

<img width="462" height="260" alt="IMG20260515153104" src="https://github.com/user-attachments/assets/cae5850f-4b9a-496b-a2f0-ea34572570ff" />

<img width="462" height="260" alt="IMG20260515153141" src="https://github.com/user-attachments/assets/d7bc625b-804e-401f-aa91-b79420a3d58a" />

</details>

<details>
  <summary><b>Alarm Clock</b></summary>
  <br/>
  
A decent result was achieved using the given code. The circuit and wiring remained the same with the sub-circut 4.

alarm clock's final wiring:

<img width="462" height="260" alt="IMG20260515191515" src="https://github.com/user-attachments/assets/24f496d1-ecfd-4c7c-82e8-6a9d0a0ab90d" />



Added features:
  
•	Crescendo Alarm Tone: The standard alarm sound was replaced with a more effective waking signal. By increasing the frequency by 30 Hz at each step of the execution loop, the acoustic output scales linearly from 600 Hz to approximately 1500 Hz. This creates an escalating tone that might increase auditory urgency.

•	Dual-Function White Button (Snooze & Toggle): A 5-minute snooze function was integrated into the system. The white button was reconfigured to handle two tasks based on press duration: a long press (over 2000 ms) toggles the global alarm ON/OFF, while a short press (under 2000 ms) activates the 5-minute snooze.

crescendo alarm tone and snooze function:
https://github.com/user-attachments/assets/74bd25c4-19ff-4205-bb60-3f3a4443709d

long press white button (alarm on/off): 
https://github.com/user-attachments/assets/c9ee8b63-cb34-4ec0-b153-db63416394e1

•	Dual-Function Red Button (Screen Switch & Dismiss): An alarm dismissal feature was added to improve user interaction. A long press (over 2000 ms) switches the LCD display between the real-time clock and the alarm setting screen. A short press (under 2000 ms) dismisses the alarm cycle.

long press red button (screen switch):
https://github.com/user-attachments/assets/3cb5f3aa-c82e-48fc-a987-97e0f5688fad

•	Background Dismiss: The dismiss function is designed to work even during active snooze intervals. If the user wakes up early, they can terminate the alarm cycle immediately without waiting for the snooze timer to expire.

snooze and background dismiss functions: 
https://github.com/user-attachments/assets/cf133f0b-5094-44a7-90c8-c1ef1a90fc69


Before these successful implementations, lots of failures occured. For example, in the one of the trials the LCD module once displayed corrupted characters and irrelevant symbols (shown below).

<img width="260" height="462" alt="IMG20260515154338" src="https://github.com/user-attachments/assets/dfd0a075-c0ff-45ed-8c9e-6dfd0b65dc35" />


</details>
























  



</details>

