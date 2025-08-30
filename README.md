# 🎵 Audio Filtering using FIR Filter (FPGA Implementation)

## 📌 Overview
This project implements an **Audio Filter using FIR filters** on a **Xilinx Zedboard**.  
The system supports **Low-pass, High-pass, and Band-pass filtering** of real audio signals.  

Designed using:
- MATLAB & Simulink (Filter design & HDL Workflow Advisor)
- Vivado (Reference design & integration)
- Verilog (HDL code generated & tested)
- Zedboard with ADAU1761 Audio Codec

---
## 📂 Repository Structure
```bash
FIR-Audio-Filter/
│── src/              # Verilog source files (generated from MATLAB HDL Coder)
│   ├── Audio_Filter_IP_src_Biquad_Filter_LPF.v
│   ├── Audio_Filter_IP_src_Biquad_Filter_HPF.v
│   ├── Audio_Filter_IP_src_Biquad_Filter_BPF.v
│   ├── Audio_Filter_IP_src_Filter_block.v
│   └── ...
│
│── docs/             # Documentation & diagrams
│   ├── block_diagram.png
│   ├── system_architecture.png
│   ├── output_waveform.png
│   └── zedboard_setup.png
│
│── results/          # Simulation and FPGA output
│   ├── simulation_waveforms.png
│   ├── test_results.txt
│   └── demo_ui.png
│
└── README.md         # Project documentation
```

## 🛠️ Features
- FIR-based **Biquad Filter Implementation**
- Supports **Low-pass, High-pass, Band-pass**
- **User Interface (MATLAB GUI)** for filter selection
- Real-time audio playback through headphone jack
- FPGA-controlled **LED indicators** for filter selection:
  - LD0 → Pass-through  
  - LD1 → Low-pass filter  
  - LD2 → Band-pass filter  
  - LD3 → High-pass filter  

---

## 🖼️ Block Diagrams & Architecture
| System Block Diagram | FPGA Integration | Audio Output |
|----------------------|------------------|--------------|
| ![Block](docs/block_diagram.png) | ![Architecture](docs/system_architecture.png) | ![Waveform](docs/output_waveform.png) |

---

## 🔧 Implementation Steps
1. **Filter Design** in MATLAB/Simulink (LPF, HPF, BPF)  
2. **Generate HDL IP** using HDL Workflow Advisor  
3. **Integrate with Vivado** (AXI4-Stream Audio Reference Design)  
4. **ARM Executable Generation** for FPGA tuning  
5. **FPGA Deployment** on Zedboard  
6. **Audio Output Verification** using earphones/speakers  

---

## 📂 Verilog Source Files
- `Audio_Filter_IP_src_Biquad_Filter_LPF.v`
- `Audio_Filter_IP_src_Biquad_Filter_HPF.v`
- `Audio_Filter_IP_src_Biquad_Filter_BPF.v`
- `Audio_Filter_IP_src_Filter_block.v`
- `Audio_Filter_IP_src_Data_Type_Conversion.v`

---

## 📊 Results
- FIR filter successfully implemented on Zedboard  
- Audio processed with selectable LPF, HPF, BPF  
- Filter coefficients generated via MATLAB  
- Verified using real audio playback and simulation  

---
  

