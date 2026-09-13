# Địa Chỉ IPv6

![image](https://github.com/user-attachments/assets/24dc01d9-975f-4612-9774-18c0bb9d0493)

**IPv6** là thế hệ kế nhiệm của IPv4. Trái ngược với IPv4, địa chỉ **IPv6** dài **128 bit**. **Tiền tố (prefix)** xác định phần mạng và phần host. Internet Assigned Numbers Authority (**IANA**) là tổ chức chịu trách nhiệm gán các địa chỉ IPv4 và IPv6 cũng như các phần mạng liên quan của chúng. Về lâu dài, **IPv6** được kỳ vọng sẽ hoàn toàn thay thế IPv4, vốn vẫn đang được sử dụng phổ biến trên Internet hiện nay. Tuy nhiên, về nguyên tắc, IPv4 và IPv6 có thể được sử dụng đồng thời (**Dual Stack**).

IPv6 tuân theo nhất quán nguyên tắc **end-to-end** (đầu cuối đến đầu cuối) và cung cấp các địa chỉ IP có thể truy cập công khai cho bất kỳ thiết bị đầu cuối nào mà không cần đến NAT. Do đó, một giao diện có thể có nhiều địa chỉ IPv6, và cũng có những địa chỉ IPv6 đặc biệt được gán cho nhiều giao diện.

**IPv6** là một giao thức có nhiều tính năng mới, đồng thời cũng có nhiều ưu điểm khác so với IPv4:

- Không gian địa chỉ lớn hơn
- Tự cấu hình địa chỉ (SLAAC)
- Nhiều địa chỉ IPv6 trên mỗi giao diện
- Định tuyến nhanh hơn
- Mã hóa đầu cuối đến đầu cuối (IPsec)
- Gói dữ liệu lên đến 4 GByte

![image](https://github.com/user-attachments/assets/b095f713-6260-4190-9e02-8afd380d38b4)

Có bốn loại địa chỉ IPv6 khác nhau:

![image](https://github.com/user-attachments/assets/12a0ec8c-babf-4210-81d5-c5b9056a9b0b)

### Hệ Thập Lục Phân (Hexadecimal System)

Hệ thập lục phân (hex) được sử dụng để làm cho cách biểu diễn nhị phân trở nên dễ đọc và dễ hiểu hơn. Chúng ta chỉ có thể thể hiện 10 trạng thái (0-9) với hệ thập phân và 2 trạng thái (0 / 1) với hệ nhị phân bằng cách sử dụng một ký tự duy nhất. Trái ngược với hệ nhị phân và hệ thập phân, chúng ta có thể sử dụng hệ thập lục phân để thể hiện 16 trạng thái (0-F) chỉ với một ký tự duy nhất.

![image](https://github.com/user-attachments/assets/3aa779d7-2070-4096-a029-309859c09c0e)

Hãy xem một ví dụ với một địa chỉ IPv4, để thấy địa chỉ IPv4 (**192.168.12.160**) sẽ trông như thế nào khi biểu diễn dưới dạng thập lục phân.

![image](https://github.com/user-attachments/assets/2c376308-4d60-418e-8040-07c59fe5edb1)

Tổng cộng, một địa chỉ IPv6 bao gồm **16 byte**. Do độ dài của nó, một địa chỉ **IPv6** được biểu diễn dưới dạng ký hiệu **thập lục phân (hexadecimal)**. Vì vậy, **128 bit** được chia thành **8 khối**, mỗi khối nhân với 16 bit (hay **4 chữ số hex**). Cả bốn chữ số hex được nhóm lại và ngăn cách bằng dấu hai chấm (**:**) thay vì một dấu chấm đơn giản (**.**) như trong IPv4. Để đơn giản hóa cách viết, chúng ta bỏ qua ít nhất **4** số 0 đứng đầu trong các khối, và chúng ta có thể thay thế chúng bằng hai dấu hai chấm (**::**).

Một địa chỉ IPv6 có thể trông như sau:

- IPv6 Đầy Đủ: **fe80:0000:0000:0000:dd80:b1a9:6687:2d3b/64**
- IPv6 Rút Gọn: **fe80::dd80:b1a9:6687:2d3b/64**

Một địa chỉ IPv6 bao gồm hai phần:

- **Tiền Tố Mạng (Network Prefix)** (phần mạng)
- **Bộ Nhận Diện Giao Diện (Interface Identifier)**, còn được gọi là **Hậu Tố (Suffix)** (phần host)

**Tiền Tố Mạng** xác định mạng, subnet, hoặc dải địa chỉ. **Bộ Nhận Diện Giao Diện** được hình thành từ địa chỉ MAC **48-bit** (mà chúng ta sẽ thảo luận sau) của giao diện, và trong quá trình này được chuyển đổi thành một địa chỉ **64-bit**. Độ dài tiền tố mặc định là **/64**. Tuy nhiên, các tiền tố phổ biến khác bao gồm **/32**, **/48**, và **/56**. Nếu chúng ta muốn sử dụng các mạng của riêng mình, chúng ta sẽ nhận được một tiền tố ngắn hơn (ví dụ: **/56**) so với **/64** từ nhà cung cấp dịch vụ của mình.

Trong RFC 5952, cách viết địa chỉ IPv6 nêu trên đã được định nghĩa như sau:

- Tất cả các ký tự chữ cái luôn được viết bằng chữ thường.
- Tất cả các số 0 đứng đầu của một khối luôn được lược bỏ.
- Một hoặc nhiều khối liên tiếp gồm **4 số 0** (hex) được rút gọn bằng hai dấu hai chấm (**::**).
- Việc rút gọn thành hai dấu hai chấm (**::**) chỉ được thực hiện **một lần duy nhất**, tính từ bên trái.
