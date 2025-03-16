---
tags:
  - 🌱
date: 12--Aug--2024
alias: 
modified: 12--Aug--2024
---
# Dependency structure
To show which words depend on which other words, aka how they are related such as modifier or arguments.

A formal saying would be that the structure consists of relations between lexical items, normally **binary directed relation** called dependencies. The directed relation is normally **typed** with the grammatical relation.

What is typed dependency. It means that there is a labelling of the dependency. Untyped means its just directed arrow.

We can formulate the dependency parsing with these conditions
- Only one word dependent of root
- Do not allow cycles
Then we can guarantee the following
- directed acyclic graph

# How to do dependency parsing
Transition based dependency parsing!
Arc-standard transition based parser d
- shift: take word from buffer put in stack
To make attachment decisions by adding dependent on left/right
- left arc: top → 2nd top, aka 2nd top is a dependent of the top
- right arc: 2nd top → top, top is a dependent of 2nd top

# Evaluation

UAS (unlabelled accuracy score). Not looking at the labels but the arrows to check if its correct.
LAS. Look at labels, arrows and compute accuracy.
$$\frac{correct}{total}$$
# Machine learning vs DNN
sparse features to learn
incomplete problem, only seen small fraction of these words
expensive computation to look at features and look up weights

Instead learn a dense compact feature representation. Aka DNN

#? what is the link with treebank

---
Links:
