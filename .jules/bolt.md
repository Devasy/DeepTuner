## 2024-10-26 - [Optimized Triplet Data Generation]
**Learning:** Replaced O(N) list comprehensions inside the training loop with O(1) dictionary lookups and rejection sampling. This reduced batch generation time by ~8x (1.27s -> 0.15s) for 20k images.
**Action:** Always check data generator loops for list comprehensions scanning the full dataset.
