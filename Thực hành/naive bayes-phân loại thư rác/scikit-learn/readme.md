# Bài này mình sử dụng data là tiếng anh để đơn giản hơn
# Phân loại thư rác là một khởi đầu đơn giải mà không kém phần quan trọng trong phân loại
Với bài này mình sẽ đi qua 4 bước
1. Preparing the text data.
2. Creating word dictionary.
3. Feature extraction process
4. Training the classifier

# 1. Preparing the text data.
Ở bước này , sẽ chuẩn bị dữ liệu mà xử lý qua dữ liệu này ,(làm sạch), ở phần này ta sẽ xoá sạch những ký tự chung chung, không có góp phần nào vào việc xác nhận đây có phải mail spam hay không ?

Email có thể chứa những kí tự như dấu . chữ số hay stop word. những thứ này không có lợi ích nào cho việc phát hiện mail spam ,vậy việc của ta sẽ là loạt bỏ những thứ đó

