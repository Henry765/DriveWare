# WakeupDriver

App that alerts drivers if sleeping  



The absolute band power for a given frequency range (for instance, alpha, i.e. 9-13Hz) is the logarithm of the sum of the Power Spectral Density of the EEG data over that frequency range

delta_absolute	1-4Hz			
theta_absolute	5-8Hz			
alpha_absolute	9-13Hz			
beta_absolute	12-30Hz			
gamma_absolute	30-50Hz

alpha_relative = (10^alpha_absolute / (10^alpha_absolute + 10^beta_absolute + 10^delta_absolute + 10^gamma_absolute + 10^theta_absolute))
beta_relative = (10^beta_absolute / (10^alpha_absolute + 10^beta_absolute + 10^delta_absolute + 10^gamma_absolute + 10^theta_absolute))
theta_relative = (10^theta_absolute / (10^alpha_absolute + 10^beta_absolute + 10^delta_absolute + 10^gamma_absolute + 10^theta_absolute))
gamma_relative = (10^gamma_absolute / (10^alpha_absolute + 10^beta_absolute + 10^delta_absolute + 10^gamma_absolute + 10^theta_absolute))
delta_relative = (10^delta_absolute / (10^alpha_absolute + 10^beta_absolute + 10^delta_absolute + 10^gamma_absolute + 10^theta_absolute))

Above data are computed using raw EEG data.

Some of the values will be negative (i.e. when the absolute power is less than 1) They are given on a log scale, units are Bels.
