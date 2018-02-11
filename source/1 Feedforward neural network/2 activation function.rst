.. 注释     {}:译者的话 {.}:演讲者当时的动作        _xx_  _.yy.__ : 译者觉得要将xx换成yy才是对的, 可能是youtube自动翻译造成的错误、也可能是作者自己说错了、或别的啥


激活函数
==========================================================

.. toctree::
| in this video we'll see different potential choices for the activation function of neuron

| pic 1 : nn network pic 
| so we previously   the compuatation    that is made in the neuron      and we saw that involve this g function which we call the activation function      
| so here we'll just see different popular choices for activation functions in the neuron networks 

| pic 2: linear activation function pic
| a first choice is to simply use a linear activation function 
| so in this case the activation function g  {.上图公式g(a)=a中的g}  takes its pre-activation and simply outputs it 	
| so if we were to plot _the_ _.this._ activation function you get a straight line {.上图的斜直线} like this 
| so you doesn't perform any squashing {.squashing } of  the input _that is_  
| _. _it_ {.activation function} takes._ the input and reproduces _it_ {input}
| so it won't be upper bounded or lower bounded   
| and partly for that reason _it_'s {.activation function} not very interesting 
| it doesn't introduce any nonlinearities in the computation of    the neuron   which might be useful for performing more complicated computations 

| pic 3: sigmod function pic
| a more interesting choice is the sigmoid activation function
| so it takes this form {.sigm(a)=1/(1+exp(-a))} _which_
| _.so we'll._ some time noted as with acronym s-ig-m _and_ {不需要"and"} for short {."sigm("}
| and it simply takes the pre-activation {."(a)"}     and it computes this formula {."1/(1+exp(-a))"} here 
| so it's 1 over 1 plus the exponential of minus the pre-activation 
| and so if we draw {"function image"} this function   what we see is {"see" 还是 "is" ? } that it will squash {."squash"} the _neurons of the_ _.neuron's._  pre-activation   between 0 and 1
| we see {"image: y [0,1]"} that all output values are between 0 and 1 here 
| and so the bigger the pre-activation {."曲线 x right"}    the more it will saturate towards 1
| and smaller the _.pre._ activation {."曲线 x往左"} towards minus infinite    the more it will saturate towards 0 {."曲线 y 0"} instead
| so this neuron is always positive {."positive"}   because it's always strictly greater {."image y 0 上"} than 0
| it's bounded {."Bounded"} _that is the output of neuron_ _.the activation of the neuron cannot be smaller than 0    nor  greater than 1  {."曲线 y 0往下  1往上  "} 
| and this activation function is strictly increasing 
| that is    the bigger pre-activation    the higher the activation of the neuron will be  

| pic 4: tanh function 
| another popular choice is the     hyperbolic tangent  or   tange   
| so it's a t-a-n-h for short {."tanh"} 
| and it's slightly more complicated 
| it also involves  an exponential {."exp(a)"}
| so one form is this form  here  {."(exp(a)-exp(-a))/(..+..)"}       
|     _what's_  _.where._  the exponential the pre-cativation   minus   the exponential of minus the pre-activation    divided by    the sum of   the exponential of the pre-activaion     plus    the exponential of minus the pre-activation   
| and it can also be {."(exp(2a)-1)/(..+1)"} written in this form    which is more convenient     because it computes just one exponential    
| so 用这个 {."(exp(2a)-1)/(..+1)"}  {这句话 听不出来 youtube的自动翻译也是不对的}
| so it might be more computationally efficient 
| and this {."(exp(2a)-1)/(..+1)"} is just obtained by multiplying by the exponential of the pre-activation {. 分子 分母"(exp(a)-exp(-a))/(..+..)"} at the numerator and the denominator of this formula here {. 分子 分母"(exp(a)-exp(-a))/(..+..)"} 
| so _if you_ _.we._ plot this function   we see {."图像 y [1,-1] "}   that now we get an output  which is constrained between minus 1 and 1 
| so this neuron will say that   it squashes {."squash"} the neuron's pre-activation
|       so this should be pre-activation here {."squashed ... input between" 中的input划掉 并改为pre-activation}          
| between minus 1 and 1 
| so it can be positive or negtive  {."... positive ... negative"}
| it's also bounded      similarly like the sigmoid  activation function {."Bounded"}
| and it is also strictly increasing {."...increasing"}


| pic 5: rectified linear function
| and the final popular choice for the activation function  is   what is called the rectified linear activation function 
| so we noted reclin {."reclin(a)"} for short 
| and it's simply the maximum between 0 and the pre-activation {."max(0,a)"}
| and so if we plot it {"沿着图像两条折线"}      
| we get a straight line here {"沿着图像右边斜线"} like a linear function    if the input __is positive_     _is greater than 0__    {."图像 x 【0,正无穷)" } 
| and othersise it's just 0  {."沿着图像左边平线"}     so it's a __straight line_     _horizontal line__
| and if the _input_ {应该是pre-activation} is negative {."图像负半边"}    it always  outputs 0 
| so here it's {."Bounded"} only bounded by below by zero       
| so it's always non-negative    
| it's not upper bounded {."Not ... bounded"}    
|  because the greater the pre-activation here      the greater the output will be   {."沿右边斜线向右上方"}
| so _this can grow_    _.this always grows._     and    _can converge to_    _.the output can converge to._ or diverge towards infinite     if the _input_ {应该是pre-activation} goes  _towards the_ _.towards._ of the infinity 
| and in practice we see that it tends to give neurons {."Tends to give neurons ..."}                _that  are sparse_        _.that have sparse activities._         what we mean by that    is  that  it tends to get neurons  that are often exactly zero {."左边平线 y 0"}    which was not the case for the sigmoid or tanh     
| the sigmoid or the tanh need to have _pre-activations_ {这里应该是activation}   that are exactly a particular value 
| so in the sigmoid case to get zero _you need_ _.it needs._ to be minus infinite 
| so it doesn't happen really
| and for the _times_    _.tanh   it's._ to be equal to zero     in the pre-activation needs to be exactly zero 
| in this case   there's  this whole range  {."左边平线 x (负无穷,0]"}  of pre-activations    which will output exactly zero 
| so for this reason we often get zeros as the activation of the neuron across many different inputs 
| and so we'll say that for that reason  this neuron will have sparse activations or sparse activities



| and so those are four     different choices    popular choices   for the activation function of a neuron 