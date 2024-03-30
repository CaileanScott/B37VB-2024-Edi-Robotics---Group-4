# Open-Loop-Motor-Control-Report
### Contact Details
Lewis Gill, H00436489, lg2050@hw.ac.uk 

Cailean Scott, , cs2091@hw.ac.uk

### Revision History
*Table 1*
| 27th of Marth 2024 | Version 1     | Final Draft   |              
| -------------      | ------------- | ------------- | 
| Lewis Gill         | Cailean Scott |               | 
### Contents
*Table 2*
| contents            | paragragh no. |          
| -------------       | ------------- |
| Introduction        | 1st paragragh | 
| Experimental method | 2nd paragraph |
| Results             | 3rd paragragh |
| Analysis            | 4th paragragh |
| Conclusion          | 5th paragragh |


### Introduction
Open loop control is a method of system control where there is no feedback in the control system. This is a type of continuous control of which the output has absolutely no impact or effect on the input hence has no feedback. Some simple examples of open loop control systems are a lightbulb or TV remote where their respective outputs have no effect on their inputs. 
### Experimental Method
Our task was to use an open-loop control system to control two drive motors to move a buggy to fit certain requirements. The control system consists of the firmware running on the ATMega328P MCU and the H-Bridge IC is used to provide power to the two motors.  We were required to operate the buggy at 3 different speeds in response to changes made to our input code in Arduino IDE. Firstly we wired our microcontroller unit to the breadboard attached on the buggy however at first we could not get the motors to operate. Upon analysis of our wiring we could see that the reason for the motors not working was that we put 2 wires into the ground therefor shorting the circuit.  Once this issue was solved we set the speed parameters of the pulse width modulation (PWM) on the buggy between -255 and 255 where any positive number is forwards and any negative number put the motor in reverse. Initially we set the PWM to 200 on each side however we noticed that despite this the buggy was not travelling in a straight line meaning one motor was going faster then the other.  Therefor we adjusted the values of the of each motor’ PWM in the code to make the buggy go in a straight line. We found that if we kept the left PWM value at 200 and reduced the right PWM value to 160 the buggy travelled in a straight line. We then repeated this process two more times reducing the values to 140 and 100, then 100 and 60 of the left and right motors respectively, in order to operate the motor at 3 different speeds. 
### Results 
#### The PWM Values at different speeds 
*Table 3*
| Speed no.#      | Speed no.1    | Speed no.2    | Speed no.3    |  Speed no.4    |           
| -------------   | ------------- | ------------- | ------------- |  ------------- | 
| Right PWM Value |     200       |      160      |     100       |       60       |
| Left  PWM Value |     200       |      200      |     140       |       100      |

### Analysis
In the open loop motor experiment, we used 3 unique PWM Values to show change in the speed of the buggy (shown in table 3). Firstly, we did Speed no.1, this was with both PWM Values being equal at 200, as we ran the Buggy we discovered that one of the motors was slower than the other making the Buggy drift toward the left. For the second attempt we adjusted the speeds to have the Right PWM value lowered to 160 and keeping the Left PWM value at 200 to counteract the natural drifting, this was a successful change, and our Buggy was then going in a straight-line with the 40 PWM value difference. When doing Speed no.3 we used the same difference in PWM values but lowered both overall PWM values by 60, which still drove straight but at a slower speed. Finally, Speed no.4 we again kept the same difference in PWM Value and again lowered the overall PWM Value down by 40 and again was again successful at an even slower speed.
### Conclusion
In conclusion, we used open loop control to operate the two motors with the H bridge IC to power them. During this part of the experiment, we discovered that the two motors ran at different speeds when at the same PWM as show in our results and analysis. So then we adjusted the code changing the PWM value to change the speed of the buggy whist making sure we kept a difference of 40 PWM to ensure that it remained driving in a straight-line no matter the speed of the buggy. We had to run the buggy at below 200 PWM and below as that’s near the top side of the -255 to 255 parameters of the buggy. We accidently wired the buggy incorrectly by putting a wire into the ground as a result it shorted the circuit, once we discovered the issue it was an easy fix and a good learning experience during this assignment.
