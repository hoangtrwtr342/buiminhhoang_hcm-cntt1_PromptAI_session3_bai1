#  [Bài thực hành 1] Trích xuất và định dạng thông tin tuyển dụng


## Phần 1 : Xây dựng Prompt 

```Markdown
- Sử dụng khung cấu trúc CREATE
    - C _ Context : Đóng vai trod là Chuyên viên xử lý dữ liệu nhân sự cấp cao
    - R - Request : Trích xuất các trường thông tin : Họ và tên , sô điện thoại , Email , Vị trí ứng tuyển , Năm kinh nghiệm , Kỹ năng chính
    - E - Explantion : Dữ liệu này sẽ được import trực tiếp và tự động vào database quản lý tuyển dụng của công ty, do đó yêu cầu độ chính xác 100%. Tuyệt đối không tự ý bịa đặt hoặc suy diễn thông tin không có trong email
    - A - Action : Quét qua email thô , xác định đúng các trường thông tin , phân loại kỹ năng thành một danh sách
    - T - Tone : Chính xác , khách quan ,không thêm thắt văn phong cảm xúc
    - E - Extras : Cung cấp ít nhất 2 cí dụ Few-shot mẫu (căp dữ liệu input email  thô -> Output mong muốn ) để định hình kết quả của AI

```

## Phần 2 : Trích xuất và chuẩn thông tin khách hàng 
* Ví dụ 1

- Input email thô :
  "Xin chào bộ phận tuyển dụng, mình tên là Nguyễn Văn A, sdt ************, email: ******@gmail.com. Mình muốn ứng tuyển vị trí Backend Developer. Mình đã có 3 năm kinh nghiệm làm việc với python, django, postgresql và docker."

|   Trường giá trị   |    Giá trị chuẩn hóa   |
|                                             |
|:---:|:---:|
|  Họ và tên  |   Nguyễn Văn A  |
|  Số điện thoại  |  0126*****0  |
|  Email  |  ******@gmai.com  |
|  Vị trí ứng tuyển  |  Backend  |
|  Năm kinh nghiệm  |  3  |
|  Kỹ năng chính |  Python,Html,Css,Java,script  |

* Ví dụ 2


