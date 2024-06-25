# tensorflow_study
# 6月25日
1.zip的用法\
将两个数或向量合成，整合成一个向量\
例如：\
a=tf.constant([1.0,2.0,3.0])\
b=tf.constant([0,1,2])\
ZIP=zip(a,b)\
zip_list=list(ZIP)\
则zip_list=[(<tf.Tensor: shape=(), dtype=float32, numpy=1.0>, <tf.Tensor: shape=(), dtype=int32, numpy=0>), (<tf.Tensor: shape=(), dtype=float32, numpy=2.0>, <tf.Tensor: shape=(), dtype=int32, numpy=1>), (<tf.Tensor: shape=(), dtype=float32, numpy=3.0>, <tf.Tensor: shape=(), dtype=int32, numpy=2>)]\
可见zip函数可以将向量合成，每个值由原先的向量决定\
2.关于tf.constant函数\
创建一个常量，常量的值由dtype决定\
例如：\
import tensorflow as tf\
a=tf.constant([1,2,3],dtype=tf.float32)\
此时a的数值类型为float32而不是创建时写的int32\
import tensorflow as tf\
a=tf.constant([1.0,2.0,3.0],dtype=tf.int64)\
此时报错，因为float无法转化为int型
