# stm32-hardware-design-v0.2
Complete STM32F4 PCB design with full manufacturing package - My first MCU board design

## 📋 Project Overview
My first complete STM32 microcontroller board design from scratch. This project represents my journey from following tutorials to independent hardware design.

**Key Features:**
- STM32F407VGT6 microcontroller (ARM Cortex-M4, 168MHz)
- USB 2.0 Full Speed interface
- UART, I2C, SPI breakout headers
- Proper power supply filtering (digital/analog separation)
- SWD debug interface
- User-configurable boot modes

## 🎯 Design Goals
1. Learn professional PCB design workflow
2. Understand STM32 power architecture
3. Practice manufacturable design (DRC/DFM)
4. Create complete manufacturing package

## 📁 Repository Structure

## 🛠️ Design Decisions & Lessons Learned

### Power Supply Design
- Used AP2112K LDO for clean 3.3V rail
- Separate VDDA supply with ferrite bead isolation
- Proper decoupling: 10µF bulk + 100nF per pin + 10nF high-frequency

### Component Selection
- **0603 package** chosen over 0402 for better manufacturability
- Crystal oscillator with 20ppm stability for USB compliance
- Reset circuit with debouncing capacitor

### PCB Layout
- 2-layer design (cost-effective for learning)
- Controlled impedance where possible
- Proper ground plane stitching
- Manufacturing-friendly clearances (0.15mm minimum)

## 🔧 Manufacturing Instructions

### Ordering PCBs
1. Upload all files in `manufacturing/gerber/` to JLCPCB/PCBWay
2. Use standard 1.6mm FR-4, HASL finish
3. Minimum clearance: 0.15mm (6mil)

### Assembly
1. Use `manufacturing/bom/stm32_v0.2_bom.csv` for components
2. Use `manufacturing/pick-and-place/stm32_v0.2_pos.csv` for assembly
3. Recommended: Start with just MCU, crystals, and power section

## 📈 Version History
- **v0.1** - Initial design, DRC clearance issues with 0402 components
- **v0.2** - Fixed DRC issues with 0603 components, improved layout, complete manufacturing package


## 📚 Resources & References
- [STM32F407 Datasheet](datasheets/STM32F407VGT6.pdf)
- [KiCad Documentation](https://docs.kicad.org)
- [Phil's Lab Tutorials](https://www.youtube.com/c/PhilsLab)

## 👨‍💻 About the Designer
Final year electronics student learning hardware design through hands-on projects. This board represents my transition from tutorial-following to independent design.



---
*If you build this board or have suggestions, please open an issue or pull request!*
