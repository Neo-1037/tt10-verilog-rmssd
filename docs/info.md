<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

 How it works

The project focuses on real-time heart rate variability (HRV) calculation based on the RMSSD (Root Mean Square of Successive Differences) method. It integrates an ECG signal acquisition system using an AD8232 module. Here's the general flow of the system:

ECG Acquisition: The AD8232 module is used to collect ECG signals, which are then processed to identify the R-peaks in the ECG waveform.
RR Interval Calculation: The time between successive R-peaks (the RR intervals) is extracted from the ECG signal.
RMSSD Calculation: Once the RR intervals are obtained, the RMSSD value is calculated. RMSSD is a commonly used HRV metric, and it is determined by calculating the square root of the mean of the squared differences between successive RR intervals.
Implementation on Hardware: The RMSSD value is then computed on hardware using TinyTapeout, which allows efficient processing for real-time feedback.
 How to test

Connect the AD8232 Module: First, ensure the AD8232 module is connected to your hardware setup (e.g., TinyTapeout or other microcontroller platforms).
Collect ECG Data: Use the system to collect ECG signals in real-time. The data will be sent to the processing unit.
Verify R-Peak Detection: Ensure that the system correctly detects the R-peaks in the ECG signal.
Check RR Interval Calculation: Validate that the RR intervals are accurately computed based on the detected R-peaks.
Validate RMSSD Output: Ensure that the RMSSD is calculated correctly based on the RR intervals.
Real-Time Feedback: Once RMSSD is computed, provide real-time feedback to the user (such as displaying the value or sending it to a connected device).

 External hardware

AD8232 Module: Used to capture the ECG signal from the body.
TinyTapeout (or another FPGA): Used for processing the data in real-time, including RMSSD calculation.
Microcontroller (Optional): For managing communications and additional processing tasks, if necessary.
Display/Output Device: (e.g., LED or Screen) to show the RMSSD values or send feedback to the user.
Power Supply: For powering the AD8232 module and other hardware components.
