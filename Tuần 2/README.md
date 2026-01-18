# Student Data Analysis (Phân tích điểm số học sinh)

Dự án này là bài tập thực hành về kỹ thuật **Kiểm thử đơn vị (Unit Testing)** với Java và JUnit 5. Chương trình cung cấp các chức năng xử lý danh sách điểm số của học sinh, bao gồm việc lọc dữ liệu hợp lệ, đếm số lượng học sinh giỏi và tính điểm trung bình.

## 📋 Mục tiêu

- Viết mã nguồn Java sạch sẽ (Clean Code).
- Áp dụng **JUnit 5** để viết các test case (Normal, Boundary, Exception).
- Làm quen với quy trình Git/GitHub cơ bản.

## ✨ Tính năng chính

Chương trình `StudentAnalyzer` cung cấp 2 chức năng chính:

1.  **`countExcellentStudents(List<Double> scores)`**:
    -   Đếm số lượng học sinh có điểm **>= 8.0**.
    -   Tự động bỏ qua các điểm không hợp lệ (nhỏ hơn 0 hoặc lớn hơn 10).
    -   Trả về 0 nếu danh sách rỗng.

2.  **`calculateValidAverage(List<Double> scores)`**:
    -   Tính điểm trung bình cộng của các điểm hợp lệ (từ 0 đến 10).
    -   Bỏ qua các điểm sai dữ liệu.
    -   Trả về 0.0 nếu không có điểm nào hợp lệ hoặc danh sách rỗng.

## 🛠️ Công nghệ sử dụng

-   **Ngôn ngữ:** Java (JDK 8 trở lên)
-   **Kiểm thử:** JUnit 5 (Jupiter)
-   **Quản lý dự án:** Maven
-   **IDE:** Visual Studio Code (với Extension Pack for Java)

## 📂 Cấu trúc dự án

```text
student-analyzer/
├── src/
│   ├── main/java/com/example/
│   │   └── StudentAnalyzer.java       # Mã nguồn chính
│   └── test/java/com/example/
│       └── StudentAnalyzerTest.java   # Mã nguồn kiểm thử (Unit Tests)
├── pom.xml                            # Cấu hình Maven & thư viện JUnit
└── README.md                          # Tài liệu hướng dẫn