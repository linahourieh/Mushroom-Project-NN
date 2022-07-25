This is a journal of observations during my first implementation of NN.

1) First Problem:
I choose a dataset that was clean and clear, that helped me a lot and saved much time. However, it needed a little processing. Also, I took some time to figure out the dimensions of the dataset
at the end I figured it out

2) Plan the network:
I set up a drawing called compuattional graph of the neural network, I started with 4 layers; 8 units, 4 units, 3 units and 1 unit. Set up the dimensions of weights and bias vectors

3) Initializaion Debug:
After writing the scratch of initialization, some problems arose. 
- check the keys 
- check shape of W1 b1 and WL bL
- chech the values if they fit our assumptions; for example i used random initialization from a normal distribution, this increases the chance of values around the zero to be picked more

4) Scratch forward_propagation:
- Helper Functions:
These were the easiest. However, double check them. You may do a mistake like me and get weird results without knowing why.
(I wrote sigmoid as 1/ 1 * e**-z instead of 1/ 1 + e**-z, that allowed some values in the last layer to be equal to 1. when I calculated the cost function,
it gave me error RuntimeWarning: divide by zero encountered in log)

- Try to write a pseduocode starting from the last function, the one that gives you the final result, up to every other function needed.
- check AL.shape
- Describe AL

5) Try to build cache inside the feed forward
6) Write cost function: easy, check the output so far

7) Building Backpropagation:
This was definietly the hardest part, I copied the code from deep learning ai course

8) Updating the parameters and essembling the model is easy 
9) I trained it for 3000 iterations, it gave 0.068 as cost, but after doubling the iteration number, the cost decreased to 0.02

10) I tried training for 2000,3000, and 6000 and sat a graph for that
11) Then I tried to implement L2 regularization, I edited both cost function and Update_parameters function.
