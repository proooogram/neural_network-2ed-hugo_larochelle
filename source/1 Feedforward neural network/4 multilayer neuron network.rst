.. 注释     
.. {;xx} : xx是译者添加的 作为补充   
.. ~.xx.~  {}:针对xx 译者要说的话          
.. ~.xx.~  {.}:针对xx 演讲者当时的动作         ;  "xx"表示演讲者标出了讲义中的xx 
.. ~.xx.~  #.yy.# : 译者觉得要将xx换成yy才是对的
.. ~.xx.~  #..yy.# : 译者觉得 youtube自动翻译造成的错误          
.. #-.yy.# : 译者觉得 作者说错话了 试图用后面的词 来替代 yy    
.. ??yy??  : 译者没听出来 并用yy来占位
.. ~.xx.~  ~..yy..~:  xx和yy意思是一样的。本来只需要xx出现，或yy出现，不需要同时出现。比如为了不同角度的表达
.. Rimg : 右边图像
.. Limg : 左边图像


多层神经网络
==========================================================

.. toctree::








.. image:: picture/1_04_multilayer_neural_network.pdf.page2-xx.png
   :scale: 50%

in this video we'll formally introduce the multi-layer neural network. 
we see previously that there are certain problems that a single artificail neuron can not model well , 
because it's a problem which is saying a classifiation setting that is not linear separable .
however we've seen that we can actually take our input representation 
and try to (instead) transform it in some way  by applying some perhaps simple transformation {Rimg x y ; AND AND}.
like applying in this case here the AND {Rimg y ; AND} function   #-.over.#      
		to transform ??version?? of the input   
		to obtain the new representation of our input vector  which is now linearly separable .
and if the computation of this representation {Rimg x y ; AND AND }  can be made by artificial neurons , 
then this suggesting a more complicated model {Limg } for more complicated problems {Limg}   
	which would consist  in  first computing a set or a number of artificial neurons {Rimg x y; AND AND}     that will compute this new represetation 
and then connecting those neurons to an output neuron {Rimg XOR }    which would do the rest of job,   
and finish  the computation of our more complicated function .
so this will be the inspiration behind the use and development of multi-layer neural networks .


.. image:: picture/1_04_multilayer_neural_network.pdf.page3-shlnn.png
   :scale: 50%
   
so let's look at this idea more formally  in the case of a single hidden layer .
so what mean ??by?that?? the hidden layer    is the computation of this representation which will make the problem more linearly separable .
and so in the single layer neural network  we'll have the first part {Bottom2Layer} of the computation which will compute the representation.
and then finally the computation of our output unit {Top1Layer}   which will perform the computation of our binary classification .
so more formally when we're computing the hidden layer   we will compute again a pre-activation {"pre-activation"} function .
and now in this hidden layer {Middle_1_Lay} we see   here{Middle_1_Lay}  we might have several neurons not just a single neuron .
and so each of the i-th neuron {Middle_1_Lay ; h(x)i : "i" } _which_>that_    I will call whose    activation function   the output activation   will be h(x)i 
	will be connected to all potential inputs  {Bottom_1_Lay}.
and so the connection between the i-th  {Bottom_1_Lay and Middle_1_Lay ;   W(1)i,j : "i"  :: Middle_1_Lay i-th} hidden neuron with the j-th input {Bottom_1_lay j-th }
	will be contained in some matrix    which we will call W and indicates opponent in parentheses one {W(1)i,j : "(1)"  }.
so this {W(1)i,j : "(1)"} is to refer to the case where we have just a single hidden layer . 
so W1 is the weight matrix for the first hidden layer .
and similarly we will have biases {"b(1)i"}.
and so the bias of the i-th {Middle_1_Lay h(x)i neuron} hidden unit will be bi     and the one here {"b(1)i":"(1)"}   and the exponent{"b(1)i":"(1)"} is to refer to the first hidden layer again.
{start to explain Left}
so whenever we are computing the pre-activation , we will actually have a vector {"a(x)=b(1)+W(1)x":"a(x)"} of pre-activation     
	where the i-th {"a(x)i=b(1)i+sum W(1)i,j xj":"a(x)i":"i"} element of that vector will the i-th pre-activation  for the i-th neuron in that hidden layer ,
and i-th pre-activation will get    the i-th bias   plus  the weighted combination of all inputs xj  
	and where xj will be multiplied  by its connection with the i-th neuron .
and if we want to perform this computation {"a(x)i=b(1)i+sum W(1)i,j xj"} for each hidden unit .
so in fact we can write it into matrix form {"a(x)=b(1)+W(1)x"} to obtain directly the pre-activation vector  {"a(x)=b(1)+W(1)x":"a(x)"}.
and this {"a(x)=b(1)+W(1)x"} would only essentially correspond to taking the vector x {"a(x)=b(1)+W(1)x":x} multiplying it by our matrix w(1) {"a(x)=b(1)+W(1)x":w(1)} and then adding the whole vector of biases b(1) {"a(x)=b(1)+W(1)x":b(1)}.
so indeed if we take x {M} and mutiply by w {M}, 
	we will get is 
		that for the i-th row  will get a term which corresponds to the sum of all the elements over that row of matrix w1 multiplied by the corresponding elements in the vector x.
ok so we see that this {"a(x)=b(1)+W(1)x"} and this {"a(x)i=b(1)i+sum W(1)i,j xj"} is actually equivalent .
{start Left h(x)=g(a(x))}
then to compute the hidden layer activation {"Hidden layer activation"}		.
we simply apply our activation function {"h(x)=g(a(x))":g} over all the elements in the vector {"h(x)=g(a(x))":a(x)} .
so here in my notation {"h(x)=g(a(x))":g(a(x))} , I' assuming we're doing an element-wise application of the activation function g {"h(x)=g(a(x))":g} 
	that we've chosen either the sigmoid or the tanh or reclin and so on.