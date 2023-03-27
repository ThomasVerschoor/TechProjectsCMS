# HC - SR04
HCSR04 is a popular ultrasonic sensor that can measure distances of up to 400 cm. It is widely used in robotics, IoT, and automation projects for measuring the distance between the sensor and an object.

Working principle
------------------
The working principle of HCSR04 is based on the time-of-flight measurement of ultrasound waves. It consists of an ultrasonic transmitter and a receiver. The transmitter emits a high-frequency ultrasound pulse, which bounces back from an object and is received by the receiver. The sensor measures the time taken by the ultrasound pulse to travel back and forth between the sensor and the object, and calculates the distance using the speed of sound in air.

Pin Configuration
------------------
The HCSR04 sensor has four pins:

| Pin        | Description           |
| ------------- |:-------------:|
| Vcc    | Power supply pin which requires a 5V DC supply |
| Trig    | Trigger pin used to initiate the measurement of distance      |
| Echo | Echo pin which receives the reflected ultrasound signal    |   
| GND    | Ground pin |


Example code
------------------

```
#define trigPin 2
#define echoPin 3

void setup() {
  Serial.begin (9600);
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
}

void loop() {
  long duration, distance;
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  duration = pulseIn(echoPin, HIGH);
  distance = duration * 0.034 / 2;
  Serial.print("Distance: ");
  Serial.println(distance);
  delay(500);
}
```


Datasheet
------------------
Link coming soon



Applications
------------------
The HCSR04 sensor finds its applications in a wide range of fields like:

Obstacle detection and avoidance in robotics
Measuring the level of liquid in a tank
Monitoring the proximity of objects in automated manufacturing
Measuring the distance between vehicles in automated parking systems


Where to buy?
------------------
Link to Amazon.
