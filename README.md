# Autonomous Hovercraft
Pure Embedded C Autonomous Hovercraft powered by an ATMega328 microcontroller, capable of navigating a maze and making turns.

## Features
- Zero use of Arduino library. All GPIO, PWM, ADC, and I2C (TWI) communication is handled via direct MCU register writes.
- Hovercraft stabilizes itself using the IMU gyroscope.
- Obstacle avoidance using HC-SR04 US Sensors (front, left side)
- Real-time telemetry in CMD for debugging using UART -> Format: L:[dist]cm R:[dist]cm IR:[dist]cm | Yaw:[angle] | Acc X:[val]

<img width="600" height="700" alt="image" src="https://github.com/user-attachments/assets/65776f14-1098-4d70-9588-73d2b3b8321d" />

## Hardware Configuration
#### Pin Mapping:

###### Fans
Lift Fan (MEC0251V1-000U-A99): Port Pin PD4 | Function: Cushion Lift | Mode: Digital Output
Thrust Fan (AFB1212SH ): Port Pin PD5 | Function: Propulsion | Mode: PWM (Timer0 - OC0B)

###### Servo Motor (HS-311)
Steering Servo: Port Pin PB1 | Function: Direction | Mode: 16-bit PWM (Timer1 - OC1A)

###### IMU (MPU-6050)
IMU (MPU6050) SDA: Port Pin PC4 | Function: I2C Data | Protocol: TWI
IMU (MPU6050) SCL: Port Pin PC5 | Function: I2C Clock | Protocol: TWI

###### US Sensors (HC-SR04):
US Left Trig: Port Pin PB3 | Function: Trigger | Mode: Output

US Left Echo: Port Pin PD2 | Function: Pulse In | Mode: External Interrupt (INT0)

US Right Trig: Port Pin PB5 | Function: Trigger | Mode: Output]

US Right Echo: Port Pin PD3 | Function: Pulse In | Mode: External Interrupt (INT1)

###### IR Sensor ()
IR Sensor: Port Pin PC0 | Function: Obstacle Detection | Mode: ADC Channel 0]

###### Power:
2x LiPo batteries (GENS 450 ACE25-0450-0201)


