# 🚗 8×8 LED Matrix Speed & RPM Display

A compact, real-time vehicle dashboard display using an 8×8 LED matrix. It shows speed in large digits and RPM as a horizontal bar chart, designed for embedded platforms like Arduino or ESP32.

---

## 📌 Project Goals

- ✅ Display two-digit vehicle speed using a custom 5×3 font.
- ✅ Visualize RPM as a color-coded horizontal bar chart.
- ✅ Maintain real-time responsiveness with minimal hardware.
- ✅ Provide a clean, readable layout on an 8×8 LED matrix.

---

## 🧠 Features

| Feature             | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| Speed Display       | Two-digit speed shown using a custom 5×3 font across the top 5 rows.        |
| RPM Bar Chart       | Bottom two rows show RPM as horizontal bar chart.                           |
| Color Thresholds    | Green (<4000 RPM), Yellow (4000–6000 RPM), Red (>6000 RPM).                 |
| Real-Time Updates   | Speed and RPM polled every 100ms from OBD-II.                               |
| Compact Layout      | Efficient use of matrix space for dual-purpose display.                     |

---

## 🧱 Matrix Layout

| Row (Y) | Purpose                  |
|--------|--------------------------|
| 0–4    | Speed digits (5×3 font)  |
| 5      | Optional spacing         |
| 6–7    | RPM bar chart            |

---

## 🔧 Data Sources

- **Speed**: OBD-II PID `$0D` (Vehicle Speed)
- **RPM**: OBD-II PID `$0C` (Engine RPM)

---

## ⚙️ Rendering Logic

### Speed Digits
- Rendered using a custom 5×3 font.
- Positioned side-by-side across top 5 rows.
- Updated every 100ms.

### RPM Bar Chart
- 0–8000 RPM mapped to 8 columns (1000 RPM per column).
- Color-coded:
  - 🟩 Green: <4000 RPM
  - 🟨 Yellow: 4000–6000 RPM
  - 🟥 Red: >6000 RPM
- Rendered on rows 6–7.

---

## 🚧 Constraints

- Must fit within 8×8 LED matrix resolution.
- RPM bar must not interfere with digit legibility.
- Graceful fallback on OBD-II polling failure.
- Optional: brightness control for ambient readability.

---

## 🧪 Success Criteria

- Speed digits are legible at a glance.
- RPM bar updates smoothly and reflects engine load.
- Color transitions are intuitive and responsive.
- System operates reliably under typical driving conditions.

---

## 📦 Future Enhancements

- 🔆 Brightness auto-adjustment via ambient light sensor.
- ⚙️ Gear shift indicator based on RPM and speed.
- 📱 Bluetooth configuration for thresholds and colors.
- 📊 Logging mode for telemetry capture.

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to change.

---

## 📄 License

[MIT](LICENSE)

---

## 🧭 Maintainer

**Tim** – Senior Product Manager at Brigade Electronics Group Plc  
Focused on workplace safety innovation through AI and digital imaging.
