# Black-box-MPC

+ Totally random excitation (random controller ON/OFF) for many days/years

+ Based on simulation outputs, train a model which, based on: current (indoor & outdoor) state, current control action, next e.g. 5 control actions and outdoor conditions -> estimates the next e.g. 5 rewards (energy + comfort)

+ Based on this model, at any given time step of the validation tests, using the current state, the forecasted outdoor states, and all possible combinations of control setpoints for the next e.g. 5 timesteps, estimate the next e.g. 5 rewards (weighed with a forgetting γ-factor) and choose the combination with the best accumulated reward

+ Apply the first setpoint of the combination and rerun the inferencing model

+ Retrain the model at a weekly or monthly basis
