# Bill of Materials
| Item # | Quantity | Ref | Manufacturer | Manufacturer Part Number |Description | Type
| --: | :--: | :----: | :-----: | :-----: | :-----: | :---: |
| 1 | 1 | R1 | YAGEO | RC0603JR-07330RL | 330 Ω | SMT
| 2 | 2 | R2, R3 | YAGEO | RC0603JR-0710KL | 10 kΩ | SMT
| 3 | 2 | C1, C2 | YAGEO | CC0603JRNPO9BN100 | 10 pF | SMT
| 4 | 3 | C3, C4, C7 | YAGEO | CC0603KRX7R9BB104 | 100 nF | SMT
| 5 | 1 | C6 | YAGEO | CC0603KRX7R9BB104 | 1 uF | SMT
| 6 | 1 | D1 | Hubei KENTO Elec | KT-0603G | Green LED | SMT
| 7 | 1 | D2 | Hubei KENTO Elec | KT-0603R | Red LED | SMT
| 8 | 1 | SW1 | Omron Electronics | B3U-1000P | Push Switch | SMT
| 9 | 1 | Y1 | YXC Crystal Oscillators | X322516MOB4SI | 16 MHz Crystal | SMT
| 10 | 1 | U1 | Microchip Technology | ATmega328P-AN | 32 pin, TQFP Microcontroller  | SMT
| 11 | 2 | J1, J2 | hanxia | HX PH254-01-04-Z-L11.5 straight pin header | 12 pin header, = 2.54mm | THT
| 12 | 1 | J3 | hanxia | HX PH254-01-04-Z-L11.5 straight pin header | 6 pin header, P = 2.54mm | THT

# Pinout
Pins are used and connected, unless specified otherwise
###  U1
| Pin # | Name | Description / Connected to
| --: | :--: | :----: |
| 1 | PD3 | J1-Pin7
| 2 | PD4 | J1-Pin6
| 3 | GND | Ground
| 4 | VCC | Supply voltage
| 5 | GND | Ground, Unused
| 6 | VCC | Supply voltage, Unused
| 7 | XTAL1/PB6 | Oscilation input, Y1-Pin1
| 8 | XTAL2/PB7 | Oscilation input, Y1-Pin3
| 9 | PD5 | J1-Pin5
| 10 | PD6 | J1-Pin4
| 11 | PD7 | J1-Pin3
| 12 | PB0 | J1-Pin2
| 13 | PB1 | J1-Pin1
| 14 | PB2 | Unconnected
| 15 | PB3 | MOSI, J2-Pin11
| 16 | PB4 | MISO, J2-Pin10
| 17 | PB5 | SCK, J2-Pin9
| 18 | AVCC | Supply voltage for ADC
| 19 | ADC6 | Analog input 6, Unconnected
| 20 | AREF | Analog reference
| 21 | GND | Ground, Unused
| 22 | ADC7 | Analog input 7, Unconnected
| 23 | PC0 | Analog input 0, J2-Pin8
| 24 | PC1 | Analog input 1, J2-Pin7
| 25 | PC2 | Analog input 2, J2-Pin6
| 26 | PC3 | Analog input 3, J2-Pin5
| 27 | PC4 | Analog input 4, Unconnected
| 28 | PC5 | Analog input 5, Unconnected
| 29 | RESET/PC6 | Reset signal, J1-Pin10, J2-Pin3, J3-Pin1
| 30 | PD0 | RXI, J1-Pin11, J3-Pin3
| 31 | PD1 | TXO, J1-Pin12, J3-Pin2
| 32 | PD2 | J1-Pin8

###  Y1
| Pin # | Description / Connected to
| --: | :----: |
| 1 | Oscilation output, U1-XTAL1
| 2 | Ground
| 3 | Oscilation output, U1-XTAL2
| 4 | Ground

### J1
| Pin # | Connected to
| --: | :----: |
| 1 | Digital input 9, U1-PB0
| 2 | Digital input 8, U1-PB1
| 3 | Digital input 7, U1-PD7
| 4 | Digital input 6, U1-PD6
| 5 | Digital input 5, U1-PD5
| 6 | Digital input 4, U1-PD4
| 7 | Digital input 3, U1-PD3
| 8 | Digital input 2, U1-PD2
| 9 | Ground
| 10 | U1-Reset, J2-Pin3, J3-Pin1
| 11 | U1-RXI, J3-Pin3
| 12 | U1-TXO, J3-Pin2

### J2
| Pin # | Connected to
| --: | :----: |
| 1 | Power Supply
| 2 | Ground
| 3 | U1-Reset, J1-Pin10, J3-Pin1
| 4 | Supply voltage
| 5 | Analog input 0, U1-PC0
| 6 | Analog input 1, U1-PC1
| 7 | Analog input 2, U1-PC2
| 8 | Analog input 3, U1-PC3
| 9 | U1-PB5, R1
| 10 | MISO, U1-MISO
| 11 | MOSI, U1-MOSI
| 12 | AU1-PB2

### J3
| Pin # | Connected to
| --: | :----: |
| 1 | U1-Reset, J1-Pin10, J2-Pin3
| 2 | U1-TXO, J1-Pin12
| 3 | U1-RXI, J1-Pin11
| 4 | Supply voltage
| 5 | Ground
| 6 | Ground

###  D1, D2
The leds are polarized, the pin order maters
| Pin # | Description
| --: | :----: |
| 1 | Power output
| 2 | Power input
- D1 is connected to Ground (1) and Supply volatage (2)
- D2 is connected to Ground (1) and R1 (2)

### R1, R2, R3
The resistors are not polarized, the pin order does not mater
- R1 is connected to (U1-PB5, J2-Pin9) and D1-P2
- R2 is connected to Ground and D2-P1
- R3 is connected to Supply voltage and (SW1, U1-Reset, J1-Pin10, J2-Pin3)

### C1, C2, C3, C4, C6, C7
The capacitors are not polarized, the pin order does not mater
- C1 is connected to (U1-XTAL1,Y1-Pin1) and Ground
- C2 is connected to (U1-XTAL2,Y1-Pin3) and Ground
- C3 is connected to Supply voltage and U1-AREF
- C4 is connected to SW1 and Ground
- C6 is connected to Supply voltage and Ground
- C7 is connected to Supply voltage and Ground

### SW1
The switch is not polarized, the pin order does not mater
Connected to C4 and (R3, U1-Reset, J1-Pin10, J2-Pin3)

# Notes
- C5 is missing from provided shematic
