.. 注释 ():同位语  []:省略了 但其实是不可少的  {}:译者的话  "(x1,x2)":平面上的点坐标为(x1,x2)

人工神经元
==========================================================

.. toctree::

| in this video we will introduce the concept of an artificial neuron which is going to be the basic building block we will using to construct complicated neural networks

.. image:: picture/1_01_artificial_neuron.pdf.page2.png 
   :scale: 50%

| so an artificial neuron is simply a computational unit which will make a particular computation

| based on other units it's connected to

| so in the case of a signle artificial neuron like this one here

| it's going to be connected directly on an input description of some object we want to extract information from

| so this input description we'll call it X

| so here here both X is a _sense_ (essentially) a vector which contains the scalar x1 up to Xd where d is the size of the vector . ok.

| so notice that I'll be using bold as when I'm denoting vectors and matrices as well

| and whenever it's not involved and it corresponds to a scalar value. ok.

| so Xi is the i-th element of vector X

| and so this artificial neuron is going to read the information from this X vector and perform a particular computation which will dictate its value the value of the neuron and this value will essentially indicate whether some particular feature or information about the subject that we're manipulating is present or not in the object described by the vector X

| now the computation will perform can be decomposed into two steps there's going to be first a computation of pre activation of the neuron

| sometimes when you look at the literature you see the expression instead of input activation

| but I'll avoid using input activation because for X we often use also _the verb_ (the word) input to describe it

| so instead I'll talk about this as the pre activation

| and the pre activation which I'll note a of X for a given neuron is simply going to be some scalar b which we're going to call refer to the neuron bias plus product between a weight vector w with some the input vector x so we can write it into vector form here or we can write it into a more scalar form where we have b plus the summation over _all i_ (so all indices) within the vector of the i-th element of w times the i-th element of x and then from this pre activation the neuron will compute its activation which is sometimes referred to as the output activation of the neuron by simply taking the pre activation and passing it through a activation function so this g function here is what we're going to call activation function and are going to be different choices of potential activation functions we will be able to use

| so the output activation I will often know that as h of x and that will be the activation if I don't say output if I just say activation I _meet_ (mean) the output activation of a given neuron

| and so if we just put the expression for a of x explicitly there will be the activation function applied on this linear transformation of the input vector made of the elements Xi

| so w we will refer to it as the vector of connection weights and that's because as in this visualization here we can think of the elements of w as the strength of the connection between the neurons to which out neuron is connected to

| in this case these neurons would be input neurons there would be neurons that take the value of each of the element in input vector so w will be the vector of connection weights b will be a bias it's bias because (it's) if we have no input b would be the pre activation so by observing a particular input then we are essentially going away from this initial value b of the pre activation of the neuron and then as I said g will be the activation function


.. image:: picture/1_01_artificial_neuron.pdf.page3.png 
   :scale: 50%
 
| there is a 2d visualization of the activation of a neuron so imagine we have a vector made of two element x1 and x2 and then we'll notice y so I could have written instead h of x here as the output activation of the neuron so first thing we see here is that on this axis here we get values that are between minus 1 and 1 and that will be because in this specific example the range of values we can get once we pass the pre activation through the activation function is a number between minus 1 and 1

| and now what we see is that for different values of x we get a different output and specifically for all the values that lay here we get an output for the neuron an activation of minus 1 (...ai...) very close to minus 1

| and for all values of x here we get value of 1 so in this particular case we have a non-official (artificial ) neuron that detects whether some given input point x1 x2 belongs to this part of the space or this part of space so you can think of it as (...ai...) the artificial neuron as a binary classifier that separates points in one region and some other region for now we won't discuss how we actually find parameters of neuron that determine what regions it's actually separating so for now we'll just assume that someone have given us the value of the weight vector w and the bias vector b which determines the sharpe of this function and we'll see how we can actually have neurons that will train to discover good values of these parameters so fow now we'll just assume that someone have given us these values

| also geometrically it turns out that the vector w will actually be perpendicular with respect to the hyperplane in the space that separates these two regions that the neuron is distinguishing (is separating ) so this vector w determines essentially the orientation of this ridge between the two parts of the space that the neuron is separating and the bias b will essentially determine along this direction where the ridge will be (so if the bias is if the bias large) so when the bias is increasing then the ridge will be moving in the opposite direction of w so this would correspond to a perhaps negative value of b and if you have the more strongly positive value of b then the ridge would be moving in this direction okay so I won't exactly explain why this is but you can sit down and try to figure out why it is that w is perpendicular to this ridge and why is it that when b is decrease (is increasing ) then the ridge would be moiving this way so this is the description of the computation that the artificial neuron is performing

