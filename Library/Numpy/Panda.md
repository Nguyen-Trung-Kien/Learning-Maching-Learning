# bài này sẽ nói về panda và làm việc với panda
Pandas là 1 thư viện hỗ trợ cho việc xử lý data dưới dạng bảng , vào thôi

## import thư viện
![image](https://user-images.githubusercontent.com/65381453/129439329-e01cba9d-b35e-46c6-b4c1-9f3e8fe4377e.png)

*dataset của mình lấy ở đây: https://www.kaggle.com/c/titanic/data?select=test.csv*
## đọc data

![image](https://user-images.githubusercontent.com/65381453/129439385-abca596e-7600-4d20-a673-cdf05a7a2d52.png)

1. gán biến df cho data vừa import

## Trính xuất dữ liệu

Mình sử dụng hàm head(5) để xem 5 hàng đầu tiên của bảng

![image](https://user-images.githubusercontent.com/65381453/129439415-b3df7e8c-a893-4ac8-8475-eae8d3fa632a.png)

## hàm shape 
hàm shape để xem độ dài của bảng

![image](https://user-images.githubusercontent.com/65381453/129439574-2be00d05-02f6-4678-a00b-ec42bbfb04d3.png)
## hàm Info()
hàm này dùng để xem thông tin của các cột

![image](https://user-images.githubusercontent.com/65381453/129439669-6274cdd1-a309-4748-a603-c2f00f7e4531.png)

nó liệt kê các thông tin của cột, 

*Tại sao có những cột có số lượng nhỏ hơn*

Bởi vì nó có những *missing data* được thể hiện = những giá trị NaN~~ NotaNumber
# describe()


![image](https://user-images.githubusercontent.com/65381453/129441309-a51ec335-8161-49b0-b9d0-48141152c38e.png)

Và những cột sumary thuộc những kiểu số , thống kê những cột đó

![image](https://user-images.githubusercontent.com/65381453/129441420-d8c8ccb5-7eaa-4d66-9f11-19012a86b60d.png)

Các giá trị bao gồm:
1. count: đếm
2. mean : giá trị trung bình
3. std : độ lệch chuẩn
4. min : giá trị nhỏ nhất
5. max : giá trị max tuỳ theo trường hợp

*có thể sử dụng thêm describe(inclulde = "all") cho tất cả*
