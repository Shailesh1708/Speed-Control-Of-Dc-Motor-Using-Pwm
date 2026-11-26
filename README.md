# Exp-5: Speed-Control-Of-Dc-Motor-Using-Pwm

### Name: Shailesh S S
### Reg No.: 212225040397

## Aim:
To control the speed of DC Motor using Pulse Width Modulation (PWM).

## Compnent Required:
1. Arduino Uno.
2. DC Motor.
3. N-channel MOSFET.
4. 10 KΩ Potentiometer.
5. 9V Battery.
6. Breadboard.
7. Connecting wires.
8. USB interfacing cable.
9. Tinkercad Circuits software.


## Procedure:
1. Open Tinkercad Circuits and create a new circuit.
2. Place the Arduino Uno, breadboard, DC motor, N-channel MOSFET, potentiometer and 9V battery in the workspace.
3. Connect the 5V pin of the Arduino to the positive rail of the breadboard.
4. Connect the GND pin of the Arduino to the negative rail of the breadboard.
5. Connect the middle terminal of the potentiometer to analog input pin A0 of the Arduino.
6. Connect the two outer terminals of the potentiometer to 5V and GND, respectively.
7. Connect the gate terminal of the MOSFET to digital PWM pin 9 of the Arduino.
8. Connect the DC motor to the MOSFET and 9V battery as shown in the circuit diagram.
9. Connect the negative terminal of the battery to the common ground of the circuit.
10. Write the Arduino program to read the potentiometer value using analogRead() and control the motor speed using analogWrite().
11. Start the simulation and rotate the potentiometer to vary the motor speed.
12. Observe how the DC motor speed changes according to the potentiometer position.


## Program:

```
int MPin = 9;   //motor pin
int Analog = A0;  // Analog Input
int Ainp = 0; // Read analog input, initialized to zero  
  
void setup()
{
  
  Serial.begin(9600);
  pinMode(MPin, OUTPUT);
  pinMode(Analog, INPUT);
}

void loop()
{

Ainp = analogRead(A0);

int Speed = map(Ainp, 0, 1024, 0, 255);
delay(100);
Serial.println(Speed);
analogWrite(MPin, Speed);  

```

## Circuit Diagram:

<img width="1481" height="732" alt="circuit diagram" src="https://github.com/user-attachments/assets/9c226540-8b34-47da-8224-4432811c40a3" />

## Schematics:

<img width="1125" height="872" alt="schem" src="https://github.com/user-attachments/assets/c8b68b3e-6f6d-4e5b-8482-86d344bcd7c1" />


## Output:
<img width="1765" height="922" alt="output" src="https://github.com/user-attachments/assets/29ac3a51-79a6-4d0f-87fa-81253a0d5bc4" />

## Result:
Thus, a simulation to control the speed of DC Motor using Pulse Width Modulation (PWM) was performed and executed successfully.
