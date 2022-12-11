---
cover: ../../.gitbook/assets/GITHUB.png
coverY: 0
---

# 🧿 Parameter details

_**Frequency and presence penalties**_

_The frequency and presence penalties found in the Completions API can be used to reduce the likelihood of sampling repetitive sequences of tokens. They work by directly modifying the logits (un-normalized log-probabilities) with an additive contribution._

```
mu[j] -> mu[j] - c[j] * alpha_frequency - float(c[j] > 0) * alpha_presence
```

Where:

* `mu[j]` is the logits of the j-th token
* `c[j]` is how often that token was sampled prior to the current position
* `float(c[j] > 0)` is 1 if `c[j] > 0` and 0 otherwise
* `alpha_frequency` is the frequency penalty coefficient
* `alpha_presence` is the presence penalty coefficient

As we can see, the presence penalty is a one-off additive contribution that applies to all tokens that have been sampled at least once and the frequency penalty is a contribution that is proportional to how often a particular token has already been sampled.

Reasonable values for the penalty coefficients are around 0.1 to 1 if the aim is to just reduce repetitive samples somewhat. If the aim is to strongly suppress repetition, then one can increase the coefficients up to 2, but this can noticeably degrade the quality of samples. Negative values can be used to increase the likelihood of repetition.
