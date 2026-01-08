---
layout: single
title: "Prediction Markets Aren't Free"
date: 2026-01-09
author_profile: true
---

A common defense of prediction markets goes something like this: trading is zero-sum, so there is no social cost. Money just moves from wrong people to right people. The market aggregates information, prices converge to truth, and everyone benefits from better forecasts.

I want to push back on this. Even when trading is zero-sum, prediction markets have real costs. Whether those costs are justified depends on what decisions the markets actually inform.

## The zero-sum fallacy

It is true that for every dollar won, a dollar is lost. But this does not mean prediction markets are welfare-neutral. There are at least three categories of cost that the zero-sum framing ignores.

**Real resource costs.** Platforms spend money on liquidity subsidies, rewards programs, and infrastructure. Traders spend time and effort acquiring information. These are real resources that could be deployed elsewhere. Even if the trading itself nets to zero, the ecosystem around it does not.

**Information acquisition costs.** When informed traders profit, they are compensated for costly research. These costs are real, even if they do not show up on any balance sheet.

**Regressive transfers under concave utility.** This is the one I find most interesting, and the one that gets least attention.

## Gambling harm is not about net transfers

Suppose trading is literally zero-sum: aggregate profits equal aggregate losses. Under linear utility, this is welfare-neutral. But utility is not linear. Under any concave utility function, a dollar matters more to someone with less wealth than to someone with more.

This has a striking implication. If prediction markets systematically transfer wealth from less-skilled (or less-wealthy) traders to more-skilled (or more-wealthy) traders, aggregate welfare falls even though aggregate wealth is unchanged. The transfers themselves are harmful.

To see this formally, consider CRRA utility $u(w) = \frac{w^{1-\gamma}}{1-\gamma}$ with risk aversion $\gamma > 0$. A mean-preserving spread in the wealth distribution, holding total wealth constant, reduces total utility. If prediction markets increase wealth dispersion, they reduce welfare under this measure, even with zero fees and zero-sum trading.

This is the same logic that makes regressive taxation harmful and progressive taxation (potentially) beneficial. It is not about the total size of the pie. It is about how the pie is distributed, and how much each slice matters to its holder.

## Who loses in prediction markets?

The empirical question is whether prediction markets actually produce regressive transfers. The evidence, though limited, suggests they do. Polymarket's leaderboards show persistent winners, while losses are dispersed across a larger number of smaller traders. 

This pattern is not surprising. Prediction markets reward information and sophistication. Those with better models, faster data, or larger bankrolls have systematic advantages. Retail participants, trading on vibes or entertainment value, tend to lose.

Even if informed traders merely break even after accounting for their research costs, the retail traders still lose. Their losses fund the information acquisition that makes prices accurate. This is the real cost of information aggregation: someone has to pay for the research, and in prediction markets, it is the less-informed participants.

If utility is concave, this transfer is welfare-reducing. A hundred retail traders each losing $100 experience more aggregate utility loss than a sophisticated trader gains from $10,000 that merely covers their research costs. The market "works" in the sense that prices are accurate, but the cost of that accuracy falls disproportionately on those least able to bear it.

## When are prediction markets worth it?

None of this means prediction markets are bad. It means they are costly. The question is whether the benefits justify the costs.

The benefit of a prediction market is improved forecast accuracy. If the market price is more accurate than available alternatives, and if that accuracy informs valuable decisions, then the market creates social value.

This suggests a simple framework: prediction markets are justified when the value of improved forecasts exceeds the real resource costs plus the welfare cost of regressive transfers.

For some markets, this test is easy to pass. Election forecasts inform campaign strategy, media coverage, and policy expectations. Recession probabilities inform investment and hiring decisions. If prediction markets improve these forecasts even modestly, the decision stakes are large enough to justify substantial costs.

For other markets, the test is harder. Sports betting markets are highly accurate, but what decisions do they inform? Entertainment value is real, but it is not clear that society needs a more precise probability that the Chiefs beat the Ravens. The costs, including gambling harm and wealth transfers from recreational bettors to sharps, may well exceed the benefits.

## The taxonomy

This gives us a way to think about prediction markets that goes beyond "good" or "bad":

**Truth engines:** Markets where improved forecasts inform high-stakes decisions. Election markets, macro forecasts, geopolitical risk. The accuracy gains might justify the costs.

**Costly entertainment:** Markets where accuracy is high but decision stakes are low. Sports, entertainment awards, reality TV outcomes. The costs may not be justified, but the harm is limited.

**Casinos with a price chart:** Markets where accuracy gains are minimal, decision stakes are low, and the primary activity is gambling. The social cost exceeds the social benefit.

The same platform can host all three types of markets. Polymarket's election coverage is plausibly a truth engine. Its sports markets are probably costly entertainment. Some of its more obscure markets may be casinos with price charts.

## Conclusion

The claim that prediction markets are "free" because trading is zero-sum is wrong. Real resource costs exist. Information acquisition is costly. And if you believe utility is concave, wealth transfers from losing traders to winning traders are intrinsically harmful, even when they net to zero.

Whether prediction markets are socially valuable depends on whether their accuracy gains justify these costs. For high-stakes decisions, they probably do. For pure entertainment, the case is weaker. The useful question is not "are prediction markets good?" but "which prediction markets are worth their costs?"

---

*This is a blog-level treatment of an idea that did not survive as a research paper. The welfare framework is real, but the empirical inputs (information costs, wealth effects, decision stakes) are hard to measure. As a way of thinking about the problem, I still find it useful.*
