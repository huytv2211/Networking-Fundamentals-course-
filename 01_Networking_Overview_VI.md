# Tổng Quan Về Mạng
Một mạng cho phép hai máy tính giao tiếp với nhau. Có rất nhiều **cấu trúc liên kết (topologies)** (dạng lưới/dạng cây/dạng sao), **phương tiện truyền dẫn (mediums)** (ethernet/cáp quang/cáp đồng trục/không dây), và **giao thức (protocols)** (TCP/UDP/IPX) có thể được sử dụng để thiết lập mạng.


# Thông Tin Cơ Bản
Hãy cùng xem sơ đồ tổng quan sau đây về cách một hệ thống làm việc tại nhà (Work From Home) có thể hoạt động.
![basic_information_image](https://github.com/user-attachments/assets/bcc3f0c5-ae6c-4d11-a2cd-6e19bd95bf80)

Toàn bộ internet được xây dựng dựa trên rất nhiều mạng con được chia nhỏ, như được thể hiện trong ví dụ và được đánh dấu là "Mạng Gia Đình" (Home Network) và "Mạng Công Ty" (Company Network). Chúng ta có thể hình dung việc kết nối mạng giống như việc gửi thư hoặc bưu kiện từ máy tính này đến máy tính khác.

Giả sử chúng ta có một tình huống là muốn truy cập vào trang web của một công ty từ **"Mạng Gia Đình"** của mình. Trong trường hợp đó, chúng ta trao đổi dữ liệu với trang web của công ty đặt tại **"Mạng Công Ty"** của họ. Cũng giống như khi gửi thư hay bưu kiện, chúng ta biết địa chỉ nơi các gói tin cần đến. Địa chỉ trang web hay **Uniform Resource Locator (URL)** mà chúng ta nhập vào trình duyệt còn được gọi là **Fully Qualified Domain Name (FQDN)**.

Thực tế là chúng ta biết địa chỉ, nhưng không biết **vị trí địa lý** chính xác của địa chỉ đó. Trong tình huống này, bưu điện có thể xác định vị trí chính xác, sau đó chuyển tiếp các gói tin đến nơi cần đến. Vì vậy, bưu điện của chúng ta sẽ chuyển tiếp gói tin đến bưu điện trung tâm, đại diện cho **Nhà Cung Cấp Dịch Vụ Internet (Internet Service Provider - ISP)** của chúng ta.

Bưu điện của chúng ta chính là **bộ định tuyến (router)** mà chúng ta sử dụng để kết nối với **"Internet"** trong mạng máy tính.

Ngay khi chúng ta gửi gói tin qua bưu điện **(router)** của mình, gói tin sẽ được chuyển tiếp đến **bưu điện trung tâm (ISP)**. Bưu điện trung tâm này sẽ tra cứu trong **sổ đăng ký địa chỉ/danh bạ (Domain Name Service)** để tìm nơi địa chỉ đó nằm ở đâu, và trả về tọa độ địa lý tương ứng **(địa chỉ IP)**. Bây giờ khi đã biết vị trí chính xác của địa chỉ, gói tin của chúng ta sẽ được gửi trực tiếp đến đó bằng một "chuyến bay thẳng" thông qua bưu điện trung tâm của chúng ta.

Sau khi máy chủ web nhận được gói tin của chúng ta với yêu cầu hiển thị nội dung trang web của họ, máy chủ web sẽ gửi lại cho chúng ta gói tin chứa dữ liệu để hiển thị trang web đó, thông qua bưu điện **(router)** của **"Mạng Công Ty"**, đến đúng địa chỉ trả về được chỉ định **(địa chỉ IP của chúng ta)**.
