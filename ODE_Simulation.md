# Downloading necessary packages 
import numpy as np

import matplotlib.pyplot as plt 

from scipy.integrate import odeint

# Defining the Exponential Growth Model
def bac(P,t): 
    k = .3
    dPdt = k*P
    return dPdt 
# Defining Initial Coniditions and Timespan, Integrating with ODEINT
P0 = 100 
t = np.linspace(0,10,30)
y = odeint(bac,P0,t) 

# Plotting graphs 
plt.plot(t,y,'b-') 

# Defining the Logistic Growth Model 
def baclog(P,t): 
    k = .3 
    dPdt = .3 * P * (1 - (P/1000))
    return dPdt 
# Defining Initial Coniditions and Timespan, Integrating with ODEINT
P0 = 100
t = np.linspace(0,250,1000) 
y = odeint(baclog,P0,t) 

# Plotting 
plt.plot(t,y,'b:') 

# Defining the Lotka-Volterra Model(Original Parameters)
alpha = 1.0 
beta = .1 
gamma = 1.5 
delta = .075

def model(z,t, alpha, beta, gamma, delta): 
    x = z[0] 
    y = z[1]

    dxdt = alpha * x - beta * x * y 
    dydt = delta * x * y - gamma * y 
    
    return [dxdt,dydt]  

# Defining the Lotka-Volterra Model(Increased Predation Rate)
alpha = 1.0 
beta = .2
gamma = 1.5 
delta = .075

def model(z,t, alpha, beta, gamma, delta): 
    x = z[0] 
    y = z[1]

    dxdt = alpha * x - beta * x * y 
    dydt = delta * x * y - gamma * y 
    
    return [dxdt,dydt]  

# Defining the Lotka-Volterra Model( Increased Predator Conversion Rates)
alpha = 1.0 
beta = .1 
gamma = 1.5 
delta = .090

def model(z,t, alpha, beta, gamma, delta): 
    x = z[0] 
    y = z[1]

    dxdt = alpha * x - beta * x * y 
    dydt = delta * x * y - gamma * y 
    
    return [dxdt,dydt]  

# Defining Initial Coniditions and Timespan, Integrating with ODEINT
z0 = [40,9] 
t = np.arange(0,20,.2)
sol = odeint(model, z0, t, args = (alpha, beta, gamma, delta)) 

# Plotting 
plt.plot(t,sol[:,0],'b-')
plt.plot(t,sol[:,1],'r-')
