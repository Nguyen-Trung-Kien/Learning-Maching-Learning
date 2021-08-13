# Hi bài này nói về tensorflow
là thư viện mã nguồn mở cho machine learning nổi tiếng nhất thế giới, được phát triển bởi các nhà nghiên cứu từ Google, nó có những phép toán mạnh mẽ để hỗ trợ cho maching learning, và điểm mấu chốt của ternsoflow là Computational Graph.

Trong quá trình thực thi của , tensorflow chia ra 2 phần để thực hiện
1. Xây dựng đồ thị (Graph)
2. Sử dụng 1 session để tinsh toán trong đồ thị

## xây dựng đồ thị
tensorflow sử dụng đồ thị để biểu diễn phép toán

Bao gồm các cạnh và các đỉnh, và các cạnh
1. Đỉnh (Node) đại diện cho biến đầu vào, phép tính toán
2. Các cạnh (Edge) đại điện cho dữ liệu truyền bên trong Graph

![image](https://user-images.githubusercontent.com/65381453/129317572-e9c40dcc-1c75-495f-ab7b-1a6c0f39e19f.png)

ví dụ:

```
import tensorflow as tf
a = tf.add(4, 5)
// Hoặc
import tensorflow as tf
x = tf.constant(3)
y = tf.constant(5)
a = tf.add(x, y)
```
![image](https://user-images.githubusercontent.com/65381453/129324335-a3b2400f-f5a4-4569-862b-165f0431a0f7.png)

## Sử dụng session
Sử dụng session để thực hiện tính toán với đồ thị để lấy ra các giá trị của a

```
import tensorflow as tf
a = tf.add(4, 5)
with tf.Session() as sess:
  print(sess.run(a))
```

*Chúng ta phải khởi tạo đầy đủ Graph trước khi đổ giá trị của các node(Tensor) vào trong Graph.*
## Thuật toán hỗ trợ 
1. Linear regression: tf.estimator.LinearRegressor
2. Classification: tf.estimator.LinearClassifier
3. Deep learning classification: tf.estimator.DNNClassifier
4. Deep learning wipe and deep: tf.estimator.DNNLinearCombinedClassifier
5. Booster tree regression: tf.estimator.BoostedTreesRegressor
6. Boosted tree classification: tf.estimator.BoostedTreesClassifier
