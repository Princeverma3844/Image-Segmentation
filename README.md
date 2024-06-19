# Image Segmentation Techniques: KMeans Clustering and Ratio-Cut Clustering

## Introduction
Image segmentation is a critical technique in computer vision that divides an image into distinct segments, each representing different objects or elements. This approach enhances image analysis by focusing on specific components, such as color, brightness, or texture, rather than the entire image. Image segmentation is widely used in fields like medical imaging, self-driving cars, and surveillance.

## KMeans Clustering
KMeans clustering is a valuable method for image segmentation, dividing an image into K distinct clusters based on pixel values. Here's a summary of the process:
1. **Initialization**: Pixels are randomly assigned to K clusters.
2. **Centroid Calculation**: The algorithm calculates the centroid (average value) of each cluster.
3. **Reassignment**: Pixels are reassigned to the cluster with the nearest centroid.
4. **Iteration**: Steps 2 and 3 are repeated until pixel assignments no longer change or a maximum number of iterations is reached.

**Results**: KMeans clustering effectively segments images into K regions, each represented by the color of its centroid. However, it can struggle when the optimal number of clusters is unknown or varies significantly.

## Ratio-Cut Clustering Technique
Ratio-Cut clustering is a graph-theory-based method for image segmentation. An image is conceptualized as a graph where each pixel is a node, and edges represent the similarity between pixels. The goal is to divide the graph into subgraphs (segments) using the "ratio cut" criterion, which measures the total weight of cut edges divided by the combined sizes of the subgraphs.

**Equations**: The affinity matrix is calculated using specific equations, resulting in the Laplacian matrix L = D - W, where D is the degree matrix and W is the weight matrix. Solving for the H matrix (top K eigenvalue vectors) provides features for image points.

**Results**: Ratio-Cut clustering produces segments that are internally cohesive and distinct from each other. It's effective for segments with uniform texture or color but may struggle with high image noise or varying segment sizes.

## Final Analysis
Comparing KMeans and Ratio-Cut clustering reveals distinct advantages and limitations:
- **KMeans Clustering**: Simpler and faster, suitable for images with distinct color intensities. Struggles with determining the optimal number of clusters and significant variations in cluster numbers.
- **Ratio-Cut Clustering**: More intricate and effective for uniform segments. Utilizes graph theory for cohesive subgraphs but may falter with high noise or varying segment sizes.

## Results
# K-Means
 ![image](https://github.com/Princeverma3844/Image-Segmentation/assets/123489193/90e5f3ea-dc44-4503-86b7-66941375b4ef)
# Ratio-Cut
![image](https://github.com/Princeverma3844/Image-Segmentation/assets/123489193/f3cd519d-d815-40ce-8077-9108491024dc)


