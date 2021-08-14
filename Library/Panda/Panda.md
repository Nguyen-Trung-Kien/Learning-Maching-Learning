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
# Loc()
sử dụng để lọc ??

sử dụng nó để filter các giá trị của cột,vv

![image](https://user-images.githubusercontent.com/65381453/129447245-f1829c31-ff55-49a2-ab35-4038ea42db5d.png)

bạn cũng có thể sử dụng dấu & | để thêm vào điều kiện

![image](https://user-images.githubusercontent.com/65381453/129447463-c231f9d6-89eb-4f50-807d-737b12d7cebe.png)

hoặc có thể thêm những cột xuất hiện

![image](https://user-images.githubusercontent.com/65381453/129447624-ea22a2d1-a44e-4063-a8bc-b2cbdb849312.png)
# iLoc()
còn gọi indexlocation lựa chọn những cột, hàng mà bạn muốn

![image](https://user-images.githubusercontent.com/65381453/129447900-7ef85c7c-d4a3-4f22-a83a-e3f5287887b8.png)

đưa ra thông tin

more, more

![image](https://user-images.githubusercontent.com/65381453/129448192-316f77f0-7e92-4dad-bdcb-1cab8c7c9a88.png)
# xem kiểu dữ liệu
![image](https://user-images.githubusercontent.com/65381453/129451611-f77b70a7-f717-434e-807f-315ff8a95c8e.png)

một số kiểu dữ liệu :
1. 'O' : Object
2. 'b' : Boolean
3. 'u' : unsigned integer
4. 'i' : integer
5. 'f' : float
6. 'c' : complex-float
7. 'S','a' : string
8. 'U' : Unicode
9. 'V' : raw data

# Apply()

Sử dụng hàm apply để thay đổi thành phần của cột

![image](https://user-images.githubusercontent.com/65381453/129452323-0d6832c8-2bc3-4344-bb01-c77ac280093a.png)

# add thêm 1 cột vào

ví dụ tui sẽ tạo ra 1 cột ABC = PassengerId x Pclass       

sẽ như vầy

![image](https://user-images.githubusercontent.com/65381453/129452730-143d73fc-50c4-4e41-bd8b-9e22db04ae55.png)

đấy ra được cột ABCN
# Tính tổng 1 cột như thế nào
sum thôi

![image](https://user-images.githubusercontent.com/65381453/129452820-51bd67ea-a944-41cf-a029-27778b31ac43.png)
# Groupby
sử dụng hàm groupby để gom dữ liệu cần sài
![image](https://user-images.githubusercontent.com/65381453/129452911-f0730dc5-dbd2-40c5-8d60-ef570f79d57e.png)
# Sort
![image](https://user-images.githubusercontent.com/65381453/129452997-b9435313-f500-4257-9c01-a810ccfec5ad.png)

sử dụng sort_values() để sắp xếp, mặc định là tăng dần
# Unique
dã sử :)) muốn count số lượng tuổi 

sử dụng value_counts()

![image](https://user-images.githubusercontent.com/65381453/129453264-bbe65c7b-8835-4e63-80ed-ce9c8c8718d0.png)

và đếm số lượng tuôti

![image](https://user-images.githubusercontent.com/65381453/129453276-887e70c0-058a-4bd9-a5cc-bf1aad88664e.png)

hoặc sử dụng 1 hàm unique

![image](https://user-images.githubusercontent.com/65381453/129453371-a4a68110-20c7-45e7-9e0a-076f9a832680.png)

