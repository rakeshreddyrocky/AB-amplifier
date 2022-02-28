# Parallel-coupled-AB-amplifier
The purpose of this Hackathon is to implement the proposed design in 28 nm PDK (Process Design Kit) suing CMOS technology.

As a result of literature survey and Implemantation, this is a final Report Submission for successful completion of Parallel_AB amplifier design and simulation, for Cloud Based Analog IC Design Hackathon
# Table of Contents
1.Introduction
2.Working
3.Reference Circuit
4.Implimentation
5.Schematic results
6.Challanges
7.Limitations
8.REfarences
9.Acknowledgements
10.Author
# Introduction
Power amplifiers (PAs) are among the most crucial functional blocks in the radio frequency (RF) frontend for reliable wireless communication. PAs amplify and boost the input signal to the required output power. The signal is amplified to make it sufficiently high for the transmitter to propagate the required distance to the receiver. Attempted advancements of PA have focused on attaining high-performance RF signals for transmitters. Such PAs are expected to require low power consumption while producing a relatively high output power with a high efficiency. However, current PA designs in nanometer and micrometer complementary metal–oxide semiconductor (CMOS) technology present inevitable drawbacks, such as oxide breakdown and hot electron effect. A well-defined architecture, including a linear and simple functional block synthesis, is critical in designing CMOS PA for various applications.
# Working
In the PA design in CMOS technology, two main issues must be addressed Oxide breakdown and the hot carrier effect. In this design, two amplifiers operate in parallel to improve the dynamic range and power efficiency. The input transistor M1 was biased with a fixed voltage of 1.2 V. The cascode configuration was formed by the CS transistors M1, M2, M3, and M4, and the CG transistors M5 and M6. The CS transistors form the transconductance of the class-A and the class-B PAs in order to provide more linear transconductance, which led to high power gain of 12dB. At low input levels, the class-A amplifier contributed the majority of the gain, and the class B amplifier had a very low gain. As the input level increased, the gain of the class- B amplifier increased, and its contribution to the overall gain increased proportionately. The outputs from both amplifiers were combined in the current domain with a slight overhead, thereby producing an improved isolation property and highpower efficiency of 44%. AC coupling capacitors and the matching network were used for the output impedance matching.
# Refarence circuit
