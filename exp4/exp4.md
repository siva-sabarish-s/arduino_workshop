---
sidebar_position: 4
title: MQ135 Gas Sensor
---

# MQ135 Air Quality Monitoring

This project monitors air quality using MQ135 gas sensor.

---

[GAS_Sensor](../image/smoke_senor.jpeg)

---

## How It Works

- MQ135 detects gases like CO₂ and smoke.
- Analog output provides gas concentration value.
- Digital output triggers when threshold exceeds.

---

## Complete Arduino Code

```cpp
int analogPin = A0;
int digitalPin = 2;

void setup() {
  Serial.begin(9600);
  pinMode(digitalPin, INPUT);
}

void loop() {
  int analogValue = analogRead(analogPin);
  int digitalValue = digitalRead(digitalPin);

  Serial.print("Air Quality: ");
  Serial.println(analogValue);

  delay(1000);
}
