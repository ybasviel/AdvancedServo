# AdvancedServo
Advanced Servo Library for Arduino and ESP32

An angle offset can be set to correct for differences in angle commands due to differences in individual servos, installation, and coordinate systems.

## example
```cpp
#include "AdvancedServo.h"

AdvancedServo s;

void setup() {
  s.attach(3);

  s.setOffset(20);
  // or
  s.offset = 20;

  s.write(90);
  // it works as s.write(90 + 20)

  s.read();
  // it returns s.read() - 20
}

void loop() {
}
```
