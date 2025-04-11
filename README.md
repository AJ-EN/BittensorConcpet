# Bittensor Explained: Web Page & Simulation

## Description

This project provides an interactive web page designed to help understand the core concepts of the Bittensor network, as described in the original whitepaper ("Bittensor: A Peer-to-Peer Intelligence Market" by Yuma Rao). It includes:

1.  An **Explanation Tab:** Breaks down key ideas like peer-to-peer intelligence markets, stake, weights, trust, incentives, and collusion resistance into easy-to-understand sections.
2.  A **Simulation Tab:** A simplified, visual simulation demonstrating how peers might rank each other, how stake (influence) is distributed based on trust and incentives, and how the system aims to resist manipulation by colluding groups ('cabals').

## Features

* **Dual Tabs:** Easily switch between a conceptual explanation and an interactive simulation.
* **Clear Explanations:** Uses simple language and analogies to explain complex Bittensor mechanics.
* **Interactive Simulation:**
    * Visualize peers, their stake, and their voting patterns (weights).
    * Run the simulation step-by-step or automatically.
    * Observe how stake distribution changes based on simplified Rank, Trust, and Incentive calculations.
    * See the effect of a 'cabal' (colluding group) on the network dynamics.
    * Hover over peers to highlight their outgoing votes.
    * Simulation log detailing calculations per round.
* **Responsive Design:** Basic responsiveness for viewing on different screen sizes.

## How to Use

1.  Clone or download the repository.
2.  Open the `bittensor_explainer.html` file (or whatever you have named the main HTML file) directly in your web browser (like Chrome, Firefox, Safari, Edge).
3.  No installation or build steps are required.

## Simulation Details

The simulation provides a *simplified* model of the Bittensor incentive mechanism:

* **Peers:** Represented as nodes in a network.
* **Stake (S):** Numerical value and bar indicating influence. Initial stake is distributed evenly.
* **Weights (W):** Peers assign weights to others. Honest peers slightly favor trusted/high-stake peers; Cabal peers only vote internally. Visualized as lines on hover.
* **Rank (R):** Calculated based on the stake-weighted sum of incoming weights.
* **Trust (T):** Simplified calculation based on whether a peer receives votes from a majority (>50%) of the network's stake (using a sigmoid function for smoothing).
* **Incentive (I):** Calculated simply as `Rank * Trust`.
* **Inflation:** New stake is introduced each round and distributed proportionally based on each peer's Incentive score.
* **Cabal:** A small group of peers (marked red) that only vote for each other, demonstrating the collusion resistance mechanism (they struggle to gain influence without broad network trust).

**Note:** This simulation is for educational purposes to illustrate the *concepts* and does not replicate the full complexity or exact mathematical formulas of the actual Bittensor network.

## Technologies Used

* HTML
* CSS (Tailwind CSS via CDN)
* JavaScript (Vanilla JS for simulation logic and interactivity)

## Source Concept

This explanation and simulation are based on the concepts presented in the Bittensor whitepaper:
* Rao, Y. (n.d.). *Bittensor: A Peer-to-Peer Intelligence Market*. [www.bittensor.com](https://bittensor.com/whitepaper) (or link to the specific PDF if available).

