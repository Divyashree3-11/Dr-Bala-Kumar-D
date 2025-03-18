## IDEAL SAMPLING
## AIM:
  To Perform construction and re-construction of Impulse or Ideal Sampling using python. 
## APPARATUS REQUIRED:
  Python IDE with Numpy and Scipy
## CODE:
```
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import resample
fs = 100
t = np.arange(0, 1, 1/fs) 
f = 5
signal = np.sin(2 * np.pi * f * t)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
reconstructed_signal = resample(signal_sampled, len(t))
plt.figure(figsize=(10, 4))
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/8c8610c1-e9e4-41a5-8566-5e1f948e125c)
![image](https://github.com/user-attachments/assets/f20ffa3a-c647-4adc-8b85-4dbcb66eb477)
![image](https://github.com/user-attachments/assets/2cbbd95a-0577-4d01-a3ee-54ee49c8194e)

## RESULT:
Thus, Construction and Re-construction of Ideal or Impulse Sampling has been verified using python.





