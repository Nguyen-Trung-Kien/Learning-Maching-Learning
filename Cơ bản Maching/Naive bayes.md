# nghiên cứu về naive bayes
Naïve Bayes Classifiers là một trong những thuật toán đem lại hiệu quả cho những bài toán phân lớp trong NLP nhờ độ chính xác cao, thời gian huấn luyện mô hình nhỏ.
## Định lý bayes
Định lý Bayes cho phép tính xác suất xảy ra của một sự kiện ngẫu nhiên A khi biết sự kiện liên quan B đã xảy ra.

Xác suất này được ký hiệu là P(A|B), và đọc là “xác suất của A nếu có B”. 
Đại lượng này được gọi xác suất có điều kiện hay xác suất hậu nghiệm vì nó được rút ra từ giá trị được cho của B hoặc phụ thuộc vào giá trị đó.

Theo định lí Bayes, xác suất xảy ra A khi biết B sẽ phụ thuộc vào 3 yếu tố:
1. Xác suất xảy ra A của riêng nó, không quan tâm đến B. Kí hiệu là P(A) và đọc là xác suất của A. 
2. Xác suất xảy ra B của riêng nó, không quan tâm đến A. Kí hiệu là P(B) và đọc là “xác suất của B”.Đại lượng này còn gọi là hằng số chuẩn hóa (normalising constant)
3. Xác suất xảy ra B khi biết A xảy ra. Kí hiệu là P(B|A) và đọc là “xác suất của B nếu có A”. Đại lượng này gọi là khả năng (likelihood) xảy ra B khi biết A đã xảy ra. 

*định lý Bayes sẽ giúp ta tính ra xác suất xảy ra của một giả thuyết bằng cách thu thập các bằng chứng nhất quán hoặc không nhất quán với một giả thuyết nào đó.*

Công thức của Bayes

![image](https://user-images.githubusercontent.com/65381453/130014319-25e8ece8-9875-43fc-9b9b-924f285867f8.png)

Hoặc dạng khác

![image](https://user-images.githubusercontent.com/65381453/130014945-7b635738-3376-40f4-b5ef-69cf215d57a5.png)

Ví dụ:

Một lớp học 40 học sinh trong đó có:
1. 30 người học sinh giỏi
2. 10 người học sinh trung bình
3. Số lượng nữ giới trong lớp là 15
4. Và số lượng nữ giới trong những hs giỏi là 5

nếu chọn ngẫu nhiên 1 người thì tỉ lệ nữ hs giỏi

dựa theo công thức bayes

P(nữ|hsgioi) = p(hsgioi|nữ) x p(nữ) /p(hs)

p(hsgioi|nữ) = 5/30

P (nữ ) = 15/40

p(hs) = 1

P(nữ|hsgioi) = (5/30 x 15/40 )/1

= 1/16

*đơn giản dễ hiểu phải k*
##  Phân lớp Naive Bayes
Bộ phân lớp Naive bayes hay bộ phân lớp Bayes (simple byes classifier) hoạt động như sau:
1. Gọi D là tập dữ liệu huấn luyện, trong đó mỗi phần tử dữ liệu X được biểu diễn bằng một vector chứa n giá trị thuộc tính A1, A2,...,An = {x1,x2,...,xn}
2. Giả sử có m lớp C1, C2,..,Cm. Cho một phần tử dữ liệu X, bộ phân lớp sẽ gán nhãn cho X là lớp có xác suất hậu nghiệm lớn nhất. Cụ thể, bộ phân lớp Bayes sẽ dự đoán X thuộc vào lớp Ci nếu và chỉ nếu:


*P(Ci | X) > P(Cj | X) (1<= i, j <=m, i != j)*
```
Xác xuất Ci xảy ra khi có X *lớn hơn* Xác xuất Cj xảy ra khi có X thì bộ phân lớp Bayes sẽ dự đoán X thuộc vào lớp Ci
```

3. Để tìm được xác suất lớn nhất , ta nhận thấy các giá trị P(X) là giống nhau với mọi lớp nên không cần tính.Do đó ta chỉ cần tìm giá trị lớn nhất của P(X|Ci) * P(Ci) ,P(Ci) được ước lượng bằng |Di|/|D|, trong đó Di là tập các phần tử dữ liệu thuộc lớp Ci. Nếu xác suất tiền nghiệm P(Ci) cũng không xác định được thì ta coi chúng bằng nhau P(C1) = P(C2) = ... = P(Cm), khi đó ta chỉ cần tìm giá trị P(X|Ci) lớn nhất.
4. Khi số lượng các thuộc tính mô tả dữ liệu là lớn thì chi phí tính toàn P(X|Ci) là rất lớn, dó đó có thể giảm độ phức tạp của thuật toán Naive Bayes giả thiết các thuộc tính độc lập nhau. Khi đó ta có thể tính:


P(X|Ci) = P(x1|Ci)...P(xn|Ci)

Ví dụ tiếp:

Xác suất để 1 người dính covid là 35% và xác suất không dính covid là 65%

https://1upnote.me/post/2018/11/ds-ml-naive-bayes/

https://viblo.asia/p/thuat-toan-phan-lop-naive-bayes-924lJWPm5PM
