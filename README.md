# DESIGN AND SIMULATION OF A DIGITAL DATA TRANSMISSION ERROR DETECTION SYSTEM USING XOR LOGIC

##📌 Project Overview

This project demonstrates the **design and simulation of a digital data transmission error detection system using XOR logic**. The system detects whether transmitted binary data has been altered during transmission by comparing the original transmitted data with the received data.

The circuit is designed and simulated using **Logisim**, a digital logic circuit simulation tool.

## 🎯 Objectives

* To understand the fundamentals of digital data transmission.
* To design an error detection circuit using XOR gates.
* To compare transmitted and received binary data.
* To detect errors in transmitted data.
* To simulate and verify the circuit using Logisim.

## ⚙️ Working Principle

An **XOR (Exclusive-OR) gate** produces:

| Input A | Input B | XOR Output |
| ------- | ------- | ---------- |
| 0       | 0       | 0          |
| 0       | 1       | 1          |
| 1       | 0       | 1          |
| 1       | 1       | 0          |

For each corresponding transmitted and received bit:

* **Same bits → XOR output = 0**
* **Different bits → XOR output = 1**

The XOR outputs are combined to generate the final **Error Detected** signal.

If all XOR outputs are `0`, the transmitted and received data are identical.

If any XOR output is `1`, an error is detected.

## 🔌 Circuit Design

For a 4-bit data transmission system:

```text
Transmitted Data        Received Data
     D3 ---------------- R3
        \              /
         \            /
          └── XOR ───┘
               |
              E3

     D2 ---------------- R2
        \              /
         \            /
          └── XOR ───┘
               |
              E2

     D1 ---------------- R1
        \              /
         \            /
          └── XOR ───┘
               |
              E1

     D0 ---------------- R0
        \              /
         \            /
          └── XOR ───┘
               |
              E0

          E3, E2, E1, E0
                 |
                 ▼
          Error Detection
```

Each XOR gate compares one transmitted bit with its corresponding received bit.

## 🧪 Simulation

The circuit is implemented and tested in **Logisim** using different combinations of transmitted and received data.

### Example Test Cases

| Transmitted Data | Received Data | Result           |
| ---------------- | ------------- | ---------------- |
| `1010`           | `1010`        | ✅ No Error       |
| `1010`           | `1000`        | ❌ Error Detected |
| `1101`           | `1101`        | ✅ No Error       |
| `1101`           | `1111`        | ❌ Error Detected |

## 🛠️ Components Used

* XOR Gates
* Input switches/pins
* Output LEDs/indicators
* Logic gates for combining error signals
* Connecting wires
* Logisim

## 💻 Software Used

**Logisim** – Digital logic circuit design and simulation software.

## 🌐 Applications

This type of error detection logic can be used in:

* Digital communication systems
* Computer networks
* Data transmission systems
* Serial communication
* Embedded systems
* Digital storage systems

## ⚠️ Limitations

* The circuit can **detect** errors but does not correct them.
* More complex communication systems may require advanced techniques such as:

  * Parity checking
  * Checksum
  * Cyclic Redundancy Check (CRC)
  * Error-correcting codes

## ✅ Conclusion

The project demonstrates how **XOR logic can be used to detect errors in digital data transmission**. By comparing each transmitted bit with its corresponding received bit, the circuit identifies whether the data has been altered during transmission.

The Logisim simulation provides a simple and visual method for understanding the operation of digital error detection circuits.

## 👥 Project Team

| Details           | Information                               |
| ----------------- | ----------------------------------------- |
| **Team Members**  | ______________________________            |
| **Course**        | Electronics and Communication Engineering |
| **Subject**       | ______________________________            |
| **Faculty**       | ______________________________            |
| **Academic Year** | 2026–2027                                 |

## 📂 Repository Structure

```text
Digital-Data-Transmission-Error-Detection/
│
├── README.md
├── circuit/
│   └── error_detection.circ
│
├── screenshots/
│   └── circuit_simulation.png
│
└── presentation/
    └── project_presentation.pptx
```

## 📜 License

This project is created for **academic and educational purposes**.
