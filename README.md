# Network Community Detection and Comparison

This repository contains Python code to perform community detection on a network using different algorithms, such as Louvain, Infomap, and Label Propagation. The detected communities are then compared using evaluation metrics. The code utilizes various Python libraries for network analysis and visualization.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Functions](#functions)
- [Community Detection Algorithms](#community-detection-algorithms)
- [Comparing Communities](#comparing-communities)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Community detection is an essential task in network analysis that involves identifying groups of nodes within a network that are more densely connected to each other than to nodes outside those groups. This repository demonstrates how to perform community detection using different algorithms and evaluate the quality of detected communities using evaluation metrics.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/4Pranjal/network-community-detection.git
   cd network-community-detection
   ```

2. Install required libraries:
   ```bash
   pip install python-louvain networkx leidenalg matplotlib python-igraph scikit-learn
   ```

3. Upload your network file (e.g., `airports_UW.net`) to the repository directory.

## Usage

1. Open the Python script `community_detection_comparison.py` in your preferred Python environment.
2. Replace `file_path` with the path to your uploaded network file.
3. Run the script to perform community detection, visualization, and comparison.

## Functions

Several utility functions are defined to facilitate community detection and evaluation:

- `read_pajek(file_path)`: Reads a network from a Pajek file and returns a NetworkX graph.
- `plot_communities(G, partition, title)`: Plots detected communities on the network graph.
- `jaccard_index(true_partition, pred_partition)`: Computes the Jaccard index to compare community similarity.
- `normalized_mutual_information(true_partition, pred_partition)`: Computes normalized mutual information for community comparison.
- `adjusted_rand_index(true_partition, pred_partition)`: Computes adjusted Rand index for community comparison.
- `modularity(G, partition)`: Computes the modularity of a partition in the graph.

## Community Detection Algorithms

Three community detection algorithms are implemented:

1. **Louvain Method (`apply_louvain`):**
   - Uses the Louvain algorithm to detect communities in the network.
   - Returns a partition of nodes.

2. **Infomap (`apply_infomap`):**
   - Uses the Infomap algorithm to detect communities in the network.
   - Returns a partition of nodes.

3. **Label Propagation (`apply_label_propagation`):**
   - Uses the Label Propagation algorithm to detect communities in the network.
   - Returns a partition of nodes.

## Comparing Communities

Detected communities are compared using the following metrics:

- **Jaccard Index:** Measures the similarity of communities based on shared nodes.
- **Normalized Mutual Information:** Measures the amount of information shared between communities.
- **Adjusted Rand Index:** Measures the similarity of communities, considering all pairs of nodes.

## Contributing

Contributions to improve code functionality, add new algorithms, or enhance the documentation are welcome. Here's how you can contribute:

1. Fork the repository.
2. Create a new branch.
3. Make your improvements.
4. Open a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
