# Địa Chỉ IP

![image](https://github.com/user-attachments/assets/8f02fbc9-f541-4503-95c5-15f80290e7fe)

Mỗi host nằm trong mạng có thể được xác định bằng địa chỉ **Media Access Control** (**MAC**). Điều này cho phép trao đổi dữ liệu trong cùng một mạng. Nếu host từ xa nằm trong một mạng khác, việc chỉ biết địa chỉ **MAC** là không đủ để thiết lập kết nối. Việc đánh địa chỉ trên Internet được thực hiện thông qua địa chỉ **IPv4** và/hoặc **IPv6**, được cấu thành từ **địa chỉ mạng (network address)** và **địa chỉ host (host address)**.

Không quan trọng đó là một mạng nhỏ, chẳng hạn như mạng máy tính gia đình, hay toàn bộ Internet. Địa chỉ IP đảm bảo việc chuyển giao dữ liệu đến đúng bên nhận. Chúng ta có thể hình dung cách biểu diễn của địa chỉ **MAC** và **IPv4** / **IPv6** như sau:

- **IPv4** / **IPv6** - mô tả địa chỉ bưu điện và khu vực duy nhất của tòa nhà bên nhận.
- **MAC** - mô tả chính xác tầng và căn hộ của bên nhận.

Một địa chỉ IP duy nhất có thể được dùng để gửi đến nhiều bên nhận (broadcasting), hoặc một thiết bị có thể phản hồi với nhiều địa chỉ IP. Tuy nhiên, cần đảm bảo rằng mỗi địa chỉ IP chỉ được gán một lần duy nhất trong phạm vi mạng.


## Cấu Trúc IPv4

Phương pháp phổ biến nhất để gán địa chỉ IP là **IPv4**, bao gồm một số nhị phân **32-bit** được kết hợp thành **4 byte**, mỗi byte là một nhóm **8-bit** (**octet**) có giá trị từ **0-255**. Các giá trị này được chuyển đổi thành các số thập phân dễ đọc hơn, ngăn cách bằng dấu chấm và được biểu diễn dưới dạng ký hiệu thập phân có dấu chấm (dotted-decimal notation).

Vì vậy, một địa chỉ IPv4 có thể trông như thế này:

![image](https://github.com/user-attachments/assets/334ea9cf-20b4-4607-93d0-9c6d4e8c0b4f)

Mỗi giao diện mạng (card mạng, máy in mạng, hoặc router) đều được gán một địa chỉ IP **duy nhất**.

Định dạng **IPv4** cho phép 4.294.967.296 địa chỉ duy nhất. Địa chỉ IP được chia thành **phần host** và **phần mạng**. **Router** sẽ gán **phần host** của địa chỉ IP tại nhà hoặc do một quản trị viên thực hiện. **Quản trị viên mạng** tương ứng sẽ gán **phần mạng**. Trên Internet, đây là **IANA** [(Internet Assigned Numbers Authority)](https://www.iana.org/), tổ chức phân bổ và quản lý các địa chỉ IP duy nhất.

Trước đây, việc phân loại chi tiết hơn cũng đã được thực hiện. Các khối mạng IP được chia thành **lớp A - E**. Các lớp khác nhau khác biệt nhau về độ dài tương ứng của phần host và phần mạng.

![image](https://github.com/user-attachments/assets/dde16279-abf2-4a23-8346-024cd3697967)

## Mặt Nạ Mạng Con (Subnet Mask)

Việc phân chia sâu hơn các lớp này thành các mạng nhỏ hơn được thực hiện với sự trợ giúp của **subnetting** (chia mạng con). Việc phân chia này được thực hiện bằng cách sử dụng **netmask (mặt nạ mạng)**, có độ dài bằng với một địa chỉ IPv4. Cũng giống như với các lớp, nó mô tả vị trí bit nào trong địa chỉ IP đóng vai trò là **phần mạng** hoặc **phần host**.

![image](https://github.com/user-attachments/assets/3bd8ab9b-0390-45a1-9c78-3752a2fd13e4)

## Địa Chỉ Mạng và Địa Chỉ Cổng Mặc Định (Gateway)

**Hai** địa chỉ **IP** bổ sung được thêm vào trong **cột IP** được dành riêng cho cái gọi là **địa chỉ mạng (network address)** và **địa chỉ broadcast (broadcast address)**. Một vai trò quan trọng khác là **default gateway (cổng mặc định)**, tên gọi của địa chỉ IPv4 của **router** kết nối các mạng và hệ thống có giao thức khác nhau, đồng thời quản lý địa chỉ và phương thức truyền dữ liệu. Thông thường, **default gateway** sẽ được gán địa chỉ IPv4 đầu tiên hoặc cuối cùng có thể gán được trong một mạng con. Đây không phải là một yêu cầu kỹ thuật bắt buộc, nhưng đã trở thành một tiêu chuẩn phổ biến trong môi trường mạng ở mọi quy mô.

![image](https://github.com/user-attachments/assets/334d9561-5166-478b-8781-dc6a4d8d1770)

## Địa Chỉ Broadcast

Nhiệm vụ của địa chỉ IP **broadcast** là kết nối tất cả các thiết bị trong một mạng với nhau. **Broadcast** trong một mạng là một thông điệp được truyền đến tất cả các thành viên trong mạng và không yêu cầu bất kỳ phản hồi nào. Bằng cách này, một host gửi một gói dữ liệu đến tất cả các thành viên khác của mạng cùng một lúc, và khi làm như vậy, nó thông báo **địa chỉ IP** của mình, mà các bên nhận có thể sử dụng để liên hệ với nó. Đây là địa chỉ **IPv4 cuối cùng** được sử dụng cho **broadcast**.

![image](https://github.com/user-attachments/assets/5d0bd1d0-1668-498c-ab2a-5b184df72006)

## Hệ Nhị Phân

Hệ nhị phân là một hệ thống số chỉ sử dụng hai trạng thái khác nhau được biểu diễn bằng hai số (**0** và **1**), trái ngược với hệ thập phân (0 đến 9).

Như chúng ta đã thấy, một địa chỉ IPv4 được chia thành 4 octet. Mỗi **octet** bao gồm **8 bit**. Mỗi vị trí của một bit trong một octet có một giá trị thập phân cụ thể. Hãy lấy địa chỉ IPv4 sau đây làm ví dụ:

- Địa chỉ IPv4: **192.168.10.39**

Dưới đây là ví dụ về hình dạng của **octet đầu tiên**:

### Octet Thứ 1 - Giá Trị: 192

![image](https://github.com/user-attachments/assets/eeb5b750-49e5-4c6c-aaee-2dfb9dce7bd4)

Nếu chúng ta tính tổng của tất cả các giá trị này cho mỗi octet mà bit được đặt bằng 1, chúng ta sẽ có tổng:

![image](https://github.com/user-attachments/assets/a00ca544-6c45-4775-9fec-8a03162df9c4)

Toàn bộ cách biểu diễn từ nhị phân sang thập phân sẽ trông như thế này:

### IPv4 - Ký Hiệu Nhị Phân (Binary Notation)

![image](https://github.com/user-attachments/assets/327a9ae7-d3d4-4888-a592-af692d0b15f3)

- Địa chỉ IPv4: **192.168.10.39**

Phép cộng này được thực hiện cho mỗi octet, dẫn đến cách biểu diễn thập phân của **địa chỉ IPv4**. Subnet mask cũng được tính toán theo cách tương tự.

### IPv4 - Từ Thập Phân Sang Nhị Phân

![image](https://github.com/user-attachments/assets/9df5dfcb-7052-4ff6-b4a2-ecd6dbfc3fd5)

### Subnet Mask

![image](https://github.com/user-attachments/assets/0ba343eb-b1c3-4e7e-aa61-9c1bd3ffca4a)

- Địa chỉ IPv4: **192.168.10.39**
- Subnet mask: **255.255.255.0**

### CIDR

**Classless Inter-Domain Routing** (**CIDR**) là một phương pháp biểu diễn thay thế cho việc gán cố định giữa địa chỉ IPv4 và các lớp mạng (A, B, C, D, E). Việc phân chia dựa trên subnet mask hoặc cái gọi là **hậu tố CIDR (CIDR suffix)**, cho phép phân chia không gian địa chỉ IPv4 theo từng bit, và từ đó chia thành các **mạng con (subnet)** có kích thước bất kỳ. **Hậu tố CIDR** cho biết có bao nhiêu bit tính từ đầu địa chỉ IPv4 thuộc về phần mạng. Đây là một ký hiệu biểu diễn **subnet mask** bằng cách chỉ ra số lượng bit **1** trong subnet mask.

Hãy tiếp tục sử dụng địa chỉ IPv4 và subnet mask sau đây làm ví dụ:

- Địa chỉ IPv4: **192.168.10.39**
- Subnet mask: **255.255.255.0**

Bây giờ, toàn bộ cách biểu diễn của địa chỉ IPv4 và subnet mask sẽ trông như thế này:

- CIDR: **192.168.10.39/24**

Do đó, hậu tố CIDR chính là tổng số các số 1 trong subnet mask.

![image](https://github.com/user-attachments/assets/892b9a3e-8b80-43d9-9276-d605acf799b1)

**(bạn có thể đọc thêm phần mô tả đơn giản hơn về chủ đề này (CIDR) được tạo bởi AI tại phần ([Thông Tin Thêm](#cidr-1))**

---
## Thông Tin Thêm

![image](https://github.com/user-attachments/assets/d5addb2e-2af9-4fde-a069-16b1f43bc24e)
![image](https://github.com/user-attachments/assets/ec4b8467-1470-447d-a679-11ed75f212e0)


### CIDR
#### CIDR Là Gì?
CIDR (Classless Inter-Domain Routing) là một cách để mô tả và tổ chức các địa chỉ IP và mạng. Nó thay thế cho hệ thống cũ, trong đó các địa chỉ IP được chia thành các nhóm cố định (Lớp A, B, C, v.v.).
Thay vì sử dụng các nhóm cố định đó, CIDR sử dụng một con số gọi là hậu tố CIDR (ví dụ: /24) để cho biết bao nhiêu phần của địa chỉ IP thuộc về phần "mạng" và bao nhiêu phần dành cho từng thiết bị riêng lẻ.

#### Hậu Tố CIDR Là Gì?
Hậu tố CIDR là số lượng số 1 trong subnet mask.
Subnet mask chỉ đơn giản là một cách để chia một địa chỉ IP thành hai phần:

- Phần mạng (network part) (dùng chung cho tất cả các thiết bị trong cùng một mạng)
- Phần host (host part) (riêng biệt cho từng thiết bị trong mạng)

Ví dụ:

**Subnet mask:** 255.255.255.0

- Ở dạng nhị phân, đây là `11111111.11111111.11111111.00000000`.
- Nó có 24 số 1, vì vậy hậu tố CIDR là **/24**.

Vì vậy, thay vì viết địa chỉ IP và subnet mask riêng biệt, chúng ta viết:
`192.168.10.39/24`

#### Phân Tích Ví Dụ

Hãy sử dụng ví dụ mà bạn đã đưa ra:
- **Địa chỉ IP:** 192.168.10.39
- **Subnet Mask:** 255.255.255.0
- **Ký Hiệu CIDR:** 192.168.10.39/24

Điều này có nghĩa là:

1. 24 bit đầu tiên của địa chỉ IP (`192.168.10`) thuộc về phần mạng.
2. 8 bit còn lại (phần `.39`) dành cho các thiết bị (host) trong mạng đó.
