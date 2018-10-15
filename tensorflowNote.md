# Tensorflow语法

---

##  一 程序结构

1. 赋值 (y = 39)
> y = tf.constant(39,name='y')

2. 创建变量(loss = (y - y_hat).2)

 > loss = tf.Variable((y - y_hat) ** 2,name='loss')

3.  初始化

 > init = tf.global_variables_initializer()

4. 惯用写法

 >  with tf.Session() as session:
 >
 >    session.run(init)
 >
 >    print(session.run(loss))

5. 使用tensorflow编程的步骤

  a. 创建尚未被执行的变量；

     Create Tensors(Variables) that not yet executed/evaluated.

  b. 写下变量之间的操作（运算）；

    Write operations between those Tensors.

  c. 初始化变量；

    Initialize your Tensors.

  d. 创建一个session；

  Create a Session.

  f. 运行session，你写下的变量的运算会随之运行。

  Run the Session.This will run the operations you'd written above.

6. 使用placeholder来稍后为变量赋值

  创建一个placeholder

  > x = tf.placeholder(tf,int64,name = 'x')

  在后续操作中为x赋值(feed data)

  > print(sess.run(2 * x,feed_dict = {x:3}))

  > sess.close()

  为两个变量赋值

  >sess.run(cost,feed_dict{z : logits,y : labels})

## 二 函数
1. 矩阵相乘

 > tf.matmul(...,...)

2. 加法

 > tf.add(...,...)

3. 创建session

 > tf.Session()

4. 运行session

 > session.run(...)

5. 创建placeholder

 > tf.placeholder(tf.float32,shape = (...,...),name = '...')

6. 计算sigmoid函数

 > tf.sigmoid(...)

  计算reLU函数

  > tf.nn.relu(...)

7. feed data

 > sess.run(...,feed_dict = {x : z})

8. 使用session的两种方式

 method 1 :

 > sess = tf.Session()
 >
 > result = sess.run(...,feed_dict = {...})

 method 2 :

 > with tf.Session() as sess:
 >
 >  result = sess.run(...,feed_dict = {...})

9. 交叉验证损失

 >  tf.nn.sigmoid_cross_entropy_with_logits(logits = ...,labels)

10. one_hot 矩阵生成

 > tf.one_hot(labels,depth,axis = 0)

11. 初始化元素值为1的矩阵

 > tf.ones(shape)

12. 初始化元素值为0的矩阵

 > tf.zeros(shape)

13. 初始化

 xavier初始化

 > W1 = tf.get_variable("W1",[25,12288],Initializer = tf.contrib.layers.xavier_initializer(seed = 1))

 0初始化

 > b1 = tf.get_variable("b1",[25,1],Initializer = tf.zeros_initializer())

## 卷积神经网络

1. 卷积

 > tf.nn.conv2d(X,W1,strides = [1,s,s,1],padding = 'SAME')

2. 最大池化

 > tf.nn.max_pool(A,ksize = [1,f,f,1],strides = [1,s,s,1],padding = 'SAME')

3. relu  

 > tf.nn.relu(Z)

4. 展开成一维

 > tf.contrib.layers.flatten(P)

5. 全连接

 > tf.contrib.layers.fully_connected(F,num_outputs)

6. softmax交叉验证损失

 > tf.nn.softmax_cross_entropy_with_logit(logits = Z3,labels = Y)
 >
 >tf.reduce_mean 
