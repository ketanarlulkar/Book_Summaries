Notes from [A Programmer's Guide to Data Mining](http://guidetodatamining.com/)

# Chapter 2: Collaborative filtering
## _I like what you like_

### 1. If your data is dense (almost all attributes have non-zero values) and the magnitude of the attribute values is important, use distance measures such as Euclidean or Manhattan.
- Manhattan Distance -> Fast computation
- Euclidean Distance (Pythagorean Theorem) -> Slow computation
#### Minkowski Distance Metric
  <p align="center">
    <img src="https://latex.codecogs.com/svg.latex?d%28x%2Cy%29%20%3D%20%28%5Cdisplaystyle%5Csum%5Climits_%7Bk%3D1%7D%5En%20%7Cx_%7Bk%7D-y_%7Bk%7D%7C%5E%7Br%7D%29%5E%7B1/r%7D">
  </p>
  <dt>When</dt>
  <dt>r = 1: The formula is Manhattan Distance</dt>
  <dt>r = 2: The formula is Euclidean Distance</dt> 
<br />

### 2. If the data is subject to grade-inﬂation (different users may be using different scales) use Pearson's R.
  <p align="center">
    <img src="https://latex.codecogs.com/svg.latex?r%20%3D%20%5Cfrac%7B%5Cdisplaystyle%5Csum%5Climits_%7Bk%3D1%7D%5En%20%28x_%7Bi%7D-%5Cbar%7Bx%7D%29%28y_%7Bi%7D-%5Cbar%7By%7D%29%7D%7B%5Csqrt%7B%5Csum%5Climits_%7Bk%3D1%7D%5En%28x_%7Bi%7D-%5Cbar%7Bx%7D%29%5E2%7D%5Csqrt%7B%5Csum%5Climits_%7Bk%3D1%7D%5En%28y_%7Bi%7D-%5Cbar%7By%7D%29%5E2%7D%7D">
  </p>

### 3. If the data is sparse consider using Cosine Similarity.
  <p align="center">
    <img src="https://latex.codecogs.com/svg.latex?cos%28x%2Cy%29%20%3D%20%5Cfrac%7Bx.y%7D%7B%5Cleft%20%5C%7C%20x%20%5Cright%20%5C%7C%5Ctimes%20%5Cleft%20%5C%7C%20y%20%5Cright%20%5C%7C%7D">
  </p>
  Where, . indicate dot product and ||x|| indicates the length of the vector x, calculated as
  <p align="center">
    <img src="https://latex.codecogs.com/svg.latex?%5Cleft%20%5C%7C%20x%20%5Cright%20%5C%7C%20%3D%20%5Csqrt%7B%5Csum_%7Bi%3D1%7D%5E%7Bn%7Dx_%7Bi%7D%5E2%7D">
  </p>
