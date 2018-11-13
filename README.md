// Programme
    const int r1 = 2;
    const int r2 = 3;
    const int r3 = 4;
    const int trigPin = 12;
    const int echoPin = 11;
    long duration;
    int distance;
    float vout;
    void setup() 
    {
    pinMode(trigPin, OUTPUT); // Sets the trigPin as an Output
    pinMode(echoPin, INPUT); // Sets the echoPin as an Input
    pinMode(r1, OUTPUT);
    pinMode(r2, OUTPUT);
    pinMode(r3, OUTPUT);
    digitalWrite(r1, HIGH);
    digitalWrite(r2, HIGH);
    digitalWrite(r3, HIGH);
    Serial.begin(9600); // Starts the serial communication
    delay(1000);
    }
    void loop() 
    {
    if((vout<=300)&&(vout>=21)
    {
    digitalWrite(r1, LOW);
    digitalWrite(r2, HIGH);
    digitalWrite(r3, HIGH);
    digitalWrite(trigPin, LOW);
    delayMicroseconds(2);
    digitalWrite(trigPin, HIGH);
    delayMicroseconds(10);
    digitalWrite(trigPin, LOW);
    duration = pulseIn(echoPin, HIGH);
    distance= duration*0.034/2;
    vout=distance;
    delay(500);
    Serial.print("Distance in cm: ");
    Serial.println(distance);
    }
    if((vout<=20)&&(vout>=11)
    {
    digitalWrite(r2, LOW);
    digitalWrite(r1, HIGH);
    digitalWrite(r3, HIGH);
    digitalWrite(trigPin, LOW);
    delayMicroseconds(2);
    digitalWrite(trigPin, HIGH);
    delayMicroseconds(10);
    digitalWrite(trigPin, LOW);
    duration = pulseIn(echoPin, HIGH);
    distance= duration*0.034/2;
    vout=distance;
    delay(500);
    Serial.print("Distance in cm: ");
    Serial.println(distance);
    }
    if((vout<=10)&&(vout>=1)
    {
    digitalWrite(r1, HIGH);
    digitalWrite(r2, HIGH);
    digitalWrite(r3, LOW);
    digitalWrite(trigPin, LOW);
    delayMicroseconds(2);
    digitalWrite(trigPin, HIGH);
    delayMicroseconds(10);
    digitalWrite(trigPin, LOW);
    duration = pulseIn(echoPin, HIGH);
    distance= duration*0.034/2;
    vout=distance;
    delay(500);
    Serial.print("Distance in cm: ");
    Serial.println(distance);
    }
    else
    {
    digitalWrite(r1, HIGH);
    digitalWrite(r2, HIGH);
    digitalWrite(r3, HIGH);
    digitalWrite(trigPin, LOW);
    delayMicroseconds(2);
    digitalWrite(trigPin, HIGH);
    delayMicroseconds(10);
    digitalWrite(trigPin, LOW);
    duration = pulseIn(echoPin, HIGH);
    distance= duration*0.034/2;
    vout=distance;
    delay(500);
    Serial.print("Distance in cm: ");
    Serial.println(distance);
    }
