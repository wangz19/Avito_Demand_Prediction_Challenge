# Avito_Demand_Prediction_Challenge
Avito, Russia’s largest classified advertisements website, is deeply familiar with this problem. Sellers on their platform sometimes feel frustrated with both too little demand (indicating something is wrong with the product or the product listing) or too much demand (indicating a hot item with a good description was underpriced).  In their fourth Kaggle competition, Avito is challenging you to predict demand for an online advertisement based on its full description (title, description, images, etc.), its context (geographically where it was posted, similar ads already posted) and historical demand for similar ads in similar contexts. With this information, Avito can inform sellers on how to best optimize their listing and provide some indication of how much interest they should realistically expect to receive.

### This Kaggle competition tried to predict the sale probability of items based on their structureed website information and unstructured description and images. This was a regression problem and RSME is used as evaluation metric. The basic model is a LightGB model with TF_IDF title and description features.Then I implemented a parrallel image processing code to extract image information such as hueness, brightness, RGB values, etc. The image feature give little boost on the crossvaliation score. I stacked a second layer Ridge model which improve the public lead board (LB) score from 0.2269 to 0.2221. Finally, the public blend model give the best LB 0.2204.
