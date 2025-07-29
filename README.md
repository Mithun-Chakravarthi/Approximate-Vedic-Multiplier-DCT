##  Project Origin

This project originates from the need to make image compression more power-efficient for embedded and real-time applications. Traditional image compression algorithms like JPEG rely heavily on the Discrete Cosine Transform (DCT), which involves numerous multiplication operations. These multiplication steps, especially in hardware implementations, are computationally expensive and contribute significantly to power consumption and delay. Conventional multipliers used in the DCT block are accurate but not optimized for power-sensitive environments, making them less suitable for battery-powered or real-time systems.


##  Problem Statement

In typical JPEG compression, the DCT step is the most multiplication-intensive block. While accurate multipliers ensure precision, they are not ideal for systems where energy efficiency is a constraint. As the demand for real-time image processing grows in edge devices, there is a pressing need to reduce the computational overhead of exact arithmetic units without severely impacting output quality.


##  Proposed Solution

To address this, an approximate eight by eight Vedic multiplier was designed using the Urdhva Tiryakbhyam sutra and integrated into the DCT block of a JPEG compressor. The core idea is to replace exact multiplications in the DCT computation with approximate ones that are less complex and more power-efficient, especially targeting the least significant bits to minimize error impact. The proposed multiplier uses a novel approximate full adder in its partial product accumulation stage and was evaluated for power, area, delay, and error metrics. The modified DCT block, implemented in Verilog and tested using a Python testbench, was further integrated into a JPEG compression flow.


##  Results Achieved

Certainly, Mithun. Here's the **"Results Achieved"** section with proper formatting and exact **numerical values** instead of written words:

---

## 📊 Results Achieved

The approximate DCT block, integrated with the proposed 8×8 Approximate Vedic Multiplier (AVM-8bit), achieved the following improvements over a conventional JPEG DCT compressor:

**Power Consumption:** Reduced from 0.221 W to **0.1 W** (a **54% reduction**).
**PSNR (Peak Signal-to-Noise Ratio):** Achieved **31.89 dB**, compared to **32.17 dB** of the accurate version.
**SSIM (Structural Similarity Index):** Reached **0.886**, compared to **0.8915** of the accurate version.
**Compression Ratio:** Obtained **1.69×**, nearly equal to the **1.71×** from the exact DCT block.
**Operating Frequency:** Improved to **166.7 MHz** due to positive timing slack.
**Error Rate of AVM-8bit:** Recorded **49.56%**, which is lower than many existing approximate multipliers.* **Normalized Mean Error Distance (NMED):** **0.6769**
**Mean Relative Error Distance (MRED):** **1.39%**
**Resource Utilization:** Used **105 LUTs** and **32 IOBs**, slightly less than the exact multiplier (108 LUTs).

These results demonstrate that the proposed approximate design achieves significant power savings and improved speed while maintaining image quality nearly identical to the accurate DCT-based JPEG compressor.



##  Research Paper

The research has been peer-reviewed and published at the 2025 IEEE International Conference on Integrated Circuits and Communication Systems.
**Read the full paper here:**
[https://ieeexplore.ieee.org/document/10967620](https://ieeexplore.ieee.org/document/10967620)


