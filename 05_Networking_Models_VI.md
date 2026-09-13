# Các Mô Hình Mạng (Networking Models)

Có hai mô hình mạng mô tả việc giao tiếp và truyền dữ liệu từ host này sang host khác, được gọi là **mô hình ISO/OSI** và **mô hình TCP/IP**. Đây là một cách biểu diễn đơn giản hóa các tầng (layer) để chuyển đổi các Bit được truyền tải thành nội dung mà chúng ta có thể đọc được.

![image](https://github.com/user-attachments/assets/b6cbcf95-2a12-46a5-8ae0-cf2dab22ad54)

## Mô Hình OSI

Mô hình **OSI**, thường được gọi là mô hình tầng **ISO/OSI**, là một mô hình tham chiếu có thể được sử dụng để mô tả và định nghĩa việc giao tiếp giữa các hệ thống. Mô hình tham chiếu này có **bảy** tầng riêng biệt, mỗi tầng đảm nhận các nhiệm vụ được phân định rõ ràng.

Thuật ngữ **OSI** là viết tắt của mô hình **Open Systems Interconnection** (Kết Nối Các Hệ Thống Mở), được công bố bởi **Liên Minh Viễn Thông Quốc Tế (International Telecommunication Union - ITU)** và **Tổ Chức Tiêu Chuẩn Hóa Quốc Tế (International Organization for Standardization - ISO)**. Vì vậy, mô hình **OSI** thường được gọi là mô hình tầng **ISO/OSI**.

## Mô Hình TCP/IP

**TCP/IP (Transmission Control Protocol/Internet Protocol)** là thuật ngữ chung dùng để chỉ nhiều giao thức mạng khác nhau. Các giao thức này chịu trách nhiệm cho việc chuyển mạch và vận chuyển các gói dữ liệu trên Internet. Toàn bộ Internet được xây dựng dựa trên họ giao thức **TCP/IP**. Tuy nhiên, **TCP/IP** không chỉ đề cập đến hai giao thức này mà thường được sử dụng như một thuật ngữ chung cho toàn bộ một họ giao thức.

Ví dụ, **ICMP (Internet Control Message Protocol)** hoặc **UDP (User Datagram Protocol)** đều thuộc họ giao thức này. Họ giao thức này cung cấp các chức năng cần thiết để vận chuyển và chuyển mạch các gói dữ liệu trong một mạng riêng hoặc mạng công cộng.

## ISO/OSI so với TCP/IP

**TCP/IP** là một giao thức giao tiếp cho phép các host kết nối với Internet. Nó đề cập đến **Transmission Control Protocol** được sử dụng trong và bởi các ứng dụng trên Internet. Trái ngược với **OSI**, nó cho phép nới lỏng các quy tắc cần phải tuân theo, miễn là các nguyên tắc chung được tuân thủ.

Mặt khác, **OSI** là một cổng giao tiếp giữa mạng và người dùng cuối. Mô hình OSI thường được gọi là mô hình tham chiếu vì nó mới hơn và được sử dụng rộng rãi hơn. Nó cũng được biết đến với giao thức nghiêm ngặt và các giới hạn của mình.

## Truyền Gói Tin

Trong một hệ thống phân tầng, các thiết bị trong một tầng trao đổi dữ liệu theo một định dạng khác được gọi là **đơn vị dữ liệu giao thức (protocol data unit - PDU)**.

Ví dụ, khi chúng ta muốn duyệt một trang web trên máy tính, phần mềm máy chủ từ xa trước tiên sẽ chuyển dữ liệu được yêu cầu đến tầng ứng dụng. Dữ liệu được xử lý theo từng tầng, mỗi tầng thực hiện các chức năng được giao. Sau đó, dữ liệu được truyền qua tầng vật lý của mạng cho đến khi máy chủ đích hoặc một thiết bị khác nhận được nó. Dữ liệu lại được định tuyến qua các tầng một lần nữa, với mỗi tầng thực hiện các hoạt động được giao cho đến khi phần mềm nhận sử dụng dữ liệu đó.

![image](https://github.com/user-attachments/assets/aaa450a6-bdaa-439f-a140-23d969cebca3)

Trong quá trình truyền tải, mỗi tầng sẽ thêm một **header** (tiêu đề) vào **PDU** từ tầng trên, dùng để kiểm soát và xác định gói tin. Quá trình này được gọi là **đóng gói (encapsulation)**.

Header và dữ liệu cùng nhau tạo thành PDU cho tầng tiếp theo. Quá trình này tiếp tục đến **Tầng Vật Lý (Physical Layer)** hoặc **Tầng Mạng (Network Layer)**, nơi dữ liệu được truyền đến bên nhận. Bên nhận sẽ thực hiện quá trình ngược lại và giải nén dữ liệu ở từng tầng bằng thông tin trong header. Sau đó, ứng dụng cuối cùng sẽ sử dụng dữ liệu đó. Quá trình này tiếp tục cho đến khi toàn bộ dữ liệu đã được gửi và nhận xong.

![image](https://github.com/user-attachments/assets/d1a2cf2d-325c-4b96-a4fa-2d89f7eadbce)
