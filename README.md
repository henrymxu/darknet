![Darknet Logo](http://pjreddie.com/media/files/darknet-black-small.png)

# Custom Darknet #
This version of darknet allows the user to save the results of classifications.
The results are saved as a json file containing the various detections along with their properties (class, bounding box).

To run this custom command, use `validate`.

# Single Image Validation
Running the detector on a single image located at `~/Documents/ImageSet/gallardo/image_39.jpg`
and outputting the results at `~/Documents/ImageSet/gallardo/results.json`.

`./darknet validate cfg/yolov3.cfg cfg/yolov3.weights ~/Documents/ImageSet/gallardo/result.json ~/Documents/ImageSet/gallardo/image_39.jpg`

* (Assuming you are in the darknet directory)
# Multiple Image Validation
To run the detector on multiple images, leave the image path blank.  Once the weights are loaded, input each image path
one at a time.  The results will still all be saved in the same file.  Input a blank file name to end the process.

`./darknet validate cfg/yolov3.cfg cfg/yolov3.weights ~/Documents/ImageSet/gallardo/result.json`


* (Assuming you are in the darknet directory)

The images that are passed in cannot use `~` as apart of the path.

To automate the usage of the detector with multiple images, create a text file with 
all the paths of the images you wish to be validated and run the following command.

`cat image_list.txt | ./darknet detect cfg/yolov3.cfg yolov3.weights ~/Documents/ImageSet/gallardo/result.json`

* (Assuming you are in the darknet directory)
* (Assuming image path list is found in image_list.txt with paths seperated by new lines)

# Darknet #
Darknet is an open source neural network framework written in C and CUDA. It is fast, easy to install, and supports CPU and GPU computation.

For more information see the [Darknet project website](http://pjreddie.com/darknet).

For questions or issues please use the [Google Group](https://groups.google.com/forum/#!forum/darknet).
