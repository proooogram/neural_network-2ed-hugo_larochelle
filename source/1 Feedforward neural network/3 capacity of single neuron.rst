.. 注释

单神经元能力
==========================================================

.. toctree::

| pic 1 
| this video we will discuss capacity of single neuron that is complexcity of computation it can perform.
| so we see before that in 2 demintions  
| if we draw the output of activation of a giving neuron    there will be something look like  this   
| ... we will get some ridge between two part of the space where the ridge essentionlly define by the ori...tation of ridge  define by vector w   
| and bias also determe the persition of this ridge 
| so with a neuron that perform this type of computation  
| we could be called binary classification   ~.that is.~  #.if use.# sigmoid activation function     
| we could inerpret the activation of neuron as estimating   the propbility that some input x belongs to the class 1    
| so let's assume in binary classification  y can be etheir zero or one   
| and  we could think of the output of the activation of neuron as giving us what's the estimate neuron that the input actually belong to the category one. 
| and then the probility that will belong to category two ~.base on the neuron.~ that ... just be 1 minus this. 
| because propbility must sum to 1.  
| and so we could do this if we use sigmoid   because sigmoid is a bound between 0 and 1. 
| and so we also g...r...t  that we get the output of the  activation of neuron   a number which can interpret as propbility .  
| so this in fact  exactly form for a classifier  is known as logistic regression classifier.  
| and  the weight performing  classification is that if the output of neuron   so in other words  ~.if.~ #.it is.# the estimate of propbility that x belong to the class 1  is greater than zero point five  
| then we will category the input into the class or category 1  .   
| another wise our classifier would ~.output.~ #.prediction.# the input belongs to class 0 .    
| and so if we were to draw this in 2D  then ~.if we look at .~  #.what is known.#  as decision boundary     .  where the decision boundary is essentially the surface where some input can     equally belong to the class 0 or 1    equally belong to any 2 class
| what we get acutally is that's the classifier is performing a linear classification  that is drawn a line between two regions   the region that is assoicial with one class       the other region that is assoicial with the other class     it's drawing a boundary which is actually linear.     
| so in 2D  correspond to a line   and  in more dimensions it correspond to a hyperplan .   
| so if every problem where we want to classify objects describe by input vectors into 2 diffenrent classes .   if we can draw a hyperplan or a line ~.into.~ #.between.#  these two type of objects   then a single artificial neuron could do that for us.  it could model that type of desicion .


| pic 2 : or and and 
| so there is few example of simple functions which can be model by a linear classifier .     
| so if we have a binary inputs that are either zero or one     so we have x1 that can be 0 or 1     x2 that can be 0 or 1      
| and then we want to model the OR function which take the OR of x1 and x2 .   
| so for 0 OR 0  it will output 0  so that will be class 0.  and for 0 1 , 1 1 or 1 0  it will output 1 .     so the trangles are correspond to class 1      
| ... we can see that if we draw this  we can easyly pass a line between all the circles and all the trangles    all the 0 and all the ones.
| it's another function that'll be more complicated     AND function over negation over x1 and x2 .     then we get all the these gays {AND(x1_,..)图下三个小圈}  will be  of class 0  and this {AND(x1_,..)图下那个小三角形} will be class 1 .   and ... again we can pass line between the two classes.   
| ... get another example but instead of negation of x2 {. AND(.., x2_}      where we get  a class 1 here {AND(..,x2_)图下三角形}    the others {AND(..,x2_)图下三个圈圈} are 0 .    again we can pass a straight line .
| so these sample functions can easyly be model by a single artificial neuron 

| pic 3 : XOR XOR 
| however there are many problems in practice that are not will sperated linearly .   
| actually they are very simple function that are not even linearly seprable .  so ...there... is another simple function     the XOR function .  so this is a function that output 0 if either both inputs x1 and x2 are 0  or they are both 1  and it only outputs 1 so for these two gays when the either one of the inputs are 1 .    
| so in this case   here {x2轴 1} we have 1   here {x1轴 0} we have 0   for this point {左XOR 左上三角形}        here {x1轴 1} this one  x1 is 1  and x2 is 0  for this point {左XOR 右下三角形}.
| and so in this case we see that we cannot draw just a single line {左XOR画分割点的各种一条直线}  that will actually separate on one side all ... be 0 and one side all ... 1.  so it's not linearly separateble .   
| and yet ...say... actually very very simple problem .    
| so this suggest that single artificial neuron will not be sufficient for many problems that we are want to perform this kind of binary classification.   
| however we known ~.it that's.~   #.it's.#  a such simple function  ~.that.~   #.if.# we had instead plot on this axis {右XOR 横坐标轴} the result of apply AND function over negation of x1 and x2  like we see in previous ...lin...        and on this axis {右XOR 纵坐标轴} ~.we actually draw the.~   #.we use as.# the value of this axis    the output of AND function over x1 and negation of x2 .
| then this point {左XOR 左下圈圈 } and this point {左XOR 右上圈圈}  will be clasp over a single point {右XOR 左下圈圈} .    and then this point {左XOR 左上三角形} will correspond now to that point {右XOR 右下三角形}    and this point {左XOR 右下三角形} to that point {右XOR 右上三角形}.
| and so in this case we can actually draw a single line {右XOR 虚斜直线} between the cirles {右XOR 左下圈圈} and trangles {右XOR 右上两个三角形}  between the points associated to class 0   and the points assocated to class 1 .
| so what it saying is that  ~.if we get.~   #.if we compute.#     ~.an altinate repesentation.~     #.a better repsentation.#  of our input vector  the problem might be linearly sperateble .      
| and this also suggest that  if we have  these {右XOR 两轴 两AND}  the ...sad... reperentation which is actually repsentable by a single neuron    that's the case for this AND function {右XOR 横轴AND} and this AND function {右XOR 纵轴AND}      we see before that we can actually model these two functions by a single neuron   
| then this suggest that      by ~.having other neurons.~    #.connecting by other neurons.#   ~.which would.~      
| so we have the neuron that compute this {右XOR 纵轴AND}    the neuron that compute that {右XOR 横轴AND}.      
| if    ~.connect the these two neuron {右XOR 横轴AND 纵轴AND} to another neuron {右XOR XOR}.~      #.connecte {the  neuron} {右XOR XOR} directly to these artificial neurons {右XOR 横轴AND 纵轴AND} here.#     then we might able to compute ~.a function.~   #. ...s...l function.#   that require ~.more complicated computations.~  #. more complicated desicion surface .#    .
| this will be the main inituition behind developing more complicated multi-layer neuron networks  which we will see in next video.