# phase-modulation

**AIM:**

To implement and analyze phase modulation (PM) using SICLAB.

**APPARATUS REQUIRED:**

• Computer with i3 Processor

• SCI LAB

**THEORY:**

Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message signal.

The general form of a PM signal can be represented as:
<img width="606" height="341" alt="image" src="https://github.com/user-attachments/assets/8566ff1a-badb-4f30-bf2d-41055d982763" />



**ALGORITHM:**

Initialize Parameters:
o Set values for carrier amplitude (AcA_cAc), carrier frequency (fcf_cfc), message frequency (fmf_mfm), sampling frequency, and phase deviation sensitivity (kpk_pkp).

Generate Time Axis:
o Create a time vector for the signal duration based on the sampling frequency.

Generate Message Signal:
o Define the message signal as a cosine wave.

Generate PM Signal:
o Apply the PM modulation formula to obtain the modulated signal.

Plot the Signals:
o Use Scilab to plot the message signal, carrier signal, and phase-modulated signal.

**PROGRAM:**


```
Am=10.83;
fm=812;
fs=81200;
t=0:1/fs:2/fm;
Ac=17.32;
fc=8120;
B=2.63;
em=Am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em);
ec=Ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec);
efm=Ac*cos((2*3.14*fc*t)+B*sin(2*3.14*fm*t)); 
subplot(4,1,3);
plot(t,efm);
epm=Ac*cos((2*3.14*fc*t)+B*cos(2*3.14*fm*t));
subplot(4,1,4);
plot(t,epm);
```

**OUTPUT:**

**SIGNED OUTPUT**:

**RESULT:**
The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.
