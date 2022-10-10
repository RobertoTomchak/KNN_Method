# KNN_Method
## Definition
This is a study of the usage of the KNN Method on the Iris database.
The KNN Method stands for K-Nearest Neighbours, which is a Machile Learning Model that used Supervised Learning. Here, we compare the eucledian distance between the unkown point (aka the data we want to classify) from each point we know (aka the data used for training). Then, we consider the category of each of the K points which have the smallest distances. For example, if K=3, we considerer the nearest 3 points. The most frequent category is considered to be the category of the unkown point.

## How do we choose the value of K?
Because we are considering the K nearest points, the value of K has to be between 1 and the total number of points used for the training of the model. Other than that, there's not a correct value of K that has to be used for each KNN model. However, very small values of K (for example, K=1) can be a little problematic, since you're ignoring a lot of data, and can lead to a lot of errors. On the other hand, big values of K (for example, K=50 in our example that has 50 total points in the training data) can lead to serious erros, since you're considering data that is not "similar" to the unkown point. 
In this study, we can see that happening. We see that the values of K that provide an accuracy highter than 90% are between 1 and 28 (with the exception of K=26). It's interesting to see that K=1 actually provides a very high accuracy (96%). Unfortunately, it's unlikely that this will happen in any situation, since the accuracy depends on how well the KNN method fits the database.
It's also recomended that you use a prime value for K, since it helps avoid ties between different categories.

#When can the KNN method be used?
Since it's a Supervised Learning Model, the best way to know if the KNN method fits the situation is to just test it with a test dataset. In this example, we use 50 of the 150 plants for testing.
However, there's some things to consider. First, the function used in this study considers that all variables have the same magnitude. For example, if you had a dataset with the variables "age" and "salary", the variable "salary" would end up impacting the choice of the category a lot more than the variable "age", since its magnitude is a lot bigger. Second, in this study is also considered that all variables have the same impact on the choice of category. If you throw a variable that isn't relevant for the choice of category, it probably would let to a lot of errors.
To avoid the first problems, you can rescale the variables, so they have the same magnitude. For the second problem, you can use weights in each variable, according to it's relevance for the choice of category (however, you need a lot of data to choose the correct weights).

#Conclusion
Overall, the KNN method fits very well with the Iris Database. But, that might not be the case for most of databases, since you have to consider the 2 problems mentioned.
