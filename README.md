# Mushroom-Project-NN
A L-Layers Neural Network written from scratch with documentation, classifying mushrooms into edible or poisonous. 
This is a journal of observations during my first implementation of NN.

1) First Problem:
I choose a dataset that was clean and clear, that helped me a lot and saved much time. However, it needed a little processing. Also, I took some time to figure out the dimensions of the dataset.

2) Plan the network:
I set up a drawing called compuational graph of the neural network, I started with **4 layers = 8 units, 4 units, 3 units and 1 unit**. Set up the dimensions of weights and bias vectors



![//home/lina/Downloads/nn%20(1).svg](https://raw.githubusercontent.com/linahourieh/Mushroom-Project-NN/main/nn%20(1).svg)

3) Initializaion Debug:
After writing the scratch of initialization, some problems arose. 
- check the keys 
- check shape of W1 b1 and WL bL
- chech the values if they fit our assumptions; for example i used random initialization from a normal distribution, this increases the chance of values around the zero to be picked more

4) Scratch forward_propagation:
- Helper Functions:
These were the easiest. However, double check them. You may do a mistake like me and get weird results without knowing why.
(I wrote sigmoid as 1/ 1 * e**-z instead of 1/ 1 + e**-z, that allowed some values in the last layer to be equal to 1. when I calculated the cost function, it gave me error RuntimeWarning: divide by zero encountered in log)

- Try to write a pseduocode starting from the last function, the one that gives you the final result, up to every other function needed.
- check AL.shape
- Describe AL

5) Try to build cache inside the feed forward. However before doing that try to scheme the cache through the functions it helps a lot.

6) Write cost function: easy, check the output if it is logical.

7) Building Backpropagation:
This was definietly the hardest part, I tried to write it but I ended up copying the code from deep learning ai course.

8) Updating the parameters and essembling the model is easy 

9) I trained it for 3000 iterations, it gave 0.068 as value for cost function, but after doubling the iteration number, the cost decreased to 0.02

10) I drew the graph of J(w,b) cost function with respect to the number of iterations.

![](https://github.com/linahourieh/Mushroom-Project-NN/blob/main/Cost%20function%20after%206000%20iterations.png)

11) The Accuracy was:
**Expected Output**:

<table>
    <tr>
    <td>
        <b>Train Accuracy</b>
    </td>
    <td>
    99.81
    </td>
    </tr>
    <tr>
    <td>
        <b>Dev Accuracy</b>
    </td>
    <td>
    99.63
    </td>
    </tr>
    <tr>
    <td>
        <b>Test Accuracy</b>
    </td>
    <td>
    99.75
    </td>
    </tr>
</table>


11) Although no overfitting is happening, I tried to implement L2 regularization
, I edited both cost function and Update_parameters function.
That was wromh, only the cost function and dW needs to be edited
