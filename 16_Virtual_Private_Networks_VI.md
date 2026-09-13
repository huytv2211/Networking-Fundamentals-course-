# Mạng Riêng Ảo (Virtual Private Networks)

![image](https://github.com/user-attachments/assets/2f9d663f-dc44-490b-a3b9-ae3d23e45df8)

**Mạng Riêng Ảo** (**VPN**) là một công nghệ cho phép thiết lập một kết nối an toàn và được mã hóa giữa một mạng riêng và một thiết bị từ xa. Điều này cho phép máy từ xa truy cập trực tiếp vào mạng riêng, cung cấp quyền truy cập an toàn và bảo mật đến các tài nguyên và dịch vụ của mạng. Ví dụ, một quản trị viên ở một địa điểm khác cần quản lý các máy chủ nội bộ để nhân viên có thể tiếp tục sử dụng các dịch vụ nội bộ. Nhiều công ty giới hạn quyền truy cập vào các máy chủ, vì vậy các máy khách chỉ có thể tiếp cận những máy chủ đó từ mạng cục bộ. Đây là lúc VPN phát huy tác dụng, khi quản trị viên kết nối đến máy chủ VPN qua internet, xác thực bản thân, và từ đó tạo ra một đường hầm được mã hóa để những người khác không thể đọc được dữ liệu đang được truyền tải. Ngoài ra, máy tính của quản trị viên cũng được gán một địa chỉ IP cục bộ (nội bộ) để thông qua đó anh ta có thể truy cập và quản lý các máy chủ nội bộ. Các quản trị viên thường sử dụng VPN để cung cấp quyền truy cập từ xa an toàn và tiết kiệm chi phí vào mạng của một công ty. VPN thường sử dụng cổng **TCP/1723** cho các kết nối VPN [Point-to-Point Tunneling Protocol](https://www.lifewire.com/home-networking-4781492) (**PPTP**) và **UDP/500** cho các kết nối VPN [IKEv1](https://www.cisco.com/c/en/us/support/docs/security-vpn/ipsec-negotiation-ike-protocols/217432-understand-ipsec-ikev1-protocol.html) và [IKEv2](https://nordvpn.com/blog/ikev2ipsec/).

Điều này cho phép nhân viên truy cập vào mạng và các tài nguyên của nó, chẳng hạn như email và máy chủ tệp, từ các địa điểm từ xa, chẳng hạn như tại nhà riêng hoặc khi đang đi công tác. Có nhiều lý do khiến các quản trị viên sử dụng VPN. VPN mã hóa kết nối giữa thiết bị từ xa và mạng riêng, khiến kẻ tấn công gặp khó khăn hơn nhiều trong việc chặn và đánh cắp thông tin nhạy cảm. Nhờ đó, toàn bộ giao tiếp trở nên an toàn hơn.

Một lý do khác là VPN cho phép nhân viên truy cập vào mạng riêng và các tài nguyên của nó từ xa, từ bất kỳ đâu, miễn là họ có kết nối internet. Điều này đặc biệt hữu ích cho những nhân viên cần làm việc từ xa, chẳng hạn như những người đang đi công tác hoặc làm việc tại nhà. Ngoài ra, VPN có thể tiết kiệm chi phí hơn so với các giải pháp truy cập từ xa khác, chẳng hạn như đường dây thuê riêng (leased line) hoặc các kết nối chuyên dụng, vì chúng sử dụng internet công cộng để kết nối người dùng từ xa với mạng riêng.

Hơn nữa, chúng ta có thể sử dụng VPN để kết nối nhiều địa điểm từ xa, chẳng hạn như các văn phòng chi nhánh, thành một mạng riêng duy nhất, giúp việc quản lý và truy cập vào các tài nguyên mạng trở nên dễ dàng hơn. Tuy nhiên, cần có một số thành phần và yêu cầu nhất định để một VPN có thể hoạt động:

![image](https://github.com/user-attachments/assets/e56022cb-af9a-463a-a04e-ec94fd401397)

Máy khách VPN và máy chủ VPN sử dụng các cổng này để thiết lập và duy trì kết nối VPN. Ở tầng TCP/IP, một kết nối VPN thường sử dụng giao thức [Encapsulating Security Payload](https://www.ibm.com/docs/en/i/7.4?topic=protocols-encapsulating-security-payload) (**ESP**) để mã hóa và xác thực lưu lượng VPN. Điều này cho phép máy khách VPN và máy chủ VPN trao đổi dữ liệu qua internet công cộng một cách an toàn.

## IPsec

[Internet Protocol Security](https://www.cloudflare.com/learning/network-layer/what-is-ipsec/) (**IPsec**) là một giao thức bảo mật mạng cung cấp mã hóa và xác thực cho các giao tiếp internet. Đây là một giao thức bảo mật mạnh mẽ và được sử dụng rộng rãi, cung cấp mã hóa và xác thực cho các giao tiếp internet, và hoạt động bằng cách mã hóa phần tải trọng dữ liệu (data payload) của mỗi gói IP và thêm vào một **header xác thực** (**AH**), được sử dụng để xác minh tính toàn vẹn và tính xác thực của gói tin. IPsec sử dụng sự kết hợp của hai giao thức để cung cấp khả năng mã hóa và xác thực:

1. [Authentication Header](https://www.ibm.com/docs/en/i/7.1?topic=protocols-authentication-header) (**AH**): Giao thức này cung cấp tính toàn vẹn và tính xác thực cho các gói IP nhưng không cung cấp khả năng mã hóa. Nó thêm một header xác thực vào mỗi gói IP, chứa một checksum mật mã học có thể được sử dụng để xác minh rằng gói tin chưa bị can thiệp.

2. [Encapsulating Security Payload](https://www.ibm.com/docs/en/i/7.4?topic=protocols-encapsulating-security-payload) (**ESP**): Giao thức này cung cấp khả năng mã hóa và xác thực tùy chọn cho các gói IP. Nó mã hóa phần tải trọng dữ liệu của mỗi gói IP và tùy chọn thêm một header xác thực, tương tự như AH.

IPsec có thể được sử dụng theo hai chế độ.

![image](https://github.com/user-attachments/assets/b399fd88-4aa4-4e83-bd71-a1118082de1f)

Ví dụ, một quản trị viên có thể đặt một tường lửa ở giữa. Để tạo điều kiện cho lưu lượng VPN IPsec từ một máy khách VPN nằm bên ngoài tường lửa đến một máy chủ VPN bên trong, tường lửa cần phải cho phép các giao thức sau:

![image](https://github.com/user-attachments/assets/774b7592-f58e-4cf2-813f-884f7346ff04)

Các giao thức này là cần thiết để tạo điều kiện cho lưu lượng VPN IPsec vì chúng cung cấp tính bảo mật và mã hóa cần thiết cho việc giao tiếp an toàn qua internet công cộng. Nếu không có các giao thức này, lưu lượng VPN sẽ dễ bị chặn và can thiệp.

## PPTP

[Point-to-Point Tunneling Protocol](https://www.vpnranks.com/blog/pptp-vs-l2tp/) (**PPTP**) là một giao thức mạng cho phép tạo ra các VPN bằng cách thiết lập một đường hầm an toàn giữa máy khách VPN và máy chủ VPN, đóng gói dữ liệu được truyền tải trong đường hầm này. Ban đầu là một phần mở rộng của Point-to-Point Protocol (PPP), PPTP được hỗ trợ bởi nhiều hệ điều hành.

Tuy nhiên, do các lỗ hổng bảo mật đã được biết đến, PPTP không còn được coi là an toàn nữa. Nó có thể tạo đường hầm cho các giao thức như IP, IPX, hoặc NetBEUI thông qua IP, nhưng phần lớn đã được thay thế bởi các giao thức VPN an toàn hơn như L2TP/IPsec, IPsec/IKEv2, và OpenVPN. Kể từ năm 2012, việc sử dụng PPTP đã giảm sút vì phương thức xác thực của nó, MSCHAPv2, sử dụng mã hóa DES đã lỗi thời, có thể dễ dàng bị bẻ khóa bằng phần cứng chuyên dụng.
