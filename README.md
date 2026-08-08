# 7-Segment Traffic Light Countdown System (Arduino)

A traffic light controller simulation using an Arduino UNO, a 1-digit 7-segment display, and three indicator LEDs (Red, Green, Yellow). The system counts down on the display while cycling through traffic light states.

---

## 🛠 Hardware Components

* **1x** Arduino UNO R3
* **1x** 1-Digit 7-Segment Display (Segments connected to Pins 4–11)
* **3x** LEDs (Red, Green, Yellow)
* **3x** Current-limiting Resistors
* **1x** Breadboard
* Jumper Wires & USB Power Cable

---

## 🔌 Pin Connections

Based on `7SegmentDisplay.ino`:

| Component | Pin / Color | Arduino Pin | Notes |
| :--- | :--- | :--- | :--- |
| **Green LED** | `green` | `Digital Pin 2` | Active HIGH |
| **Red LED** | `red` | `Digital Pin 3` | Active HIGH |
| **Yellow LED** | `yellow` | `Digital Pin 12` | Active HIGH |
| **7-Segment Display** | `segment[]` array | `Digital Pins 4, 5, 6, 7, 8, 9, 10, 11` | Segment control outputs |

---

## ⚙️ How the Code Works

1. **Traffic Light Sequence:**
   * **Red Light Phase:** Turns Red LED ON (`Pin 3 HIGH`) and counts down on the 7-segment display from **9 down to 0** (1 second per digit).
   * **Green Light Phase:** Turns Red OFF, Green LED ON (`Pin 2 HIGH`), and counts down from **9 down to 0**.
   * **Yellow Light Phase:** Turns Green OFF, Yellow LED ON (`Pin 12 HIGH`), and performs a quick countdown from **2 down to 0**.
2. **Looping:** Once the Yellow light phase finishes, the sequence restarts from the Red light phase automatically.

---

## 🚀 How to Run

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/cktang59/7SegmentDisplay.git](https://github.com/cktang59/7SegmentDisplay.git)
