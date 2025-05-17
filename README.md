# Eisbach inline match method

Isabelle's Eisbach match method provides a powerful mechanism for building scalable automation, 
allowing proof methods to be applied conditionally based on logical patterns matched within 
proof premises or conclusions. However, invoking match introduces a new subgoal context, which 
instantiates all schematic variables (?x) in the current proof goal. This behaviour poses 
challenges for proof strategies that depend on delaying the instantiation of schematic 
variables until later in the proof. The revised match method presented here avoids the creation
of a new subgoal context, thereby preserving these schematic variables. 

The ultimate aim of this work is to persuade the Isabelle maintainers to add an option to 
Eisbach’s match method that allows users to control whether a subgoal context is introduced.

## Requirements 

These theories have been tested with [Isabelle/HOL 2025](https://isabelle.in.tum.de/installation.html) and the latest stable [AFP](https://www.isa-afp.org/).

## Installation

Build in the root of the repository (where `ROOT` file is located) using `isabelle build -D .`.

To use these theories in your own work, add this repository to Isabelle: `isabelle components -u .`.
