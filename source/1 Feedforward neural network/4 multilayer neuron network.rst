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
so what mean 