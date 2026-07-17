## Simulation and Computation of Various Ordinary Differential Equation Models using Jupyter Notebook 
This project contains the simulation of two bacterial growth models and the Lotka-Volterra predatory prey model in jupyter notebook. Further parameter explorations are conducted with the Lotka-Volterra model as well. 

## Methods 
- Equation integration 
- Equation graphing 

## Tools Used 
- Numpy 
- Matplotlib 
- Scipy.integrate

## Files 
- ODE_Simulation.md :  Main simulation script

# Results of the Lotka-Volterra Model Parameter Exploration 
- With an increase predator conversion rate, we observe oscillations of a greater amplitude. Higher predator conversion leads to predators reproducing more effeciently, leading to prey populations decreasing to a seemingly unchanged trough.The reduced predator population then lessened predation pressure, allowing the prey population to recover for a longer period and reach a higher peak before predator numbers began increasing again.
- Within the explored parameter changes, with an increased predation rate, we observe a sharp decrease in both the minimum and maximum of the prey populations. The predator populations appear approximately unaffected. 

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


<img width="543" height="440" alt="original_parameters" src="https://github.com/user-attachments/assets/9f93ca49-ab91-474d-b6fc-17f683bcfb60" />

Original Parameters 

<img width="543" height="440" alt="beta_variation" src="https://github.com/user-attachments/assets/290e43eb-c9fb-45af-a75d-ce1bb0bd7ac4" /> 

Higher Predation Rate 

<img width="543" height="440" alt="delta_variation" src="https://github.com/user-attachments/assets/77b88a30-ece9-4893-8d3d-9e37cd192c51" />

Higher Predator Conversion Rate  
