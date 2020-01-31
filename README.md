# Visualization of dominant modes of variability in 3D human faces
 
 * Objective here is to visualize the dominant modes of variability in 3D faces mainly, and not focus on facial texture. <!-- Though, typically Active Shape Model (ASM) is used to extract the texture of the interested object with a base (template) model using an extension of eigenvector algorithm.  -->


* The attached [notbook](eigenface_3d_vz_sml.ipynb) analyzes the variability in given data and also presents some extreme variant of 3D faces generated using eigenfaces, which captures at least 98% variability in the data.  


## Dataset

 * Synthetic 3D Face of about 500 faces is available.

 * Each of the faces is represented by 7160 dimension 3D coordinates.  


## Computing Eigen 3D Faces

 * To compute eigenfaces using Principal Component Analysis (PCA), each 3D face coordinates of N points are arranged in 3N (3\*N) dimensions, that is, a 3D face composed of 7160 points by 3 ordnaties is represented by 21470 points (3\*7160).    

 * To get back eigenface from eigenvector the 3N points are reshaped to [N \* 3] dimension.  




## Average 3D Face

 * The average face is mean of all the faces that also acts as template face for visualizing variability in generated 3D faces. 




## Generating Variations in Faces using Eigenface

<!-- ![](https://latex.codecogs.com/svg.latex?$$X&space;\&space;\approx&space;\&space;\bar{X}&space;&plus;&space;\sum_{i=1}^{k}&space;b_i&space;\mathbf{u_i}$$) -->

<!-- ![](https://latex.codecogs.com/svg.latex?$$X&space;\&space;=&space;\&space;\bar{X}&space;&plus;&space;\left&space;\{&space;\sum_{i=1}^{K_d}&space;b_{di}&space;\mathbf{u}_{di}&space;\right\}_{d=1}^3&space;$$) -->

<!-- ![](resources/face_gen.png) -->

![](https://latex.codecogs.com/svg.latex?$$\mathit{x}&space;\&space;=&space;\&space;\bar{X}&space;&plus;&space;\sum_{i=1}^{K}&space;b_{i}&space;\mathbf{u}_{i}$$)

 * where ![](https://latex.codecogs.com/svg.latex?$$\mathit{x}$$) is a new face which is generated using ![](https://latex.codecogs.com/svg.latex?$k$) eigenfaces (![](https://latex.codecogs.com/svg.latex?$u_{i}$)) by varying magnitude of ![](https://latex.codecogs.com/svg.latex?$b_{i}$). 
 
 * Variant of faces are generated using **average face** as template and adding extreme combination of eigenvectors (![](https://latex.codecogs.com/svg.latex?$&space;-3&space;\sqrt{\lambda}&space;\le&space;b_{di}&space;\le&space;3&space;\sqrt{\lambda}&space;$)) to show range of faces that can be produced.  


<!-- $x \ \approx \  \bar{X}  + \sum_{i=1}^{k} b_i \mathbf{u_i} $ \\ -->


<!-- $ -3 \sqrt{\lambda} \le bi \le 3 \sqrt{\lambda} $ -->


## Conclusions
 
 * Very few eigenfaces (38) are needed to capture (98%) of variability in data. Although, the data being synthetic with not much variability in it is also playing a role in requiring very few eigenfaces to capture 98% variability.

 * One can generate any number of faces using a combination of eigenfaces.   




## References

[[1]](resources/MeshMonkintensive3Dphenotyping.pdf) White, Julie D., et al. "MeshMonk: Open-source large-scale intensive 3D phenotyping." Scientific reports 9.1 (2019): 1-11.

[[2]](resources/An_Introduction_to_ActiveShapeModels.pdf) Cootes, Tim, E. R. Baldock, and J. Graham. "An introduction to active shape models." Image processing and analysis (2000): 223-248.



