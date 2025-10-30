# FMUSINGPYTHON

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as np
import matplotlib.pyplot as plt

Am=2.3
Ac=4.6
fc=2170
fm=217
fs=21700
beta=3.6
t=np.arange(0, 2/fm, 1/fs)
m=Am* np.cos(2*np.pi*fm*t)

c=Ac* np.cos(2*3.14*fc*t)

efm=Ac*np.cos((2*np.pi*fc*t)+beta*np.sin(2*np.pi*fm*t))

plt.subplot(3, 1, 1)
plt.plot(t, m)
plt.show()

plt.subplot(3, 1, 2)
plt.plot(t, c)
plt.show()

plt.subplot(3, 1, 3)
plt.plot(t, efm)
plt.show()
```

Output Waveform

![WhatsApp Image 2025-10-30 at 08 25 49_d1ae7f70](https://github.com/user-attachments/assets/84d2da1b-f54e-475d-ac9c-d79fc13c4396)


Tabular Column

![WhatsApp Image 2025-10-28 at 22 35 21_83479a14](https://github.com/user-attachments/assets/3d5b872c-4c1e-46b5-b52a-cae0696d25f4)

Calculation



Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
