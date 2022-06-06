# Facebook Friend Recommend
Given a pair of user ids, predict whether a directed link should be present from one user to the other.
- Domain : Social Media
- Type of problem: Binary Classification
- Objective: Given a pair of user ids, predict whether a directed edge should be present from one user to the other.
- Performance Metric: Improve the F1 Score.
- Solution:
1. Given 9.43 Million pairs of users which have a directed edge present between them. E.g. Pair 1 = (U2, U12) such that U2 -> U12 (not necessary that U12 -> U2)
2. Generated 9.43 Million new pairs from the same set of users provided, such that none of these pairs have a directed edge between them, this is done to balance the dataset.
3. Performed Stratified Splitting to obtain train and test sets such that both the sets have balanced class distribution (i.e. Number of linked pairs = Number of unlinked pairs).
4. Generated graph features like Jaccard, Cosine, Adar, Katz, Page Rank, Preferential Attachment, SVD and more using the subgraph created from the linked pairs in the train data. Majorly utilized Nerworkx for graph operations and Modin with Ray as backend for faster dataframe operations for feature engineering.
5. Built and tuned a Light GBM model which achieved an F1 Score of 0.93 and AUC of 0.95.
- Utilized Google Cloud Platform (GCP) Compute Engine for memory intensive tasks.
