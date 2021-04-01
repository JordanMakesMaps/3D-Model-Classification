# Classifying 3D Models of Coral Reefs using Structure-from-Motion and Multiview Semantic Segmentation

We present a novel method that can efficiently provide semantic labels of functional groups to 3D reconstructed models created from commonly used SfM software (i.e., Agisoft Metashape) using Fully Convolutional Networks (FCNs). Unlike other methods ours involves creating dense labels for each of the images used in the 3-D reconstruction and then reusing the projection matrices created during the SfM process to project semantic labels onto either the point cloud or mesh to create fully classified versions.  

Although SfM has become widely adopted by ecologists, deep learning presents a steep learning curve for many. Because of this we provide a comprehensive workflow with detailed instructions and open-sourced our programming code to assist others in replicating our methodology. Our method provides researchers with the ability to assess precise changes in 3-D community composition of reef habitats in an entirely novel way, providing more insight into changes in ecological paradigms, such as those that occur during coral-algae shifts.  




# Workflow  

1.) 

