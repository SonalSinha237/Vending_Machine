# Vending Machine

A vending machine automates the product sales at public places. It is possible to set differnet pricing for different products. The user chooses the product and inputs money. The machine dispenses the product and gives the change if applicable.

In this case, only one product is there in the machine. User can enter three different coins: 10, 20 & 50. Based on the prce of the product, machine dispenses the product and gives the change.  Later the same idea can be extended to more products.

The machine is designed using the concept of Finite State Machines (FSM).

## Finite State Machines (FSM)

FSM is a model used to represent and control the behavior of systems that can exist in a finite number of states. It consists of a set of states, transitions between those states, and an initial state. The system moves from one state to another in response to external inputs, called events. Key components of FSMs:
 - States: The possible conditions the machine can be in.
 - Transitions: These define the movement from one state to another in response to specific events or conditions. Transitions are triggered by input events and are associated with specific actions or outputs.
 - Inputs: Signals that trigger state transitions.
 - Outputs: Actions taken based on the current state and input.

## Design

- The inputs are fixed as 3 different currency coins (Rs.10, 20 and 50) and price of the product is kept as Rs.40.
- One coin out of the three should be entered at once.
- With every positive edge of the clock, the machine reads the input and decides the next state.
- As we add more coins subsequently, the system transitions to the next stage.
- The system returns to the initial stage (S_initial) if it reaches state 40 (S_40) or above beacause product's price has already been fulfillesd and there's no point in adding more coins.
- If any state is having a sum of Rs.40 or more, the product is dispensed. Along with that, a flag is raised in case of change.
- The number of states and transitions are fixed before the coding. There are total 9 states including the initial state.

## FSM Diagram of Machine
