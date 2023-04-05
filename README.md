# Animal-Detection-using-deep-learning-
This is a deep learning model which uses CNN to predict the images of animals and say what type of animal they are.

animaldetection1.pynb is a jyputer notebook file where i have given the code for running the model has been given

This model has not been loaded(I can not load a file larger than 25mb in github)




# Load and preprocess the image
To test your image u will have to add to image in jpg format in this folder and change it in this part of the code


img_path = '1.jpg'


img = image.load_img(img_path, target_size=(224, 224))  # resizing to 224x224


x = image.img_to_array(img)


x = np.expand_dims(x, axis=0)


x = x / 255.0  # scaling pixel values to [0,1]
 
# To save the model
In the animaldetection1.pynb in last four blocks i have written the code so that u can load the model and use it for other purposes.



from tensorflow.keras.models import load_model


import os



model.save(os.path.join('models','wildclassifier.h5'))


new_model = load_model('models/wildclassifier.h5')


new_model.predict(np.expand_dims(resize/255, 0))



U will have to create a folder with name models(it can be any name as long as u change it in the above code) so that it saves the model.

# About the dataset used 
The dataset i used to train this model,i will provide a link down below


https://www.kaggle.com/datasets/iamsouravbanerjee/animal-image-dataset-90-different-animals?select=name+of+the+animals.txt

There are 90 classes where i have only used 56 classes(u can use how many classes u want as long as u can bring appropriate changes to the model's code)

From that link all the classes that i have choosen are these

class_names = ['antelope', 'badger', 'bat', 'bear', 'bison', 'boar', 'cat', 'chimpanzee', 'cow', 'coyote', 'deer', 'dog', 'donkey', 'duck', 'elephant', 'flamingo', 'fox', 'goat', 'goose', 'gorilla', 'hamster', 'hare', 'hedgehog', 'hippopotamus', 'hornbill', 'horse', 'hummingbird', 'hyena', 'kangaroo', 'koala', 'leopard', 'lion', 'okapi', 'orangutan', 'owl', 'ox', 'panda', 'parrot', 'pelecaniformes', 'pig', 'pigeon', 'porcupine', 'possum', 'raccoon', 'reindeer', 'rhinoceros', 'sandpiper', 'sheep', 'snake', 'squirrel', 'tiger', 'turkey', 'wolf', 'wombat', 'woodpecker', 'zebra']


