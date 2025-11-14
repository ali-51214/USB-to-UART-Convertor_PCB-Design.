# 🔌 USB-to-UART Converter (CH340) — Custom PCB Design

This project is a custom USB-to-UART converter built around the **CH340** interface IC.  
I designed this board to practice PCB layout techniques and improve reliability over the generic USB-UART modules available online — particularly by adding:

- ✓ **Power LED indicator**
- ✓ **ESD protection**
- ✓ **Reverse polarity protection**
- ✓ **Stable USB routing**
- ✓ **Clean power filtering**

This board helps interface a laptop with embedded systems during debugging, serial monitoring, or firmware development.

---

## 📸 Project Images

> Upload your images to the GitHub repository, then add the links like this:

**USB-to-UART PCB — 3D View**

![3D View](images/3d_view.png)

**Top Layer**

![Top Layer](images/top_layer.png)

**Schematic**

![Schematic](images/schematic.png)

---

## 🧰 Features

### 🔷 CH340 USB-to-UART IC
- Handles serial communication between USB and TTL UART.
- Widely supported on Windows, Linux, and macOS.

### 🔷 Power-On LED Indicator
- Turns ON when USB is connected.
- Helps confirm power connection instantly.

### 🔷 ESD Protection on USB Lines
- Implemented using **TPD2EUSB30DRTR** (TVS diode).
- Protects USB D+ and D− lines from voltage spikes and static discharge.

### 🔷 Reverse Polarity Protection
- Diodes added on the power rail to prevent accidental damage.

### 🔷 Decoupling Capacitors
- Placed close to the CH340 IC.
- Smooths voltage and stabilizes communication.

### 🔷 USB Data Line Considerations
- Controlled-impedance routing.
- Minimal stubs.
- Short, clean differential pair routing for reliable USB signaling.

---

## 🧑‍🏭 What I Did in This Project

This project helped me strengthen several aspects of PCB design and hardware development:

### ✔ **1. Schematic Design**
- Created a clean schematic using Altium Designer.
- Added necessary protections (ESD, reverse polarity, power filtering).
- Proper pin mapping of the CH340 IC.
- Verified all USB connections against datasheets.

### ✔ **2. PCB Layout**
- Created custom footprints.
- Routed **high-speed USB differential pairs**.
- Maintained proper clearances and controlled trace lengths.
- Implemented star-point grounding for noise reduction.
- Added silkscreen labels for TX, RX, VCC, GND.

### ✔ **3. Power Integrity**
- Placed decoupling capacitors close to VCC pins.
- Added a power LED with current-limiting resistor.
- Ensured stable 5V → 3.3V regulation (if required).

### ✔ **4. Protection Circuit Design**
- TVS diode on USB lines.
- Reverse polarity diode on VBUS.
- Added ferrite bead option for EMI filtering.

### ✔ **5. Manufacturing & Outputs**
- Generated Gerber files for fabrication.
- Verified design with DRC (Design Rule Check).
- Exported 3D model for mechanical preview.

---

## 📂 Repository Structure

