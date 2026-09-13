# Các Giao Thức Phổ Biến

Các giao thức Internet là các quy tắc và hướng dẫn được tiêu chuẩn hóa, được định nghĩa trong các RFC, quy định cách các thiết bị trong một mạng nên giao tiếp với nhau. Chúng đảm bảo rằng các thiết bị trong một mạng có thể trao đổi thông tin một cách nhất quán và đáng tin cậy, bất kể phần cứng và phần mềm được sử dụng là gì. Để các thiết bị có thể giao tiếp trong một mạng, chúng cần được kết nối thông qua một kênh giao tiếp, chẳng hạn như kết nối có dây hoặc không dây. Sau đó, các thiết bị trao đổi thông tin bằng cách sử dụng một tập hợp các giao thức được tiêu chuẩn hóa, định nghĩa định dạng và cấu trúc của dữ liệu được truyền tải. Hai loại kết nối chính được sử dụng trên các mạng là [Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) (**TCP**) và [User Datagram Protocol](https://en.wikipedia.org/wiki/User_Datagram_Protocol) (**UDP**).

Chúng ta cần tìm hiểu và biết về các giao thức khác nhau và được sử dụng phổ biến nhất. Như chúng ta đã học, các giao thức này là nền tảng của mọi giao tiếp giữa các thiết bị và máy tính của chúng ta trong các mạng. Chúng tôi đã tổng hợp bên dưới nhiều giao thức trong số này mà chúng ta sẽ tìm hiểu xuyên suốt các module. Chúng ta hiểu chúng càng rõ, chúng ta càng có thể làm việc với chúng hiệu quả hơn.

## Transmission Control Protocol (TCP)

**TCP** là một giao thức **hướng kết nối (connection-oriented)**, thiết lập một kết nối ảo giữa hai thiết bị trước khi truyền dữ liệu bằng cách sử dụng [Bắt Tay Ba Bước (Three-Way-Handshake)](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment). Kết nối này được duy trì cho đến khi việc truyền dữ liệu hoàn tất, và các thiết bị có thể tiếp tục gửi dữ liệu qua lại chừng nào kết nối vẫn còn đang hoạt động.

Ví dụ, khi chúng ta nhập một URL vào trình duyệt web, trình duyệt sẽ gửi một yêu cầu HTTP đến máy chủ lưu trữ trang web đó bằng cách sử dụng **TCP**. Máy chủ phản hồi bằng cách gửi lại mã HTML của trang web cho trình duyệt bằng **TCP**. Trình duyệt sau đó sẽ sử dụng mã này để hiển thị trang web trên màn hình của chúng ta. Quá trình này phụ thuộc vào việc một kết nối **TCP** được thiết lập giữa trình duyệt và máy chủ web, và được duy trì cho đến khi việc truyền dữ liệu hoàn tất. Kết quả là, **TCP** đáng tin cậy nhưng chậm hơn UDP vì nó đòi hỏi thêm chi phí (overhead) để thiết lập và duy trì kết nối.

![image](https://github.com/user-attachments/assets/c385dea1-9fa9-4088-a413-8d5c2a8a8c23)
![image](https://github.com/user-attachments/assets/d446b470-fad1-4527-9a6d-02f75f15f550)
![image](https://github.com/user-attachments/assets/aa929886-3883-4efb-93d3-94a9cd72d4e3)

## User Datagram Protocol (UDP)

Mặt khác, **UDP** là một giao thức **phi kết nối (connectionless)**, có nghĩa là nó không thiết lập kết nối ảo trước khi truyền dữ liệu. Thay vào đó, nó gửi các gói dữ liệu đến đích mà không kiểm tra xem chúng đã được nhận hay chưa.

Ví dụ, khi chúng ta phát trực tuyến hoặc xem một video trên một nền tảng như YouTube, dữ liệu video được truyền đến thiết bị của chúng ta bằng cách sử dụng **UDP**. Điều này là vì video có thể chấp nhận một số mất mát dữ liệu, và tốc độ truyền tải quan trọng hơn độ tin cậy. Nếu một vài gói dữ liệu video bị mất trong quá trình truyền tải, điều đó sẽ không ảnh hưởng đáng kể đến chất lượng tổng thể của video. Điều này khiến **UDP** nhanh hơn TCP nhưng kém tin cậy hơn vì không có gì đảm bảo rằng các gói tin sẽ đến được đích.

![image](https://github.com/user-attachments/assets/95e90b22-b861-4681-9c37-050e9ed538c1)
![image](https://github.com/user-attachments/assets/ebb968a6-4f4a-4b74-a1fe-5940b2bb38fb)

### ICMP

[Internet Control Message Protocol](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol) (**ICMP**) là một giao thức được các thiết bị sử dụng để giao tiếp với nhau trên Internet cho nhiều mục đích khác nhau, bao gồm báo cáo lỗi và cung cấp thông tin trạng thái. Nó gửi các yêu cầu và thông điệp giữa các thiết bị, có thể được sử dụng để báo cáo lỗi hoặc cung cấp thông tin trạng thái.

### Yêu Cầu ICMP (ICMP Requests)

Một yêu cầu là một thông điệp được gửi từ thiết bị này đến thiết bị khác để yêu cầu thông tin hoặc thực hiện một hành động cụ thể. Một ví dụ về yêu cầu trong ICMP là yêu cầu ping, dùng để kiểm tra kết nối giữa hai thiết bị. Khi một thiết bị gửi một yêu cầu **ping** đến thiết bị khác, thiết bị thứ hai sẽ phản hồi bằng một thông điệp **ping reply** (phản hồi ping).

### Thông Điệp ICMP (ICMP Messages)

Một thông điệp trong ICMP có thể là một yêu cầu hoặc một phản hồi. Bên cạnh các yêu cầu và phản hồi ping, ICMP còn hỗ trợ các loại thông điệp khác, chẳng hạn như thông điệp lỗi, **destination unreachable** (đích không thể truy cập được), và các thông điệp **time exceeded** (vượt quá thời gian). Các thông điệp này được sử dụng để truyền đạt nhiều loại thông tin và lỗi khác nhau giữa các thiết bị trong mạng.

Ví dụ, nếu một thiết bị cố gắng gửi một gói tin đến một thiết bị khác và gói tin đó không thể được chuyển giao, thiết bị đó có thể sử dụng ICMP để gửi một thông điệp lỗi trở lại cho bên gửi. ICMP có hai phiên bản khác nhau:

**ICMPv4**: Chỉ dành cho IPv4
**ICMPv6**: Chỉ dành cho IPv6

ICMPv4 là phiên bản gốc của **ICMP**, được phát triển để sử dụng với IPv4. Nó vẫn được sử dụng rộng rãi và là phiên bản phổ biến nhất của ICMP. Mặt khác, ICMPv6 được phát triển dành cho IPv6. Nó bao gồm các chức năng bổ sung và được thiết kế để khắc phục một số hạn chế của ICMPv4.

![image](https://github.com/user-attachments/assets/5713ad92-7184-4a70-b90b-c9a1402d3880)

Một phần quan trọng khác của ICMP đối với chúng ta là trường [Time-To-Live](https://en.wikipedia.org/wiki/Time_to_live) (**TTL**) trong header của gói ICMP, giới hạn "thời gian sống" của gói tin khi nó di chuyển qua mạng. Nó ngăn các gói tin lưu chuyển vô thời hạn trên mạng trong trường hợp xảy ra vòng lặp định tuyến (routing loop). Mỗi khi một gói tin đi qua một router, router sẽ giảm giá trị **TTL đi 1**. Khi giá trị TTL đạt **0**, router sẽ loại bỏ gói tin đó và gửi một thông điệp ICMP **Time Exceeded** trở lại cho bên gửi.

Chúng ta cũng có thể sử dụng **TTL** để xác định số lượng chặng (hop) mà một gói tin đã đi qua và khoảng cách gần đúng đến đích. Ví dụ, nếu một gói tin có **TTL** là 10 và mất 5 chặng để đến được đích, chúng ta có thể suy ra rằng đích đến cách khoảng 5 chặng. Ví dụ, nếu chúng ta thấy một lệnh ping có giá trị **TTL** là **122**, điều đó có thể có nghĩa là chúng ta đang giao tiếp với một hệ thống Windows (mặc định **TTL 128**) nằm cách 6 chặng.

Tuy nhiên, cũng có thể suy đoán được hệ điều hành dựa trên giá trị **TTL** mặc định mà thiết bị sử dụng. Mỗi hệ điều hành thường có một giá trị **TTL** mặc định khi gửi các gói tin. Giá trị này được thiết lập trong header của gói tin và bị giảm đi 1 mỗi khi gói tin đi qua một router. Do đó, việc kiểm tra giá trị **TTL** mặc định của một thiết bị giúp chúng ta có thể suy ra hệ điều hành mà thiết bị đó đang sử dụng. Ví dụ: các hệ thống Windows (**2000/XP/2003/Vista/10**) thường có giá trị **TTL** mặc định là 128, trong khi các hệ thống macOS và Linux thường có giá trị **TTL** mặc định là 64, và giá trị **TTL** mặc định của Solaris là 255. Tuy nhiên, điều quan trọng cần lưu ý là người dùng có thể thay đổi các giá trị này, vì vậy chúng không nên được xem là một cách xác định chắc chắn hệ điều hành của một thiết bị.

### VoIP

[Voice over Internet Protocol](https://www.fcc.gov/general/voice-over-internet-protocol-voip) (**VoIP**) là một phương pháp truyền tải giọng nói và các giao tiếp đa phương tiện. Ví dụ, nó cho phép chúng ta thực hiện các cuộc gọi điện thoại bằng cách sử dụng kết nối internet băng thông rộng thay vì đường dây điện thoại truyền thống, chẳng hạn như Skype, Whatsapp, Google Hangouts, Slack, Zoom, và các dịch vụ khác.

Các cổng VoIP phổ biến nhất là **TCP/5060** và **TCP/5061**, được sử dụng cho [Session Initiation Protocol](https://en.wikipedia.org/wiki/Session_Initiation_Protocol) (SIP). Tuy nhiên, cổng TCP/1720 cũng có thể được một số hệ thống VoIP sử dụng cho [giao thức H.323](https://en.wikipedia.org/wiki/H.323), một tập hợp các tiêu chuẩn cho giao tiếp đa phương tiện qua các mạng dựa trên gói tin (packet-based network). Tuy nhiên, SIP vẫn được sử dụng rộng rãi hơn H.323 trong các hệ thống VoIP.

![image](https://github.com/user-attachments/assets/7718a4c7-5ed4-4b83-a7c9-6b5fa263a9dd)

### Rò Rỉ Thông Tin (Information Disclosure)

Tuy nhiên, SIP cho phép chúng ta liệt kê (enumerate) các người dùng hiện có cho các cuộc tấn công tiềm ẩn. Điều này có thể được thực hiện cho nhiều mục đích khác nhau, chẳng hạn như xác định tình trạng sẵn sàng của người dùng, tìm hiểu thông tin về khả năng hoặc dịch vụ của người dùng, hoặc thực hiện các cuộc tấn công brute-force vào tài khoản người dùng sau này.

Một trong những cách có thể dùng để liệt kê người dùng là yêu cầu SIP **OPTIONS**. Đây là một phương thức được sử dụng để yêu cầu thông tin về khả năng của một máy chủ SIP hoặc các user agent, chẳng hạn như các loại phương tiện mà nó hỗ trợ, các codec mà nó có thể giải mã, và các chi tiết khác. Yêu cầu **OPTIONS** có thể được sử dụng để dò thông tin từ một máy chủ SIP hoặc user agent, hoặc để kiểm tra kết nối và tình trạng sẵn sàng của nó.

Trong quá trình phân tích, chúng ta có thể phát hiện ra một tệp **SEPxxxx.cnf**, trong đó **xxxx** là một mã định danh duy nhất, đây là một tệp cấu hình được Cisco Unified Communications Manager (trước đây gọi là Cisco CallManager) sử dụng để định nghĩa các cài đặt và tham số cho một điện thoại IP hợp nhất của Cisco (Cisco Unified IP Phone). Tệp này chỉ định model điện thoại, phiên bản firmware, cài đặt mạng, và các chi tiết khác.
