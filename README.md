# IDD-Fa19-Lab1: Blink!

**A lab report by Ben Kadosh**




## Part A. Set Up a Breadboard
<img src="https://github.com/BenKadosh1/IDD-Fa19-Lab1/blob/master/IDD_Fa19_Lab1_Img1.jpg" width=450 height=450>

The left and right sides of the breadboard were not connected for simplicity during this lab.

## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?**

On a 100 ohm resistor, the color stripes would be: 
 - Brown (1st band)
 - Black (2nd band)
 - Brown (3rd band)

This leads to values of 1, 0 (10) for the first two bands times a multiplier of 10 for the third band resulting in 100 ohm resistance. Depending on the quality of the resistor, the tolerance will vary and therefore the fourth band could be a series of different colors. 

For the 220 ohm resistors we used in lab 1, the color stripes were: 
 - Red (1st band)
 - Red (2nd band)
 - Black (3rd band)
 - Black (4th band)
 - Brown (5th band)

This leads to values of 2, 2, 0, 0  (220) for the first three bands times a multiplier band of 1 for the fourth band, resulting in 220 ohm resistance. The resistor had a tolerance of +/- 1%.  
 
**b. What do you have to do to light your LED?**

In part b of the lab, in order to get the LED to light up we physically had to press the button to close the circuit. In my case, I had to press the buttion to connect the electrical flow from row 22 to row 24 by pushing the button and closing the circuit. 

<img src="https://github.com/BenKadosh1/IDD-Fa19-Lab1/blob/master/IDD_Fa19_Lab1_Img2.jpg" width=450 height=450>
<img src="https://github.com/BenKadosh1/IDD-Fa19-Lab1/blob/master/IDD_Fa19_Lab1_Img3.jpg" width=450 height=450>


## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**

No lines of code need to be changed to make the LED blink. This assumes that there is a wire inserted in the proper digital pin and that it is also connected to the LED in the breadboard. 

**b. What line(s) of code do you need to change to change the rate of blinking?**

In order to change the rate of blinking, we need to update the "delay(1000)" lines of code found in rows 34 and 36 of the built-in sample in the Arduino IDE. By changing the delay variable we can increase or decrease how much time there is between the LED light being turned on and off and thus the rate of blinking. 

**c. What circuit element would you want to add to protect the board and external LED?**
 I would consider adding a fuse to the circuit in case the current exceeds design and leads to the LED burning out. In addition, we could add a resistor to the circuit to limit the current to ensure it doesn't exceed limits that would cause the LED to stop working. 
 
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**

At around 10 milliseconds --> delay(10) I was no longer able to perceive the LED blinking. 
\
In order to prove that the LED would still, in fact, be blinking, one could connect the circuit board to an oscilloscope which would graphically depict the changes in voltage over time, proving that at points there was no electrical flow and that the LED was blinking on and then off for short periods of time. 

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**

[Modified Blink Code](https://github.com/BenKadosh1/IDD-Fa19-Lab1/blob/master/Blink_Ben_Kadosh.ino)

### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**
\
[Blinking LED Youtube Link](https://www.youtube.com/watch?v=6ssTY8aDUTY)

## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**

I was able to get the LED to glow through almost the entire range of the potentiometer, however there was still a faint signal of light that could be seen at the tail end. This is most likely because the resistance in the potentiometer was not strong enough to reduce the current flowing to the LED enough that the human eye would not be able to see it. 

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**
In order to make the code control the circuit we built, we had to update the led variable from the default 9 in the Arduino example to 11 to correspond to the jumper wire connected to pin 11. 
\
In addition, the brightness and fadeAmount variables could be updated to change the fade format.

int led = 11  
int brightness = 3 \
int fadeAmount = 8  
  
  


**b. What is analogWrite()? How is that different than digitalWrite()?**
analogWrite mimics an analog voltage signal in the Arduino. As the lab mentions, "The Arduino cannot output an analog voltage, only 0 or 5Vs." In order to allow users to be able to simulate different voltages being passed to the LED and thus control its percevied brightness, analogWrite uses pulse width modulation to control how frequently the electrical flow is turned on and off in the circuit. 

Conversely, digitalWrite can take only one of two states, HIGH/LOW, on/off where it either passes electricity or it doesn't.


## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

**d. Is information stored in your device? Where? How?**

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

### 3. Build your light!

**Make a video showing off your Frankenlight.**

**Include any schematics or photos in your lab write-up.**
