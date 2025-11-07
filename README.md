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
```
import  numpy as np
import matplotlib.pyplot as plt
Am=5.9
fm=469
Ac=11.8
fc=4690
fs=476900
b=6
t=np.arange(0, 2/fm, 1/fs)

m = Am*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)

c= Ac*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)

s=Ac*np.cos(2*3.14*fc*t+b*np.sin(2*3.14*fm*t))
plt.subplot(3,1,3)
plt.plot(t,s)
```


Output Waveform
<img width="680" height="515" alt="image" src="https://github.com/user-attachments/assets/f6792179-9485-49b5-af12-33c53ab85f0b" />




Tabular Column
<img width="700" height="939" alt="image" src="https://github.com/user-attachments/assets/0b6b5bcc-e991-411c-a460-714ad366780d" />


Calculation
<img width="958" height="923" alt="image" src="https://github.com/user-attachments/assets/893d7051-a888-4f25-917f-cd12d9acd5ed" />





Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
