# Chia Mạng Con (Subnetting)

![image](https://github.com/user-attachments/assets/7b9181f6-3c06-4d9a-904f-1ceb0531bc74)


Việc chia một dải địa chỉ IPv4 thành nhiều dải địa chỉ nhỏ hơn được gọi là **subnetting** (chia mạng con).

Một subnet (mạng con) là một phân đoạn logic của một mạng sử dụng các địa chỉ IP có cùng địa chỉ mạng. Chúng ta có thể hình dung một subnet giống như một lối vào được đánh dấu trên một hành lang tòa nhà lớn. Ví dụ, đây có thể là một cánh cửa kính ngăn cách các phòng ban khác nhau của một tòa nhà công ty. Với sự trợ giúp của subnetting, chúng ta có thể tự tạo ra một subnet cụ thể hoặc tìm ra các thông tin tổng quan sau đây của mạng tương ứng:

- Địa chỉ mạng (Network address)
- Địa chỉ broadcast (Broadcast address)
- Host đầu tiên (First host)
- Host cuối cùng (Last host)
- Số lượng host (Number of hosts)

Hãy lấy địa chỉ IPv4 và subnet mask sau đây làm ví dụ:

- Địa chỉ IPv4: **192.168.12.160**
- Subnet Mask: **255.255.255.192**
- CIDR: **192.168.12.160/26**

Chúng ta đã biết rằng một địa chỉ IP được chia thành **phần mạng (network part)** và **phần host (host part)**.

### Phần Mạng (Network Part)

![image](https://github.com/user-attachments/assets/ff619ad7-a618-4bf2-8419-c4a3f233758a)

Trong subnetting, chúng ta sử dụng subnet mask như một khuôn mẫu cho địa chỉ IPv4. Từ các bit **1** trong subnet mask, chúng ta biết được những bit nào trong địa chỉ IPv4 **không thể** thay đổi. Những bit này là **cố định** và do đó xác định "mạng chính" mà subnet đó nằm trong đó.

### Phần Host (Host Part)

![image](https://github.com/user-attachments/assets/2e8e5016-aaa6-4be1-97a1-fc53d02c1eee)

Các bit trong **phần host** có thể được thay đổi để tạo ra địa chỉ **đầu tiên** và **cuối cùng**. Địa chỉ đầu tiên là **địa chỉ mạng (network address)**, và địa chỉ cuối cùng là **địa chỉ broadcast (broadcast address)** cho subnet tương ứng.

**Địa chỉ mạng** có vai trò quan trọng đối với việc chuyển giao một gói dữ liệu. Nếu **địa chỉ mạng** của địa chỉ nguồn và địa chỉ đích giống nhau, gói dữ liệu sẽ được chuyển giao trong cùng một subnet. Nếu các địa chỉ mạng khác nhau, gói dữ liệu phải được định tuyến đến một subnet khác thông qua **default gateway (cổng mặc định)**.

**Subnet mask** xác định vị trí sự phân chia này diễn ra.

### Phân Chia Giữa Phần Mạng & Phần Host

![image](https://github.com/user-attachments/assets/987ab36c-51f1-434b-803a-7c2830ffb2ea)

### Địa Chỉ Mạng (Network Address)

Vì vậy, nếu bây giờ chúng ta đặt tất cả các bit trong **phần host** của địa chỉ IPv4 thành **0**, chúng ta sẽ có được **địa chỉ mạng** tương ứng của subnet đó.

![image](https://github.com/user-attachments/assets/a203f0c8-19e7-41ae-a1de-27e92e32033b)

### Địa Chỉ Broadcast (Broadcast Address)

Nếu chúng ta đặt tất cả các bit trong **phần host** của địa chỉ IPv4 thành **1**, chúng ta sẽ có được **địa chỉ broadcast**.

![image](https://github.com/user-attachments/assets/45dbfdd3-ae44-4938-8603-9826334104d5)

Vì bây giờ chúng ta đã biết rằng các địa chỉ IPv4 **192.168.12.128** và **192.168.12.191** đã được sử dụng, tất cả các địa chỉ IPv4 còn lại tương ứng sẽ nằm trong khoảng **192.168.12.129-190**. Bây giờ chúng ta biết rằng subnet này cung cấp cho chúng ta tổng cộng **64 - 2** (địa chỉ mạng & địa chỉ broadcast), tức là **62** địa chỉ IPv4 mà chúng ta có thể gán cho các host của mình.

![image](https://github.com/user-attachments/assets/b429c77c-a138-4d5f-888b-26b80bf8966f)

### Chia Mạng Con Thành Các Mạng Nhỏ Hơn

Bây giờ, giả sử rằng chúng ta, với tư cách là quản trị viên, được giao nhiệm vụ chia subnet được gán cho chúng ta thành 4 subnet bổ sung. Do đó, điều quan trọng cần biết là chúng ta chỉ có thể chia các subnet dựa trên hệ nhị phân.

![image](https://github.com/user-attachments/assets/41371a2b-32d3-4c64-97a6-be047649f60e)

Vì vậy, chúng ta có thể chia số 64 host mà chúng ta đã biết cho 4. Số 4 tương đương với lũy thừa 2^2 trong hệ nhị phân, vì vậy chúng ta tìm ra được số bit của subnet mask mà chúng ta cần mở rộng thêm. Vậy chúng ta biết các thông số sau:

- Subnet: **192.168.12.128/26**
- Số Subnet Cần Thiết: **4**

Bây giờ chúng ta tăng/mở rộng subnet mask của mình thêm **2 bit**, từ **/26** thành **/28**, và nó sẽ trông như thế này:

![image](https://github.com/user-attachments/assets/f00fe1fa-8a9d-43c9-9405-d4938f93a0a3)

Tiếp theo, chúng ta có thể chia **64** địa chỉ IPv4 mà chúng ta có sẵn thành **4 phần**:

![image](https://github.com/user-attachments/assets/223fd0d3-55e4-4de7-8e67-001e25ddaffe)

Vì vậy, chúng ta biết được mỗi subnet sẽ có kích thước bao nhiêu. Từ giờ trở đi, chúng ta bắt đầu từ địa chỉ mạng đã được cấp cho chúng ta (192.168.12.128) và cộng thêm **16** host **4** lần:

![image](https://github.com/user-attachments/assets/a06521db-f303-4396-832d-80128d6891af)

### Chia Mạng Con Bằng Nhẩm (Mental Subnetting)

Có vẻ như có rất nhiều phép tính liên quan đến việc chia mạng con, nhưng mỗi octet đều lặp lại theo cùng một cách, và mọi thứ đều là lũy thừa của hai, nên không cần phải ghi nhớ quá nhiều. Điều đầu tiên cần làm là xác định octet nào sẽ thay đổi.

![image](https://github.com/user-attachments/assets/7341ab2e-c31a-4af6-84ec-3a4fa940b287)

Chúng ta có thể xác định octet nào của địa chỉ IP có thể thay đổi bằng cách ghi nhớ bốn con số đó. Với Địa Chỉ Mạng: **192.168.1.1/25**, có thể thấy ngay rằng 192.168.2.4 sẽ không nằm trong cùng một mạng, vì subnet **/25** có nghĩa là chỉ có octet thứ tư mới có thể thay đổi.

![image](https://github.com/user-attachments/assets/ebfde63d-0325-47a1-833e-4c6cb369f37d)

Bằng cách ghi nhớ các lũy thừa của hai cho đến số tám, việc tính toán có thể trở nên tức thì. Tuy nhiên, nếu quên, cách nhanh hơn có thể là nhớ chia đôi số 256 theo số lần tương ứng với số dư.

Phần khó nhất ở đây là xác định phạm vi địa chỉ IP thực tế, vì trong mạng máy tính, số 0 là một con số chứ không phải là số rỗng (null). Vì vậy, trong ví dụ **/25** của chúng ta với 128 địa chỉ IP, dải đầu tiên là **192.168.1.0-127**. Địa chỉ đầu tiên là địa chỉ mạng, và địa chỉ cuối cùng là địa chỉ broadcast, điều này có nghĩa là **dải IP có thể sử dụng** sẽ trở thành **192.168.1.1-126**. Nếu địa chỉ IP của chúng ta nằm trên 128, thì **dải IP có thể sử dụng** sẽ là 192.168.1.129-254 (128 là địa chỉ mạng và 255 là địa chỉ broadcast).
