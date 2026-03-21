# ALU-RTL-to-GDS
8 bit ALU Full RTL to GDS Flow using OpenLane Sky130 PDK  
# 8-bit ALU — Full RTL to GDS Flow 🔧

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![PDK](https://img.shields.io/badge/PDK-Sky130A-blue)
![Tool](https://img.shields.io/badge/Tool-OpenLane_v1.0.2-orange)

## 📌 Overview
Designed and implemented a fully functional **8-bit Arithmetic Logic Unit (ALU)** using complete ASIC design flow from RTL to GDS on **Sky130 130nm PDK** using OpenLane.

---

## ⚙️ Supported Operations
| Opcode | Operation | Description |
|--------|-----------|-------------|
| 000 | ADD | A + B with carry |
| 001 | SUB | A - B |
| 010 | AND | A & B |
| 011 | OR | A OR B |
| 100 | XOR | A ^ B |
| 101 | NOT | ~A |
| 110 | LSH | A << 1 |
| 111 | RSH | A >> 1 |

---

## 🛠️ Tools Used
| Tool | Version | Purpose |
|------|---------|---------|
| Verilog HDL | - | RTL Design |
| iverilog | 12.0 | Simulation |
| GTKWave | 3.3.116 | Waveform Viewer |
| Yosys | 0.33 | Synthesis |
| OpenLane | v1.0.2 | Physical Design |
| Sky130A PDK | 130nm | Process Design Kit |
| KLayout | 0.28.16 | GDS Viewer |

---

## 📊 Design Results
| Metric | Value |
|--------|-------|
| Total Cells | 235 |
| Total Wires | 231 |
| Wire Bits | 254 |
| ANDNOT Gates | 89 |
| OR Gates | 65 |
| NOR Gates | 24 |
| XOR Gates | 12 |
| Die Area | 200 x 200 µm |
| PDK | Sky130A 130nm |

---

## 🔄 Design Flow

RTL Design → Simulation → Synthesis → Floorplan → Placement → Routing → GDS ✅


---

## 📁 Project Structure

ALU_Project/
├── rtl/
│   └── alu_8bit.v
├── testbench/
│   └── alu_tb.v
├── simulation/
│   └── alu_wave.vcd
├── synth/
│   └── synth.ys
├── reports/
│   └── synth_report.txt
└── docs/
    ├── gtkwave.png
    ├── schematic.png
    ├── layout.png
    └── synthesis.png


---

## 📸 Screenshots

### GTKWave Simulation
![GTKWave](<img width="1600" height="1008" alt="image" src="https://github.com/user-attachments/assets/96672fb2-6b10-4c32-b139-402d602ed102" />
)

### Yosys Schematic
![Schematic](docs/schematic.png)

### KLayout GDS Layout
![Layout](docs/layout.png)

### Synthesis Report
![Synthesis](docs/synthesis.png)

---

## 🚀 How to Reproduce
bash
# Clone
git clone https://github.com/Devnmakwana/ALU-RTL-to-GDS.git

# Simulate
iverilog -o simulation/alu_sim rtl/alu_8bit.v testbench/alu_tb.v
vvp simulation/alu_sim
gtkwave simulation/alu_wave.vcd

# Synthesize
yosys synth/synth.ys


---

## 👨‍💻 Author
**Dev Makwana**
- 🎓 3rd Year ECE, Government Engineering College Gandhinagar
- 🏆 2nd Runner-up NEC 2025, IIT Bombay (1700+ teams)
- 🔗 [LinkedIn](https://linkedin.com/in/dev-makwana-a8815129a)

---
⭐ Star this repo if you found it helpful!


---

## ▶️ Steps on GitHub
1. Go to your repo
2. Click *Add file* → *Create new file*
3. Type filename: README.md
4. Paste above content
5. Click *Commit new file* ✅
