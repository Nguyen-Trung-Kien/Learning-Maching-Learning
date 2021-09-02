# Bài này sẽ nói về phân biệt bắc và nam
# thực hành lại tại https://machinelearningcoban.com/2017/08/08/nbc/

![image](https://user-images.githubusercontent.com/65381453/131816336-7b56c57e-ed8c-4fb8-8113-da9a99591d9a.png)

có 2 class là B và N , đầu tiên ta cần tìm p(B) và p(N) 

p(B) = 3/4 và p(N) = 1/4

tập hợp các từ tạo thành từ điển Bag of word 

V={hanoi, pho, chaolong, buncha, omai, banhgio, saigon, hutiu, banhbo}

Đây là quá trình test

![image](https://user-images.githubusercontent.com/65381453/131817545-18985310-a087-4277-b6bc-4614f55c8bef.png)

ta được 2 giá trị là 1.5×10−4 và 1.75×10−5 , 2 đại lượng này không phải là xác suất cần tìm mà chỉ là 2 đại lượng tỉ lệ thuận với hai xác suất đó.

p(B|d5)=1.5×10−41.5×10−4+1.75×10−5≈0.8955,    p(N|d5)=1−p(B|d5)≈0.1045

# Mình sẽ làm lại bài này theo thư viện

