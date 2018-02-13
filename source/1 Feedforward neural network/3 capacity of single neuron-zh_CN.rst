.. 注释     
.. {;xx} : xx是译者添加的 作为补充   
.. ~.xx.~  {}:针对xx 译者要说的话          
.. ~.xx.~  {.}:针对xx 演讲者当时的动作         ;  "xx"表示演讲者标出了讲义中的xx 
.. ~.xx.~  #.yy.# : 译者觉得要将xx换成yy才是对的
.. ~.xx.~  #..yy.# : 译者觉得 youtube自动翻译造成的错误          
.. ~.xx.~  ~..yy..~:  xx和yy意思是一样的。本来只需要xx出现，或yy出现，不需要同时出现。比如为了不同角度的表达

单神经元能力
==========================================================

.. toctree::

| pic 1 
| 在这个视频中 我们会讨论单神经元的能力 {这能力}即神经元能执行的计算的复杂性
| 上次课， 我们已经看到 在二维空间， 
|         如果我们画一个给定神经元的输出或激活{. 图像 y1 h(x)} ，  会看到像这样的图像，
|         在这图像中 我们会获得 在空间两部分之间的 岭{画出岭} ，   在这图像中    岭   完全被岭的方向定义  被向量w定义    
|         且 {在这图像中} 偏执决定了岭的位置

| pic 1.5: capacity,decision boundary of neuron
| 带有 执行这种类型计算 的神经元
| 我们能执行二分类 {."binary classification"}   
| 如果我们用这个sigmoid激活函数   我们能解释 一个神经元的激活 为 估算   某个输入向量x {. "p(y = 1| x)"中的x} 属于类别1 的 概率{. "p(y = 1| x)"} .
| 让我们假定 在二分类中 y为0或1  {. 手写 " y 属于 集合{0,1}"}
| 然后我们考虑 一个神经元的输出或激活 {. "p(y = 1| x)"} 为 给我们                输入属于类别1{. "p(y = 1| x)"中的1 }  此神经元的估算是多少 .
| 属于类别2的 概率估值 是 1减去这个{. "p(y = 1| x)"}.
| 因为 概率必须和为1
| 所以 如果用sigmoid 我们能做这 {神经元的激活 解释为 属于类别1的概率}  因为sigmoid介于0和1之间
| {;它}总是向我们保证 在一个神经元的激活或输出    我们得到一个 能被解释为一个概率的 数
| 实际上    一个分类器的 这精确的形式         是以   logistic回归分类器 {. "logistic regression classifier"}   被知道的
| 它执行分类的 方式 是      如果神经元的输出      换句话说     如果神经元的 x属于类别1的概率 估值  大于0.5  {."if greater than 0.5"中的0.5}
|       则我们会 归类 输入 到 类别1 {."predict class 1"中的1} .
| 否则 我们的分类器将输出 输入属于类别0的 预测
| 如果我们 在二维中 画这{右函数图像}      如果我们看这{."decision boundary"}即决策边界  {在这个函数图像中}此决策边界本质上是 某输入对等的属于0或1 对等的属于任意类别 的表面
| 我们获得的实际上是    此分类器在执行一个线性分类        它{此分类器}画了 在两个区域间的 一条直线 {.右图像中灰白界线}     一个区域是和一个类别关联的  另一个区域是和另一类别关联的        它{此分类器}在画一个 实际为线性的 边界 
| 直观上 {决策边界}是一条直线        在多维时 {决策边界}会是一个超平面 
| 如果我们有一个   我们想 分  由输入向量描述的物体 到 两个不同类别 的    问题 .  如果我们能 画 一个超平面或一条直线 进 这两物体类别之间 .  那么 一个单人工神经元 能 为我们 做这{这个分类问题}. 它{此神经元}能 建模 这种决策过程.



| pic 2 : or and and 
| 这是 一些   能被一个线性分类器建模的 简单函数的  例子
| 如果我们有一个二维输入，该输入的 每维量为0或1  {.OR图像, x1 x2, 0 1}     故我们有 能为0或1的x1 {.OR图像, x1, 0 1}   能为0或1的x2{.OR图像, x2, 0 1} 
| 然后我们想 建模    取x1或x2的{."OR(x1,x2)"}  "或"函数{."OR(x1,x2)"中的OR}   
| 所以 对于 0 0    {.OR图像, x1,x2, 0 0}     该分类器会输出0{.OR图像, 左下角圈圈}  所以这是类别0          而 对于  1 0 , 1 1 or 0 1 {.OR图像, x1,x2,1 0,1 1,0 1} 该分类器会输出1 {.OR图像, 右侧三个三角形}.        所以 三角形们{.OR图像, 右侧三个三角形}相当于类别1
| 好了 我们能看到 如果我们画这{.OR图像, 虚斜直线}      我们很容易  在 所有圆圈和所有三角形 所有0和所有1 之间 打通一条直线
| 它是另一个 有点复杂的 函数{.AND(x1_,x2)}  取x1非、x2的与 .     然后 我们得到     所有这些家伙 {AND(x1_,..)图下三个小圈} 会是类别0           这个 {AND(x1_,..)图下那个小三角形} 会是类别1.   事实上 又一次  我们能 在两类别之间 打通一条直线{.AND(x1_,x2)图像, 虚斜直线} .
| 我们有另一个例子 {也是"与"函数} 但x2取非    ，  此函数  在这{AND(..,x2_)图下三角形} 我们得到一个类别1   在其他处 {AND(..,x2_)图下三个圈圈} 是类别0.     我们也能 {在两个类别之间} 打通 一条直线 {.AND(x1,x2_)图像, 虚斜直线} .
| 这些例子函数能很容易的 被 一个单人工神经元 建模

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