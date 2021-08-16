# Bài này mình sẽ nói về bài toán hồi quy
đi vào ví dụ để hiểu nhé

ví dụ có 1 mẫu 6 trẻ em có tuổi từ 1-6 với cân nặng như sau

![image](https://user-images.githubusercontent.com/65381453/129469943-6b92126a-481c-4705-a50e-d3a2436c4ace.png)

Thì lưu đồ data sẽ như sau

![image](https://user-images.githubusercontent.com/65381453/129478617-13d1300a-606b-4799-af6e-a68673c87e17.png)

Khi nối lại nó đi theo đường ziczac

![image](https://user-images.githubusercontent.com/65381453/129479422-838cbd2e-d5fb-42a4-bd89-6408cdfe8ea2.png)

theo mẫu trên nếu ta cho 1 dữ liệu là một trẻ em có tuổi là Y và cân nặng là X thì để tìm được Y ta có công thức như sau
```
Y = aX +b
```

Y và X đều là ma trận hoặc vector

vì vậy để tìm ra Y thì ta phải sử dụng hàm số dự đoán để train, và đầu ra chính là Y có thể xẩy ra.

, theo hình trên ta thấy rằng nó không đi theo đường thẳng, có nghĩa là độ chính xác của nó không đạt mức 100%, bởi vì có sự sai lệch ở một số điểm, sự sai lệch này được gọi là phần dư (residual) hoặc errors.

## Hàm mất mát (Loss Function)

là giá trị được trả về là 1 số không âm, thể hiện mức độ chênh lệch giữa giá trị mà model của ta dự đoán và giá trị thực tế

![image](https://user-images.githubusercontent.com/65381453/129480147-4236bc5d-ab43-42ac-9e47-c3f34cb2f28c.png)

vậy ta có thể khẳng định rằng, 
```
Nếu phần dư càng nhỏ thì mối liên hệ giữa x,y càng lớn và ngược lại
```

![image](https://user-images.githubusercontent.com/65381453/129480933-f2873e92-1a7b-4b49-b870-8dc3774642b7.png)

*howkteam*

Thông thường để giá trị được tính toán nhanh hơn thì sẽ biến X là input đầu vào trở thành ma trận 

![image](https://user-images.githubusercontent.com/65381453/129481022-7ef157a3-109b-4e8c-a74a-69e362586a7e.png)

công thức pheta

![image](https://user-images.githubusercontent.com/65381453/129485328-b73bf349-9492-4ad5-ae49-128179b702c8.png)


### Đi vào thực tế nha

vẫn là bài toán cũ, nhưng mình sẽ cho dữ liệu nhiều hơn 1 tý

![image](https://user-images.githubusercontent.com/65381453/129485338-d13ab4a8-9346-4458-876d-9b108ffb6135.png)

Gọi X là số cân nặng  , và độ tuổi là Y. Gọi hàm  y^ là hàm sẽ dự đoán:

![image](https://user-images.githubusercontent.com/65381453/129485441-564d589d-eece-41fe-97d7-46878ff60e41.png)

*thêm cột ones để có thể nhân ma trận*

Đầu tiên: 

1. Mô phỏng X bằng numpy

![image](https://user-images.githubusercontent.com/65381453/129486234-db1df700-9bf5-4e92-9c8f-b4f2629e43dc.png)
```
X0 = np.array([[10],[13],[15],[20],[23],[26],[28],[37],[40],[33],[45]])

ones = np.ones((11,1) ,dtype=int)
```
Tiếp theo là nối theo chiều dọc
```
X = np.concatenate((X0,ones),axis=1)
```
Kết quả
![image](https://user-images.githubusercontent.com/65381453/129486293-11a6bc89-784e-45a5-875e-30462dce61f5.png)

Giá trị của y là

![image](https://user-images.githubusercontent.com/65381453/129486411-aabc5a40-5c0a-4168-a104-f6c3f99a3402.png)


```
[[ 1]
 [ 2]
 [ 3]
 [ 4]
 [ 5]
 [ 6]
 [ 7]
 [10]
 [12]
 [ 9]
 [15]]
```

Mô phỏng dữ liệu bằng matplotlib ta có từ X0 và Y

![image](https://user-images.githubusercontent.com/65381453/129488555-81497dff-b388-48a6-a36a-d10ba79c698c.png)

Tính trực tiếp <a href="https://www.codecogs.com/eqnedit.php?latex=\inline&space;\large&space;\theta=(X^TX)^{-1}X^Ty" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\inline&space;\large&space;\theta=(X^TX)^{-1}X^Ty" title="\large \theta=(X^TX)^{-1}X^Ty" /></a> theo công thức <a href="https://www.codecogs.com/eqnedit.php?latex=\inline&space;\large&space;\theta=(X^TX)^{-1}X^Ty" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\inline&space;\large&space;\theta=(X^TX)^{-1}X^Ty" title="\large \theta=(X^TX)^{-1}X^Ty" /></a>

```
np.linalg.inv() dùng để tính ma trận nghịch đảo

theta = np.linalg.inv(X.T.dot(X)).dot(X.T.dot(Y))
```
kết quả:

![image](https://user-images.githubusercontent.com/65381453/129489208-b9d9aab3-9a41-499e-90bf-ac17f34b0097.png)

vậy nó có dạng

<a href="https://www.codecogs.com/eqnedit.php?latex=\inline&space;\large&space;\hat{Y}&space;=&space;X\theta&space;=&space;\begin{bmatrix}&space;X_0\&space;1&space;\end{bmatrix}&space;\begin{bmatrix}&space;\0.377943&space;\\\-3.23667906&space;\end{bmatrix}&space;=&space;0.377943X_0&space;&plus;&space;-3.23667906" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\inline&space;\large&space;\hat{Y}&space;=&space;X\theta&space;=&space;\begin{bmatrix}&space;X_0\&space;1&space;\end{bmatrix}&space;\begin{bmatrix}&space;\0.377943&space;\\\-3.23667906&space;\end{bmatrix}&space;=&space;0.377943X_0&space;&plus;&space;-3.23667906" title="\large \hat{Y} = X\theta = \begin{bmatrix} X_0\ 1 \end{bmatrix} \begin{bmatrix} \0.377943 \\\-3.23667906 \end{bmatrix} = 0.377943X_0 + -3.23667906" /></a>

bây giờ ta có thể phỏng đoán được độ tuổi khi cho 1 cân nặng cụ thể

![image](https://user-images.githubusercontent.com/65381453/129596008-58e33d64-6337-4d02-887f-18fa77ded578.png)

*Nói tóm ta tìm kiếm hệ số của biến độc lập và giá trị độ lệch của hàm mất mát*

Ta check lại bằng thư viện scikit-learn

![image](https://user-images.githubusercontent.com/65381453/129603714-fb3bbece-e421-4e0e-8d77-1c5ea9e51b92.png)

```
from sklearn import datasets, linear_model

liner = linear_model.LinearRegression(fit_intercept=False)
liner.fit(X,Y) # thực hiện train dữ liệu trên tập train
```
kết quả

![image](https://user-images.githubusercontent.com/65381453/129603796-1a7a138a-bd8b-4a82-a47a-eade46c7aaa0.png)

hoàn toàn giống nhau
