## Week 2 Quiz - Deep convolutional models

1. Which of the following do you typically see as you move to deeper layers in a ConvNet?

    - [ ] $n_H$ and $n_W$ increases, while $n_c$ also increases
    - [ ] $n_H$ and $n_W$ increases, while $n_c$ decreases
    - [ ] $n_H$ and $n_W$ decreases, while $n_c$ also decreases
    - [x] $n_H$ and $n_W$ decreases, while $n_c$ increases

2. Which of the following do you typically see in a ConvNet? (Check all that apply.)

    - [x] Multiple CONV layers followed by a POOL layer
    - [ ] Multiple POOL layers followed by a CONV layer
    - [x] FC layers in the last few layers
    - [ ] FC layers in the first few layers

3. In order to be able to build very deep networks, we usually only use pooling layers to downsize the height/width of the activation volumes while convolutions are used with “valid” padding. Otherwise, we would downsize the input of the model too quickly.

    > should be "SAME" padding

    - [ ] True
    - [x] False

4. Training a deeper network (for example, adding additional layers to the network) allows the network to fit more complex functions and thus almost always results in lower training error. For this question, assume we’re referring to “plain” networks.

    > should be skip connection

    - [ ] True
    - [x] False

5. The following equation captures the computation in a ResNet block. What goes into the two blanks above?

    $$a^{[l+2]} = g(W^{[l+2]} g(W^{[l+1]} a^{[l]} + b^{[l+1]}) + b^{[l+2]} + \_) + \_$$

    $a^{[l]}$ and 0, respectively

6. Which ones of the following statements on Residual Networks are true? (Check all that apply.)

    - [ ] A ResNet with L layers would have on the order of $L^2$ skip conncections in total.
    - [x] Using a skip-connection helps the gradient to backpropagate and thus helps you to train deeper networks.
    - [ ] The skip-conncetions compute a complex non-linear function of the input to pass to a deeper layer in the network.
    - [x] The skip-connection makes it easy for the newwork to learn an identity mapping between the input and the output within the ResNet block.

7. Suppose you have an input volume of dimension 64x64x16. How many parameters would a single 1x1 convolutional filter have (including the bias)?

    16 + 1 = 17

8. Suppose you have an input volume of dimension $n_H \times n_W \times n_C$. Which of the following statements you agree with? (Assume that “1x1 convolutional layer” below always uses a stride of 1 and no padding.)

    - [ ] You can use a pooling layer to reduce $n_H$, $n_W$, and $n_C$.
    - [x] You can use a pooling layer to reduce $n_H$, $n_W$, but not $n_C$.
    - [x] You can use a 1x1 convolutional layer to reduce $n_C$ but not $n_H$, $n_W$.
    - [ ] You can use a 1x1 convolutional layer to reduce $n_H$, $n_W$ and $n_C$.

9.  Which ones of the following statements on Inception Networks are true? (Check all that apply.)

    - [ ] Making an inception network deeper (by stacking more inception blocks together) should not hurt training set performance.
    - [x] A single inception block allows the network to use a combination of 1x1, 3x3, 5 x 5 convolutions and pooling.
    - [ ] Inception networks incorpoarates a variety of network architectures (similar to fropout, which randomly cheeses a network architecture on each step) and thus has a similar regularizing effect as dropout.
    - [x] Inception block usually use 1x1 convolutions to reduce the input data volume's size before appliying 3x3 and 5x5 convolutions.

10. Which of the following are common reasons for using open-source implementations of ConvNets (both the model and/or weights)? Check all that apply.
    - [ ] The same techniques for winning computer vision competitions, such as using multiple crops at test time, are widely used in practical deployments (or production system deployments) of ConvNets.
    - [x] Parameters trained for one computer vision task are often usedful as pretraining for other computer vision tasks.
    - [ ] A model trained for one computer vision task can usually be used to perform data augmentation even for a different computer vision task.
    - [x] It is a convenient way to get working an implememntation of a complex ConvNet architecture.
