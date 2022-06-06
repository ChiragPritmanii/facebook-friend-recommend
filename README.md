# Facebook Friend Recommend
Given a pair of user ids, predict whether a directed link should be present from one user to the other.
- Domain : Social Media
- Type of problem: Binary Classification
- Objective: Given a pair of user ids, predict whether a directed edge should be present from one user to the other.
- Performance Metric: Improve the F1 Score.
- Solution:
1. Given 9.43 Million pairs of users which have a directed edge present between them.
2. Generated 9.43 Million new pairs of users from the same set of users provided, such that these
3. pairs represent no directed edge between them to balance the dataset.
4. Generated graph features like Jaccard, Cosine, Adar, Katz, Page Rank, Preferential Attachment,
5. SVD and more using the subgraph created from the pairs with links (i.e. pairs with directed edges) in the train data. Majorly utilized Nerworkx for graph operations and Modin with Ray as backend for faster dataframe operations during featurization.
5. Built a Light GBM model which achieved an F1 Score of 0.879.
- Utilized Google Cloud Platform (GCP) Compute Engine for memory intensive tasks.
