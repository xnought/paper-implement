# The Perceptron 

The paper that started it all.

## Implementations

- Single Perceptron binary linear classifier
- Multi-Layer Perceptron binary non-linear classifier

## Papers
- https://www.ling.upenn.edu/courses/cogs501/Rosenblatt1958.pdf
- https://gwern.net/doc/ai/nn/1962-rosenblatt-principlesofneurodynamics.pdf
- https://www.wikiwand.com/en/articles/Perceptron

## Notes
- Main questions about brain are how is information detected, stored, then used 
- How might information be stored? 1 to 1 as codes (like RAM) or stored within some other medium (like networks of neurons and firing patterns)
- It could be that we have stimulus that directly indexes into a symbol and that is what get's read out as an action. Or it could be patterns that result in other patterns, which then can be used later on for actions. 
- Also implicitly says that it's not one neuron that stores a mapping to all possible actions, that would be untenable! Patterns and changes in pathways among densely connected networks can support that many outcomes though!
- Positive/negative reinforcement might change the neural growth. Thus changing behavior.
- Neurons in perceptron model are modeled after all or nothing sum of inhibition or excitation
- Connections start out random
- Inhibitory connections are meant to reduce pathways that are not directly used
- The first paper just defines the concept of the perceptron, not how to actually update the weights in response to a loss function in a supervised way

