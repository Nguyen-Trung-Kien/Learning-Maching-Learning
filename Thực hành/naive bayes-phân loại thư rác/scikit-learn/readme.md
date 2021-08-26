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

Đầu tiên ở đây, mình có sử dụng data set và hãy xem

![image](https://user-images.githubusercontent.com/65381453/130807880-6da2f057-5b1b-4735-9782-465b5677c121.png)

Cột đầu tiên là số lượng từ của mail , có vẻ không sử dụng đến nên mình sẽ xoá đi

![image](https://user-images.githubusercontent.com/65381453/130808456-7bae70e1-f17d-43a7-b41d-5a32a540c928.png)

Và cột thứ 2

![image](https://user-images.githubusercontent.com/65381453/130809492-0554d08b-fef6-4d9e-808c-1239ef1ac633.png)


# Đầu tiên mình sẽ không có xử lý trước, và chạy thử nó sẽ ntn
