# Simulating the 2D Ising Model using a Monte Carlo algorithm
# This project can be viewed at https://nbviewer.jupyter.org/github/pinech/Py-Projects/blob/master/Ising%20Model%20Markov%20Chain%20Montre%20Carlo%20Simulations.ipynb


The Ising Model is a simple and effective physical model of a magnet. 
A magnet's strength is measured by its magnetization, which arises from the combination of all particles in a lattice, each with either spin-up or spin-down.
Each particle is like a dipole - a North-South magnet - if we line up all the "magnets" (i.e. individual particles) within the lattice to face the same direction, then the magnet system will gain an overall magnetization - it will be magnetic.
However, if all the particles in the lattice have random spins, then the overall magnetization of the system should be close to zero as they will cancel each other with enough samples.

The Ising model simulates the process whereby individual particles are represenhted as individual dipoles - spin-up and spin-down - arranged on a gird or lattice.

Theoretically, this model can be further defined and scaled up to any lattice dimension.
Here, I simulate a 2D Ising model using Monte Carlo methods on a square lattice system of 20*20 spins.
