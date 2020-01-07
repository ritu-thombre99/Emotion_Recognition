Topic: Emotion recognition through facial expressions

Architecture: Multilayer Perceptron model was used
	Input layer with 2304 neurons
	Hidden layer with 30 neurons
	Output layer with 7 neurons
	Feed forward and error backpropagation was used in the MLP
	Activation function : Sigmoidal
	
Preprocessing:

	Input was taken from a .csv file and converted to a dataframe with Pandas.
	Pixels were in the form of a string, which were then converted to 2-D INT array of 48*48 using numpy
	Mini batch gradient descent was used for training the model and the batch-size was 10
	
Database:

	Database was a .csv file with : 1) Labels(0-6 representing 7 emotions)
					2) 48*48 pixels in the form of string
					3) Whether data is used for training or testing
					

Experimental analysis:

	a.Number of classes and samples:
				Number of training inputs : 10,000
				Number of testing inputs : 1,000
				Samples : 1) Training
					  2) Testing
	
	b.Accuracy : Accuracy obtained was around 80%.
		     Two boundary conditions were found.
	
	c.Number of iterations : 30 epochs
	
	d.Improvements: 1) Increasing the number of hidden layers in the MLP
			2) Using CNN to furthur increase the efficiency and accuracy of the model.
