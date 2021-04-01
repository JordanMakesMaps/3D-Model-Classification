# Classifying 3D Models of Coral Reefs using Structure-from-Motion and Multiview Semantic Segmentation

We present a novel method that can efficiently provide semantic labels of functional groups to 3D reconstructed models created from commonly used SfM software (i.e., Agisoft Metashape) using Fully Convolutional Networks (FCNs). Unlike other methods ours involves creating dense labels for each of the images used in the 3-D reconstruction and then reusing the projection matrices created during the SfM process to project semantic labels onto either the point cloud or mesh to create fully classified versions.  

Although SfM has become widely adopted by ecologists, deep learning presents a steep learning curve for many. Because of this we provide a comprehensive workflow with detailed instructions and open-sourced our programming code to assist others in replicating our methodology. Our method provides researchers with the ability to assess precise changes in 3-D community composition of reef habitats in an entirely novel way, providing more insight into changes in ecological paradigms, such as those that occur during coral-algae shifts.  
  
  
 ![side-by-side](Figures/side_by_side.png)



# Workflow:    

A.) Extract still images from video footage;  
B.) Import into `Patch Extractor` or similiar tool (e.g., [CPCe](https://hcas.nova.edu/tools-and-resources/cpce/index.html) or [CoralNet](https://coralnet.ucsd.edu/));  
C.) Extract patches of each class category of interest;    
D.) Train a patch-based image classifier (e.g., convolutional neural network);  
E.) Use trained classifier to automatically add additional sparse labels to each image;  
F.) Pass sparse labels and corresponding images to [Fast-MSS](https://github.com/JordanMakesMaps/Fast-Multilevel-Superpixel-Segmentation);    
G.) Convert sparse to dense labels automatically;    

*Optional:*  
H.) Train a deep learning [semantic segmenation algorithm](https://github.com/qubvel/segmentation_models) on dense labels;  
I.) Use deep learning model to obtain more accurate dense labels for these images, and those collected from similar habitats, thus skipping steps A - H.  

![getting_dense_labels](Figures/getting_dense_labels.png)

# Requirements:  
- cv2
- numpy
- pandas
- skimage
- matplotlib
- fast_slic

# TODO
- Finish readme
- Update notebooks to include markdown comments
