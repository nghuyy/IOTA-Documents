### Cập nhật bảng lệnh mới theo bảng lệnh sau

Ví dụ:    
    1. Lưu Local Store: I101":1,1,'Xin chào, anh bạn!'"
    2. Đọc Local Store: I101":2,1"
    3. Xóa I101"3,1" Xóa dữ liệu lưu 1 và I101"3" Xóa hết local store
    
     
```
SET_LOCAL_STORE: 1, // 1[Vị trí lưu],2[Nội dung] Lưu tạm dữ liệu trên trình duyệt, dữ liệu này là có thể bị sửa đổi và không bảo mật,
// tuy nhiên không bị mất cho đến khi người dùng xóa thủ công
READ_LOCAL_STORE: 2, //1[Vị trí lưu] Đọc local store
DEl_LOCAL_STORE: 3, //1[Vị trí lưu, nếu bỏ trống tất cả sẽ bị xóa] Xóa dữ liệu đã ghi
```
