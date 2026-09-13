# Tầng Mạng (Network Layer)

**Tầng mạng (Layer 3 - Network Layer)** của **OSI** kiểm soát việc trao đổi các gói dữ liệu, vì các gói tin này không thể được định tuyến trực tiếp đến bên nhận và do đó phải được cung cấp các node định tuyến. Các gói dữ liệu sau đó được chuyển từ node này sang node khác cho đến khi chúng đến được đích. Để thực hiện điều này, **tầng mạng** xác định từng node mạng riêng lẻ, thiết lập và giải phóng các kênh kết nối, đồng thời đảm nhận việc định tuyến và kiểm soát luồng dữ liệu. Khi gửi các gói tin, các địa chỉ sẽ được đánh giá, và dữ liệu được định tuyến qua mạng từ node này sang node khác. Thông thường, không có việc xử lý dữ liệu ở các tầng cao hơn **L3** tại các node. Dựa trên các địa chỉ, việc định tuyến và xây dựng các bảng định tuyến được thực hiện.

Tóm lại, tầng này chịu trách nhiệm cho các chức năng sau:

- Đánh Địa Chỉ Logic (Logical Addressing)
- Định Tuyến (Routing)

Các giao thức được định nghĩa ở mỗi tầng của **OSI**, và các giao thức này đại diện cho một tập hợp các quy tắc để giao tiếp ở tầng tương ứng. Chúng trong suốt (transparent) đối với các giao thức của các tầng phía trên hoặc phía dưới. Một số giao thức thực hiện các nhiệm vụ của nhiều tầng và mở rộng qua hai tầng trở lên. Các giao thức được sử dụng nhiều nhất ở tầng này bao gồm:

- IPv4 / IPv6
- IPsec
- ICMP
- IGMP
- RIP
- OSPF

Tầng này đảm bảo việc định tuyến các gói tin từ nguồn đến đích bên trong hoặc bên ngoài một mạng con (subnet). Hai mạng con này có thể có các lược đồ đánh địa chỉ khác nhau hoặc các loại địa chỉ không tương thích với nhau. Trong cả hai trường hợp, việc truyền dữ liệu mỗi lần đều đi qua toàn bộ mạng lưới giao tiếp và bao gồm việc định tuyến giữa các node mạng. Vì việc giao tiếp trực tiếp giữa bên gửi và bên nhận không phải lúc nào cũng khả thi do sự khác biệt giữa các mạng con, các gói tin phải được chuyển tiếp từ các node (router) nằm trên đường đi. Các gói tin được chuyển tiếp sẽ không đến được các tầng cao hơn mà thay vào đó được gán một đích trung gian mới và được gửi đến node tiếp theo.

![image](https://github.com/user-attachments/assets/5b54150a-8dba-49a3-9108-7a0df84c0e92)
