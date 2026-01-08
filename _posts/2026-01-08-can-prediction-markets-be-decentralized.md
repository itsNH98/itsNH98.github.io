---
layout: single
title: "Can Prediction Markets Be Truly Decentralized?"
date: 2026-01-08
author_profile: true
---

Polymarket bills itself as a decentralized prediction market. Trades settle on-chain, contracts are non-custodial, and resolution is handled by UMA, a "decentralized oracle" where pseudonymous tokenholders vote on outcomes. The pitch is that no central authority controls the market.

I want to argue that this framing is misleading, and that the March 2025 UMA controversy illustrates why fully decentralized prediction markets may be fundamentally fragile.

## The oracle problem

A prediction market needs someone to determine whether the event actually happened. Did Trump win? Did GDP exceed 3%? Someone has to say yes or no, and the money flows accordingly.

In traditional markets like Kalshi, a regulated entity makes this determination. The incentive to resolve honestly comes from reputation, legal liability, and the desire to stay in business. In Polymarket's original design, this role was delegated to UMA tokenholders voting pseudonymously.

The problem is that pseudonymous voting breaks the reputation mechanism.

## One-shot deviations and cheap pseudonyms

Consider oracle voting as a repeated game. Let $\delta \in (0,1)$ denote the discount factor and $\pi$ the one-shot gain from misresolving a market. In a standard repeated game, cooperation can be sustained via grim-trigger strategies if the present value of continued cooperation exceeds the one-shot deviation payoff:

$$\frac{V}{1-\delta} \geq \pi$$

where $V$ is the per-period payoff from honest participation. The threat of permanent exclusion disciplines potential deviators.

But this logic requires persistent identities. In pseudonymous governance, identities are cheap. A tokenholder who manipulates a vote can sell their tokens, create a new wallet, and re-enter the game. Formally, if creating a new identity costs $c \approx 0$, then the effective discount factor for any single identity approaches zero. The repeated game collapses to a sequence of one-shot games, and the grim-trigger equilibrium unravels.

This creates a simple calculus: if the profit from misresolving a market $(\pi)$ exceeds the cost of acquiring enough voting power $(K)$, manipulation is profitable. As prediction market open interest grows, $\pi$ grows with it. The collateral staked by honest voters does not automatically scale with market size, so eventually $\pi > K$.

To their credit, UMA's own documentation [acknowledged this vulnerability](https://github.com/UMAprotocol/docs/blob/9bacee04464202ca04e65d83a2773f9a0cde6326/docs/oracle/known-issues.md), framing oracle voting as a game where rational voters compare the bribe payoff against the reward for honest participation. Their proposed mitigation was dynamic governance: tokenholders could vote to increase rewards whenever a bribery threat emerged. But this assumes the threat is observable and that governance can respond faster than attackers can act.

## March 2025: theory meets practice

In March 2025, the theory met practice. An actor known as "BornTooLate.Eth" accumulated over 1.3 million UMA tokens, becoming a top-5 token staker, and used this position to influence the resolution of a [Polymarket market on whether Ukraine would agree to give Trump administration access to rare earth minerals](https://polymarket.com/event/ukraine-agrees-to-give-trump-rare-earth-metals-before-april). The resolution was disputed, with accusations that it contradicted the platform's own guidelines. ([Coindesk coverage](https://www.coindesk.com/markets/2025/03/26/polymarket-suffers-uma-governance-attack-after-rouge-actor-becomes-top-5-token-staker))

Interestingly, nobody appears to have made much money from the attack. But the episode demonstrated the vulnerability: sufficient token accumulation can contestably influence outcomes, and the cost of doing so does not automatically scale with the value at stake.

Note that Polymarket has since moved to a system of whitelisted proposers for resolution, though it is not clear this was a direct response to the March 2025 event. Regardless, the shift effectively centralizes the oracle function. The "decentralized" prediction market now relies on a curated set of trusted resolvers.

## The irony

This is not a criticism of Polymarket. Moving to whitelisted proposers was probably the right call. The irony is that it reveals the limits of the decentralization narrative.

Fully decentralized prediction markets face a fundamental tension: the value of the market creates the incentive to attack its resolution mechanism. Without either (a) slashable collateral that scales with market size, or (b) identity-bound reputation, honest resolution is not incentive-compatible at scale.

Kalshi solves this by being a regulated, centralized entity. Polymarket effectively solved it by partially centralizing. The "decentralized prediction market" that actually works may be one that is not fully decentralized at all.

## Conclusion

None of this means prediction markets are bad or that blockchain infrastructure is useless. On-chain settlement, transparent order books, and non-custodial trading are genuine innovations. But the resolution layer, the part that determines who gets paid, seems to require some form of centralized trust or identity-bound accountability.

The question "can prediction markets be truly decentralized?" has, I think, a tentative answer: not without solving the oracle problem, and solving the oracle problem may require giving up on full decentralization.

---

*This is a blog-level treatment of an idea I decided not to pursue as a research paper. The game theory is not novel, and Polymarket's move to whitelisted proposers largely resolved the practical issue. But as a window into the tensions between decentralization and incentive compatibility, I think it is still interesting.*
