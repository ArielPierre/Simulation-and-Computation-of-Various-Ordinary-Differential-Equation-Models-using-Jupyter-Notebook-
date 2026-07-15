## Simulation and Computation of Various Ordinary Differential Equation Models using Jupyter Notebook 
This project contains the simulation of two bacterial growth models and the Lotka-Volterra predatory prey model in jupyter notebook. 

## Methods 
- Equation integration 
- Equation graphing 

## Tools Used 
- Numpy 
- Matplotlib 
- Scipy.integrate

## Files 
- ODE_Simulation.md :  Main simulation script

## Visualizations 

Exponential Bacterial Growth 


$$
\frac{dP}{dt} = kP , k = .3 
$$ 


<img width="561" height="413" alt="bacterialgrowthexpotential" src="https://github.com/user-attachments/assets/ffef821f-e88b-4a92-a3df-b327ae6de2df" />

Logistic Baterial Growth 


$$
\frac{dP}{dt} = kP\left(1 - \frac{P}{K}\right)
$$ 

<img width="561" height="413" alt="logisticbacterialgrowth" src="https://github.com/user-attachments/assets/c366a89d-ce79-48c7-a75c-d1a760c58be8" />


Lotka-Volterra Predator Prey Model 

$$ 
\frac{dx}{dt} = \alpha x - \beta xy 
\quad 
\frac{dy}{dt} = \delta xy - \gamma y 
$$ 

<img width="543" height="413" alt="LVmodel" src="https://github.com/user-attachments/assets/43ca5088-1372-4486-9218-f91d5c571425" />
