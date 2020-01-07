Topic: Emotion recognition through facial expressions

Architecture: Convolutional Neural Network was used
	Input layer with 2304 neurons
	8 hidden layers:
		1) CNN layer with 64 neurons and filter size of 3*3
		2) CNN layer with 64 neurons
		3) CNN layer with 64 neurons
		
		/* Maxpooling after this to reduce 48*48 image to 24*24 */
		
		4) CNN layer with 32 neurons and filter size of 3*3
		5) CNN layer with 32 neurons
		6) CNN layer with 32 neurons
		
		/* Maxpooling after this to reduce 24*24 image to 12*12 */
		/* model.flatten() used to flatten and connect CNN layer to Dense layer
		
		7) Dense layer with 128 neurons
		8) Dense layer with 64 neurons
	Output layer with 7 neurons
	Activation function : Relu
	Activation function for Output layer : Softmax
	Categorical crossentropy gradient descent for loss calculation.
	
Preprocessing:

	Input was taken from a .csv file and converted to a dataframe with Pandas.
	Pixels were in the form of a string, which were then converted to 2-D INT array of 48*48 using numpy
	
Database:

	Database was a .csv file with : 1) Labels(0-6 representing 7 emotions)
					2) 48*48 pixels in the form of string
					3) Whether data is used for training or testing
					

Experimental analysis:

	a.Number of classes and samples:
				Total number of data : 35,887
				/* Training-testing split of 80-20 */
				Number of training inputs : 28709
				Number of testing inputs : 7178
				Samples : 1) Training
					  2) Testing
					  3) Validation
	
	b.Accuracy : Accuracy obtained was between 50-60%
	
	c.Number of iterations : 30 epochs
	
	d.Improvements: 1) Increasing the number of epochs
	
Furthur notes : Output of CNN was fuzzified i.e POST PROCESING FUZZIFICATION.
		Based on our observations, we defined some FUZZY RULES to furthur improve the accuracy.
