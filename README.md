# mushroom-classifier - A deep-learning based Web-Application for mushroom classification.
This project aims to provide a web-application that classifies uploaded images of mushrooms. Due to lack of computational power, I decided to limit myself to classify 10 species only:
1. Apioperdon pyriforme
2. Auricularia auricula-judae
3. Dacrymyces stillatus
4. Daedalea quercina
5.Fuscoporia ferrea
6. Psathyrella candolleana
7. Stereum hirsutum
8. Tremella mesenterica
9. Tubaria furfuracea
10. Xylaria hypoxylon
## How did I approach this project?

### 1. Data Loading and Preparation
  #### a. Original Data Source:
https://svampe.databasen.org/
  #### b. Data Loading:
Due to the large data set, I've used Dask: A flexible parallel computing library for analytics.
  #### c. Image resizing:
When using a pre-trained model with a fixed input size, one  should then resize the images to match that size. 
This is important because the model's architecture and weights are often designed to work with a specific input size. If the images are too large or too small, it can lead to suboptimal performance or errors.


### 2. Build the model(s)
With the web-application in mind, I decided to apply transfer learning using To achieve our goal, we tested three models, detailed below:


### 3. Create a web-application using Flask and TensorFlow.js
The (for now) final model was converted into TensorFlow.js format and integrated into a simple web-framework using Flask and Bootstrap. 

## Future Improvements
1.Take into account the different species distributions:

  ● Species rarity, that is, its relative frequency in the database.

  ● The geographical distribution of the species.
  
  ● Phenology of the species, its seasonality.
  
  
2. Category distribution of the fungi dataset is long-tailed:
   
  ● Long-tailed datasets can cause models to perform poorly on the tail, including the rare events or minority classes.
  
