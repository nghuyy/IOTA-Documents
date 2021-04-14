## VMBox ##
Link: https://gist.github.com/nghuyy/f7fbb5c788f9944913386f706278a46b

+ Ngoại lệ:
```text
    + Không hiển thị thông tin bắt đầu bằng : hệ thống sẽ xem đó là lệnh, sử dụng /:nội dung/ nếu muốn gởi chuỗi có dấu : bắt đầu
    + Giảm thiểu số lần gởi dữ liệu bằng cách gộp chung tất cả quy trình vào một lần gởi dữ liệu, chỉ cập nhật thông tin riêng lẻ khi cần thiết
    + Mã icon xem ở đây: https://fontawesome.com/icons?d=gallery&p=2
```

+ Toolbar:
 IOTA cho phép mặc định 6 toolbar icons từ trái qua phải đánh dấu từ 1-6 gồm 1-3 bên trái và 4-6 phải. (Không tính menu người dùng) 
 
```text
+ Toolbar Icons:
    Ẩn icon:
    :toolbar.icon.[1-6].ic-[hide]
    Đổi icon:
    :toolbar.icon.[1-6].ic-[mã icon]
    Đặt mã sự kiện chạm toolbar:
    :toolbar.icon.[1-6].iota-[nội dung sự kiện]
    Nút reload:
    :toolbar.icon.7.[hide/show] //ẩn hoặc hiện nút reload
```
![](https://next.iotabot.app/index.php/s/wz5443jKEWs7FAq/download)

Code Mẫu
```javascript
//https://iota.vsys.vn/#@testvm
if(IOTA.mess === "init" || IOTA.mess === ""){
out= [":toolbar.icon.1.ic-arrow-left",":toolbar.icon.1.iota-icon-back",":toolbar.icon.2.ic-bars",":toolbar.icon.2.iota-icon-menu",":toolbar.icon.7.hide"]
}else{
out = [":cls","Bạn đã chọn menu: " + IOTA.mess];
}
```

+ Input:

```text
    Đổi text gợi ý input:
    :input.desc./[Nội dung gợi ý]/
    Đổi button input icon
    :input.icon.[mã icon]
```
![](https://next.iotabot.app/index.php/s/Wo95AKQ4Dtx3G9L/download)

Code mẫu:
```javascript
//https://iota.vsys.vn/#@testinput
out = ":input.desc./Nhập gì đó vào đây/"
```

```javascript
//https://iota.vsys.vn/#@testinputicon
out = ":input.icon.ic-search";
```