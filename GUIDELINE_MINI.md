# Mini guideline — bài làm cá nhân

> Điền nội dung này trước khi bắt đầu gán nhãn. Giữ lại các quyết định sau khi self-QC.

## Định nghĩa lớp

| Lớp | Định nghĩa của bạn | Ví dụ/điểm phân biệt |
| --- | --- | --- |
| `car` |xe con, sedan, SUV, taxi, xe bán tải | Nhỏ và thấp nhất trong 4 lớp; có capo và cốp riêng; không có thùng hàng.|
| `truck` | xe tải chở hàng, xe đầu kéo|cabin lái tách biệt với thùng chở hàng phía sau |
| `bus` |xe buýt, minibus chở khách | Dài và cao nhất; nhiều cửa sổ dọc thân|
| `van` |xe van, minivan chở hàng hoặc chở người |Không có thùng tách biệt như truck, ngắn và thấp hơn bus; thường có cửa trượt bên hông |

## Quy tắc chung

- Box bám sát vật thể nghĩa là: box ôm sát mép ngoài cùng của phần nhìn thấy của vật thể, bao gồm cả bánh xe và gương chiếu hậu; không chừa nền thừa, không cắt mất phần nào của vật; không bao bóng đổ hay hình phản chiếu.
- Vật thể bị che khuất:  vẫn gán box quanh phần nhìn thấy được nếu nhận diện được lớp.
- Vật thể bị cắt bởi rìa ảnh: không đoán phần nằm ngoài ảnh.
- Vật thể rất nhỏ/mơ hồ: Ghi vào mini guideline và hỏi giảng viên.

## Ghi lại quyết định cho ít nhất ba ca mơ hồ

| Ảnh | Tình huống | Quyết định cuối | Lý do theo schema |
| --- | --- | --- | --- |
| `drive_001` |Xe phía trên bên phải, không đọc được đặc trưng phân biệt lớp | Không gán box|Theo đúng quy tắc "vật thể rất nhỏ/mờ hồ": không đoán mò khi không phân biệt được lớp |
| `drive_041` | Xe đỏ phía dưới bên phải bị cắt bởi rìa ảnh | Vẫn gán nhãn phần nhìn thấy |Vật thể bị che khuất nhưng vẫn nhận diện được lớp |
| `drive_040` | Xe màu đen bên phải bị xe bus che mất một nửa |Gán nhãn phần nhìn thấy | Vật thể bị che khuất nhưng vẫn nhận diện được lớp |
