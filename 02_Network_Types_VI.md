![image](https://github.com/user-attachments/assets/b9b64f8a-8e85-4185-8d3d-a56a79ddce0b)

Để hiểu về mạng máy tính, việc phân loại và xác định các mạng dựa trên **loại (types)** và **cấu trúc liên kết (topologies)** là rất quan trọng. Điều này giúp chúng ta hiểu cách dữ liệu được truyền đi, phạm vi mà mạng bao phủ, và mạng đó phù hợp nhất với mục đích gì. Thuật ngữ liên quan đến các loại mạng đôi khi có thể gây choáng ngợp do sự pha trộn giữa các thuật ngữ thực tiễn dùng trong các tình huống hàng ngày và các thuật ngữ lý thuyết được học chủ yếu trong môi trường học thuật.
Chúng ta hiếm khi nghe thấy một số thuật ngữ này trong thực tế, vì vậy phần này sẽ được chia thành **Thuật Ngữ Thông Dụng** và **Thuật Ngữ Học Thuật**.


# Các Loại Mạng
"Loại" (Types) đề cập đến bản chất của mạng, thường dựa trên quy mô hoặc mục đích sử dụng, chẳng hạn như **Mạng Cục Bộ (Local Area Network - LAN)**, **Mạng Diện Rộng (Wide Area Network - WAN)**, **Mạng Đô Thị (Metropolitan Area Network - MAN)**, và các loại khác. Chúng xác định phạm vi địa lý mà mạng bao phủ và cấu trúc kết nối của nó.
![image](https://github.com/user-attachments/assets/3df4d008-e113-4aeb-aeae-091be4a5c953)
![image](https://github.com/user-attachments/assets/0ae75375-bd08-4fe5-bd8e-0dbdc805a33e)

### 1. Thuật Ngữ Thông Dụng:
Đây là các loại mạng và thuật ngữ mà bạn sẽ thường xuyên gặp trong các ứng dụng thực tế:

LAN (Mạng Cục Bộ): Đây là mạng bao phủ một khu vực nhỏ, cụ thể như một tòa nhà, văn phòng, hoặc nhà ở. LAN được dùng để kết nối các máy tính và thiết bị ở gần nhau nhằm chia sẻ tài nguyên như máy in hoặc tệp dữ liệu.

WAN (Mạng Diện Rộng): Loại mạng này bao phủ một khu vực địa lý rộng lớn hơn nhiều và thường được dùng để kết nối nhiều mạng LAN lại với nhau. Internet là ví dụ tiêu biểu nhất của một WAN.

WLAN (Mạng Cục Bộ Không Dây): Tương tự như LAN, nhưng có khả năng kết nối các thiết bị không dây. Loại mạng này thường thấy ở nhà, quán cà phê, và văn phòng có kết nối Wi-Fi.

MAN (Mạng Đô Thị): Một mạng bao phủ khu vực rộng hơn LAN nhưng không rộng bằng WAN. Thông thường, nó kết nối nhiều mạng LAN trong phạm vi một thành phố hoặc khuôn viên, tạo điều kiện giao tiếp giữa các chi nhánh của một tổ chức hoặc các hệ thống công cộng như Wi-Fi toàn thành phố.

PAN (Mạng Cá Nhân): Một mạng có phạm vi rất hẹp, dùng để kết nối các thiết bị xung quanh một cá nhân, chẳng hạn như kết nối Bluetooth giữa điện thoại thông minh và tai nghe, hoặc giữa laptop và các thiết bị trong nhà.

### 2. Thuật Ngữ Học Thuật:
Đây là các thuật ngữ mang tính học thuật hơn hoặc ít được sử dụng bên ngoài các cuộc thảo luận chuyên môn hay các kỳ thi:

CAN (Mạng Khuôn Viên): Một mạng lớn hơn LAN nhưng vẫn giới hạn trong một khu vực địa lý nhất định như khuôn viên trường đại học, khuôn viên doanh nghiệp, hoặc khu công nghiệp.

SAN (Mạng Lưu Trữ): Một mạng cung cấp quyền truy cập vào kho lưu trữ dữ liệu tập trung ở cấp độ khối (block-level). SAN thường được sử dụng trong các trung tâm dữ liệu và môi trường lưu trữ doanh nghiệp để nâng cao hiệu suất và tính sẵn sàng.

EPN (Mạng Riêng Doanh Nghiệp): Một mạng được xây dựng và duy trì bởi một tổ chức để sử dụng riêng, nhằm kết nối nhiều địa điểm khác nhau và đảm bảo giao tiếp an toàn.

VPN (Mạng Riêng Ảo): Mặc dù không hẳn là một loại mạng dựa trên phạm vi địa lý, VPN mở rộng một mạng riêng qua một mạng công cộng. Nó cho phép người dùng gửi và nhận dữ liệu như thể thiết bị của họ được kết nối trực tiếp với mạng riêng đó.

BAN (Mạng Quanh Cơ Thể): Một loại mạng chuyên biệt liên quan đến các thiết bị điện toán đeo được (wearable) giao tiếp với nhau. Phổ biến trong công nghệ y tế và thể dục, nó bao phủ khu vực xung quanh cơ thể của một cá nhân.

# Đọc Thêm

### WAN
- WAN (Mạng Diện Rộng) thường được gọi là **Internet**.
- Một WAN thực chất chỉ là một số lượng lớn các mạng LAN được kết nối với nhau. Nhiều công ty lớn hoặc cơ quan chính phủ sẽ có một "WAN Nội Bộ" (còn được gọi là Intranet, Mạng Cách Ly - Airgap Network, v.v.).
- Nhìn chung, cách chính để chúng ta xác định một mạng có phải là WAN hay không là xem mạng đó có sử dụng giao thức định tuyến chuyên dụng cho WAN như BGP hay không, và liệu lược đồ địa chỉ IP đang dùng có nằm ngoài phạm vi RFC 1918 (10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16) hay không.

### VPN
VPN **(Mạng Riêng Ảo)** là công cụ cho phép người dùng kết nối một cách **an toàn** đến một mạng khác như thể họ đang kết nối vật lý trực tiếp với mạng đó. Điều này đạt được thông qua các **kết nối được mã hóa**, **an toàn** qua internet. Có **ba** loại VPN chính, mỗi loại được thiết kế cho các trường hợp sử dụng khác nhau nhưng đều có chung mục tiêu: **đảm bảo tính riêng tư**, **bảo mật**, và tạo cảm giác như đang là một phần của một mạng khác. Dưới đây là giải thích về **ba** loại chính:

1. Remote Access VPN (VPN Truy Cập Từ Xa):
Loại này cho phép từng người dùng cá nhân kết nối vào một mạng riêng từ một vị trí từ xa. Nó thường được nhân viên làm việc tại nhà hoặc đang đi công tác sử dụng khi cần truy cập vào các tài nguyên nội bộ của công ty như tệp tin, ứng dụng, hoặc cơ sở dữ liệu.
Nếu VPN chỉ tạo tuyến đường (route) cho các mạng cụ thể (ví dụ: 10.10.10.0/24), điều này được gọi là **Split-Tunnel VPN**, nghĩa là kết nối Internet không đi qua VPN.
Tuy nhiên, đối với một công ty, **Split-Tunnel VPN** thường không phải là lựa chọn lý tưởng vì nếu máy bị nhiễm phần mềm độc hại, các phương pháp phát hiện dựa trên mạng (network-based detection) hầu như sẽ không hoạt động do lưu lượng đó đi ra thẳng Internet.

2. Site-to-Site VPN (VPN Điểm-Nối-Điểm):
Một Site-to-Site VPN kết nối toàn bộ các mạng tại các địa điểm khác nhau, khiến chúng hoạt động như thể chúng là một phần của cùng một mạng cục bộ. Thiết lập này thường được các tổ chức có văn phòng ở nhiều thành phố, tiểu bang, hoặc thậm chí nhiều quốc gia sử dụng. VPN sẽ mã hóa dữ liệu khi nó di chuyển giữa hai địa điểm qua Internet công cộng, đảm bảo tính bảo mật. Các router ở những mạng khác nhau và tại các địa điểm vật lý khác nhau sử dụng **IPsec** (một giao thức phổ biến cho VPN) để mã hóa và xác thực lưu lượng truy cập.

3. SSL VPN:
(VPN **Secure Sockets Layer**) là một loại VPN cung cấp quyền truy cập an toàn vào các tài nguyên mạng từ xa bằng cách sử dụng giao thức **SSL/TLS (Secure Sockets Layer/Transport Layer Security)**. Loại VPN này thường được dùng để cho phép người dùng kết nối an toàn với mạng của công ty, các dịch vụ đám mây, hoặc các tài nguyên riêng khác qua internet.

### PAN / WPAN
- Các thiết bị đầu cuối hiện đại như điện thoại thông minh, máy tính bảng, laptop, hoặc máy tính để bàn có thể được kết nối tạm thời (ad hoc) để tạo thành một mạng nhằm trao đổi dữ liệu. Điều này có thể được thực hiện bằng cáp dưới dạng **Mạng Cá Nhân (Personal Area Network - PAN)**.
- Biến thể không dây, **Mạng Cá Nhân Không Dây (Wireless Personal Area Network - WPAN)**, dựa trên công nghệ Bluetooth hoặc Wireless USB. Một **mạng cá nhân không dây** được thiết lập qua Bluetooth được gọi là **Piconet**. **PAN** và **WPAN** thường chỉ mở rộng trong phạm vi vài mét, do đó không phù hợp để kết nối các thiết bị ở những phòng riêng biệt hoặc thậm chí ở những tòa nhà khác nhau.
- Trong bối cảnh **Internet of Things (IoT)**, **WPAN** được dùng để giao tiếp với các ứng dụng điều khiển và giám sát có tốc độ dữ liệu thấp. Các giao thức như **Insteon**, **Z-Wave**, và **ZigBee** được thiết kế chuyên biệt cho nhà thông minh và tự động hóa gia đình.
