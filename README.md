# Video_Game_Review_Summarization

In this project, we combine the tasks of text classification, text summarization, and text-to-speech into one final implementation for users to quickly understand videogame reviews. Our focus was on IGN videogame reviews, such as [this one](https://www.ign.com/articles/warhammer-40k-chaos-gate-daemonhunters-review). Our work involved heavy text cleaning, such as normalization via lowercasing, stopword removal, punctuation removal, and POS tagging. Below, we can get an idea of how each component worked and how we worked with our data.

## Text Classification
In this part, we worked on several things:
  - text processing
  - exploratory data analysis
  - model testing and evaluation
  - a brief demo on this component
Our dataset was the steam reviews dataset, found [here](https://www.kaggle.com/datasets/luthfim/steam-reviews-dataset), which consisted of classifying videogame reviews as either recommended or not according to the gamer.

### EDA and Text Processing
In order to better understand our data we performed some quick data processing followed by exploratory data analysis.
Here is an example of text pipeline created for initial text processing

![image](https://user-images.githubusercontent.com/69231868/170177294-2c4eb209-74e0-4003-9777-e5dd418e861b.png)

Because we worked with the steam dataset, we worked on changing the video game slang found in most reviews (e.g., "poggers" can refer to "awesome"). Below is a word cloud of some of the most prevalent words in both reviews that are recommended or not recommended.

![image](https://user-images.githubusercontent.com/69231868/170178318-3eccae5f-4f09-4505-8af2-53983785aa6f.png)

### Model Testing
When selecting models, we used the Sklearn library and performed gridsearch to find the optimal parameters for each model chosen (we test Naive Bayes, SVM, Logistic Regression, Random Forest, and Ensembles of different combinations). Our best performing model was the logistic regression, in which we can see the results below.

![image](https://user-images.githubusercontent.com/69231868/170178650-f694916d-7324-40be-b6a1-ee6c5552961c.png)

### Demo
A final demo of this component was done by copy and pasting a steam review into our code, preprocessing with our pipeline, and making a prediction using our model. This can be seen below.

![image](https://user-images.githubusercontent.com/69231868/170178982-d172bbb2-8b74-44cf-b1bc-d0e0efd10325.png)

![image](https://user-images.githubusercontent.com/69231868/170179032-1dab666a-7944-4028-8ba7-ee41cd7f0c33.png)

