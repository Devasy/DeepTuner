## 2024-05-22 - [Optimizing Triplet Data Generation]
**Learning:** Naive data sampling in triplet loss generators can lead to O(N^2) complexity per epoch if not careful. Specifically, iterating through the entire dataset to find positive/negative samples for each anchor is extremely expensive.
**Action:** Use a hash map (dictionary) to pre-group data by class labels. This allows O(1) sampling for positive/negative pairs, drastically reducing data loading overhead.
