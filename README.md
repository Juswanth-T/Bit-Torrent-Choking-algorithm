# BitTorrent Choking Algorithm - Game Theory Perspective

## Choking Algorithm

The **choking algorithm** determines which peers to upload to based on their recent download rates. Key aspects include:

- **Unchoking Limit:** Peers unchoke 4 other peers at a time (by default).
- **Download Rate Measurement:** Download rates are measured using a 20-second average.
- **Peer Selection:** Peers are selected for unchoking based on their upload contributions.

## Game Theory Analysis

The repository includes a game-theoretic analysis of peer strategies. The utility function for a peer is defined as:

$u_i(\mu_i) = d_i(\mu_i, \mu_{-i}) - c(\mu_i)$

Where:
- $d_i $: Download rate
- $\mu_i $: Upload bandwidth of peer \( i $
- $c(\mu_i)$: Cost function for uploading

## Nash Equilibrium

The analysis demonstrates:
- **Heterogeneous Groups:** A Nash equilibrium may not exist when peers have different physical upload bandwidths.
- **Homogeneous Groups:** Convergence to Nash equilibrium is possible when peers have identical bandwidths.

## Simulation

This repository includes simulation code to demonstrate the behavior of the choking algorithm under various scenarios:
- **Heterogeneous Peer Bandwidths**
- **Homogeneous Peer Groups**

## Conclusion

The **BitTorrent choking algorithm** effectively balances:
- **Fairness:** Incentivizes users to contribute bandwidth.
- **Speed:** Optimizes connection efficiency.

This approach ensures a robust and efficient peer-to-peer file-sharing network. 
