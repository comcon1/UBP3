# Universal Biopotential Amplifier - UBP3

Wideband multichannel differential amplifier with modular design and adjustable analogous commutation.

## Project video

[![Video presentation of the project](https://img.youtube.com/vi/Itqa7mGAqyA/0.jpg)](https://www.youtube.com/watch?v=Itqa7mGAqyA)

## Technical characteristics

- Input power: -15, 0, +15 V
- Type: differential
- Input resistance: 1 GOhm
- Noise level at connected inputs:
  - < 0.15 mkV (at 0.3-150 Hz)
  - < 0.8 mkV (at 0.3-1000 Hz)
- Gain coefficient:
  - Input cascade: 1, 10
  - Output cascade: 3, 10, 30, 100, 300, 1000
- Filtering:
  - Intensity: 12 dB/octave
  - LowPass: 35, 70, 150, 300, 1000, 2000, 5000, 10000, 20000 Hz 
  - HighPass: 0.1, 0.3, 1, 5, 20, 100, 300 Hz
- Output range: -5V - +5V

# Project structure

The amplifier is composed of two boards: **InputAmp** and **FilterAmp**. 

## InputAmp

Input gain board performs initial commutation of the bipolar signal with reference monopolar input and calibration signal. Next the board amplifies the signal current with 1x/10x gain.

Corresponding directory contains the complete KiCAD project including scheme and PCB.

## FilterAmp

Preamplified signal is then further amplified inside this board and undergo LowPass and HighPass filtration.

Corresponding directory contains the complete KiCAD project including scheme and PCB.

## Calibrator

Calibrator gets 0/+5V input unipolar source and gives 30/300 Hz of 1/0.1 mV square pulse unipolar signal for feeding the amplifier.

Corresponding directory contains the complete KiCAD project including scheme and PCB.

# Arrangement

Boards are designed for further geometrical stacking as shown at the how-to-assembly scheme:

![How boards are assemblied](https://github.com/comcon1/UBP3/raw/main/doc/arrangement.png)

# History

The prototype of this amplifier was firstly used by Ilya Kuzmin and colleagues for recording ECG of rats on a tredban:

- Tarasova OS, Borzykh AA, Kuz'min IV, et al. [Dynamics of heart rate changes in rats following stepwise change of treadmill running speed]. Ross Fiziol Zh Im I M Sechenova. 2012; 98(11):1372-9.

Now it is used by Georgy Nikolaev and his students for recording EEG in the research of audiogenic epilepsy on rat model:

- Fedotova IB, Surina NM, Nikolaev GM, Revishchin AV, Poletaeva II. Rodent Brain Pathology, Audiogenic Epilepsy. Biomedicines. 2021; 9(11):1641. https://doi.org/10.3390/biomedicines9111641

# Licensing 

The project "Universal Biopotential Amplifier" 
(I. Kuzmin @kuzmin-ilya, A. Nesterenko @comcon1, G. Nikolaev)  
is released under  license CC BY-SA 3.0.

Submodules listed as independent projects are not part of this project and 
are released under their own licenses.
