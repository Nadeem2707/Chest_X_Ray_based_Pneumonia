# Chest_X_Ray_based_Pneumonia

# Details on Dataset
# What is Pneumonia
- Pneumonia is an infection in one or both lungs.
- Bacteria, viruses, and fungi cause it.
- The infection causes inflammation in the air sacs in your lungs, which are called alveoli.

# General Symptoms
- fever,
- chills,
- cough,
- shortness of breath, and
- fatigue

# What are the different types - Bacterial pneumonia
- Bacteria cause most cases of community-acquired pneumonia in adults.
- can catch pneumonia when someone who is infected coughs or sneezes.
- Bacteria-filled droplets get into the air, where you can breathe them into your nose or mouth
- Bacterial pneumonia typically exhibits a focal lobar consolidation

# What are the different types - Viral pneumonia
- Viruses are the second most common cause of pneumonia.
- Many different ones cause the disease, including some of the same viruses that bring on colds and flu
- Fever, Chills, Dry cough, which may get worse and make mucus, Stuffy nose
- viral pneumonia (right) manifests with a more diffuse “interstitial” pattern in both lungs

# The Dataset
- labeled a total of 5,232 chest X-ray images from children

- training set includes 3,883 characterized as depicting pneumonia (2,538 bacterial and 1,345 viral) and 1,349 normal, from a total of 5,856 patients

- Test set includes 234 normal images and 390 pneumonia images (242 bacterial and 148 viral) from 624 patients.

# Labels

- Normal x-ray
- Pneumonia x-ray

# Quick Prototyping - Training, Validation and Inferencing
# Transfer Learning

#Base Network

- A convolutional neural network is first trained on large dataset such as coco or imagenet

- These datasets have many classes, like around 1000, 1500 classes

- Thus the final layer in the neural network has similar number of neurons

# Finetuning on custom dataset

- Custom dataset usualy has different number of classes

- You take the network and load the pretrained weights on the network

- Then remove the final layer that has the extra(or less) number of neurons

- You add a new layer with number of neurons = number of classes in your custom dataset

Optionally you can add more layers in between this newly added final layer and the old network

