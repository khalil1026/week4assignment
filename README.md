# week4assignment

from sklearn.cluster import KMeans
import numpy as np


features = data_normalized[:, :-1]  # 去掉最后一列的 flag


features = features[~np.isnan(features).any(axis=1)]


kmeans = KMeans(n_clusters=2, random_state=42)
labels = kmeans.fit_predict(features)


class_1_mean = features[labels == 0].mean(axis=0)
class_1_std = features[labels == 0].std(axis=0)

class_2_mean = features[labels == 1].mean(axis=0)
class_2_std = features[labels == 1].std(axis=0)

print("Class 1 Mean:", class_1_mean, "Std Dev:", class_1_std)
print("Class 2 Mean:", class_2_mean, "Std Dev:", class_2_std)

Class 1 Mean: [-0.30438413 -0.40355842] Std Dev: [0.78820352 0.3794673 ]
Class 2 Mean: [1.29340343 1.69680428] Std Dev: [0.63829634 0.98187561]
