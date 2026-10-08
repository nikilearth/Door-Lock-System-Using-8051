# 8051 Password-Based Door Lock System

An 8051 microcontroller system designed to provide secure, automated door access using a matrix keypad, LCD display, and motor driver.

## 📌 Features
* **Keypad Entry:** $4\times4$ matrix keypad for passcode input.
* **Status Display:** $16\times2$ LCD display showing step-by-step user prompts.
* **Motor Actuation:** L293D driver controlling a DC door lock motor.
* **Security Lockout:** Permanent lockout state triggered after repeated failed attempts.

## 🛠️ Hardware Requirements
* **Microcontroller:** AT89C51 (8051 Family)
* **Input Device:** $4\times4$ Matrix Keypad
* **Display:** LM016L $16\times2$ LCD
* **Actuator:** DC Motor + L293D H-Bridge Driver
* **Power Supply:** $5\text{V}$ DC (Logic/MCU) & $12\text{V}$ DC (Motor)

## 🔌 Pin Interfacing

| Component | Port / Pins | Function |
| :--- | :--- | :--- |
| **$4\times4$ Keypad** | `P1.0 - P1.3` | Matrix Rows (A–D) |
| | `P1.4 - P1.7` | Matrix Columns (1–4) |
| **LCD Display** | `P2.0 - P2.7` | Data Bus (`D0–D7`) |
| | `P3.0` | Register Select (`RS`) |
| | `P3.1` | Enable (`E`) |
| **L293D Driver** | `P3.2` | Channel Enable (`EN1`) |
| | `P3.3` / `P3.4` | Motor Control (`IN1` / `IN2`) |

## 🚀 How to Run

1. **Compile Code:** Compile the C source code in **Keil uVision** to build the `.hex` binary file.
2. **Load Firmware:** Open the simulation project in **Proteus ISIS**.
3. **Attach HEX File:** Double-click the **AT89C51** microcontroller chip, select the generated `.hex` file under **Program File**, and set the clock to `11.0592 MHz`.
4. **Run Simulation:** Click **Play** to test keypad entries, status displays, and motor actuation.
