# Build `Active Shape Model` (ASM) of 3D Face.
 
 * Objective here is to build active shape model to recognise 3D face mainly, and not focus on facial texture. Though, typically ASM is used to extract the texture of the interested object using a base model. 

 * To build active shape model using the algorithm given in [2]. The first prerequisite is the landmarks for each object/image and a base model. 

 * The base model is then trained on learning data to produce an active shape model which can be used for a new instance to recognise its texture. 

 * The attached [notbook](eigen3dmodel_for_active_shape_model.ipynb) is limited to analysing the variability in given data and how shows how many eigenvectors are needed to capture at least 98% variability in the data.   


## Dataset

 * Synthetic 3D Face of about 500 faces is available.





## MeshMonk: open-source large-scale intensive 3D phenotyping

 * [MeshMonk: Open-source large-scale intensive 3D phenotyping](https://www.youtube.com/watch?v=-M5ZErH99yc)




## References

[[1]](resources/MeshMonkintensive3Dphenotyping.pdf) White, Julie D., et al. "MeshMonk: Open-source large-scale intensive 3D phenotyping." Scientific reports 9.1 (2019): 1-11.

[[2]](resources/An_Introduction_to_ActiveShapeModels.pdf) Cootes, Tim, E. R. Baldock, and J. Graham. "An introduction to active shape models." Image processing and analysis (2000): 223-248.



