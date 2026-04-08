---
layout: single
title: "Free Information Increases Inequality"
date: 2026-03-18
author_profile: true
---

There is a natural intuition that making information cheaper should level the playing field. If everyone has access to the same polls, the same news, the same data, then nobody has an unfair advantage. Markets should become more equal.

I think the opposite is true, and prediction markets offer a clean place to see why.

## The mechanism

When information is expensive, unsophisticated participants occasionally get lucky. They stumble onto the right side of a trade by chance. The information asymmetry is real, but randomness gives the little guy a shot.

When information becomes free, that randomness disappears. Everyone knows the polls. Everyone has read the same analysis. The easy edge is gone. Competition shifts from "who has the information" to "who can interpret it faster and act on it first." That is a game the sophisticated always win.

Free information eliminates the amateur's only advantage, which was luck. What remains is a pure contest of speed, capital, and interpretation skill. The result is more concentration of returns, not less.

This is the core prediction of Mihet (2020), who formalizes this in a model of financial technology and inequality: reducing information costs shifts the Lorenz curve downward and increases the Gini coefficient.

## Prediction markets as a laboratory

Prediction markets are unusually well suited to testing this. Unlike equity markets, you can observe wallet-level profit and loss for every trader. Outcomes are binary, so there is no ambiguity about who was right. And there is natural variation in how freely available information is across different categories of markets.

Consider two categories on Polymarket: elections and sports.

Election markets are flooded with free information. Polls are public. Aggregators like FiveThirtyEight and Silver Bulletin synthesize everything. News coverage is constant. Anyone can form a reasonable view on the presidential race without paying for anything.

Sports markets are different. Useful information, such as injury reports, matchup analysis, and line movement, exists but is more dispersed and harder to aggregate. The information cost is higher. There is still an edge to be had from simply knowing more.

If Mihet is right, election markets should show *higher* inequality than sports markets, not lower. The abundance of free election information should push competition onto speed and interpretation, concentrating returns among the most sophisticated traders. Sports markets, where information is less democratized, should have more room for amateurs to get lucky.

In ongoing work with coauthors, I have been computing concentration metrics across Polymarket categories. The pattern is consistent with the prediction. Gains in election markets are substantially more concentrated at the top than in sports or crypto markets. The top sliver of election traders captures a larger share of total profits than the equivalent sliver in categories where information is harder to come by. Crypto markets, where edges tend to come from private or insider-type knowledge rather than public data, show the least concentration.

This is not a formal test of Mihet, and there are many confounds (volume differences, market structure, trader composition). But the gradient is in the right direction: more free information, more concentration.

## The speed channel

If this mechanism is real, it should show up in how quickly traders act after public information arrives. When a major poll drops for an election market, the first traders to react capture the price adjustment. Latecomers get nothing. Returns should be strongly correlated with speed of execution.

In sports markets, where the information edge is less about public data and more about private knowledge, speed should matter less. The profitable trades are the ones based on information that others simply do not have, not on reacting faster to information everyone can see.

## What this implies

The uncomfortable implication is that information democratization in financial markets may be regressive. Making data free and accessible sounds egalitarian, but in practice it strips away the one thing that kept markets somewhat equal: noise. When the noise is gone, skill and infrastructure dominate, and the distribution of returns becomes more concentrated.

This does not mean we should restrict information. But it does mean we should be skeptical of the claim that transparency and data access automatically benefit small participants. In a market where everyone sees the same thing, the advantage goes to whoever can process it best, and that is almost never the retail trader.

---

*This post is based on a research idea exploring Mihet's (2020) prediction using Polymarket data, where wallet-level PnL and cross-category variation in information availability provide unusually clean conditions for testing whether free information really does increase inequality.*
