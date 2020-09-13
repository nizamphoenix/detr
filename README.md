### DETR (Detection Transformer) +[wheat data set](https://www.kaggle.com/c/global-wheat-detection)

Detection Transformer leverages the transformer network(both encoder and the decoder) for Detecting Objects in Images . Facebook's researchers argue that for object detection one part of the image should be in contact with the other part of the image for greater result especially with ocluded objects and partially visible objects, and what's better than to use transformer for it. 

The main ingredients of the new framework, called DEtection TRansformer or DETR,are a set-based global loss that forces unique predictions via bipartite matching, and a transformer encoder-decoder architecture. Both model and the criterion are trained

The main motive behind DETR is effectively removing the need for many hand-designed components like a non-maximum suppression procedure or anchor generation that explicitly encode prior knowledge about the task and makes the process complex and computationally expensive
   

DETR uses a special loss called Bipartite Matching loss where it assigns one ground truth bbox to a predicted box using a matcher , thus when fine tuning the hungarian matcher(provided by sourcecode) and also the fucntion SetCriterion which gives Bipartite matching loss for backpropogation are used.
