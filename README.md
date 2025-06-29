# lcd_display.ino
# 🖥️ Arduino LCD Display Demo

This project demonstrates a basic LCD interfacing example using the Arduino Uno and 16x2 LiquidCrystal display.

---

## 🔧 Hardware Requirements

- Arduino UNO
- 16x2 LCD (HD44780 compatible)
- Jumper Wires
- Breadboard

---

## 🔌 Pin Connections

| LCD Pin | Arduino Pin |
|---------|-------------|
| RS      | 12          |
| EN      | 11          |
| D4      | 5           |
| D5      | 4           |
| D6      | 3           |
| D7      | 2           |

---

## 🧪 Behavior

- Displays "karthik" on the first row
- Displays "shinu" on the second row after 1 second
- Loops every 2 seconds

---

## 📁 File

- `code/lcd_display.ino` — Arduino sketch file

---

## 🔄 How to Upload

1. Open Arduino IDE
2. Connect your Arduino board
3. Upload the sketch
4. Power the board and see the LCD in action
// include the library code:
#include <LiquidCrystal.h>

// initialize the library by associating any needed LCD interface pin
// with the Arduino pin number it is connected to
const int rs = 12, en = 11, d4 = 5, d5 = 4, d6 = 3, d7 = 2;
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);

void setup() {
  // set up the LCD's number of columns and rows:
  lcd.begin(16, 2);
  
  // Print a message to the LCD.
  
  lcd.print("karishma");
  
  delay(1000);
}

void loop() {

  // set the cursor to column 0, line 1
  
  lcd.setCursor(0, 1);
  
  delay(1000);
  
  // print the number of seconds since reset:
  
  lcd.print("hanny");
  
  delay(1000);
}


