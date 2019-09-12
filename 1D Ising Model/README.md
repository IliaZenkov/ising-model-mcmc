# The 1D Ising Model

# This project can be viewed at https://github.com/pinech/Py-Projects/blob/master/1D%20Ising%20Model/Ferromagnetic%20Phase%20Transitions%20in%20the%201D%20Ising%20Model.ipynb


A system always tries to lower its energy to reach a minimal energy equilibrium.
At temps near T=0, a system may lower its energy by ordering its states, i.e. the spins of its particles which results
    in a non-zero magnetic moment for the system. 
At high temps (T >> J, J being the coupling parameter of the spins of the system), entropic disorder causes the system
    to choose between various configurations in its phase space which minimize energy - in the 1D Ising Model, by
    allowing disordered (random) spin configurations which reduce the system's magnetization to zero. 


The 1D Ising Model: L particles each with 1/2 integer spin exist on a 2D circular (edge-edge rollover) lattice
Where J is the gauge coupling paramater between identical particles in the lattice, energy of the lattice is given by: 
    Energy = -J/L * sum from 0 to L[(spin value of each particle in lattice) * (sum spin value of corresponding adjacent particles in the lattice)]
Consequently, where U is the Bohr Magneton constant,
    (U = elementary charge * reduced planck constant / (2 * electron rest mass * speed of light))
    the magnetic moment of the lattice is given by
        Magnetic moment = U/L * sum from 0 to L[spin value of each particle in lattice]
        
The Metropolis Algortihm can be implemented to manipulate such a 2D spin lattice to obtain snapshots of random configurations
    (to get random samples) of such a lattice and ultimately to demonstrate how such a lattice moves towards a state of lower energy and towards zero magnetization. We can also use the Metropolis algo to upscale to higher dimension spin lattice simulations.

