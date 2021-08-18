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
