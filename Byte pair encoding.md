---
tags:
  - 🌱
date: 22--Jan--2024
alias: 
modified: 22--Jan--2024
---
# Byte pair encoding
Takes a [[Corpora]] broken up into characters and then iteratively merge [[Tokens]] to learn the vocabulary.
## Algorithm 
```psuedo
V = all unique character in C
for i=1 to k do
    find most frequent pair of adj token
    t_new = t_L + t_R
    V append t_new
    Replace each t_L,t_R pair with t_new
return V
```

---
Links: [[Tokenise]]
