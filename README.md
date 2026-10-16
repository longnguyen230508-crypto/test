# Chuẩn hóa tài liệu markdown cho dự án
## Phần 1: phân tích
1. 
 Nhẩy cấp tiêu đề từ H1 xuống H3 : Đoạn mã sử dụng `# Lợi ích của rau sạch` (H1) ngay sau đó chuyển sang `### Danh sách các loại rau` (H3).
> Việc phân cấp tiêu đề bị đứt gãy khiến cấu trúc tài liệu không logic, trình đọc màn hình hoặc trình biên dịch Markdown khó xác định bố cục phân cấp, đồng thời giao diện hiển thị không đồng bộ thẩm mỹ
2. 
Lỗi cú pháp chèn hình ảnh không đúng chuẩn Markdown: Viết `[Logo Dự án] (https://greentech.vn/logo.png)` (có khoảng trắng giữa dấu ngoặc vuông và ngoặc tròn, thiếu dấu chấm than `!`)
>Cú pháp chuẩn của hình ảnh trong Markdown bắt buộc phải có dấu chấm than ở đầu `![Mô tả ảnh](đường_dẫn_ảnh)` và không được có khoảng trắng giữa `]` và `(`. Do viết sai cú pháp, trình biên dịch coi đây là một liên kết văn bản thông thường thay vì một thẻ hình ảnh  img, dẫn đến việc ảnh không thể hiển thị.
3. 
Lỗi định dạng in đậm sai cú pháp: Dùng 1 dấu sao `*Rất quan trọng*` thay vì 2 dấu sao `**Rất quan trọng**`
>1 dấu sao (`*text*`) hoặc dấu gạch dưới (`_text_`) chỉ dùng để định dạng in nghiêng , trong khi cú pháp để in đậm yêu cầu phải dùng 2 dấu sao (`**text**`) hoặc 2 dấu gạch dưới (`__text__`)
## Phần 2
- Hoàn thiện đoạn mã Markdown chuẩn:
```
# Lợi ích của rau sạch

## 1. tốt cho sức khỏe
giàu vitamin và khoáng chất
giảm nguy cơ mắc bệnh
 - **1.1 tăng cường miễn dịch**
giúp cơ thể khỏe mạnh hơn môi ngày
![](link )
## 2. an toàn và tự nhiên 
 không hóa chất, không thuốc trừ sâu 
- **2.1 bảo vệ môi trường**
giảm ô nghiễm đất  nguồn nước
> rau sạch - cho cuộc sống xanh.
