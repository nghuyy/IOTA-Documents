### Cập nhật bảng lệnh mới

Chú ý:
```
 Mã lệnh luôn là số sau dấu :.
 Các tham số có thể là số, hoặc chuỗi. Với dạng chuỗi, luôn phải nằm trong cặp dấu '' hoặc ""
 Nếu lệnh sai cấu trúc, trong cửa sổ F12 sẽ báo lỗi Parse: Unexpected token X in JSON at position 5,
 số 5 chính là vị trí lỗi của chuỗi lệnh (không tính dấu :)
 Từ nay các lệnh mới sẽ tuân theo quy tắc này, lệnh cũ sẽ được chuyển đổi dần. Trừ những lệnh theo kiểu chuỗi JSON
```

1. Local Store:
```
1. Lưu Local Store: I101":1,1,'Xin chào, anh bạn!'". Hoặc I101":1,'key1','Xin chào, anh bạn!'"
2. Đọc Local Store: I101":2,1" hoặc I101":2,'key1'"
3. Xóa Local Store: I101":3,1" Xóa dữ liệu lưu 1 và I101":3" Xóa hết local store
```
4. Hộp thoại đăng nhập:
```
 I101":4,'ico-unlock-alt Để tiến hành thanh toán, Xin đăng nhập!'",
 hiển thị hộp thoại yêu cầu đăng nhập với câu thông báo.
 Hoặc mặc định I101":4"
```
[Tùy chọn câu thoại](https://dev.iotabot.app/#@testreqlogin,init)

[Mặc định](https://dev.iotabot.app/#@testreqlogindefault,init)

5. Hộp thoại thông báo:
```
Hiển thị 1 thông báo bên trong web để người dùng chú ý, cho đến khi nào họ bấm nút đóng
I101":5,'Chú ý ico-balance-scale ','ico-award Bạn đã hoàn thành nhiệm vụ!'"
```
[Xem](https://dev.iotabot.app/#@focusalert)

6. Mở địa chỉ web trên cữa sổ popup:
```
I101":6,'https://google.vn'"
```
[Xem](https://iotabot.app/#@popup)

7. Đọc tên người dùng

I101":7"


8. Hiện thông báo hệ thống: 
```
Chú ý, đây là thông báo trực tiếp, không phải inbox, sử dụng Inbox Api nếu muốn thông báo bằng Inbox
I101":8,'Xin chào'" hoặc I101":8,'IOTA','Xin chào!'".
```
[Thông báo](https://dev.iotabot.app/#@notify)

9. Đặt hình nền
I101":9,'Địa chỉ ảnh',0" 
với 0 Mặc định
1 - chính giữa phía trên
2 - chính giữa phía dưới
3 - tự giãn theo màn hình



Khác:
```
Xem nhanh mã lệnh từ Console F12 gõ window.IOTA enter
Bật tắt Debug
debug()

```
