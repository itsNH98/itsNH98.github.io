---
layout: single
title: "Lottery-Linked Debt Is a Bad Deal"
date: 2026-03-18
author_profile: true
---

A new category of fintech product has emerged: lottery-linked debt overlays. The pitch is simple. You have credit card debt. You pay a monthly fee proportional to your balance. In exchange, you get a small chance each month that your entire balance gets wiped to zero. One lucky draw and you're debt-free.

Coffeezilla recently [investigated one such product](https://www.youtube.com/watch?v=julHFXsKsdQ&t=24s), and the basic math is damning. But I think the economics of why this works, and who it hurts, are worth unpacking more carefully.

## The structure

The contract is straightforward. You pay a fee each month, say some percentage of your outstanding balance. In return, with some small probability, your balance resets to zero. If you don't win, your balance evolves normally, except now you're also paying the fee on top of your regular interest.

For the platform to be a viable business, the fee must exceed the expected payout. Otherwise the company loses money on every customer. So the product is necessarily a negative expected value gamble for the borrower.

## Why anyone would take this deal

Under standard expected utility theory, no rational agent accepts a negatively expected gamble. The fee exceeds the expected benefit, full stop. So why do people sign up?

Prospect Theory offers a clean explanation. Two features matter here. First, people in the loss domain (which is where you are when you're in debt) tend to be risk-seeking rather than risk-averse. The debt feels like a loss, and you'd rather gamble on escaping it than grind through minimum payments. Second, people systematically overweight small probabilities. A tiny chance of debt freedom *feels* much larger than it is. These two features together mean that even a fully informed borrower, facing a transparently overpriced product, might still adopt it, not out of ignorance but out of preference.

## The mechanism of harm

Here is the part that I think is underappreciated. The fee doesn't just cost money. It changes the dynamics of your debt.

When you add a fee on top of your existing interest rate, your effective borrowing cost goes up. Your minimum payment stays the same, but now more of your income goes to fees, leaving less room to absorb expense shocks. The region of income realizations where you can't make your payment expands. In plain terms: the fee makes you more likely to default.

Meanwhile, the lottery almost never fires. The expected waiting time for a reset, given the probabilities these products use, is probably very long. But the expected time to default for someone already in distress is measured in months or a few years. The fee pushes you toward default long before the lottery has a realistic chance of saving you.

This creates two margins of harm. On the extensive margin, some borrowers who would have survived without the overlay now default. On the intensive margin, borrowers who survive (and never win the lottery) end up with higher balances, longer payoff times, and more total payments than they would have made otherwise.

## The asymmetry with lottery-linked savings

This is what I find most interesting from a design perspective. Lottery-linked *savings* products, where you deposit money and get a chance to win a prize, have been shown to be welfare-improving. They exploit the same probability overweighting to get people to save more, and the downside is bounded (you still have your savings, you just didn't win).

Lottery-linked *debt* products exploit the same behavioral tendencies but with the opposite welfare sign. The lottery is attached to a liability, not an asset. The fee compounds against you. The product extracts from exactly the people who are most vulnerable to the behavioral channel: those deep enough in debt to be risk-seeking.

Same psychology, opposite welfare implications. Whether a lottery overlay helps or hurts depends entirely on whether it's attached to an asset or a liability.

## What should be done

The policy question is whether these products should be regulated, and if so, how. One approach is to cap the fee-to-probability ratio. Another is to require that overlays be offered at actuarially fair prices (which would eliminate the business model). A third is outright prohibition.

I lean toward thinking that prohibition is the right answer for products where the fee substantially exceeds the expected payout and the target market is distressed borrowers. The behavioral channel that drives adoption is strongest precisely where the harm is greatest. Disclosure doesn't help when the adoption decision is preference-driven rather than information-driven. Telling someone the odds are bad doesn't change the fact that, from the loss domain, the gamble feels worth taking.

---

*This post is based on a theoretical analysis I wrote exploring the welfare properties of lottery-linked debt overlays under Prospect Theory preferences. TLDR: the fee kills you before the lottery saves you.*
