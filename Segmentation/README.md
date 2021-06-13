## Usage

The configurable parameters for the data generator are mostly kept in the segmentation_training.ini file.

### Under `IMAGE_FOLDERS`:
  * set `train_images_path`,`train_masks_path` to point to folders where the training images and their respective masks files are placed.

  * set `val_images_path`,`val_masks_path` to point to folders where the validation images and their respective masks files are placed.

### Under `DATA_GENERATOR_PARAMETERS`:
  * `batch_size` -> the required batch size for usage. 
  * `image_dimensions` -> image dimensions required for providing to the model. Value should be comma-separated values.
  * `num_channels` -> required number of channels for providing to the model. 
      *   By default, if "1" is given, it is assumed as a grey-scale image while reading the image.
      *   Setting value "3" ensures it is parsed as a BGR image by opencv while reading the image.
  * `augment_flag` -> Boolean flag for enabling/disabling augmentation in data generator.Set True for enabling augmentation.
  * `tiff_flag` -> Boolean flag for reading masks as "tif" format. Set True for reading masks as tif
  * `num_classes` -> the number of classes/labels reqd. This number can also be interpreted as the number of images present in each tiff file, as each image provides a label mask for that respective class.  
 
   <b>Please keep in mind the `num_channels`, `num_classes` and `batch_size` are meant to be integer values. These config values are parsed as strings and then converted internally to int. Thus the value should be a valid integer, or else the config parsing will thrown an exception while casting to int.<b>
  
  General resources regarding usage and preprocessing are provided in this repository's base README.md
