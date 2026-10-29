Aim 
Design and assess whether the robot cars is capable of navigating through the black line track and achieving success in the obstacle avoidance test. 
Setup 
The setup for a car is placed onto and driven on. It is made of an Arduino board that is used to operate the car, two motors which are used to drive the wheels, line sensors situated on the front that can see and follow the black line, and finally an ultrasonic sensor placed on the front that can detect and recognize any obstacles in its pathway. 
 
Component 	Arduino pin 
Left line sensor 	D2 
Right line sensor 	D3 
Servo signal 	D4 
Left motor speed ENA D5 
Right motor speed ENB D6 
IN1 	D8 
IN2 	D9 
IN3 	D10 
IN4 	D11 
Ultrasonic TRIG 	D12 
Ultrasonic ECHO 	D13 
 
Main components are: Line sensors, ultrasonic sensor, servo motor, dc motors , bridge and Arduino uno. 
 
Aim is to make a line following car which will stop, if any objects are in front of the car, plus it follows the line at all times, and stops at the finish. 
 
 
Logic of our project :  
 
Initially, the Arduino senses the ultrasonic sensor that is located at the front part of the car. This is where the safety test comes in. When there is an obstruction detected through the sensor, the car comes to a stop. The vehicle remains still until the object is moved out of the way. Afterward, the car resumes tracking the line. 
 
Next, the two line sensors on the underside of the car sense whether they are above the black line or on the white ground. 
 
 
 
 
 
 
 
The car follows this logic: 
Left sensor Right sensor What the car does 
White 	White 	Move forward 
Black 	White 	Turn left 
White 	Black 	Turn right 
Black 	Black 	Move slowly or stop, depending on junction/line 
 
This happens because the black line should be in the middle of two sensors instead of directly below them. Thus, when two sensors detect white, then the car would consider itself being centered to the line. 
 
When the left sensor detects black, the car goes too far towards its right side, and thus it makes the car turn left to make corrections. 
 
If the right sensor detects black, the car drifts too much towards its left side, and thus it turns right to make the correction.
