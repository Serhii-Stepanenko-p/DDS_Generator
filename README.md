# DDS Generator

**DDS Generator** is an electronic device that generates highly accurate and stable electrical signals of various shapes and frequencies.

## Author
Stepanenko Serhii

## Description
This project contains the schematic file and other supporting files for correct operation.  

The **DDS Generator** is built on the **MCU STM8S103F3P6**. The generation process works as follows:  

1. The MCU generates "raw" pulse signals through the DAC.  
2. A buffer stage (voltage follower) is used to isolate the DAC from the load.  
3. The signal path is then split into two branches: **HF** and **DDS**.  
4. For the DDS branch, the signal passes through a **Sallen-Key Low-Pass Filter (LPF)** to smooth the waveform.  
5. Before the output connectors, a **Non-Inverting Summing Amplifier** is used to adjust both the **offset** and **amplitude** of the output signal.  

These stages ensure that the final output signals are **high-quality, smooth, low-noise**, and have **low output resistance**.  