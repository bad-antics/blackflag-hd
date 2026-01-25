# Heavy Duty Connector Pinouts

## SAE J1939 9-Pin Deutsch (Type A)

```
    Standard HD Diagnostic Connector

        A    B    C
       [o]  [o]  [o]
        D    E    F
       [o]  [o]  [o]
        G    H    J
       [o]  [o]  [o]
```

| Pin | Signal | Color |
|:---:|--------|-------|
| A | Battery (+) | Red |
| B | Battery (-) | Black |
| C | CAN High (J1939) | Yellow |
| D | CAN Low (J1939) | Green |
| E | CAN Shield | Bare |
| F | J1708 (+) | Orange |
| G | J1708 (-) | Blue |
| H | Manufacturer Specific | - |
| J | Manufacturer Specific | - |

---

## SAE J1939 6-Pin Deutsch (Type B)

```
    Compact HD Connector

          A    B
         [o]  [o]
        C    D    E
       [o]  [o]  [o]
            F
           [o]
```

| Pin | Signal | Color |
|:---:|--------|-------|
| A | Battery (+) | Red |
| B | CAN High | Yellow |
| C | Battery (-) | Black |
| D | CAN Low | Green |
| E | CAN Shield | Bare |
| F | J1708 (+) | Orange |

---

## OBD-II 16-Pin (Class 4-6)

```
    J1962 Connector (Medium Duty)

     1    2    3    4    5    6    7    8
    [o]  [o]  [o]  [o]  [o]  [o]  [o]  [o]
    [o]  [o]  [o]  [o]  [o]  [o]  [o]  [o]
     9   10   11   12   13   14   15   16
```

| Pin | Signal | Protocol |
|:---:|--------|----------|
| 4 | Chassis GND | - |
| 5 | Signal GND | - |
| 6 | CAN High | J1939/ISO |
| 7 | J1708 (+) | SAE J1708 |
| 14 | CAN Low | J1939/ISO |
| 15 | J1708 (-) | SAE J1708 |
| 16 | Battery (+) | Power |

---

## Caterpillar 10-Pin

```
        1    2    3    4    5
       [o]  [o]  [o]  [o]  [o]
        6    7    8    9   10
       [o]  [o]  [o]  [o]  [o]
```

| Pin | Signal |
|:---:|--------|
| 1 | Data Link (-) |
| 2 | Data Link (+) |
| 3 | Battery (-) |
| 4 | CAN Low |
| 5 | CAN High |
| 6 | N/C |
| 7 | N/C |
| 8 | Battery (+) |
| 9 | N/C |
| 10 | Factory Use |

---

## John Deere 9-Pin

```
    Green Deutsch Connector

        A    B    C
       [o]  [o]  [o]
        D    E    F
       [o]  [o]  [o]
        G    H    J
       [o]  [o]  [o]
```

| Pin | Signal |
|:---:|--------|
| A | Battery (+) |
| B | Battery (-) |
| C | CAN High (J1939) |
| D | CAN Low (J1939) |
| E | Shield |
| F | J1939 Secondary CAN High |
| G | J1939 Secondary CAN Low |
| H | Key Power |
| J | N/C |

---

## Cummins INLINE 16-Pin

```
    Cummins Proprietary Connector

     1    2    3    4    5    6    7    8
    [o]  [o]  [o]  [o]  [o]  [o]  [o]  [o]
    [o]  [o]  [o]  [o]  [o]  [o]  [o]  [o]
     9   10   11   12   13   14   15   16
```

| Pin | Signal |
|:---:|--------|
| 1 | Battery (+) |
| 2 | Battery (+) |
| 3 | Battery (-) |
| 4 | Battery (-) |
| 5 | J1939 CAN High |
| 6 | J1939 CAN Low |
| 7 | J1708 (+) |
| 8 | J1708 (-) |
| 9 | J1939 CAN2 High |
| 10 | J1939 CAN2 Low |
| 11-16 | Reserved |

---

## Volvo 14-Pin

```
    Volvo Heavy Duty Connector

      1    2    3    4    5    6    7
     [o]  [o]  [o]  [o]  [o]  [o]  [o]
      8    9   10   11   12   13   14
     [o]  [o]  [o]  [o]  [o]  [o]  [o]
```

| Pin | Signal |
|:---:|--------|
| 1 | Battery (+) |
| 2 | Key Power |
| 3 | CAN1 High |
| 4 | CAN1 Low |
| 5 | CAN2 High |
| 6 | CAN2 Low |
| 7 | CAN3 High |
| 8 | CAN3 Low |
| 9 | J1708 (+) |
| 10 | J1708 (-) |
| 11-13 | Reserved |
| 14 | Battery (-) |

---

## Termination Resistors

| Network | Termination |
|---------|-------------|
| J1939 CAN | 120Ω each end |
| J1708 | No termination |
| ISO 15765 | 120Ω each end |

---

*BlackFlag HD - Connector Reference v1.0*
