https://colab.research.google.com/drive/1V2okeCiDhD_y9lZDvPZOE1qgB_xbEL2M?usp=sharing

# Anomaly Detection Models Configuration and Performance

## Model Parameters

Below are the configurations for different anomaly detection models:

| Model | Anomaly Count | Parameters |
|-------|---------------|------------|
| ABOD | 0 | contamination=0.05, method=fast, n_neighbors=5 |
| Cluster | 50 | alpha=0.9, beta=5, check_estimator=False, clustering_estimator=None, contamination=0.05, n_clusters=8, n_jobs=None, random_state=123, use_weights=False |
| COF | 50 | contamination=0.05, method=fast, n_neighbors=20 |
| IForest | 50 | behaviour=new, bootstrap=False, contamination=0.05, max_features=1.0, max_samples=auto, n_estimators=100, n_jobs=-1, random_state=123, verbose=0 |
| Histogram | 50 | alpha=0.1, contamination=0.05, n_bins=10, tol=0.5 |
| KNN | 46 | algorithm=auto, contamination=0.05, leaf_size=30, method=largest, metric=minkowski, metric_params=None, n_jobs=-1, n_neighbors=5, p=2, radius=1.0 |
| LOF | 46 | algorithm=auto, contamination=0.05, leaf_size=30, metric=minkowski, metric_params=None, n_jobs=-1, n_neighbors=20, novelty=True, p=2 |
| SVM | 50 | cache_size=200, coef0=0.0, contamination=0.05, degree=3, gamma=auto, kernel=rbf, max_iter=-1, nu=0.5, shrinking=True, tol=0.001, verbose=False |
| PCA | 50 | contamination=0.05, copy=True, iterated_power=auto, n_components=None, n_selected_components=None, random_state=123, standardization=True, svd_solver=auto, tol=0.0, weighted=True, whiten=False |
| MCD | 50 | assume_centered=False, contamination=0.05, random_state=123, store_precision=True, support_fraction=None |

## Clustering Performance

Performance metrics for KMeans and Hierarchical clustering:

| Model | Anomaly Count | KMeans Clusters | KMeans Silhouette | Hierarchical Clusters | Hierarchical Silhouette |
|-------|---------------|-----------------|-------------------|----------------------|------------------------|
| ABOD | 0 | 2 | 0.2097 | 2 | 0.2027 |
| Cluster | 50 | 2 | 0.2258 | 2 | 0.2232 |
| COF | 50 | 2 | 0.2248 | 2 | 0.2227 |
| IForest | 50 | 3 | 0.2128 | 2 | 0.2181 |
| Histogram | 50 | 3 | 0.2150 | 2 | 0.2174 |
| KNN | 46 | 2 | 0.2246 | 2 | 0.2221 |
| LOF | 46 | 2 | 0.2248 | 2 | 0.2221 |
| SVM | 50 | 3 | 0.2088 | 2 | 0.2118 |
| PCA | 50 | 3 | 0.2092 | 2 | 0.2097 |
| MCD | 50 | 2 | 0.2250 | 2 | 0.2140 |
