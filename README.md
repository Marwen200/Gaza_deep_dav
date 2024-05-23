# Gaza_deep_dav
A HIGH RESOLUTION GEOTAGGED SATELLITE IMAGERY DATASET FOR ANALYZING WAR-INDUCED DAMAGE

Designing practical algorithms for damage detection in satellite images requires a substantial and well-labeled dataset for training, validation, and testing. In this paper, we collect GAZADeepDav: a high-resolution PlanetScope satellite imagery dataset with 7264 tiles for no damage and 6196 tiles for damage . This work is delving into the steps of collecting the dataset, Geotagging and employing deep learning architectures to distinguish damage in war zones while also providing valuable insights for researchers undertaking similar tasks in real-world applications. The experimental results on this dataset, using SqueezeNet architecture, yielded an impressive 98.95\%  accuracy in classifying damage. The study also explored augmenting SqueezeNet with Bidirectional Long Short-Term Memory (BiLSTM) layers, resulting in a heightened accuracy of 99.10\%. The combination of SqueezeNet and BiLSTM exemplifies the potential for advanced model architectures to enhance damage classification accuracy further. 

Instructions: 
To extract the dataset, please unzip the main file 'gaza_deep_dav.zip'. There will be 3 zip files

A folder conatinaing tiles about damage taken from post war images

A second folder containing tiles about non damage from pre war images.

A Third folder containing tiles about non damage from pre war images as a second part.


Tiles creation employs a multi-step process to extract meaningful information from high-resolution PlanetScope satellite imagery(3m resolution) depicting post and pre-war scenes in Gaza. The initial step involves reading the Red, Green, and Blue bands from the imagery and normalizing the pixel values. Subsequently, the images are partitioned into smaller tiles, each measuring 128x128 pixels. Each tile undergoes a check for the absence of empty (zero) values in any of the bands. If the tile meets this criterion, we stack the bands, generating an RGB representation of the tile.
