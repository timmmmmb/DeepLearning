Goal:

The aim of this exercise is to start an empirical (experimental) investigation into the robustness of a state of the art image segmentation / object detection system.


We will use the following system for our experimentation:

	https://colab.research.google.com/github/lexfridman/mit-deep-learning/blob/master/tutorial_driving_scene_segmentation/tutorial_driving_scene_segmentation.ipynb

Testing new images:

	SAMPLE_IMAGE = 'mit_driveseg_sample.png'
	if not os.path.isfile(SAMPLE_IMAGE):
    	print('downloading the sample image...')
    	SAMPLE_IMAGE = urllib.request.urlretrieve('https://github.com/lexfridman/mit-deep-learning/blob/master/tutorial_driving_scene_segmentation/mit_driveseg_sample.png?raw=true')[0]

	
	An easy way to integrate new images for testing is to host them and supply the link as shown above.

During our experimentation we would like to evaluate a bit in terms of where the limits of the system lies and what are its weaknesses. 
This experimentation is divided into multiple categories.
For each category we make the distinction between the object we evaluate and the type of adversarial input we use.
Similar work has been done also in natural language processing where people managed to significantly reduce the performance of text classifiers by changing the order of sentences (in a way that would not change the meaning for a human being).

For modifcation of images you can use imagemagick (command line tool for modifying images on Windows and Linux).

magick convert input.jpg -rotate -180 out.jpg

magick mogrify -rotate 5 *.jpg
https://imagemagick.org/script/mogrify.php allows bluring and other effects.
