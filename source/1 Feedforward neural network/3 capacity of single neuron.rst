.. 注释     
.. {;xx} : xx是译者添加的 作为补充   
.. ~.xx.~  {}:针对xx 译者要说的话          
.. ~.xx.~  {.}:针对xx 演讲者当时的动作         ;  "xx"表示演讲者标出了讲义中的xx 
.. ~.xx.~  #.yy.# : 译者觉得要将xx换成yy才是对的
.. ~.xx.~  #..yy.# : 译者觉得 youtube自动翻译造成的错误          
.. ~.xx.~  #;.yy.# : 译者觉得 按照作者意思 作者的表达错误 需要修改          
.. ~.xx.~  ~..yy..~:  xx和yy意思是一样的。本来只需要xx出现，或yy出现，不需要同时出现。比如为了不同角度的表达

单神经元能力
==========================================================

.. toctree::

| pic 1 
| in this video we'll discuss the capacity of a single neuron that is the complexity of the computations that it can perform.
| so we've seen before that in 2 dimensions  
| if we draw the ~.output or the activation.~ {. 图像 y1 h(x)} of a given neuron,    that will look something  like  this   
| where we'll get some ridge {画出岭} between two parts of the space       where the ridge    is essentially defined by the orientation of the ridge  is defined by the vector w   
| and     the bias will also determine the position of this ridge .

| pic 1.5: capacity,decision boundary of neuron
| so with a neuron that performs ~.a.~  #.this.# type of computation  
| we could perform binary classification {."binary classification"}               
|   ~.that is.~  #.if we use.# this sigmoidal activation function         we could inerpret the activation of a neuron as estimating   ~.the probability.~  {. "p(y = 1| x)"} that some input ~.x.~  {. "p(y = 1| x)"中的x} belongs to the class ~.1.~  {. "p(y = 1| x)"中的1 } .   
| and so let's assume ~.environment.~ #..in binary classification.#    ~.y can be either 0 or 1.~   {. 手写 " y 属于 集合{0,1}"}
| and then we could think of  ~.the output or the activation.~  {. "p(y = 1| x)"}  of a neuron as giving us what's the estimate of the ~.rear on.~ #..neuron.# that the input actually belongs to the category ~.1.~  {. "p(y = 1| x)"中的1 }. 
| and then the ~.property.~ #..probability.# that will belong to category 2  ~.based on the neurons.~ estimate would just be 1 minus this {. "p(y = 1| x)"}. 
| because probabilities must sum to 1.  
| and so we could do ~.this.~ {神经元的激活 解释为 属于类别1的概率} if we use sigmoid   because the sigmoid is ~.a bound.~  #;.bounded.# between 0 and 1. 
| and so we're always guaranteed  that we get   at the output or the  activation of a neuron   a number which can be interpreted as a probability .  
| so this in fact this exact form for a classifier  is known as logistic regression classifier {. "logistic regression classifier"}.  
| and  the way it's performing  classification is that     if the output of the neuron      so in other words    if its estimate of probability that x belongs to the class 1                is greater than 0.5 {."if greater than 0.5"中的0.5}
| then we will categorize the input into the class or category 1  {."predict class 1"中的1}.   
| and otherwise our classifier would output prediction that the input belongs to the class 0 .    
| and so if we were to draw this {右函数图像} in 2D  then if we looked at {;this} {."decision boundary"}  what is known  as decision boundary      .  where the decision boundary is essentially the surface {.右图像中灰白界线} where ~.the.~ #.some.# input can     equally belong to either class 0 or 1    could equally belong to any 2 class
| then what we would get acutally is        that's     the classifier is performing a linear classification           that is   it{此分类器}'s   drawn a line {.右图像中灰白界线} between two regions    the ~.regions.~ #.region.# {.右图像中白色区域R1} that is assoicial with one class       the other region {.右图像中灰色区域R2} that is assoicial with the other class             ~.in destroying.~  #..it{此分类器}'s drawing.# a boundary  {.右图像中灰白界线} which is actually linear.     
| so intuitive  corresponds to a line{.右图像中灰白界线}   and  in more dimensions would correspond to a hyperplane . 
| so if we have a problem where we want to classify objects described by input vectors into 2 diffenrent classes .   if we can draw a hyperplane or a line{.右图像中灰白界线} into the between  these two type of objects        then a single artificial neuron could do that{这个分类问题} for us.  it{此神经元} could model that type of desicion process.


| pic 2 : or and and 
| so here's few example of simple functions which can be modeled by a linear classifier .     
| so if we have a binary inputs that are either 0 or 1 {.OR图像, x1 x2, 0 1}     so we have x1 that can be 0 or 1 {.OR图像, x1, 0 1}    x2 that can be 0 or 1 {.OR图像, x2, 0 1}     
| and then we want to model the OR function {."OR(x1,x2)"中的OR} which takes the OR of x1 and x2 {."OR(x1,x2)"}.   
| so for 0 0 {.OR图像, x1,x2, 0 0} it would output 0 {.OR图像, 左下角圈圈} so that would be class 0.  and for 1 0 , 1 1 or 0 1 {.OR图像, x1,x2,1 0,1 1,0 1}  it would output 1 {.OR图像, 右侧三个三角形}.     so the triangles{.OR图像, 右侧三个三角形} are correspond to class 1 .     
| well we can see   that   if we draw this{.OR图像, 虚斜直线}   we can easily pass a line{.OR图像, 虚斜直线} between all the circles and all the triangles    all the 0 and all the ones.
| it's another function a bit  more complicated     the AND function over negation over x1 and x2 {."AND(x1_,x2)"}.     then we get that all of these guys {AND(x1_,..)图下三个小圈}  will be  of class 0  and this {AND(x1_,..)图下那个小三角形} will be class 1 .   and indeed again we can pass a line{.AND(x1_,x2)图像, 虚斜直线} between the two classes.   
| and we  have another example but instead of negation of x2 {. AND(.., x2_}      where we get  a class 1 here {AND(..,x2_)图下三角形}  and  the others {AND(..,x2_)图下三个圈圈} are 0 .    again we can pass a straight line{.AND(x1,x2_)图像, 虚斜直线} .
| so these sample functions can easily be model by a single artificial neuron .

| pic 3 : XOR XOR 
| however there are many problems in practice that are not will separated linearly .   
| actually they are very simple function that are not even a linearly seprable .  so as an example another simple function     the XOR {.左"XOR(x1,x2)"中的XOR} function      and  so this is a function that outputs 0 {.左XOR 两个圆圈} if either both inputs x1 and x2 are 0 {.左XOR,x1 x2,0 0} or they're both 1 {.左XOR,x1 x2,1 1} and it only outputs 1 so for these two gays {.左XOR 两个三角形} when there either one of the inputs are 1 {.左XOR 两个三角形}.    
| so in this case   here {x2轴 1} we have 1   here {x1轴 0} we have 0   for this point {左XOR 左上三角形}.        and here {x1轴 1} this one  x1 is 1  and x2 is 0  for this point {左XOR 右下三角形}.
| and so in this case we see that we cannot draw just a single line {左XOR试着画分割三角形和圆圈的各种一条直线 画不出}  that would actually separate on one side all of these zeros and on one side all the ones.  so it's not linearly separable .   
| and yet it's actually very very simple problem .    
| so this suggests that a single artificial neuron will not be sufficient for many problems that we want to perform this kind of binary classification.   
| however we notice    that  it's  such a simple function     that  if we had instead plotted on this axis {右XOR 横坐标轴} the result of applying  the AND function over the negation of x1 and x2  like we've seen in previous slide           and ~.on this axis {右XOR 纵坐标轴} we actually drew the.~   #.we use as.# the value of this axis    the output of AND function over x1 and negation of x2 {.右XOR 纵坐标轴 AND(x1,x2_)}.
| then this point {左XOR 左下圈圈 } and this point {左XOR 右上圈圈}  will be collapsed over a single point {右XOR 左下圈圈} .    and then this point {左XOR 左上三角形} will correspond now to that point {右XOR 右下三角形}    and this point {左XOR 右下三角形} to that point {右XOR 右上三角形}.
| and so in this case we could actually draw a single line {右XOR 虚斜直线} between the cirles {右XOR 左下圈圈} and triangles {右XOR 右上两个三角形}  between the points associated to class 0   and the points associated to class 1 .
| so what this is saying is that  ~.if we get.~   #.if we compute.#     ~.an alternate representation.~     #.a better {'a "better" representation'} repsentation.#  of our input vector  the problem might become linearly separable .      
| and this also suggests that  if we have  this {右XOR 纵AND}    this other{右XOR 横AND}  reperentation which is actually representable by a single neuron.      and that's the case for this AND function {右XOR 横轴AND} and this AND function {右XOR 纵轴AND}.      we've seen before that we can actually model these two functions by a single neuron.   
| then this suggests that      by ~.having other neurons.~    #.connected by other neurons.#   ~.which would.~      
| so  we have a neuron that compute this {右XOR 纵轴AND}    the neuron that computes that {右XOR 横轴AND}.      
| if    ~.we connected these two neurons {右XOR 横轴AND 纵轴AND} to another neuron {右XOR XOR}.~      #.connected {the  neuron} {右XOR XOR} directly to these artificial neurons {右XOR 横轴AND 纵轴AND} here.#     then we might be able to compute ~.a function.~   #. certain functions.#   that require ~.more complicated computations.~  #. more complicated desicion surface .#    .
| this will be the main intuition behind developing more complicated multi-layer neuron networks  which we'll see in next video.