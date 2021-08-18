# hi 1 bài toán maching learning có 3 bước để hoàn thành là Modeling , Learning, Interence
1. Modeling là việc đi tìm môt mô hình thích hợp cho bài toán cần giải quyết
2. Learning là bước tiến hành tối ưu các tham số của mô hình
3. Inference là bước dự đoán ouput của mô hình dựa trên các trained parameters

Trong bài này, mình sẽ đề cập tới Learning, cụ thể hơn *learning chính là quá trình đánh giá (estimate) bộ tham số θ sao cho dữ liệu sẵn có và mô hình khớp với nhau nhất.*

Có 2 cách để đánh giá một bộ tham số
1. Dựa trên tập dữ liệu đã biết trong tập trainning (trainning data) được gọi là Maximum Likelihood Estimation or ML Estimation hoặc MLE.
2. Dựa trên nhiều yếu tố, không chỉ trên tập training mà còn dựa trên những thông tin đã biết của tập tham số.Những thông tin này có thể có được bằng cảm quan của người xây dựng mô hình. Cảm quan càng rõ ràng, càng hợp lý thì khả năng thu được bộ tham số tốt là càng cao.
# Maximum Likelihood Estimation
## 
