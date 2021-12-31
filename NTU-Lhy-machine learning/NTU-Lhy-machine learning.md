- [Lecture 1 (introduction)](#lecture-1)
- [Lecture 2 (liner regression/Model/Result/Error)](#lecture-2)
- [Lecture 3 (Bias/Variance)](#lecture-3) 

## Lecture 1

Teacher：Professor 李宏毅    
Exercise/Matlab/syllbus/video: **[http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML20.html](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML20.html)**

* show up a picture of this class;(as below)		
* 机器学习就是自动找到函数来将“输入”一一对应正确的“输出”		
* 可以是Regression/Binary classification(二选一yes/no)/Multi-class classification(多选:面包鸡蛋牛奶)/Generation(GAN生成二次元头像)		
* 需要基于Label Data的Supervised Learning，他需要基于人类的Task去评判他的Performance；那么就有一个评判标准，**例如计算这个函式的loss**；		
* Reinforcement Learning就是人类也不知道哪个对那个错，要自己去想办法去通过reward来引导自己的学习，从而提高自己的正确率；
* 给机器一大堆没有label的数据，那到底会给出什么东西，就是un-supervised learning；（用GAN去Generate些东西）		
* 所谓的搜寻需要给出一个范围，这个范围就由**Network Architecture**来提供；		
* 有现成的algorithm--Gradient Descent；	
*		
* Explainable AI （解释下为什么选对了）；		
* Adversarial Attack (如果战胜一些人为的刻意攻击)；		
* Network Compression (模型训练得太大了，放不进手机里边)；		
* Anomaly Detection (机器人能否知道自己不知道一些东西**过于哲学**)；
* Transfer Learning （用数据库里的数据训练好模型后遇到数据库之外的数据，能否很好地迁移）；			
* Meta Learning (能够自己学习“如何学习”，当今的学习其实不算特别有效，但是不是由于人类自身的限制呢？所以思考着能否用人工智慧自己来训练自己的学习方法)；		
* Life-Long Learning (解决一连串问题);

![](/picture/introduction.png)

## Lecture 2

1. Model；
2. Goodness of Function；
3. Gradient Descent；		
	* 先随机选取一个w0；
	* 计算该点的切线斜率，显然左边loss左边比较低，右边比较高；显然就右移；(但是否会陷入局部最优解，极小值)	
	* 往右移动取决于2个因素；“learning rate”和“当前斜率大小”；	
	* local optimal和global optimal；	
	* 两个参数的情形，就是分别做偏微分；		
	* 把两个偏微分上下拍成向量形式:(如下图）
	* 但不用担心，**liner regression其实是没有local optimal的**，也就是只有一个碗；			
4. 结果如何？如何在Training data提升一下，使得能够在Testing data上有更低的Average error；
5. 用复杂的程式在Training data上能够很好拟合，但却在Testing data上却有更大的error；或甚至出现了不合理的预测值；(过拟合overfitting)
6. 对物种进行了分类；不同的物种采用不同的函式去拟合；

----------
1. Redesign the Model重新整合一下model；
2. Regularization(想要一个比较平滑的函数)


	* ![](https://github.com/zarjun/Motivated-Learning/blob/main/NTU-Lhy-machine%20learning/picture/gradient.png)；
	* ![](https://github.com/zarjun/Motivated-Learning/blob/main/NTU-Lhy-machine%20learning/picture/gradientglobal.png)；
	* ![](https://github.com/zarjun/Motivated-Learning/blob/main/NTU-Lhy-machine%20learning/picture/complicatedmodel.png)；	

## Lecture 3

1. Bias and Variance of Estimator；(s^2估测σ^2)bias就是你瞄的时候就没有瞄准，variance就是你子弹出膛之后仍然会有偏差；	
2. 很直觉：简单的model实际上受到data的影响反而更小，即variance更小；		
3. 定义一个model的时候就定义了一个范围，简单的model取值的均值跟实际靶心差距较大，复杂的model取值的均值最后反而就是跟实际靶心差距较小，射程更广了。			
4. Overfitting==variance大/Underfitting==bias比较大，根本没办法很好拟合testing data;			
5. Data的数量增加一般都能够降低variance(**假如没办法搜集？**或使用Regularization的方法将曲线平滑但这可能无法兼顾bias)		
6. Training Set(Training Set 训练模型 + Validation Set 选模型)//Testing Set(public)//Testing Set(private)。如果将Training Set的model apply to Testing Set发现error太大之后，你还回去修改的话，那么其实你最终的模型就无法很好地反映private Testing Set；	
7. 	
	* ![](https://github.com/zarjun/Motivated-Learning/blob/main/NTU-Lhy-machine%20learning/picture/biasandvariance.png);		
	* ![](https://github.com/zarjun/Motivated-Learning/blob/main/NTU-Lhy-machine%20learning/picture/underfittingoverfitting.png);			* ![](https://github.com/zarjun/Motivated-Learning/blob/main/NTU-Lhy-machine%20learning/picture/TestingSet.png)	;				* ![](https://github.com/zarjun/Motivated-Learning/blob/main/NTU-Lhy-machine%20learning/picture/validation.png)	;			
