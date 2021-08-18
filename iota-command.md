## IOTA UI Command ##

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

Menu mở rộng:
``` text
    Menu mở rộng 1: 
    I101":toolbar.ex1./Nội dung toolbar/"
    Chú ý: khi cập nhật menu chính, menu con sẽ bị xóa do đó cần phải gởi lệnh thêm lại
    
    Menu con menu mở rộng 1
    I101":toolbar.ex1.[mã menu con]/Nội dung menu/"
    
    khi user bấm menu sẽ nhận lại sự kiện: click.toolbar. mã menu     
```
Demo: [https://dev.iotabot.app/#@ex1Dropdown,init]()

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


Code mẫu:
```javascript
//https://iota.vsys.vn/#@testinput
out = ":input.desc./Nhập gì đó vào đây/"
```

```javascript
//https://iota.vsys.vn/#@testinputicon
out = ":input.icon.ic-search";
```