---
tags:
  - 🌱
date: 22--Jan--2024
aliases:
  - bigram
  - trigram
  - n-gram
modified: 23--Jun--2024
---
# N gram model
Using probability to model the next likely word.
## Frequency as probability
Given a large [[Corpora|Corpus]], count the frequency of each word following some sentence.
$$P(A|Sentence)=\frac{C(Sentence)}{C(A)}$$
Then, the entire [[Probability]] can be decomposed with [[Chain rule of probability]]. Where if the sentence is made of $n$ words
$$P(X_{1} \ldots X_{n})=P(X_{1})P(X_{2}|X_{1}) \ldots= \prod^{n}_{k=1} P(X_{k}|X_{1:k-1})$$
### Limitation
Having an exact sentence to predict the next word might not exist especially since language can evolve. Instead of using the entire history, a subset could be considered.
When a sentence is long, the probability of having the exact match would also be close to zero. Thus, the use of chain rule decomposes the sentence with long history.
## Using N gram
Approximation of probability with the N words instead. In the case below, bigram uses 2.
$$P(w_{n}|w_{1:n-1}) \approx P(w_{n}|w_{n-1})$$
This hinges on the idea of [[Markovian transition model]]. 

---
Links:
