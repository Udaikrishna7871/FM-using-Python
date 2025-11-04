# FM-using-Python

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
~~~
import numpy as np
import matplotlib.pyplot as plt

Am=5.4
Ac=10.8
fm=444
fc=4440
fs=44400
t=np.arange(0,3/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
c=Ac*np.cos(2*np.pi*fc*t)
b=4.7
eFM =Ac*np.cos(2 * np.pi * fc * t + b * np.sin(2 * np.pi * fm * t))
plt.subplot(3,1,1)
plt.plot(t,m)
plt.grid()
plt.subplot(3,1,2)
plt.plot(t,c)
plt.grid()
plt.subplot(3,1,3)
plt.plot(t,eFM)
plt.grid()

plt.tight_layout()
plt.show()
~~~
Output Waveform

![WhatsApp Image 2025-11-04 at 22 06 44_ba547749](https://github.com/user-attachments/assets/dba96957-6b94-4042-805f-da3cf514d797)

Tabular Column

![WhatsApp Image 2025-11-04 at 19 25 58_d9f2f5e5](https://github.com/user-attachments/assets/993acaca-5f8e-4b57-849a-d2b1ea27ad9d)



Calculation

![WhatsApp Image 2025-11-04 at 22 10 29_b9d0a0f2](https://github.com/user-attachments/assets/698feb3e-c994-4ea9-8bbb-71f0bef1c033)



Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
