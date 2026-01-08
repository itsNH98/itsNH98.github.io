---
layout: single
title: "Prediction Market Prices Aren't Probabilities"
date: 2026-01-07
author_profile: true
---

Prediction markets are everywhere now. Polymarket shows "Trump 62%," experts cite it as the wisdom of crowds, and everyone treats these numbers as probabilities. I want to push back on this interpretation: that 62% is not a probability. It is a price.

This distinction is well understood in theory but routinely ignored in practice, and I think it deserves more attention.

## When prices equal probabilities

When can we interpret prediction market prices as probabilities? This question sparked a notable exchange in the literature. Manski (2006) showed that under risk-neutral trading, prices do not generally equal mean beliefs. Instead, price only partially identifies the central tendency of beliefs, lying in an interval whose midpoint is the equilibrium price. Wolfers and Zitzewitz (2006) responded by providing sufficient conditions under which prices do approximate mean beliefs: with log utility, for instance, prices exactly equal mean beliefs across traders. They show that for most plausible parameters, prices are close to mean beliefs, even if not identical.

Both papers, however, assume away risk premia. The problem is that this assumption rarely holds for events that load on aggregate states.

## P vs Q: physical and risk-neutral measures

Consider a prediction market contract paying $1 if event *E* occurs. Under no-arbitrage, the price satisfies:

$$p = \mathbb{E}^{\mathbb{P}}[m \cdot \mathbf{1}_E]$$

where *m* is the stochastic discount factor and $\mathbb{P}$ denotes the physical probability measure. Decomposing this:

$$p = \mathbb{P}(E) \cdot \mathbb{E}^{\mathbb{P}}[m | E]$$

The price equals the physical probability $\mathbb{P}(E)$ scaled by the conditional expected SDF. When *E* occurs in states where marginal utility is high (bad states), $\mathbb{E}^{\mathbb{P}}[m | E] > \mathbb{E}^{\mathbb{P}}[m]$, and the price exceeds the physical probability.

Equivalently, we can write:

$$p = \mathbb{Q}(E) \cdot \mathbb{E}^{\mathbb{P}}[m]$$

where $\mathbb{Q}$ is the risk-neutral measure. Market prices reflect $\mathbb{Q}(E)$, not $\mathbb{P}(E)$. The gap between the two is the risk premium.

## An example: recession contracts

Consider [Polymarket's recession contract](https://polymarket.com/event/us-recession-by-end-of-2026). Suppose you believe there is a 10% physical probability of recession. Would you pay 10 cents for a contract paying $1 if recession occurs?

I would argue that you probably would not. In a recession, your portfolio is down, your job is at risk, and that dollar matters more. The contract pays off when marginal utility is high. This is insurance, and insurance commands a premium above the actuarially fair price.

This is not mispricing. It is the $\mathbb{P}$ to $\mathbb{Q}$ wedge at work.

## What this implies

When Kalshi's recession contract trades above economists' survey probability, commentators may say that this is miscalibration or evidence of irrational pessimism. But I would suggest this simply reflects the insurance premium embedded in bad-state contingent claims.

The testable implications are straightforward:

1. Contracts on bad-state events (recession, inflation, geopolitical crises) should trade above physical probability proxies on average
2. This wedge should widen when aggregate risk measures (VIX, credit spreads) are elevated
3. Contracts on events orthogonal to aggregate risk (sports, entertainment) should not exhibit this pattern

Distinguishing the risk premium channel from behavioral explanations is the hard part, since both predict $p > \mathbb{P}(E)$ for bad-state events. The state-dependence prediction offers some discriminating power.

## Conclusion

Even Wolfers and Zitzewitz (2006), who defend the practice of treating prices as probabilities, are careful to note that their results require assumptions about risk preferences. For macro and catastrophe events, risk neutrality is almost certainly violated. Market prices for these contracts are better understood as risk-neutral probabilities $\mathbb{Q}(E)$, which incorporate both beliefs and risk premia.

Next time someone quotes a prediction market "probability" for a recession or crisis, it is worth asking: how much of that number is belief, and how much is insurance?

---

**References**

Manski, C. F. (2006). Interpreting the predictions of prediction markets. *Economics Letters*, 91(3), 425-429.

Wolfers, J., & Zitzewitz, E. (2006). Interpreting prediction market prices as probabilities. NBER Working Paper No. 12200.

---

*This is a condensed version of a research idea I am developing. The full version involves testing whether the P-Q wedge exists empirically and varies with aggregate risk. Measuring physical probabilities turns out to be harder than it sounds, which is part of what makes this interesting.*
