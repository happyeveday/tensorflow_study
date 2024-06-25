# tensorflow_study By Yang
## 6月25日
###1.zip的用法  
将两个数或向量合成，整合成一个向量  
例如：  
a=tf.constant([1.0,2.0,3.0])  
b=tf.constant([0,1,2])  
ZIP=zip(a,b)  
zip_list=list(ZIP)  
则zip_list=[(<tf.Tensor: shape=(), dtype=float32, numpy=1.0>, <tf.Tensor: shape=(), dtype=int32, numpy=0>), (<tf.Tensor: shape=(), dtype=float32, numpy=2.0>, <tf.Tensor: shape=(), dtype=int32, numpy=1>), (<tf.Tensor: shape=(), dtype=float32, numpy=3.0>, <tf.Tensor: shape=(), dtype=int32, numpy=2>)]  
可见zip函数可以将向量合成，每个值由原先的向量决定  
###2.关于tf.constant函数  
创建一个常量，常量的值由dtype决定  
例如：  
import tensorflow as tf  
a=tf.constant([1,2,3],dtype=tf.float32)  
此时a的数值类型为float32而不是创建(1,2,3)时的int32  
import tensorflow as tf  
a=tf.constant([1.0,2.0,3.0],dtype=tf.int64)  
此时会报错，因为int型隐式转化为float型是可行的，而float型转化为int型需要进行显式转化，例如对常量a中的每一个值都进行显式转化:  
float_values = [1.0, 2.0, 3.0]  
int_values = [int(value) for value in float_values]  
a = tf.constant(int_values, dtype=tf.int32)  
再次编译，成功运行  
