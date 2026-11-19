 # [BTTH] Bài tập thực hành tổng hợp
 ## **1. Thiết kế giải pháp**

Sử dụng **Prompt Chaining** gồm 3 bước chạy tuần tự:

1. **Prompt 1 – Phân tích:** Kiểm tra dữ liệu và nội dung bài làm
2. **Prompt 2 – Gia sư Feynman:** Giải thích kiến thức đơn giản, chỉ ra lỗi sai
3. **Prompt 3 – Chấm điểm:** Chấm theo Rubric và tổng hợp kết quả

**Input:** Chủ đề, bài làm sinh viên, tiêu chí và thang điểm

**Output:** Giải thích, lỗi sai, bảng điểm và nhận xét

## **2. Prompt thực thi**

**Prompt 1: Kiểm tra dữ liệu**

- Kiểm tra chủ đề, bài làm và Rubric
- Nếu thiếu dữ liệu, yêu cầu bổ sung
- Nếu dữ liệu sai định dạng, thông báo lỗi
- Không tự suy đoán dữ liệu
- Nếu thỏa mãn sang bước 2

**Prompt 2: Gia sư Feynman**

từ dữ liệu 1 giải thích kiến thức bằng ngôn ngữ đơn giản theo phương pháp Feynman đưa ví dụ  chỉ ra lỗi sai và hướng dẫn sửa chuyển sang bước 3

**Prompt 3: Chấm bài tự động**

từ bài làm và Rubric, chấm điểm từng tiêu chí tính tổng điểm nhận xét ưu nhược điểm không tự ý thay đổi thang điểm xuất kết quả dạng bảng markdown

## **3. Kết quả chạy thử**

**Đầu vào:** Bài Python tính trung bình cộng nhưng chưa xử lý danh sách rỗng

**Kết quả AI:**

- Giải thích: Trung bình cộng bằng tổng các số chia cho số lượng phần tử
- Lỗi phát hiện: Chưa kiểm tra danh sách rỗng, có thể gây lỗi chia cho 0
- Cách sửa: Thêm điều kiện kiểm tra danh sách trước khi tính

| Tiêu chí | Điểm đạt |
| --- | --- |
| Đúng logic | 4/4 |
| Xử lý lỗi | 0/3 |
| Code rõ ràng | 2/2 |
| Giải thích | 1/1 |
| **Tổng** | **7/10** |