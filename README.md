![WhatsApp Image 2025-11-28 at 14 46 44_88ab501a](https://github.com/user-attachments/assets/e181a599-c6bf-4aa2-9aa7-0e60eca77373)# Stability-Analysis-using-Polar-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=10/(S(1+0.5S)(1+0.2S)) using polar plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![Uplo![WhatsApp Image 2025-11-28 at 14 46 44_ffe7d604](https://github.com/user-attachments/assets/15f79c65-bfc3-4a62-9b92-943ec68b9077)
![WhatsApp Image 2025-11-28 at 14 46 44_4787e2b4](https://github.com/user-attachments/assets/a4c9dedd-6b20-4e7a-b71a-a3bec58ceb8b)

![WhatsApp Image 2025-11-28 at 14 46 45_ef576da9](https://github.com/user-attachments/assets/2347b75f-1b45-4441-b3c8-a3b1b2714520)


## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
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


## Output:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b908f8a2-e425-48d8-80c1-e315fdce0d20" />


## Result:
Thus the polar plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 0.7 <br>
Phase Margin = -8.8865 <br>
Gain crossover frequency = 3.7565 <br>
Phase crossover frequency = 3.1623 <br>
The system is unstable
