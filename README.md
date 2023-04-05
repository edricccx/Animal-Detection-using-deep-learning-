# Animal-Detection-using-deep-learning-
This is a deep learning model which uses CNN to predict the images of animals and say what type of animal they are.

animaldetection1.pynb is a jyputer notebook file where i have given the code for running the model has been given

This model has not been loaded(I can not load a file larger than 25mb in github)

But in the animaldetection1.pynb in last four blocks i have written the code so that u can load the model and use it for other purposes.


from tensorflow.keras.models import load_model
import os
model.save(os.path.join('models','wildclassifier.h5'))
new_model = load_model('models/wildclassifier.h5')
new_model.predict(np.expand_dims(resize/255, 0))


U will have to create a folder with name models(it can be any name as long as u change it in the above code) so that it saves the model.

The dataset i used to train this model,i will provide a link down below
https://www.kaggle.com/datasets/iamsouravbanerjee/animal-image-dataset-90-different-animals?select=name+of+the+animals.txt

There are 90 classes where i have only used 56 classes 


