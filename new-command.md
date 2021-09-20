### Cập nhật bảng lệnh mới

Chú ý:
```
 Mã lệnh luôn là số sau dấu :.
 Các tham số có thể là số, hoặc chuỗi. Với dạng chuỗi, luôn phải nằm trong cặp dấu '' hoặc ""
 Nếu lệnh sai cấu trúc, trong cửa sổ F12 sẽ báo lỗi Parse: Unexpected token X in JSON at position 5,
 số 5 chính là vị trí lỗi của chuỗi lệnh (không tính dấu :)
 Từ nay các lệnh mới sẽ tuân theo quy tắc này, lệnh cũ sẽ được chuyển đổi dần. Trừ những lệnh theo kiểu chuỗi JSON
```
Ví dụ:  
```
    1. Lưu Local Store: I101":1,1,'Xin chào, anh bạn!'". Hoặc I101":1,'key1','Xin chào, anh bạn!'"
    2. Đọc Local Store: I101":2,1" hoặc I101":2,'key1'"
    3. Xóa Local Store: I101":3,1" Xóa dữ liệu lưu 1 và I101":3" Xóa hết local store
    8. Hiện thông báo: I101":8,'Xin chào'" hoặc I101":8,'IOTA','Xin chào!'". Chú ý, đây là thông báo trực tiếp, 
    không phải inbox, sử dụng Inbox Api nếu muốn thông báo bằng Inbox
    
```    
Chi tiết lệnh(Bỏ qua phần mã khóa ở đầu, chỉ quan tâm mã số lệnh và ghi chú)     
```
    SET_LOCAL_STORE: 1, // 1[Vị trí lưu],2[Nội dung] Lưu tạm dữ liệu trên trình duyệt, dữ liệu này là có thể bị sửa đổi và không bảo mật,
    // tuy nhiên không bị mất cho đến khi người dùng xóa thủ công
    READ_LOCAL_STORE: 2, //1[Vị trí lưu, có thể là số, hoặc chuỗi] Đọc local store
    DEl_LOCAL_STORE: 3, //1[Vị trí lưu, nếu bỏ trống tất cả sẽ bị xóa] Xóa dữ liệu đã ghi
    NOTIFY: 8 //1[Nội dung] hoặc 1[Tiêu đề],2[Nội dung] Hiện thông báo
```
Khác:
```
Xem nhanh mã lệnh từ Console F12 gõ window.IOTA enter
Bật tắt Debug
debug()

```
