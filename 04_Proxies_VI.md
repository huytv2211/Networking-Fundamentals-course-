# Proxy

![image](https://github.com/user-attachments/assets/3a1fc021-8673-4823-b7bf-696b42f56d45)

## Proxy Là Gì?

Nói chung, proxy là một thiết bị hoặc dịch vụ đóng vai trò trung gian trong việc giao tiếp giữa hai bên. Vai trò then chốt của việc là trung gian trong một proxy là thiết bị trung gian đó phải có khả năng kiểm tra nội dung của lưu lượng truy cập. Nếu thiết bị trung gian chỉ đơn giản chuyển tiếp lưu lượng mà không kiểm tra, nó được gọi là Gateway, chứ không phải là proxy.

## Sự Khác Biệt Giữa VPN và Proxy:

Nhiều người nhầm tưởng rằng việc thay đổi địa chỉ IP có nghĩa là đang sử dụng proxy. Tuy nhiên, VPN (Mạng Riêng Ảo) thường được dùng phổ biến hơn để thay đổi vị trí địa lý và mã hóa lưu lượng truy cập. Nhưng trong hầu hết các trường hợp, VPN không phải là proxy, vì nó không đóng vai trò trung gian để kiểm tra nội dung; thay vào đó, nó mã hóa và truyền lưu lượng qua đường hầm (tunnel).

## Tầng OSI và Proxy:

Proxy thường hoạt động ở Tầng 7 (Tầng Ứng Dụng - Application Layer) của mô hình OSI, vì nó liên quan đến việc kiểm tra nội dung (chẳng hạn như các yêu cầu HTTP). Điều này phân biệt nó với Gateway hoặc VPN, vốn có thể hoạt động ở các tầng thấp hơn, chẳng hạn như Tầng 3 (Tầng Mạng - Network Layer).

## Các Loại Proxy:

1. Proxy Chuyên Dụng / Proxy Chuyển Tiếp (Forward Proxy)
- Loại proxy này giúp người dùng cuối kết nối với internet.
- Người dùng gửi yêu cầu của họ đến proxy, và proxy chuyển tiếp các yêu cầu đó đến đích.
- Loại này thường được sử dụng cho các mục đích như vượt qua các hạn chế truy cập, lưu trữ đệm (caching) dữ liệu, hoặc kiểm soát truy cập.

2. Proxy Ngược (Reverse Proxy)
- Loại proxy này được đặt ở phía máy chủ và quản lý các yêu cầu đến từ người dùng.
- Nó thường được sử dụng để tăng cường bảo mật, cân bằng tải (load balancing), hoặc để ẩn thông tin chi tiết của các máy chủ thực tế.
- Các công cụ như Cloudflare hoặc ModSecurity thuộc loại này.

3. Proxy Trong Suốt (Transparent Proxy)
- Trong loại proxy này, người dùng có thể không biết rằng lưu lượng của họ đang đi qua một proxy.
- Loại này thường được các tổ chức sử dụng để kiểm soát hoặc giám sát lưu lượng truy cập.


## Proxy Chuyên Dụng / Proxy Chuyển Tiếp (Forward Proxy)

**Forward Proxy** chính là những gì hầu hết mọi người hình dung khi nghĩ về một proxy. Forward Proxy là khi một máy khách (client) gửi yêu cầu đến một máy tính, và máy tính đó thực hiện yêu cầu đó.

Ví dụ, trong một mạng doanh nghiệp, các máy tính chứa dữ liệu nhạy cảm có thể không được phép truy cập trực tiếp vào Internet. Để truy cập một trang web, chúng phải đi qua một proxy (hoặc bộ lọc web). Đây có thể là một tuyến phòng thủ cực kỳ mạnh mẽ chống lại phần mềm độc hại, vì không chỉ nó cần phải vượt qua bộ lọc web (điều này khá dễ), mà nó còn cần phải nhận biết được proxy (proxy aware) hoặc sử dụng một cơ chế C2 không truyền thống (cách để phần mềm độc hại nhận thông tin chỉ thị). Nếu tổ chức chỉ sử dụng FireFox, khả năng gặp phải phần mềm độc hại có nhận biết proxy là khó xảy ra.

Các trình duyệt web như Internet Explorer, Edge, hoặc Chrome đều mặc định tuân theo cài đặt "System Proxy" (Proxy Hệ Thống). Nếu phần mềm độc hại sử dụng [WinSock](https://en.wikipedia.org/wiki/Winsock) (API gốc của Windows), nó có khả năng sẽ nhận biết được proxy mà không cần thêm bất kỳ đoạn mã nào. Firefox không sử dụng WinSock mà thay vào đó sử dụng [libcurl](https://curl.se/libcurl/), điều này cho phép nó dùng cùng một đoạn mã trên bất kỳ hệ điều hành nào. Điều này có nghĩa là phần mềm độc hại sẽ cần phải tìm kiếm Firefox và lấy cài đặt proxy từ đó, điều mà phần mềm độc hại rất khó có khả năng thực hiện.

Ngoài ra, phần mềm độc hại có thể sử dụng DNS như một [cơ chế C2](https://pentera.io/glossary/command-and-control-c2-attacks/#:~:text=Command%20and%20Control%20(C2)%20refers%20to%20the%20mechanisms%20used%20by,to%20malware%20on%20compromised%20devices.), nhưng nếu một tổ chức đang giám sát DNS (điều này dễ dàng thực hiện được bằng cách sử dụng [Sysmon](https://medium.com/falconforce/sysmon-11-dns-improvements-and-filedelete-events-7a74f17ca842)), thì loại lưu lượng này sẽ nhanh chóng bị phát hiện.

Một ví dụ khác về Forward Proxy là [Burp Suite](https://www.geeksforgeeks.org/what-is-burp-suite/), vì hầu hết mọi người sử dụng nó để chuyển tiếp các yêu cầu HTTP. Tuy nhiên, ứng dụng này là "con dao đa năng" của các HTTP Proxy và có thể được cấu hình để hoạt động như một proxy ngược hoặc proxy trong suốt!

![image](https://github.com/user-attachments/assets/74174c18-9fa6-41da-aed3-d63794427b0c)

## Proxy Ngược (Reverse Proxy)

Như bạn có thể đoán được, **reverse proxy** (proxy ngược) là ngược lại với **Forward Proxy**. Thay vì được thiết kế để lọc các yêu cầu đi ra ngoài, nó lọc các yêu cầu đi vào. Mục tiêu phổ biến nhất của một Reverse Proxy là lắng nghe (listen) trên một địa chỉ và chuyển tiếp nó đến một mạng khép kín.

Nhiều tổ chức sử dụng CloudFlare vì họ có một hệ thống mạng mạnh mẽ có thể chống chịu hầu hết các cuộc tấn công DDOS. Bằng cách sử dụng Cloudflare, các tổ chức có cách để lọc số lượng (và loại) lưu lượng truy cập được gửi đến máy chủ web của họ.

Các chuyên gia kiểm thử xâm nhập (Penetration Tester) sẽ cấu hình các reverse proxy trên các điểm cuối (endpoint) đã bị xâm nhập. Điểm cuối bị xâm nhập sẽ lắng nghe trên một cổng và gửi bất kỳ máy khách nào kết nối đến cổng đó trở lại kẻ tấn công thông qua điểm cuối bị xâm nhập. Điều này hữu ích để vượt qua tường lửa hoặc né tránh việc ghi log. Các tổ chức có thể có [Hệ Thống Phát Hiện Xâm Nhập (IDS)](https://en.wikipedia.org/wiki/Intrusion_detection_system) theo dõi các yêu cầu web ra bên ngoài. Nếu kẻ tấn công có quyền truy cập vào tổ chức qua SSH, một reverse proxy có thể gửi các yêu cầu web qua đường hầm SSH và né tránh được IDS.

Một Reverse Proxy phổ biến khác là [ModSecurity](https://modsecurity.org/), một [Tường Lửa Ứng Dụng Web (Web Application Firewall - WAF)](https://www.cloudflare.com/learning/ddos/glossary/web-application-firewall-waf/). Tường Lửa Ứng Dụng Web kiểm tra các yêu cầu web để tìm nội dung độc hại và chặn yêu cầu đó nếu nó có tính độc hại. Nếu bạn muốn tìm hiểu thêm về vấn đề này, chúng tôi khuyến nghị bạn đọc thêm về [Bộ Quy Tắc Lõi ModSecurity (ModSecurity Core Rule Set)](https://owasp.org/www-project-modsecurity-core-rule-set/), vì đây là một điểm khởi đầu tuyệt vời. Cloudflare cũng có thể hoạt động như một WAF, nhưng để làm được điều đó cần phải cho phép họ giải mã lưu lượng HTTPS, điều mà một số tổ chức có thể không muốn.

![image](https://github.com/user-attachments/assets/d2312fce-e684-4b8a-92d9-c83cac494ac3)

## Proxy Trong Suốt (Non-) Transparent Proxy

Tất cả các dịch vụ proxy này hoạt động theo kiểu **trong suốt (transparent)** hoặc **không trong suốt (non-transparent)**.

Với một **proxy trong suốt (transparent proxy)**, máy khách không biết về sự tồn tại của nó. Proxy trong suốt sẽ chặn các yêu cầu giao tiếp của máy khách đến Internet và đóng vai trò như một thực thể thay thế. Đối với bên ngoài, proxy trong suốt, cũng như proxy không trong suốt, đóng vai trò như một đối tác giao tiếp.

Nếu đó là một **proxy không trong suốt (non-transparent proxy)**, chúng ta phải được thông báo về sự tồn tại của nó. Với mục đích này, chúng ta và phần mềm mà chúng ta muốn sử dụng sẽ được cung cấp một cấu hình proxy đặc biệt để đảm bảo rằng lưu lượng đến Internet trước tiên được gửi đến proxy. Nếu cấu hình này không tồn tại, chúng ta sẽ không thể giao tiếp thông qua proxy. Tuy nhiên, vì proxy thường cung cấp con đường giao tiếp duy nhất đến các mạng khác, việc giao tiếp với Internet nói chung sẽ bị cắt đứt nếu không có cấu hình proxy tương ứng.
