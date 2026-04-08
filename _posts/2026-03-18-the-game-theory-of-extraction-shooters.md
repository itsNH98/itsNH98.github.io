---
layout: single
title: "The Game Theory of Extraction Shooters"
date: 2026-03-18
author_profile: true
---

I have been playing a lot of ARC Raiders in my spare time. It is an extraction shooter, a genre where you load into a map, gather loot, fight AI enemies, run into other players, and try to extract alive. If you die, you lose your gear. Escape from Tarkov and Hunt: Showdown are the other big names in the space.

After enough raids, you start to notice a pattern. Early in a game's life, encounters with other players are unpredictable. Sometimes they wave and move on. Sometimes they shoot. Over time, though, almost every encounter becomes a gunfight. The game gets sweatier, the casual players leave, and the lobbies turn hostile. Game theory has something to say about why this happens.

## The defect premium

Think of each encounter as a one-shot game. You can cooperate (leave the other player alone) or defect (shoot first). The payoff difference between defecting and cooperating is what I call the defect premium.

The key insight is that the defect premium increases with the aggressiveness of the lobby. When you expect most other players to shoot on sight, cooperation is dangerous. You're exposed to ambush with no way to recover your gear. Shooting first becomes self-insurance. Even if you would prefer a peaceful raid, the rational response to a hostile lobby is to be hostile yourself.

This creates a feedback loop. Some players defect. Risk-averse players experience high loss variance and start quitting. The remaining population is more aggressive on average. The defect premium rises. More players defect. The lobby becomes a "swamp," where every encounter is a gunfight and the extraction loop reduces to pure PvP with extra steps.

## The empirical pattern

You can see this play out in Steam concurrent player data across extraction titles. The typical pattern is a steep decline in the first few months after launch, often losing half or more of the player base. Some games stabilize at a smaller but sustainable level. Others collapse to near-zero and shut down.

The Cycle: Frontier is the clearest collapse case. Its developers explicitly identified cheating as the key driver, which in this framework is an extreme fairness shock that spikes the defect premium far beyond what normal PvP produces. When encounters feel not just risky but unfair, the feedback loop accelerates.

Games that survive tend to do one of two things. Either they add PvE modes that let risk-averse players enjoy the extraction loop without forced PvP exposure (Tarkov, Eldegarde), or they implement behaviour-based matchmaking that tries to separate aggressive players from passive ones (ARC Raiders).

## Why matchmaking is hard

ARC Raiders is running the most interesting experiment right now. Their developers describe tracking "who shoots first" and using that signal to sort players into lobbies. The idea is to create two effective environments within a single game mode: one where players mostly cooperate, and one where players mostly fight.

In theory, this is an endogenous two-equilibrium solution. The matchmaker doesn't impose a hard split. It nudges the population toward self-sorting based on revealed behaviour, so that aggressive players face other aggressive players and casual players get breathing room.

In practice, the matchmaker faces a tradeoff between sorting precision and queue times. To keep queues reasonable, the system must widen its tolerances. This means occasional aggressive players leak into casual lobbies. It only takes a small probability of encountering a defector to raise the perceived risk sharply for loss-averse players. The system helps, but it cannot perfectly separate the two equilibria.

The developers themselves call it "a blunt instrument."

## Design levers

The extraction genre's fundamental challenge is managing the defect premium. Several design levers work through this lens:

Reducing the payoff from predation. If killing another player yields less loot, the incentive to shoot first drops. Some games limit what can be taken from killed players.

Reducing loss severity. Insurance systems, buyback mechanics, and softened death penalties lower the variance that drives risk-averse players out. This keeps the casual population in the game longer, which slows the selection spiral.

Reducing the initiative advantage. Better audio cues, longer time-to-kill, and disengage mechanics give the cooperating player a chance to survive even when ambushed. If defecting isn't a guaranteed win, its expected value drops.

Adding PvE pressure valves. Separate PvE modes or PvE-heavy events let risk-averse players engage with the extraction loop without the PvP variance. This retains a population segment that would otherwise churn entirely.

## Why this matters beyond games

The extraction shooter is a clean real-world instance of a tipping game with endogenous composition. The population isn't fixed. Players enter and exit based on their experience, and that entry/exit changes the environment for everyone else. The result is that a game can tip from a mixed, interesting social environment into a hostile monoculture, not because of any single design failure, but because of the feedback between individual incentives and population composition.

The same structure appears in other settings. Markets where informed traders drive out uninformed participants. Neighbourhoods where certain residents leave and change the character of the community. Platforms where toxic users drive away moderate ones. The extraction shooter is just a particularly visible and data-rich instance of the general phenomenon.

---

*This post draws on a more detailed analysis using Steam telemetry data across seven extraction titles. The short version: when shooting first is self-insurance, everyone ends up shooting first.*
