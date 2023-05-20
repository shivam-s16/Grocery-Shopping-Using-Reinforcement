# RL-For-Grocery-Shopping

## Introduction

This project aims to simplify the process of monthly grocery shopping by leveraging reinforcement learning techniques. The goal is to find the optimal strategy for purchasing a list of items from different stores with varying prices, availability, and associated travel costs. The project explores various reinforcement learning algorithms to develop an agent that learns the best sequence of shop visits to minimize both time and cost.


## Problem Statement

When it comes to monthly grocery shopping, multiple store options with different pricings, item availabilities, and travel costs are involved. This project addresses this complexity using reinforcement learning to determine the most effective strategy for purchasing the required items.

## Objectives

- Simplify the grocery shopping process by automating decision-making.
- Develop an agent that learns the optimal sequence of shop visits to buy all the items.
- Minimize both the time taken and the cost associated with travel and shopping.


### Environment Components

- `shops`: List of available stores (S1, S2, ..., Sn).
- `buying_status`: List indicating whether each item (I1, I2, ..., Im) has been bought (Y) or not (N).
- `States`: Set of possible states representing the current shop and buying status.
- `State Space`: Combination of shops and item buying statuses (n * 2^m possibilities).
- `Actions`: Available actions representing shops.

### Transition Probabilities and Rewards (for 1 item to buy)

1. If the item has been bought, the session terminates.
2. If choosing to try the same shop again:
   - If the item is found:
     - Reward: Buying reward + Distance penalty + Price penalty
   - If the item is not found:
     - Reward: Distance penalty
3. If choosing to go to another shop:
   - If ending up in the chosen shop:
     - If the item is found:
       - Reward: Buying reward + Distance penalty + Price penalty
     - If the item is not found:
       - Reward: Distance penalty
   - If ending up in a shop not chosen:
     - If the item is found:
       - Reward: Buying reward + Distance penalty + Price penalty
     - If the item is not found:
       - Reward: Distance penalty

## Conclusion

The RL-For-Grocery-Shopping-Solutions project addresses the challenges of optimizing grocery shopping using reinforcement learning techniques. By developing and applying these algorithms, the project aims to provide a solution that simplifies the decision-making process for consumers, helping them save both time and money during their monthly grocery shopping.

