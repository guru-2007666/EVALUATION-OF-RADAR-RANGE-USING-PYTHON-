# EVALUATION-OF-RADAR-RANGE-USING-SCILAB-

__Aim__:

To calculate the maximum range of a radar system using the Radar Range Equation and verify the results 
through Python programming.

__Theory__:

The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum 
range at which a radar can detect a target. It is given by:

<img width="573" height="442" alt="image" src="https://github.com/user-attachments/assets/ba374d30-d11f-41e5-a4fc-a42dde71d8e7" />

__Procedure__:

1. Set Up the Python Environment: Ensure that Python is installed on your system. You can use 
Anaconda for managing Python packages and environments, or any other Python IDE of your choice. 
2. Import Necessary Libraries: Import the math library in Python. 
3. Define the Radar Range Equation Function: Create a function to calculate the maximum range using 
the Radar Range Equation. 
4. Input Parameters for the Radar System: Define the input parameters such as transmitted power, 
transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power. 
5. Calculate the Maximum Range: Use the function to calculate the maximum range of the radar. 
6. Execute the Program: Run the Python script to calculate and display the maximum range of the radar.

PROGRAM:
```

Gr = 7;
w = 8;
sigma = 9;  
pmin = 1e-9;
Gt = 6;
Pt = 0.5:0.5:100;   
Rmax1 = (((Pt .* Gt .* Gr .* (w.^2) .* sigma) ./ (((4 * %pi).^3) .* pmin))).^(1/4);
subplot(3,1,1);
plot(Pt, Rmax1);

Pt = 20;
Gt = 0.1:0.1:9;     
Rmax2 = (((Pt .* Gt .* Gr .* (w.^2) .* sigma) ./ (((4 * %pi).^3) .* pmin))).^(1/4);
subplot(3,1,2);
plot(Gt, Rmax2);

Gt = 7;
pmin = 1e-14:1e-13:1e-9;  
Rmax3 = (((Pt .* Gt .* Gr .* (w.^2) .* sigma) ./ (((4 * %pi).^3) .* pmin))).^(1/4);
subplot(3,1,3);
plot(pmin, Rmax3);
```
   
__Output__:
   


<img width="1807" height="1023" alt="image" src="https://github.com/user-attachments/assets/91546bfd-a8a5-40a1-a8da-0ba4130cfd09" />



  __Result__:
   
Thus, the maximum range of a radar system calculated using the Radar Range Equation is successfully verified using Scilab programming.



