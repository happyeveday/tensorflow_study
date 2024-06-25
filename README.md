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
可见zip函数可以将向量合成，每个值由原先的向量决定
