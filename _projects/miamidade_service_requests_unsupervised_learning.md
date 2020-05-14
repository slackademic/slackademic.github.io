---
title: 'Analyzing Government Service Requests in Miami-Dade County Via Unsupervised Learning'
subtitle:
date: 2020-05-03 00:00:00
description: This page previews my unsupervised learning project analyzing 311 service requests in Miami-Dade County.
featured_image: '/images/miamidade/clusters.png'
---

<img src="/images/miamidade/clusters.png" width="600" height="600" align="center">


## Summary

I investigate how local governments segment their constituents through servicing their demands for public services. Using a dataset of 311 service requests from [Miami-Dade County's Open Data Hub](https://gis-mdc.opendata.arcgis.com/datasets/311-service-requests-miami-dade-county-2019), I looked for patterns among a number of important features measuring variation in constituents' socioeconomic statuses, community-level civic engagement, types of services requested, length of projects, and geography. I used several unsupervised clustering algorithms (K-means, DBSCAN, Gaussian Mixture Models) to group the data and then explored the clusters produced by the best performing algorithm, using Silhouette Scores as a metric. The dataset had 319,855 service requests from county residents as of January 2020. The plot above shows a PCA two-dimensional plot of a K-means 2 cluster solution of the data (the best performing algorithm).

The project's Jupyter Notebook is [here](https://nbviewer.jupyter.org/github/slackademic/Projects/blob/master/unsupervised_learning_capstone.ipynb), but in the meantime, below you may see a series of descriptive plots of features used in the analysis and plots exploring the clusters from the K-Means two cluster solution.

### Miami-Dade 311 Service Requests Descriptive Plots

<div class="gallery" data-columns="2">
	<img src="/images/miamidade/requesttypes.png">
	<img src="/images/miamidade/histograms.png">
	<img src="/images/miamidade/requestsbyschooldistrict.png">
	<img src="/images/miamidade/requeststatus.png">
	<img src="/images/miamidade/requestsbymethod.png">
</div>

### Service Request Clusters
- I compared K-Means, DBSCAN, and Gaussian Mixture Models and a range of values for K (number of clusters) to find the highest performing cluster solution.
- Silhouette Scores were the performance metric.
- K-Means 2 Cluster Solution was the best performer. Below is a plot of a the K-Means 2 cluster solution after using PCA to reduce the data to two dimensions.

<img src="/images/miamidade/kmeans2clusters.png" width="600" height="600" align="center">

### Exploring The Two Clusters

<div class="gallery" data-columns="1">
	<img src="/images/miamidade/taxesvotersperformancebycluster.png">
	<img src="/images/miamidade/projectlengthbycluster.png">
	<img src="/images/miamidade/requesttypesbycluster.png">
	<img src="/images/miamidade/methodreceivedbycluster.png">
	<img src="/images/miamidade/projectstatusbycluster.png">
</div>
