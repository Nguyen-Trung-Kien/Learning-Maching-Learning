# Hi bài này sẽ nói về matrix
Ma trận ,là mảng mình chữ nhật bao gồm các số ,ký tự, ,vv được sắp xếp theo hàng và cột ,tập hợp các vecto có cùng kiểu và số chiều và được biểu diễn bởi một mảng hai chiều.

ví dụ:

![image](https://user-images.githubusercontent.com/65381453/129140310-25dcedc2-ffb6-4d60-b384-19f073fa8a74.png)

Mình sẽ sử dụng numpy để diễn giải

# Ma trận Đơn vị
đây là ma trận gồm đường chéo chính là 1 và phần tử còn lại là 0
![image](https://user-images.githubusercontent.com/65381453/129141603-70ca5c8d-e8a8-480a-8d3e-12ab581c4283.png)

```
numy.eye(n)
```
![image](https://user-images.githubusercontent.com/65381453/129141700-0594d463-ecd8-4357-9074-cbb89fb9b15e.png)

# Ma trận đường chéo
là ma trận vuông ngoại đường chéo chính là số bất kỳ còn lại là bằng 0

![image](https://user-images.githubusercontent.com/65381453/129141903-74cc4111-c308-4766-943a-17dcc29a5c6f.png)

```
numpy.diag(a,b,c,vv)
```
![image](https://user-images.githubusercontent.com/65381453/129141975-c940fc90-0815-4958-83cf-71f2e60f81f3.png)

# Ma trận chuyển vị
Khi nói A là ma trận chuyển vị của ma trận b thì có nghĩa, các cột của ma trận A là các hàng của ma trận B

![image](https://user-images.githubusercontent.com/65381453/129142348-80059bd2-27e3-48fa-86e2-3404adb54e3e.png)

```
Python: A.T
hoặc
np.transpose()
```
![image](https://user-images.githubusercontent.com/65381453/129142740-59cdc03c-bf5c-4d50-b993-7b8c5d80b4f9.png)

![image](https://user-images.githubusercontent.com/65381453/129142811-2ec5c581-687b-4fc0-9b62-9a312c77e321.png)

# Ma trận nghịch đảo
*Nếu tồn tại ma trận vuông B sao cho A.B = B.A = In thì ta nói ma trận A khả nghịch và B là ma trận nghịch đảo của A. *
Nếu code lại ma trận nghịch đảo thì rất mất thời gian, Np có hàm hỗ trợ*
```
np.linalg.inv(A)
```
![image](https://user-images.githubusercontent.com/65381453/129143387-a07d042b-27ed-4c59-916d-150fc4c55f9c.png)
