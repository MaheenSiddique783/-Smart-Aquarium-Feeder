# Smart-Aquarium-Feeder


This is a university microcontroller project that builds a **fully automatic fish feeder** using an STM32 microcontroller. It feeds fish at scheduled times and can also detect tank lighting conditions to control the dispensing of fish food. 

---

## 🌟 Features
- 📅 Timer-based scheduling
- 🌞 Light-based feeding control using LDR
- 🔁 LEDs for visual feedback when the motor is active
- 🕒 Time display through serial monitor (Tera Term)

---

## 📦 Components Used

| Component          | Purpose                                   |
|--------------------|--------------------------------------------|
| STM32F103RB Board  | The main brain of the system              |
| LDR (Light Sensor) | Detects tank brightness for feeding logic |
| Motor + MOSFET     | Dispenses food on trigger                 |
| Pushbutton(s)      | For manual feeding & setting time         |
| LEDs               | Indicate system states visually           |

*No prior knowledge of electronics required — each part is explained in `docs/`.*

---

## ⚙️ How It Works

1. **Timekeeping**: The DS1302 module keeps the current time even when the power is off.
2. **Scheduled Feeding**: Feeding times are stored and checked every second using TIM2.
3. **Manual Feeding**: You can wave your hand (IR sensor) or press a button to feed manually.
4. **Motor Activation**: Motor runs via a MOSFET when feeding occurs.
5. **Visual Feedback**: LEDs alternate while the motor is active.

---

## 🛠️ Setup and Build

1. Flash `main.c` to your STM32 board using Keil or STM32CubeIDE.
2. Open Tera Term and connect via USART1 to see time updates and debug logs.
3. Connect components as shown in [images/schematic.png](images/schematic.png).

---

## 🙋‍♀️ About the Author

Made by **Maheen Siddique** for the ENEL 351 Microcontroller Lab Design Project at the University of Regina.

