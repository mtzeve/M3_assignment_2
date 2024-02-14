Explanation of assignment 

Part 1

For part 1 of the assignment, we decided to work with a dataset which contains a lot of movies from Wikipedia, including their title and plot, which was our main focus. But also other things such as genre and director.
We wanted to build a gradio application, which through semantic search, would output Title and Plot of a movie based on a query as input.
For this purpose we cleaned the dataset and focused only on the two columns Plot and Title. Then we used the all-MiniLM-L6-v2 sentence transformer model to embed the dataset and convert them into vectors. We had a decently large dataset with 34k rows, we decided to run the model only once and then save the embedded data as a csv file, which we load into the notebook so we wont have to rerun the sentence transformer multiple times. 
Then we build function using the same model that would transform our query into vectors as well and then try to find the best match based on cosine similarity. The function was then designed to output two separate outputs, which were individually the Title of the movie and the Plot of the movie.
Then we integrated the function into a gradio application, which makes it possible to write your query as input and then it will find the most similar movie based on the original dataset.

Part 2
1 Gradient Descent Exercise
We used stochastic gradient descent on a house price dataset from the m1 module. We cleaned the dataset for missing values and then we decided to set our target variable (y) as the house ‘price’ and then our input features (x) were all of the other variables from the dataset, such as area, bedrooms, bathrooms etc.
Then we onehot encode all of the categorical variables, split the dataset and then we scaled the variables x and y. 
Then we convert y-train into numpy array, so we can put into a tensor. Then we convert x and y train into tensors and then implement into a feedforward neural network, here we setup our hyperparameters, loss function, optimizer using stochastic gradient descent and our training loop. 
We did two iterations of this example, where we changed the weight from 10 in the first example to a 1000 in the second  example. We see that the loss is lower with higher weight, the first one gave an average loss of 0.6605 and the secondary gave an average loss of 0.6391.

2 Attention mechanism exercise
For our attention exercise, we decided to go with two sentences. One was“The crane is a majestic bird” and the second was “He used the crane to lift the heavy machinery”. The reason for this choice was that “crane” is a polysemous word that has multiple meanings, which helps with demonstrating the functionality of attention.
To visualize the attention weight we setup a heatmap, which visualizes which words in the sentenced are especially targeted by the attention mechanism. We decided to go with a heatmap that shows both sentences on each axis, which would allow us to be able to compare the attention weight between all the pair of tokens in both sentences. This was decided to be the way to visualize it because the heatmap would not become way too complex, as both sentences are kind of short.

Dataset's (part 1) link: https://www.kaggle.com/datasets/jrobischon/wikipedia-movie-plots 
Dataset's (part 2) link: https://www.kaggle.com/datasets/harishkumardatalab/housing-price-prediction?resource=download 
