# Hi
Numpy là một thư viện  toán học nổi tiếng của python , có cực kỳ phổ biến và mạnh mẽ của python và trong bài này sẽ nghiên cứu cáhc sử dụng chúng, cho phép làm việc hiệu quả với ma trận , mảng đa chiều.

# Vì sao thường gặp numpy trong các mô hình máy học 
Oke không biết

bạn có thể thấy
![image](https://user-images.githubusercontent.com/65381453/128995621-a4efccd0-68b7-4461-9299-f2f7215928dd.png)

Thời gian tính toán của hàm sum in python trong cùng 1 phép tính là 1.37ms ? trong khi np.sum là 7.1 us , dữ liệu càng lớn thì tốc độ chên lệch càng nhiều

đó là lý do nta sử dụng numpy chứ ko sài thuần pyhon

# Thao tác với Numpy
## Khởi tạo mảng
![image](https://user-images.githubusercontent.com/65381453/128968686-d8425eaf-4ba1-478c-bbc7-f97877ec5dc3.png)

Outout:
![image](https://user-images.githubusercontent.com/65381453/128968728-0343a857-599e-4a99-a163-81eaba7c9575.png)
## Khởi tạo mảng 2 chiều
![image](https://user-images.githubusercontent.com/65381453/128968964-61f538e9-b596-455a-9dbc-b212f5f8283b.png)

Output:
![image](https://user-images.githubusercontent.com/65381453/128968989-4dfbda4e-e745-486b-a85e-5b0303574f67.png)
## Khởi tạo mảng 3 chiều
![image](https://user-images.githubusercontent.com/65381453/128969774-58a18a29-c08f-4e68-a8e6-857e2a6312fa.png)

Output:
![image](https://user-images.githubusercontent.com/65381453/128969802-4c82040a-2af2-4474-9341-b2f710bcaa2b.png)
## Một số hàm có sẵn khác
### Zeros
np.zeros(())
![image](https://user-images.githubusercontent.com/65381453/128970184-7b17624c-2cde-4669-8379-ff357b5a7d1e.png)

output:
![image](https://user-images.githubusercontent.com/65381453/128970209-70fdba04-5f8b-4020-a07f-6be634da8d6b.png)
### ones 
np.ones(())
![image](https://user-images.githubusercontent.com/65381453/128971232-07ac8131-6b26-42f1-960c-b0fa5376d66c.png)

Output:
![image](https://user-images.githubusercontent.com/65381453/128971272-d0cdc080-62eb-4d48-a240-27676d48b732.png)

### Một sô hàm khác
1. np.arange(1,13,6): tạo mảng với các phần tử từ 1 -> 12 bước nhảu là 6
2. np.full((2,3),3) : tạo mảng 2 chiều với tất cả phần tử là 3
3. np.eye(3) : tạo ma trận đơn vị với kích thước 3x3
4. np.random.random((2,3)) : tạo ma trận với các giá trị ngẫu nhiên với kích thước 2x3
5. np.linespace(1,2,5) : tạo 1 mảng có giá trị từ 1->2 cách nhau 5 lần, vd: 1,1.25,1.5,1.75,2

Tại sao cần phải sử dụng các hàm như thế này

Thỉnh thoảng cần phải tạo các cột toàn 0,1 hay giá trị mong muốn, thì đây là cách tạo

## Các thao tác trên mảng
1. dtype: kiểu dữ liệu của phần tử trong mảng
2. ndim : số chiều của mảng
3. size : số phần tử của mảng
4. shape : kích thước của mảng

# array Indexing & Slicing

![image](https://user-images.githubusercontent.com/65381453/128976688-d523ba48-b530-4e4e-a7d5-7fe384e42e29.png)

1. array[i] : Truy cập tới phần tử thứ i của mảng 1 chiều, tính từ 0
2. array[i,j] : Truy cập tới phần tử hàng i, cột j của mảng 2 chiều tính từ 0
3. array[n,i,j] : Truy cập tới phần tử chiều n, hàng i, cột j của mảng 3 chiều tính từ 0
4. array[a:b] : Truy cập tới các phần tử từ a đến b-1 trong mảng 1 chiều
5. array[:,:b] : Truy cập tới phần tử từ cột 0 đến cột b-1, của tất cả các hàng trong mảng 2 chiều.

# split 
cắt 

![image](https://user-images.githubusercontent.com/65381453/128988838-e78cd5e1-c96f-4d60-8f4c-eb41583c7538.png)

Output: 3 mảng
![image](https://user-images.githubusercontent.com/65381453/128988870-e94b4e1b-e9f0-4517-a33e-b28c62637999.png)

split chia mảng thành những phần mà người dùng xác định

# Phương sai và độ lệch chuẩn

tham khảo, mình sẽ có 1 bài về 2 cái này

1. np.mean : tính trung bình
2. np.std : tính độ lệch chuẩn  hoặc np.sqrt(np.var()) 
3. np.var : tính phương sai

https://www.mathsisfun.com/data/standard-deviation.html
# Linear
để thực hiện tích vô hướng 
#### B (3x2) và A (3x3) => B.dot(A) không được, vì vậy transpoun B.T (2x3) mới có thể nhân được
*A.dot(B) hoặc A @ B*
