# Boltzmann Machines

## Implementations

- full_boltzmann_machine.ipynb (work in progress)

## Papers

- https://www.cs.toronto.edu/~fritz/absps/cogscibm.pdf
- https://www.youtube.com/watch?v=_bqa_I5hNAo

## Notes on papers

- A learning algorithm on dense network based on statistical mechanics
- Connectionist pov: info stored between connections in networks
- Parallel updates are not straightforward since if info is dependent on other, it needs to first compute other.
- Boltzmann machine is a network with weights that can be updated based on patterns seen
- Generate a unique signature comprised of combinations of activations within the network. Then later on we can recall that we've seen such an input or reconstruct part of a input. Not exactly sure how this would work though!
- Trash idea that random networks are better than designed
- What is a boltzmann machine?
	- Units as "primitive computing elements"
	- Links between units that are bidirectional and have a single weight
	- Unit is either on or off, not in between. It is one of these states as a function of the neighboring units and linked weights connecting those units.
	- Positive weight linked between units represents that the hypothesis supported between these elements. Negative is not supported.
- Energy defined as sum of weight times if the states are on. Otherwise nothing if off. $$E = -\sum_{i<j} w_{ij}s_i s_j + \sum_{i} \theta_i s_i$$ where here $s_i$ is a particular unit being on (1) or off (0) and $w_{ij}$ is their link weight. This can be interpreted between ever link, if both units are on, count the weight contribution, otherwise do not. Essentially this is trying to find connections that activate based on the inputs which mean that hypotheses about the data are found. The second term is meant to be a threshold (which I still don't really know about). It's probably regularizing how many units can be activated. 
- To minimize the energy, we can switch the states and change the weights. If I take inputs to be encoded via the states, then it is then totally up to the weights to change to minimize energy.
- We can determine the change in energy of a particular state flip from off to on as $$\Delta E_k = \sum_{i} w_{ik}s_k - \theta_k$$. This can be found from the energy equation.
- Then they conclude that if you exceed the threshold $\theta_k$ then that is when you flip a state from 0 to 1. In other words, the contributions from neighboring units, if passed the threshold, we turn that unit on!
- To simplify the equations, we can add a bias term to all the units as $-\theta_k$ which then removes theta from both equations. This can also be interpreted as having true units with are always on and have the weight of $-\theta_k$ and are connected to each unit. 
- So then we get the new equations $E = -\sum w_{ij}s_i s_j$ and $\Delta E_k = \sum w_{ik} s_{k}$.
- Not good enough to just minimize energy, sometimes allow for flips if the energy gap is satisfied

