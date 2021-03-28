## Week 3 Quiz - Key concepts on Deep Neural Networks

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

