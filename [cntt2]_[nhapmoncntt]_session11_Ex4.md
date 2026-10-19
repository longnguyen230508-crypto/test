
## phần 1
### 1. khung tiêu đề 3 cấp
#### 1. Mở rộng khung tiêu đề ở mục 3a thành 3 cấp đầy đủ
> Thêm mục con dưới mục 1:

- 1.1. Mục tiêu

- 1.2. Đối tượng sử dụng


> Thêm mục con dưới mục 2.1:

#### 2.1.1. Luồng mượn sách qua thẻ sinh viên

   

### 2. Gắn đúng cấp Heading
- Heading 1: Dùng cho các mục chính cấp 1 (ví dụ: 1. Giới thiệu dự án, 2. Chức năng hệ thống, 3. Yêu cầu bảo mật).   

- Heading 2: Dùng cho các mục con cấp 2 (ví dụ: 2.1. Quản lý mượn sách, x.x).   


- Heading 3: Dùng cho các mục con cấp 3 (ví dụ: 2.1.1. Luồng mượn sách qua thẻ sinh viên).
### 3. Viết nội dung mô tả
- Dưới mục 2. Chức năng hệ thống (Viết 2 câu mô tả Yêu cầu chức năng - Functional Requirements):

> Hệ thống cho phép sinh viên tra cứu danh mục sách trực tuyến và thực hiện đăng ký mượn sách thông qua mã thẻ sinh viên. Đồng thời, thủ thư có thể dễ dàng quản lý trạng thái mượn trả, cập nhật danh mục và kiểm soát quá hạn của từng đầu sách.

- Dưới mục 3. Yêu cầu bảo mật (Viết 2 câu mô tả Yêu cầu phi chức năng - Non-functional Requirements):

> Hệ thống áp dụng cơ chế mã hóa mật khẩu người dùng và phân quyền truy cập nghiêm ngặt giữa sinh viên và quản trị viên để đảm bảo an toàn dữ liệu. Toàn bộ các giao dịch mượn trả sách phải được ghi log lại để phục vụ công tác kiểm tra và đối soát định kỳ.
### 4. Chèn Auto TOC
> Đặt con trỏ chuột tại vị trí đầu tài liệu, vào thẻ References ->  chọn Table of Contents và chọn kiểu mẫu mục lục tự động.   Thêm một đoạn văn bản bất kỳ để đẩy mục 3 sang trang sau, sau đó click chuột phải chọn Update Field -> chọn Update entire table để cập nhật lại số trang chính xác.
## Phần 2 – Chuẩn hóa dữ liệu & AutoFilter (Excel)
#### 3 lỗi vi phạm 5 Quy tắc Vàng:
- Hàng 1: Merge ô tiêu đề lớn.   
- Hàng 5: Để hàng trống.   
- Hàng 6: Chèn dòng "Tổng cộng" vào giữa bảng. 
#### Chuẩn hóa: Bỏ merge ô, xóa hàng 5 trống, chuyển hàng "Tổng cộng" ra ngoài bảng dữ liệu chính.   
#### Khái niệm:
- Record (Bản ghi): 1 hàng dữ liệu đầy đủ (ví dụ: thông tin phiếu mượn của 1 sinh viên).   
- Field (Trường): 1 cột thuộc tính (ví dụ: cột Mã Sách hoặc Họ Tên).   #### AutoFilter: Nhấn Ctrl + Shift + L tại hàng tiêu đề, bấm mũi tên ở cột Tình Trạng -> chọn lọc "Quá hạn". 
##  Phần 3 – Tra cứu dữ liệu (VLOOKUP)
- Công thức VLOOKUP cơ bản (Lấy Tên Sách):
` =VLOOKUP(C2, DanhMucSach!$A$2:$B$4, 2, FALSE) `
 - Hiện tượng mã S099: Trả về lỗi #N/A do mã S099 không có trong danh mục tra cứu.  
 -  Công thức bọc IFERROR chống lỗi:
 - `=IFERROR(VLOOKUP(C2, DanhMucSach!$A$2:$B$4, 2, FALSE), "Không tìm thấy sách")  `
## Phần 4 – Slide báo cáo tiến độ (PowerPoint)
**Thiết kế 1 Slide:**
- Assertion Title: Dữ liệu mượn sách đã được chuẩn hóa và tự động hóa tra cứu bằng VLOOKUP & IFERROR.
- Số liệu nổi bật: 100% dữ liệu được làm sạch và xử lý lỗi tự động.
- Biểu đồ: Donut Chart (hiển thị tỷ lệ các trạng thái: Đang mượn, Quá hạn, Đã trả).
> Rule 10/20/30: Chiếm 1 slide trong tổng số 10 slide và trình bày trong 2 phút.
