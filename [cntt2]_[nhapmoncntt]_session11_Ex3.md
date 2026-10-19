
## phần 1 
### 1. xác định các tham số cho hàm VLOOKUP
- ` Lookup_value `: giá trị cần dò tìm là mã tác giả ở cột c trong sheet Danhsachbaocao 
- `Table_array`; vùng bảng chứa dữ liệu tra cứu là sheet danhmuctacgia, từ cột mã tác giả đến cột thù lao
- `col_index_num: 
> cột D: cột số 2 trong bảng tc
> cột E: cột số 4 trong bảng tc 
> cột F: cột số 5 trong bảng tc
### 2. giải pháp xử lý bẫy 
1. sử dụng hàm `TRIM(_)` bao bọc `lookup_value` để tự động cắt bỏ khoảng trắng thừa
2. sử dụng hàm `IFERROR(_)` bọc bên ngoài hàm VLOOKUP để bắt lỗi `#N\A` 
3. cố định vùng tra cứu `Table_array` bằng ký tự`$` 
### 3. các bước thực hiện tuần tự trong excel 
- **b1**: chọn ô D2
- **b2**: xây dựng hàm VLOOKUP kết hợp `TRIM` cho giá trị dò tìm và bọc toàn bộ trong `IFERROR`
- **b3**: cố định `Table_array` bằng `F4`
- ** b4**: kéo từ ô D2 xuống hết bảng dữ liệu
- **b5**:lặp lại hoặc copy công thức sang các cột E ,F sau đó chinh sửa lại ` col_index_num` thành `4` và `5`
## phần 2 
```
=IFERROR(VLOOKUP(TRIM(C2), 'DanhMucTacGia'!$A$2:$E$100, 2, FALSE), "Chưa cập nhật") ```[cite: 1] #### **5. Viết công thức cho ô E2 (Phòng) và F2 (Thù lao)** * Công thức tại ô `E2` (Phòng trình bày): ```excel =IFERROR(VLOOKUP(TRIM(C2), 'DanhMucTacGia'!$A$2:$E$100, 4, FALSE), "Chưa cập nhật") ``` * Công thức tại ô `F2` (Thù lao): ```excel =IFERROR(VLOOKUP(TRIM(C2), 'DanhMucTacGia'!$A$2:$E$100, 5, FALSE), "Chưa cập nhật") ```

