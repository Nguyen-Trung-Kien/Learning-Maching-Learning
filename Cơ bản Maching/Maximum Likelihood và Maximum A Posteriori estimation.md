# hi 1 bài toán maching learning có 3 bước để hoàn thành là Modeling , Learning, Interence
1. Modeling là việc đi tìm môt mô hình thích hợp cho bài toán cần giải quyết
2. Learning là bước tiến hành tối ưu các tham số của mô hình
3. Inference là bước dự đoán ouput của mô hình dựa trên các trained parameters

Trong bài này, mình sẽ đề cập tới Learning, cụ thể hơn *learning chính là quá trình đánh giá (estimate) bộ tham số θ sao cho dữ liệu sẵn có và mô hình khớp với nhau nhất.*

Có 2 cách để đánh giá một bộ tham số
1. Dựa trên tập dữ liệu đã biết trong tập trainning (trainning data) được gọi là Maximum Likelihood Estimation or ML Estimation hoặc MLE.
2. Dựa trên nhiều yếu tố, không chỉ trên tập training mà còn dựa trên những thông tin đã biết của tập tham số.Những thông tin này có thể có được bằng cảm quan của người xây dựng mô hình. Cảm quan càng rõ ràng, càng hợp lý thì khả năng thu được bộ tham số tốt là càng cao.
# Maximum Likelihood Estimation
Giả sử có các điểm dữ liệu x1,x2,…,xN. Giả sử thêm rằng ta đã biết các điểm dữ liệu này tuân theo một phân phối nào đó được mô tả bởi bộ tham số θ.

Maximum Likelihood Estimation là việc đi tìm bộ tham số θ

sao cho xác suất sau đây đạt giá trị lớn nhất:

θ=maxθp(x1,…,xN|θ)    (1)

p(x1|θ) chính là xác suất xảy ra sự kiện x1

Và p(x1,…,xN|θ) chính là xác suất để toàn bộ các sự kiện x1,x2,…,xN xảy ra đồng thời

xác suất đồng thời này còn được gọi là likelihood. Ở đây, likelihood chính là hàm mục tiêu.

Maximum Likelihood chính là việc đi tìm bộ tham số θ sao cho Likelihood là lớn nhất, tức xác xuất xảy ra đồng thời các sự kiện là lớn nhất
## Independence Assumption và log-likelihood
Việc giải trực tiếp bài toán (1) thường là phức tạp vì việc đi tìm mô hình xác suất đồng thời cho toàn bộ dữ liệu là ít khi khả thi.

hai sự kiện x,y là độc lập nếu xác suất đồng thời của chúng bằng tích xác suất của từng sự kiện, nhưng mà việc tối ưu hoá một tích thường phức tạp hơn việc tối ưu một tổng, vì vậy việc tối đa hàm mục tiêu thường được chuyển về việc tối đa log của hàm mục tiêu.

Bài toán Maximum Likelihood được đưa về bài toán Maximum Log-likelihood

θ=maxθN∑n=1log(p(xn|θ)) 

# Maximum a Posteriori (Hợp lý cực đại)
Ví dụ: nếu tung đồng xu 5 lần và chỉ nhận được 1 mặt head, theo Maximum Likelihood, xác suất để có một mặt head được đánh giá là 1/5. Nếu tung đồng xu 5000 lần và nhận được 1000 lần head, ta có thể đánh giá xác suất của head là 1/5 và việc đánh giá này là đáng tin. Tuy nhiên, vì chỉ có 5 kết quả, thật khó để kết luận rằng kết quả là 1/5. 

Khi có quá ít dữ kiện, tương ứng với hiện tượng có quá ít dữ liệu trong training (low-training) chúng ta cần phải tự suy ra một vài giả thiết của các tham số. Chẳng hạn, với việc tung đồng xu, giả thiết của chúng ta là xác suất nhận được mặt head phải gần 1/2.

Maximum A Posteriori (MAP) ra đời nhằm giải quyết vấn đề này. Trong MAP, chúng ta giới thiệu một giả thiết biết trước, được gọi là prior, của tham số θ. Từ những kinh nghiệm trước đây, chúng ta có thể suy ra các khoảng giá trị và phân bố của tham số.
