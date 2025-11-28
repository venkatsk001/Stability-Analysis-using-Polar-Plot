# Stability-Analysis-using-Polar-Plot

## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=10/(S(1+0.5S)(1+0.2S)) using polar plot and verify it using MATLAB. 

## Apparatus Required:
Computer with MATLAB software

## Theory:
![WhatsApp Image 2025-11-27 at 23 50 47_fa6e6883](https://github.com/user-attachments/assets/d42838e9-1d3e-4cfe-96c3-5c53b4fe485d)
![WhatsApp Image 2025-11-27 at 23 51 21_dd7b25ce](https://github.com/user-attachments/assets/b3b05a19-fec8-43e1-9823-5c0e6fab0e6d)
![WhatsApp Image 2025-11-27 at 23 52 02_bb48875b](https://github.com/user-attachments/assets/994da64f-c19b-49ae-b998-e7d9bdcc0580)



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 

```
num=[10]
den=[0.1 0.7 1 0]
sys=tf(num,den)
[mag,phase,W]=bode(sys)
mag=squeeze(mag)
phase=squeeze(phase)
phase1=deg2rad(phase)
polarplot(phase1,mag,'linewidth',1.5)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```

## Output:

<img width="713" height="640" alt="image" src="https://github.com/user-attachments/assets/4711b265-6492-408c-8d8f-c70d45e66a71" />

## Result:
Thus the polar plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 0.7 <br>
Phase Margin = -8.8865 <br>
Gain crossover frequency = 3.7565 <br>
Phase crossover frequency = 3.1623 <br>
The system is unstable.
