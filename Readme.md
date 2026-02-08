# Schelling Social Segregation

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/MESA-Agent_Based_Modeling-orange?style=for-the-badge" alt="MESA"/>
  <img src="https://img.shields.io/badge/Simulation-Social_Dynamics-blue?style=for-the-badge" alt="Simulation"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Course-Experimental_Computing-purple?style=flat-square" alt="Course"/>
  <img src="https://img.shields.io/badge/Institution-UnB-blue?style=flat-square" alt="UnB"/>
  <img src="https://img.shields.io/badge/Type-Academic_Project-green?style=flat-square" alt="Type"/>
</p>

## Overview

The initial simulation code was obtained from the Mesa framework examples repository: https://github.com/projectmesa/mesa/tree/main/examples/schelling

The simulation aims to reconstruct the segregation phenomenon addressed by Schelling. The model consists of agents distributed on a grid, where each cell can contain at most one agent. Initially, agents could belong to two classes: red and blue. An agent's happiness is achieved if a certain number of their eight possible neighbors are the same color, and unhappy otherwise. At each step, unhappy agents choose a random empty cell to move to until they are happy. The model continues running until there are no dissatisfied agents. In order to experiment with the relationship between a larger number of classes and the number of happy agents, it was necessary to make some changes to the simulator code, which will be described in more detail in the "Changes Made" section.

## Hypothesis Description

The causal hypothesis is that the greater the number of classes into which individuals are divided, the greater the difficulty in achieving happiness for all agents. For more agents to be content with their neighborhood, it is necessary to be more flexible regarding the homophily rate.

## Changes Made

- Added the independent variable "Number of agent types" to expand and determine the number of classes present in the model
- Adapted the way class distribution was done; currently, distribution is done randomly until the density specified by the "density" variable is reached
- Added more colors to represent the various classes
- The dependent variable "happy" was transformed into the dependent variable "Percentage of happy agents" so that it represents a more collective condition of the model

## How to Use the Simulator

### Dependencies

For correct execution of the model, you must install the **mesa** package and others listed in **requirements.txt**. This can be done by executing the following command:

```bash
pip install -r requirements.txt
```

### Execution

To use the simulator and run the new model, simply execute the following command:

```bash
mesa runserver
```

## Model Variables Description

### Independent or Control Variables

- **Agent density**: Agent density, determines the number of agents and empty spaces
- **Homophily**: The tendency of individuals to associate and establish bonds with similar others
- **Number of agent types**: Number of individual classes in the model; class is the group with which the individual most identifies

### Dependent Variables

- **Percentage of happy agents**: Percentage of happy agents at that step, calculated by the number of agents who are happy with their neighborhood divided by the total number of agents
- **Number of steps until 100% happy agents**: Number of steps executed until all agents were content with their respective neighborhoods

## Academic Context

**Course**: Experimental Computing (Computação Experimental)  
**Institution**: University of Brasília (UnB)  
**Type**: Academic Project

## Contact

**Tatiana Pereira**  
Email: fpereira.tatiana@gmail.com  
LinkedIn: [linkedin.com/in/tatiana-franco-pereira](https://linkedin.com/in/tatiana-franco-pereira)  
Lattes CV: [lattes.cnpq.br/6503681647703666](http://lattes.cnpq.br/6503681647703666)

---

<p align="center">
  <i>Developed as part of Computer Science undergraduate program at UnB</i>
</p>
