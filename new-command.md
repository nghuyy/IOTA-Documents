    ##### Cập nhật bảng lệnh mới theo bảng lệnh sau
    
    ```
    SET_LOCAL_STORE: 1, // Lưu local store
    READ_LOCAL_STORE: 2, // Đọc local store
    ```
    Với lệnh mới nội dung sẽ bắt đầu bằng : + Mã lệnh + Nội dung lệnh theo ghi chú ở trên
    Ví dụ: 
    ```
    Lưu tạm dữ liệu trên trình duyệt, dữ liệu này là có thể bị sửa đổi và không bảo mật, tuy nhiên không bị mất cho đến khi người dùng xóa thủ công
    ```
    
    1. Lưu Local Store: I101":1,1,'Xin chào, anh bạn!'"
    
    ```
    Đọc dữ liệu tạm
    ```
    2. Đọc Local Store: I101":2,1"
