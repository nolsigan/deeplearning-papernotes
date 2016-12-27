## Deep Residual Learning for Image Recognition

Method to enable increasing network depth but keeping complexity low by residual learning

#### key points

* deep networks suffer from degradation problem : accuracy gets saturated and then degrades as depth increases
* let layers fit a residual mapping instead of hoping each few stacked layers
* introduces deepest network every presented, 152-resnet and won 1st price in the ILSVRC 2015
* residual function is flexible but usally uses 2,3 layers of fully connected or convolutional
* downsampling directly by convolutional layers that have a stride of 2 (In keras, called subsample)
* two ways for identity mapping when dimensions increase, zero padding and projection shortcut by 1x1 convolutions
* use bottleneck architectures on deeper networks for reasonable training time (1x1 -> 3x3 -> 1x1)

#### thoughts

* super smart idea!
* feels like human thinking about detail part by part rather than always thinking as a whole
    * ex) when calculating 2x2 + 1x3 -> think about 2x2 without considering bigger whole picture
    * then think about 4 + 1x3
