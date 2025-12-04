# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB
## AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS Needed
• Computer with i3 Processor 
• SCI LAB

## Algorithm
Define the Function: Specify the function you want to simulate. For example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
Evaluate the Function: Compute the function values at each of these sample points.
Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
Display Results: Output the computed mean variance and Cross Correlation PROCEDURE • Refer Algorithms and write code for the experiment. • Open SCILAB in System • Type your code in New Editor • Save the file • Execute the code • If any Error, correct it in code and execute again • Verify the generated results
## PROGRAM
```
//Mean
function X=f(x)
    z=3*(1-x)^3;
    X=x*z;
endfunction

a=0;
b=1;

EX=intg(a,b,f);
function Y=c(y)
    z=3*(1-y)^3;
    Y=y*z;
endfunction

EY=intg(a,b,c);
disp("i)Mean of X =",EX)
disp("ii) Mean of Y =",EY)

//Variance

function X=g(x)
    z=3*(1-x)^3;
    X=x^2*z;
endfunction

a=0;
b=1;

EX2=intg(a,b,g);
function Y=h(y)
    z=3*(1-y)^3;
    Y=y^2*z;
endfunction

EY2=intg(a,b,h);

vX2=EX2-(EX)^3;
vY2=EY2-(EY)^3;

disp("iii) Variance of X",vX2);
disp("iv) Variance of Y",vY2);

// Cross Correlation

x=input("type in the reference sequence=");
y=input("type in the second sequence=");
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);
```


## Tabulation
![WhatsApp Image 2025-12-04 at 14 04 05_f6d8649e](https://github.com/user-attachments/assets/b31961d4-4f49-478c-b113-d177f9364a7e)
![WhatsApp Image 2025-12-04 at 14 04 37_7f935069](https://github.com/user-attachments/assets/ac37ebd4-ccee-4a7a-a5e3-a2949c237030)






## OUTPUT
<img width="213" height="311" alt="image" src="https://github.com/user-attachments/assets/8cbcce3d-2afc-4fce-9105-05a2fa2d717c" />


## RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
