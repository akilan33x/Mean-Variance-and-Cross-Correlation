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


## CALCULATION
![WhatsApp Image 2025-12-03 at 13 15 21_ba44a530](https://github.com/user-attachments/assets/c7427ca5-b8c5-4db7-a431-0de1ddb06292)
![WhatsApp Image 2025-12-03 at 13 15 57_e9e37960](https://github.com/user-attachments/assets/91a3c6b9-e305-40d5-9dea-996ee049492a)
![WhatsApp Image 2025-12-03 at 13 16 25_30d788c7](https://github.com/user-attachments/assets/03774271-8d1d-40dc-91e2-2e1f45cca4ac)



## OUTPUT
<img width="766" height="720" alt="image" src="https://github.com/user-attachments/assets/15029296-7404-4913-b039-e0977291b630" />

## RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
