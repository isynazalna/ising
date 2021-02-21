# ising
A simulation for 2D Ising modeling with Monte Carlo method
Monte Carlo simulation for 2D Ising Model

This Ising model used for simulating magnetic systems (positive, negative, or random spins) by applying the Metropolis algorithm-Monte Carlo method. Run the main file, input the lattice size (favorably 100) then choose an input spin as the initial configuration. Two different temperatures (T=2.0 and T=2.5) were set. 

For instance, initialization with a chosen positive spin at T=2 (low temp) most of the spins are black, this is because the chances of flipping spins are small and the material appeals to be ferromagnetic. For the case of T=2.5, since the temperature is higher, it creates a tendency for spins to flip. Thus, the material loses the magnetization. The spins don’t seem to align, and the resulting configurations appear to be randomly disordered. That’s because of the paramagnetic behavior. 

The next part of the simulation is the observables computation: Mean Magnetization, Mean Energy, Mean Susceptibility, and Specific Heat. 
In order to compute mean energy and magnetization, we have to find a time dependency of which the energy and magnetization values change little (the time in which the energy and magnetization change little as time increases)
Therefore, we choose the precision p and check the interval (the number of time steps that should satisfy the precision). These intervals should depend on the initial configuration. Each time step we compare in current and previous steps variables (average energy and average magnetization) and compare it with the precision. If it satisfies the condition for the whole interval, we call the current time step as approximated thermalization time and start computing the variables, Mean Magnetization, Mean Energy, Mean susceptibility, and Specific Heat.



