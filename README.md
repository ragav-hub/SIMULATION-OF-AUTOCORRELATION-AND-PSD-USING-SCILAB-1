# SIMULATION-OF-AUTOCORRELATION-AND-PSD-USING-SCILAB-1

__AIM:__

Write a program for Autocorrelation and PSD of signals in SCILAB and verify Wiener-Khinchin relation. 


__EQUIPMENTS Needed:__

.Computer with i3 Processor 

.SCI LAB


__THEORY:__

The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the 
Fourier transform of the corresponding autocorrelation function.

__Algorithm:__

 1.Load or Define the Signal: Input your time-domain signal. 

 2.Compute Autocorrelation: Calculate the autocorrelation function of the signal.

3.Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like
Welch’s periodogram or by using the Fourier transform of the autocorrelation.

4.Plot Results: Visualize the autocorrelation function and PSD. 

__PROCEDURE:__


Refer Algorithms and write code for the experiment. 

Open SCILAB in System 

Type your code in New Editor 

Save the file 

Execute the code 

If any Error, correct it in code and execute again 

Verify the generated waveform using Tabulation and Model Waveform 

__PROGRAM:__
```

clc;
clear all;
close;

t = 0:0.01:%pi*2;
x = sin(2*t);

// Plot original signal
subplot(3,2,1);
plot(t, x);
title('Original Signal');

// Autocorrelation
au = xcorr(x, x);
subplot(3,2,2);
plot(au);
title('Autocorrelation');

// FFT of autocorrelation
v = fft(au);
subplot(3,2,3);
plot(abs(v));
title('FFT of Autocorrelation');

// FFT of original signal
fw = fft(x);
subplot(3,2,4);
plot(abs(fw));
title('FFT of Original Signal');

// Power spectrum
fw2 = (abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
title('Power Spectrum');

```

__OUTPUT:__

<img width="1808" height="1020" alt="Screenshot 2025-11-12 144350" src="https://github.com/user-attachments/assets/89378b5f-5b7f-4512-adc3-5997dbe8276e" />


__RESULT:__

Thus, a program is written autocorrelation and PSD of signals in SCILAB and Wiener-Khinchin relation is verified successfully
