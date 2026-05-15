# Test data for custom/clustering, clustermetrics and clustervisualization modules

Minimal hand-rolled test files used by the following custom modules:
- `custom/clustering`
- `custom/clustermetrics`
- `custom/clustervisualization`

**Files:**
- `test.eigenvec`      : small example PCA output (200 samples)
- `test_clusters.csv`  : example cluster assignments (KMeans + DBSCAN)
- `test_features.tsv`  : example feature matrix for clustering

These files are **hand-rolled minimal examples** created specifically for testing the input format parsing of the modules (technical validity only, as per precedent in PR #2049).

No biological interpretation should be inferred from the values.
