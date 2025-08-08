# 🏏 T20 Cricket Game on FPGA (DE10-Lite)

Ever imagined simulating a full-fledged cricket match on an FPGA board?  
This project brings a mini **T20 cricket match to life** using Verilog and the DE10-Lite FPGA board — complete with score tracking, wickets, innings, and even live display on 7-segment LEDs!

---

## 💡 What This Project Does

- Lets you play a cricket game by pressing a button for each delivery
- Uses a **random generator (LFSR)** to simulate real cricket events (singles, sixes, wickets, extras, etc.)
- Keeps track of **runs, wickets, balls**, and **switches innings**
- Displays **scores in real-time** using 7-segment displays
- Uses **LEDs to show ball count**
- Declares the **winner** at the end of the match

---

## 🔧 What’s Under the Hood

This project is written in **Verilog HDL** and divided into well-structured modules:

| Module | What it Does |
|--------|---------------|
| `project` | Main wrapper that connects everything |
| `debounce` | Cleans up button presses |
| `lfsr` | Generates random scores or events |
| `score_and_wickets` | Updates score/wickets based on the delivery |
| `score_comparator` | Compares final scores to declare a winner |
| `led_controller` | Tracks number of balls using LEDs |
| `bcdDisplay` | Converts binary score to human-readable format on 7-segs |
| `lab6`, `bcd7seg` | Handle 7-segment display outputs |
| `scroll_Leds`, `slowClock_10Hz`, `D_FF` | Support functions like clock division and LED scrolling |

---

## 🧰 Hardware Setup

- **Board:** DE10-Lite (Intel FPGA)
- **Inputs:** Push buttons (for deliveries)
- **Outputs:** 
  - LEDs → show number of balls
  - 7-segment displays → show runs, wickets, and match result

---

## 🎮 How to Play

1. Upload the project to your DE10-Lite board.
2. Press the **delivery button** to simulate a bowl.
3. Watch the **runs/wickets update** live.
4. After 10 wickets or 120 balls, the **inning switches**.
5. Once both innings are done, the **winner is declared**!


