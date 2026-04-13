# Yahtzee
Notebook-driven final project for Probabilistic Systems Analysis that uses dynamic programming and multinomial distributions to build a Yahtzee-playing agent. Final paper titled "EE104..." analyzes performance of Yahtzee-playing agent when using dp-generated state-space vs a greedily generated space. 

## What the project does

- Represents Yahtzee rolls as count vectors instead of ordered dice.
- Enumerates all reachable count states for 5 dice.
- Uses multinomial probabilities to evaluate reroll outcomes.
- Builds per-category policies with dynamic programming.
- Simulates full Yahtzee games using the precomputed policies.

## Repository layout

- DataPreparation.ipynb: Generates state-space, which stores the probability mass function at all unique positions in the game in a matrix, for both the DP and greedy approach.
- EE104 Probablistic Systems Analysis Final Paper.pdf - Doran Tavrow: Submitted paper containing data collected from Yahtzee agent
- Yahtzee.ipynb: Contains Yahtzee class that runs user-inputted number of games
- graphing.ipynb: Notebook used to prepare graphs for paper

## Folder layout

- all_greedy: contains pmfs for greedy agent
- all_DP: contains pmfs for DP agent
- graphing_data: contains Yahtzee.ipynb results for 10,000 simulated games using all_greedy and all_DP

## Limitation
The state-spaces are generated independently for each category instead of solving the full 13-turn Yahtzee game optimally.
