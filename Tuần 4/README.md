# Báo Cáo Kiểm Thử Hiệu Năng với JMeter

## 1. Mục tiêu kiểm thử
- **Website mục tiêu:** `https://vnexpress.net`
- **Mục đích:** Đánh giá thời gian phản hồi, thông lượng và tỷ lệ lỗi của hệ thống trang tin tức VnExpress dưới các mức độ tải khác nhau.

## 2. Thiết kế kịch bản kiểm thử (Test Scenarios)

### Kịch bản 1: Kịch bản cơ bản
- **Số lượng người dùng (Threads):** 10
- **Số lần lặp (Loop Count):** 5
- **Hành vi:** Gửi yêu cầu HTTP GET đến Trang chủ (`/`).

### Kịch bản 2: Kịch bản tải nặng
- **Số lượng người dùng:** 50
- **Ramp-up Period:** 30 giây
- **Số lần lặp (Loop Count):** 1
- **Hành vi:** Gửi yêu cầu HTTP GET đến Trang chủ (`/`) và Trang Khoa học (`/khoa-hoc`).

### Kịch bản 3: Kịch bản tùy chỉnh
- **Số lượng người dùng:** 20
- **Thời gian chạy (Duration):** 60 giây (Vòng lặp Infinite)
- **Hành vi:** Gửi yêu cầu HTTP GET đến Trang Thể thao (`/the-thao`) và Trang Giải trí (`/giai-tri`).

## 3. Phân tích kết quả kiểm thử

*(Sinh viên chèn các ảnh chụp Summary Report của 3 kịch bản vào đây)*

Dựa vào kết quả thu được từ JMeter, ta có bảng tổng hợp các chỉ số quan trọng sau:

| Kịch bản | Tổng số Request | Thời gian phản hồi trung bình (Average) | Thông lượng (Throughput) | Tỷ lệ lỗi (Error Rate) |
| :--- | :--- | :--- | :--- | :--- |
| **KB 1 (Cơ bản)** | 50 | ~ 1411 ms | 6.3 requests/sec | 0.00% |
| **KB 2 (Tải nặng)** | 100 | ~ 105 ms | 3.4 requests/sec | 0.00% |
| **KB 3 (Tùy chỉnh)** | 784 | ~ 1533 ms | 12.8 requests/sec | 0.00% |

## 4. Kết luận
Qua 3 kịch bản kiểm thử, hệ thống của VnExpress cho thấy khả năng chịu tải cực kỳ ấn tượng. Dù ở mức tải cơ bản (10 users), tải nặng dồn dập (50 users) hay duy trì liên tục trong 1 phút (20 users), tỷ lệ lỗi luôn giữ ở mức tuyệt đối **0.00%**. Thời gian phản hồi có sự biến động tùy thuộc vào nội dung trang, nhưng nhìn chung hệ thống hoạt động rất trơn tru và đáp ứng tốt các yêu cầu.