## Week 4 Quiz - Key concepts on Deep Neural Networks

1. What is the "cache" used for in our implementation of forward propagation and backward propagation?

    - [ ] It is used to keep track of the hyperparameters that we are searching over, to speed up computation. 
    - [ ] We use it to pass variables computed during backward propagation to the corresponding forward propagation step. It contains useful values for forward propagation to compute activations. 
    - [ ] It is used to cache the intermediate values of the cost function during training. 
    - [x] We use it to pass variables computed during forward propagation to the corresponding backward propagation step. It contains useful values for backward propagation to compute derivatives. 
    </br>***Note:&nbsp;The "cache" records values from the forward propagation units and sends it to the backward propagation units because it is needed to compute the chain rule derivatives.***
</br>

2. Among the following, which ones are "hyperparameters"? (Check all that apply.)

    - [x] learning rate α
    - [x] number of layers LL in the neural network
    - [x] number of iterations
    - [x] size of the hidden layers n^[l]
</br>

3. Which of the following statements is true? 

    - [x] The deeper layers of a neural network are typically computing more complex features of the input than the earlier layers.
    - [ ] The earlier layers of a neural network are typically computing more complex features of the input than the deeper layers. 
</br>

4. Vectorization allows you to compute forward propagation in an LL-layer neural network without an explicit for-loop (or any other explicit iterative loop) over the layers l=1, 2, …,L. True/False?

    - [ ] True
    - [x] False
    </br>***Note:&nbsp;Forward propagation propagates the input through the layers, although for shallow networks we may just write all the lines, in a deeper network, we cannot avoid a for loop iterating over the layers.***
</br>

5. Assume we store the values for n^[l] in an array called layers, as follows: layer_dims = [n_x, 4,3,2,1]. So layer 1 has four hidden units, layer 2 has 3 hidden units and so on. Which of the following for-loops will allow you to initialize the parameters for the model?

    ```
    for(i in range(1, len(layer_dims))):
        parameter[‘W’ + str(i)] = np.random.randn(layers[i], layers[i - 1])) * 0.01
        parameter[‘b’ + str(i)] = np.random.randn(layers[i], 1) * 0.01
    ```
</br>

6. Consider the following neural network.
    </br>![Neural network](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/cwmw1nrfEeeJIwrF5BVsIg_e9a22da9e380c0350d2dfd47dcf34503_Screen-Shot-2017-08-06-at-12.42.46-PM.png?expiry=1617062400000&hmac=A-eSdVA8D4fHZWNB9Lm9yrgkgru9F5aVRXgT5rg2N0Q)</br> 
    How many layers  does this network have?

    - [x] The number of layers L is 4. The number of hidden layers is 3.
    </br>***Note:&nbsp;As seen in lecture, the number of layers is counted as the number of hidden layers + 1. The input and output layers are not counted as hidden layers.***
    - [ ] The number of layers L is 3. The number of hidden layers is 3.
    - [ ] The number of layers L is 4. The number of hidden layers is 4. 
    - [ ] The number of layers L is 5. The number of hidden layers is 4. 
</br>

7. During forward propagation, in the forward function for a layer ll you need to know what is the activation function in a layer (Sigmoid, tanh, ReLU, etc.). During backpropagation, the corresponding backward function also needs to know what is the activation function for layer ll, since the gradient depends on it. True/False?

    - [x] True
    </br>***Note:&nbsp;As you've seen in the week 3 each activation has a different derivative. Thus, during backpropagation you need to know which activation was used in the forward propagation to be able to compute the correct derivative.***
    - [ ] False
</br>

8. There are certain functions with the following properties: 

    - [x] True
    - [ ] False
</br>

9. Consider the following 2 hidden layer neural network:</br>
    ![Neural network](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8sF12nrfEeeumw4MySoK5g_36df26a0659f76c6566ff4f3706e6ad2_Screen-Shot-2017-08-05-at-12.50.32-PM.png?expiry=1617062400000&hmac=7WVOakam6jRLlTgbqYJJwBmBDgoFWU1siggitKXIiU0)
    Which of the following statements are True? (Check all that apply).
    
    - [x] W^[1] will have shape (4, 4)
    - [x] b^[1] will have shape (4, 1)
    - [x] W^[2] will have shape (3, 4)
    - [x] b^[2] will have shape (3, 1)
    - [x] W^[3] will have shape (1, 3)
    - [x] b^[3] will have shape (1, 1)
</br>

10. Whereas the previous question used a specific network, in the general case what is the dimension of W^{[l]}, the weight matrix associated with layer *l*?

    - [x] *W^[l]* has shape (*n^[l],n^[l−1]*)
