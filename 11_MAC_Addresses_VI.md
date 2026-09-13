# Địa Chỉ MAC

![image](https://github.com/user-attachments/assets/32196890-25f6-4436-b21f-eadcd81cd7b7)

Mỗi host trong một mạng đều có một địa chỉ **Media Access Control** (**MAC**) riêng, dài **48-bit** (**6 octet**), được biểu diễn dưới dạng thập lục phân (hexadecimal). **MAC** là **địa chỉ vật lý** cho các giao diện mạng của chúng ta. Có một số tiêu chuẩn khác nhau cho địa chỉ MAC:

- Ethernet (IEEE 802.3)
- Bluetooth (IEEE 802.15)
- WLAN (IEEE 802.11)

Điều này là do địa chỉ **MAC** đánh địa chỉ cho kết nối vật lý (card mạng, Bluetooth, hoặc bộ chuyển đổi WLAN) của một host. Mỗi card mạng có địa chỉ MAC riêng của nó, được cấu hình một lần từ phía phần cứng của nhà sản xuất nhưng luôn có thể được thay đổi, ít nhất là tạm thời.

Hãy cùng xem một ví dụ về địa chỉ MAC như sau:

Địa chỉ MAC:

- **DE:AD:BE:EF:13:37**
- **DE-AD-BE-EF-13-37**
- **DEAD.BEEF.1337**

![image](https://github.com/user-attachments/assets/528a32b8-1288-46a5-bc7d-a15860fe8cdd)

Khi một gói IP được chuyển giao, nó phải được đánh địa chỉ ở **tầng 2** đến địa chỉ vật lý của host đích, hoặc đến router / NAT, đơn vị chịu trách nhiệm định tuyến. Mỗi gói tin có một **địa chỉ bên gửi** và một **địa chỉ đích**.

Địa chỉ MAC bao gồm tổng cộng **6 byte**. Nửa đầu (**3 byte / 24 bit**) là cái gọi là **Organization Unique Identifier** (**OUI**), được định nghĩa bởi **Institute of Electrical and Electronics Engineers** (**IEEE**) cho từng nhà sản xuất tương ứng.

![image](https://github.com/user-attachments/assets/7977ec4d-ff60-4e31-b03c-1ee1da97e1b3)

Nửa còn lại của địa chỉ MAC được gọi là **Individual Address Part** (Phần Địa Chỉ Riêng) hoặc **Network Interface Controller** (**NIC**), do các nhà sản xuất gán. Nhà sản xuất chỉ thiết lập chuỗi bit này một lần duy nhất, và nhờ đó đảm bảo rằng toàn bộ địa chỉ là duy nhất.

![image](https://github.com/user-attachments/assets/99d63759-5c15-4b58-8f23-f7129d6a8c85)

Nếu một host có địa chỉ IP đích nằm trong cùng một subnet, việc chuyển giao sẽ được thực hiện trực tiếp đến địa chỉ vật lý của máy tính đích. Tuy nhiên, nếu host này thuộc về một subnet khác, khung Ethernet (Ethernet frame) sẽ được đánh địa chỉ đến **địa chỉ MAC** của router chịu trách nhiệm (**default gateway**). Nếu địa chỉ đích của khung Ethernet trùng khớp với **địa chỉ tầng 2** của chính nó, router sẽ chuyển tiếp khung này lên các tầng cao hơn. **Address Resolution Protocol** (**ARP**) được sử dụng trong IPv4 để xác định địa chỉ MAC tương ứng với các địa chỉ IP.

Cũng giống như địa chỉ IPv4, cũng có một số khu vực được dành riêng cho địa chỉ MAC. Ví dụ, bao gồm phạm vi cục bộ dành cho MAC.

![image](https://github.com/user-attachments/assets/a03ea1af-7bb4-415f-831c-39bcd9605b53)

Hơn nữa, hai bit cuối cùng trong octet đầu tiên có thể đóng một vai trò quan trọng khác. Như chúng ta đã biết, bit cuối cùng có thể có hai trạng thái, 0 và 1. Bit cuối cùng này xác định địa chỉ MAC đó là **Unicast** (**0**) hay **Multicast** (**1**). Với **unicast**, điều này có nghĩa là gói tin được gửi chỉ đến một host cụ thể duy nhất.

### MAC Unicast

![image](https://github.com/user-attachments/assets/cff5b6e2-fbd3-42b1-9f0b-e52a8e1e2d52)

Với **multicast**, gói tin chỉ được gửi một lần đến tất cả các host trong mạng cục bộ, sau đó mỗi host sẽ quyết định có chấp nhận gói tin hay không dựa trên cấu hình của mình. Địa chỉ **multicast** là một địa chỉ duy nhất, giống như địa chỉ **broadcast**, có các giá trị octet cố định. **Broadcast** trong một mạng đại diện cho một lời gọi phát quảng bá, trong đó các gói dữ liệu được truyền đồng thời từ một điểm đến tất cả các thành viên của một mạng. Nó chủ yếu được sử dụng khi địa chỉ của bên nhận gói tin chưa được biết. Một ví dụ là các giao thức **ARP** (**dành cho địa chỉ MAC**) và **DHCP** (**dành cho địa chỉ IPv4**).

Các giá trị được xác định của mỗi octet được đánh dấu **màu xanh lá**.

### MAC Multicast

![image](https://github.com/user-attachments/assets/c0525292-e6e0-4385-803b-ce551aa78189)

### MAC Broadcast

![image](https://github.com/user-attachments/assets/92b918d3-3268-4701-af08-4ad9ec97e077)

Bit áp chót trong octet đầu tiên xác định đây có phải là một **OUI toàn cầu (global OUI)**, được định nghĩa bởi IEEE, hay là một địa chỉ MAC được **quản lý cục bộ (locally administrated)**.

### OUI Toàn Cầu

![image](https://github.com/user-attachments/assets/559c07ef-1e8c-421f-a281-e1a6256407dd)

### Quản Lý Cục Bộ

![image](https://github.com/user-attachments/assets/d14cb089-d689-47df-9b87-868f21dddce1)

## Giao Thức Phân Giải Địa Chỉ (Address Resolution Protocol)

![image](https://www.networkacademy.io/sites/default/files/inline-images/how-arp-works.gif)

Địa chỉ MAC có thể bị thay đổi/thao túng hoặc giả mạo, và vì vậy, chúng không nên được dựa vào như là phương tiện bảo mật hoặc nhận dạng duy nhất. Các quản trị viên mạng nên triển khai thêm các biện pháp bảo mật bổ sung, chẳng hạn như phân đoạn mạng (network segmentation) và các giao thức xác thực mạnh, để bảo vệ chống lại các cuộc tấn công tiềm ẩn.

Có một số hướng tấn công có thể khai thác thông qua việc sử dụng địa chỉ MAC:

- **Giả mạo MAC (MAC spoofing):** Điều này liên quan đến việc thay đổi địa chỉ MAC của một thiết bị để trùng khớp với địa chỉ của một thiết bị khác, thường nhằm mục đích chiếm quyền truy cập trái phép vào một mạng.
- **Làm tràn ngập MAC (MAC flooding):** Điều này liên quan đến việc gửi rất nhiều gói tin với các địa chỉ MAC khác nhau đến một switch mạng, khiến nó đạt đến giới hạn dung lượng của bảng địa chỉ MAC và khiến nó không thể hoạt động đúng cách.
- **Lọc địa chỉ MAC (MAC address filtering)**: Một số mạng có thể được cấu hình chỉ cho phép truy cập đối với các thiết bị có địa chỉ MAC cụ thể, điều mà chúng ta có thể khai thác bằng cách cố gắng truy cập vào mạng bằng một địa chỉ MAC giả mạo.

## Giao Thức Phân Giải Địa Chỉ (Address Resolution Protocol)

[Address Resolution Protocol](https://en.wikipedia.org/wiki/Address_Resolution_Protocol) (**ARP**) là một giao thức mạng. Đây là một phần quan trọng trong giao tiếp mạng, được dùng để phân giải một địa chỉ IP ở tầng mạng (tầng 3) thành một địa chỉ MAC ở tầng liên kết dữ liệu (tầng 2). Nó ánh xạ địa chỉ IP của một host đến địa chỉ MAC tương ứng của nó nhằm tạo điều kiện giao tiếp giữa các thiết bị trên một [Mạng Cục Bộ](https://en.wikipedia.org/wiki/Local_area_network) (**LAN**). Khi một thiết bị trên LAN muốn giao tiếp với một thiết bị khác, nó sẽ gửi một thông điệp broadcast chứa địa chỉ IP đích và địa chỉ MAC của chính nó. Thiết bị có địa chỉ IP trùng khớp sẽ phản hồi bằng địa chỉ MAC của chính nó, và sau đó hai thiết bị này có thể giao tiếp trực tiếp bằng cách sử dụng địa chỉ MAC của chúng. Quá trình này được gọi là phân giải ARP (ARP resolution).

ARP là một phần quan trọng trong quá trình giao tiếp mạng vì nó cho phép các thiết bị gửi và nhận dữ liệu bằng cách sử dụng địa chỉ MAC thay vì địa chỉ IP, điều này có thể hiệu quả hơn. Có hai loại thông điệp yêu cầu có thể được sử dụng:

### ARP Request (Yêu Cầu ARP)

Khi một thiết bị muốn giao tiếp với một thiết bị khác trên một LAN, nó sẽ gửi một yêu cầu ARP để phân giải địa chỉ IP của thiết bị đích thành địa chỉ MAC của nó. Yêu cầu này được phát broadcast đến tất cả các thiết bị trên LAN và chứa địa chỉ IP của thiết bị đích. Thiết bị có địa chỉ IP trùng khớp sẽ phản hồi bằng địa chỉ MAC của mình.

### ARP Reply (Phản Hồi ARP)

Khi một thiết bị nhận được một yêu cầu ARP, nó sẽ gửi một phản hồi ARP đến thiết bị yêu cầu kèm theo địa chỉ MAC của mình. Thông điệp phản hồi này chứa cả địa chỉ IP và địa chỉ MAC của cả thiết bị yêu cầu và thiết bị phản hồi.

### [Ghi Nhận Bằng Tshark](#Tshark-Capture) Đối Với Các Yêu Cầu ARP

![image](https://github.com/user-attachments/assets/0da980e3-2ba3-40bb-bd02-c9330aa6b0dc)

Thông điệp "**who has**" (ai có) ở dòng thứ nhất và thứ ba cho thấy rằng một thiết bị đang yêu cầu địa chỉ MAC cho địa chỉ IP được chỉ định, trong khi dòng thứ hai và thứ tư thể hiện phản hồi ARP kèm theo địa chỉ MAC của thiết bị đích.

Tuy nhiên, giao thức này cũng dễ bị tấn công, chẳng hạn như [Giả Mạo ARP (ARP Spoofing)](https://en.wikipedia.org/wiki/ARP_spoofing), có thể được sử dụng để chặn hoặc thao túng lưu lượng truy cập trên mạng. Tuy nhiên, để bảo vệ chống lại các cuộc tấn công như vậy, điều quan trọng là phải triển khai các biện pháp bảo mật như tường lửa và hệ thống phát hiện xâm nhập.

**[Giả mạo ARP](#arp-spoofing)**, còn được gọi là **đầu độc bộ nhớ đệm ARP (ARP cache poisoning)** hoặc **định tuyến đầu độc ARP (ARP poison routing)**, là một cuộc tấn công có thể được thực hiện bằng các công cụ như [Ettercap](https://github.com/Ettercap/ettercap) hoặc [Cain](https://github.com/xchwarze/Cain) & Abel, trong đó chúng ta gửi các thông điệp ARP giả mạo qua một LAN. Mục tiêu là liên kết địa chỉ MAC của chúng ta với địa chỉ IP của một thiết bị hợp pháp trên mạng của công ty, từ đó cho phép chúng ta chặn được lưu lượng dành cho thiết bị hợp pháp đó. Ví dụ, điều này có thể trông giống như sau:

![image](https://github.com/user-attachments/assets/242b6178-5ecd-405b-9994-b55bcad7a5ae)

Dòng thứ nhất và thứ tư cho thấy chúng ta (**10.129.12.100**) đang gửi các thông điệp ARP giả mạo đến mục tiêu, liên kết địa chỉ MAC của mình với địa chỉ IP của mục tiêu (**10.129.12.101**). Dòng thứ hai và thứ ba cho thấy mục tiêu đang gửi một yêu cầu ARP và phản hồi đến địa chỉ MAC của chúng ta. Điều này cho thấy rằng chúng ta đã đầu độc thành công bộ nhớ đệm ARP của mục tiêu và tất cả lưu lượng dành cho mục tiêu giờ đây sẽ được gửi đến địa chỉ MAC của chúng ta.

Chúng ta có thể sử dụng việc đầu độc ARP để thực hiện nhiều hoạt động khác nhau, chẳng hạn như đánh cắp thông tin nhạy cảm, chuyển hướng lưu lượng, hoặc khởi động các cuộc tấn công MITM (Man-in-the-Middle). Tuy nhiên, để bảo vệ chống lại việc giả mạo ARP, điều quan trọng là phải sử dụng các giao thức mạng an toàn, chẳng hạn như IPSec hoặc SSL, và triển khai các biện pháp bảo mật như tường lửa và hệ thống phát hiện xâm nhập.

---

## Đọc Thêm

### Ghi Nhận Bằng Tshark (Tshark Capture)

TShark là một công cụ phân tích giao thức mạng. Nó cho phép bạn ghi lại dữ liệu gói tin từ một mạng đang hoạt động, hoặc đọc các gói tin từ một tệp ghi nhận đã được lưu trước đó, sau đó in ra dạng đã giải mã của các gói tin đó ra màn hình chuẩn (standard output) hoặc ghi các gói tin vào một tệp. Định dạng tệp ghi nhận gốc của TShark là định dạng pcapng, đây cũng là định dạng được sử dụng bởi Wireshark và nhiều công cụ khác.
**[Trang Hướng Dẫn tshark(1)](https://www.wireshark.org/docs/man-pages/tshark.html)**

### Giả Mạo ARP (ARP Spoofing)

![image](https://www.networkacademy.io/sites/default/files/inline-images/arp-spoofing.gif)

Giả mạo ARP là một loại tấn công trong đó kẻ tấn công gửi các thông điệp ARP (Address Resolution Protocol) giả mạo qua một mạng cục bộ. Điều này dẫn đến việc liên kết địa chỉ MAC của kẻ tấn công với địa chỉ IP của một máy tính hoặc máy chủ hợp pháp trên mạng. [Tìm hiểu thêm về Giả Mạo ARP](https://www.veracode.com/security/arp-spoofing#:~:text=ARP%20spoofing%20is%20a%20type,or%20server%20on%20the%20network.)

### Ettercap

![image](https://github.com/user-attachments/assets/80ea8d4e-ccfe-4187-bbac-0ded983a61dc)

Ettercap là một bộ công cụ toàn diện cho các cuộc tấn công man-in-the-middle. Nó có tính năng theo dõi (sniffing) các kết nối đang hoạt động, lọc nội dung theo thời gian thực, và nhiều thủ thuật thú vị khác. Nó hỗ trợ phân tích chủ động và thụ động nhiều giao thức khác nhau, đồng thời bao gồm nhiều tính năng để phân tích mạng và host. [thông tin thêm](https://www.ettercap-project.org/index.html)
