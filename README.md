# Simple Reflex Agent

## Project Overview

This project demonstrates the implementation of a **Simple Reflex Agent** using Python. The agent operates in a basic two-room vacuum environment and makes decisions based only on the current condition of the environment.

The goal of the agent is to clean both rooms by selecting an action according to predefined condition-action rules.

## Objective

The objective of this project is to understand how a simple reflex agent works and how an intelligent agent can make decisions based on its current percept without storing information about previous states.

The agent evaluates:

- Its current location
- Whether the current room is clean or dirty

Based on these conditions, the agent performs an appropriate action.

## Environment

The environment contains two rooms:

- Room A
- Room B

Each room can be in one of two states:

- Clean
- Dirty

The vacuum agent can be located in either Room A or Room B.

## Agent Actions

The agent can perform the following actions:

- **Suck**: Cleans the current room
- **Move Right**: Moves from Room A to Room B
- **Move Left**: Moves from Room B to Room A
- **No Action**: Used when the cleaning task is complete

## Agent Logic

The agent follows simple condition-action rules.

```text
If the current room is dirty:
    Clean the room

If the agent is in Room A and the room is clean:
    Move to Room B

If the agent is in Room B and the room is clean:
    Move to Room A
```

The agent does not maintain memory of previous actions. Its decision is based only on the current percept.

## Example

An example initial environment may look like:

```text
Agent Location: Room A

Room A: Dirty
Room B: Dirty
```

The agent may perform the following sequence:

```text
1. Detect Room A is dirty
2. Clean Room A
3. Move to Room B
4. Detect Room B is dirty
5. Clean Room B
6. Cleaning task completed
```

Final environment:

```text
Room A: Clean
Room B: Clean
```

## Test Conditions

The agent can be tested using different initial environmental conditions.

### Test Case 1

```text
Agent Location: A
Room A: Dirty
Room B: Dirty
```

Expected result:

```text
Both rooms are cleaned.
```

### Test Case 2

```text
Agent Location: A
Room A: Clean
Room B: Dirty
```

Expected result:

```text
The agent moves to Room B and cleans it.
```

### Test Case 3

```text
Agent Location: B
Room A: Dirty
Room B: Clean
```

Expected result:

```text
The agent moves to Room A and cleans it.
```

## Technologies Used

- Python
- Google Colab / Jupyter Notebook
- Simple Reflex Agent Architecture
- Rule-Based Decision Making

## Project Structure

```text
Simple-Reflex-Agent/
│
├── README.md
├── simple_reflex_agent.ipynb
└── simple_reflex_agent.py
```

The exact files may vary depending on the implementation.

## Key Concepts Demonstrated

This project demonstrates several fundamental concepts in Artificial Intelligence:

- Intelligent agents
- Simple reflex agents
- Environment perception
- Condition-action rules
- Agent actions
- Rule-based decision making

## Limitations

A simple reflex agent has several limitations.

The agent:

- Does not remember previous states
- Does not learn from experience
- Cannot plan future actions
- Makes decisions only from the current percept
- Works best in simple and fully observable environments

For more complex environments, model-based, goal-based, utility-based, or learning agents may be more appropriate.

## Conclusion

This project demonstrates the basic behavior of a Simple Reflex Agent using a two-room vacuum environment. The agent observes the current state of its environment and selects an action using predefined rules.

Although the approach is simple, it provides a foundation for understanding how intelligent agents perceive environments, make decisions, and perform actions.

## Author

**Chakradhar Patnam**

Applied Machine Intelligence and Reinforcement Learning
