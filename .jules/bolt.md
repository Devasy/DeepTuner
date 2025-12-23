## 2024-05-23 - [O(N) to O(1) Data Generator Sampling]
**Learning:** In ML data generators, naive list comprehensions inside the `__getitem__` loop can be disastrous for performance. Specifically, filtering a large dataset (`N` items) to find samples of a specific class for every item in a batch results in `O(N * batch_size)` complexity.
**Action:** Always pre-compute a `label -> [indices]` map (index) during initialization or after shuffling. This allows O(1) sampling of positive/negative pairs, reducing per-batch complexity to `O(batch_size)`.
