---
tags:
  - 🌱
date: 12--Aug--2024
alias: 
modified: 12--Aug--2024
---
# Hiden markov model tagger
Built upon [[Hidden Markov Model]] with 2 more assumption
1. Probability of word appearing depends on its own tag and independent of other neighbouring word and tag. This is [[Output independence]] applied.
2. Bigram assumption that the probability of a tag is dependent only on previous tag rather than a sequence. This is [[Markovian transition model|Markov assumption]] applied.
## Formulation
The decoding goal is to assign a tag sequence that is most probable given a word sequence.
$$\hat t_{1:n} = \arg \max_{t_{1:n}} P(t_{1:n}|w_{1:n})$$
To compute the probabilities, we can use [[Bayes Theorem]] to break the equation down into components that are available to us.
$$\hat t_{1:n} = \arg \max \frac{P(w_{1:n}|t_{1:n})P(t_{1:n})}{P(w_{1:n})}$$
We can drop the denominator since we are comparing the highest probability across the same divisor. That is we can view $P(w_{1:n})$ a constant during the calculation.

We can now compute the components of the equation. The first is the Emission probability. This is computed using assumption (1) stated above.
$$P(w_{1:n}|t_{1:n}) \approx \prod P(w_{i}|t_{i})$$
The next is the transition probability, computed using assumption (2)
$$P(t_{1:n}) \approx \prod P(t_{1}|t_{i-1})$$
Putting both equations together, we can form the

---
Links:
