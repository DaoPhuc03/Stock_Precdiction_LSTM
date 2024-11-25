# Stock_Precdiction_LSTM
Mô tả quá trình xây dựng một mô hình dự đoán giá cổ phiếu sử dụng mạng nơ-ron hồi quy LSTM (Long Short-Term Memory) trong Python. Các bước chính trong đoạn code bao gồm:

Tải file và nhập các thư viện cần thiết: Sử dụng google.colab để tải dữ liệu và các thư viện như pandas, numpy, MinMaxScaler từ sklearn, các thành phần của mô hình LSTM từ tensorflow.keras, và matplotlib để vẽ biểu đồ.

Đọc và xử lý dữ liệu từ file CSV: Đoạn code đọc dữ liệu từ một file CSV, chuyển đổi cột thời gian sang định dạng datetime, tạo ra cột mới chỉ gồm ngày và tổng hợp dữ liệu để lấy giá mở cửa và đóng cửa theo từng ngày.

Chuẩn hóa dữ liệu: Sử dụng MinMaxScaler để chuẩn hóa dữ liệu giá đóng cửa vào khoảng [0,1] để chuẩn bị cho quá trình huấn luyện mô hình.

Chuẩn bị dữ liệu cho LSTM: Tạo các chuỗi dữ liệu (features và labels) dựa trên số lượng ngày quan sát (look_back) để dự đoán giá vào ngày tiếp theo.

Chia dữ liệu thành tập huấn luyện và kiểm thử: Phân chia dữ liệu thành 80% cho huấn luyện và 20% cho kiểm thử.

Xây dựng mô hình LSTM: Mô hình bao gồm các lớp LSTM, Dropout để tránh overfitting và một lớp Dense làm lớp đầu ra.

Huấn luyện mô hình: Huấn luyện mô hình với dữ liệu đã được chuẩn bị, sử dụng kiểm định chéo để đánh giá và điều chỉnh mô hình trong quá trình huấn luyện.

Dự đoán và đánh giá mô hình: Thực hiện dự đoán trên tập huấn luyện và kiểm thử, chuyển kết quả dự đoán từ dạng chuẩn hóa về dạng giá gốc, và vẽ biểu đồ để trực quan hóa kết quả so sánh giữa giá thực tế và dự đoán.

Tính toán sai số dự đoán: Tính sai số RMSE (Root Mean Square Error) cho tập huấn luyện và kiểm thử để đánh giá độ chính xác của mô hình.
![image](https://github.com/user-attachments/assets/7a895930-810c-4162-8acf-46b2bb1ca433)
