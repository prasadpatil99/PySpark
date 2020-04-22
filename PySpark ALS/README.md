## PySpark - Collaborative Filtering
> **Collaborative Filtering** - *Collaborative filtering propose to build a model from user's past preferences as well similar decisions made by other users. Further similar user recommendations are modified with user preference to obtain subtle results.*

Traditional collaborative filtering has typical challenges like 
 - **Popularity Bias** : refers to system which has most number of interactions
 - **Item Cold-Start Problem** : refers when item's rating are new then it rely on user profile
 - **Scalability Issue** : refers to lack of ability to scale larger dataset in the database.
These problems can be solved with Matrix Factorization Method it decomposes user-item interaction matrix into product of lower dimensionality rectangular matrices. A common analogy for matrix decomposition is the factoring of numbers alike factoring of 10 into 2 x 5. There are several decomposition methods as LU Decomposition & QR Decomposition. <br>
**LU** - LU Decomposition is for square matrices and decomposes a matrix into L and U components where L is the lower triangle matrix and U is the upper triangle matrix. The variation of LU, LUP can also be used sometimes if it is hard to interpret the results where L & U may reorder matrix formation and P can be used to re-order result to original order.<br>  
**QR** - QR decomposition is for m x n matrices (not limited to square matrices) and decomposes a matrix into Q and R components. Where Q is matrix with the size m x m, and R is an upper triangle matrix with the size m x n.

**Alternating Least Square (ALS)** used here is also matrix factorization algorithm which executes in a parallel fashion. It helps in building large-scale collaborative filtering problems. ALS uses L2 regularization and minimizes two loss functions alternatively it first holds user matrix and runs gradient descent with item matrix; then it holds item matrix and runs gradient descent with user matrix.

## Reference
https://spark.apache.org/docs/2.2.0/ml-collaborative-filtering.html
https://machinelearningmastery.com/introduction-to-matrix-decompositions-for-machine-learning/
