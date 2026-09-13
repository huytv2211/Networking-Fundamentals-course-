# Mạng Không Dây (Wireless Networks)

![image](https://github.com/user-attachments/assets/924f27b3-2f67-4f98-add1-574709ae583e)

Mạng không dây là các mạng máy tính sử dụng kết nối dữ liệu không dây giữa các node mạng. Những mạng này cho phép các thiết bị như laptop, điện thoại thông minh, và máy tính bảng giao tiếp với nhau và với Internet mà không cần các kết nối vật lý như dây cáp.

Mạng không dây sử dụng công nghệ tần số vô tuyến (**RF**) để truyền dữ liệu giữa các thiết bị. Mỗi thiết bị trong một mạng không dây có một bộ chuyển đổi không dây (wireless adapter) chuyển đổi dữ liệu thành tín hiệu RF và gửi chúng qua không khí. Các thiết bị khác trong mạng nhận các tín hiệu này bằng bộ chuyển đổi không dây của riêng chúng, và dữ liệu sau đó được chuyển đổi trở lại thành dạng có thể sử dụng được. Các mạng này có thể hoạt động trong nhiều phạm vi khác nhau, tùy thuộc vào công nghệ được sử dụng. Ví dụ, một mạng cục bộ (LAN) bao phủ một khu vực nhỏ, chẳng hạn như một ngôi nhà hoặc văn phòng nhỏ, có thể sử dụng một công nghệ không dây gọi là **WiFi**, có phạm vi vài trăm feet. Mặt khác, một mạng diện rộng không dây (**WWAN**) có thể sử dụng công nghệ viễn thông di động như dữ liệu di động (**3G, 4G LTE, 5G**), có thể bao phủ một khu vực rộng lớn hơn nhiều, chẳng hạn như toàn bộ một thành phố hoặc khu vực.

Do đó, để kết nối với một mạng không dây, một thiết bị phải nằm trong phạm vi của mạng và được cấu hình với các cài đặt mạng chính xác, chẳng hạn như tên mạng và mật khẩu. Sau khi kết nối, các thiết bị có thể giao tiếp với nhau và với Internet, cho phép người dùng truy cập vào các tài nguyên trực tuyến và trao đổi dữ liệu.

Việc giao tiếp giữa các thiết bị diễn ra qua sóng RF trong các băng tần **2.4 GHz** hoặc **5 GHz** trong một mạng WiFi. Khi một thiết bị, chẳng hạn như laptop, muốn gửi dữ liệu qua mạng, trước tiên nó sẽ giao tiếp với [Điểm Truy Cập Không Dây (Wireless Access Point)](https://en.wikipedia.org/wiki/Wireless_access_point) (**WAP**) để yêu cầu quyền truyền dữ liệu. WAP là một thiết bị trung tâm, giống như một router, kết nối mạng không dây với mạng có dây và kiểm soát quyền truy cập vào mạng.
Sau khi WAP cấp quyền, thiết bị gửi sẽ truyền dữ liệu dưới dạng tín hiệu RF, được các bộ chuyển đổi không dây của các thiết bị khác trong mạng nhận. Sau đó, dữ liệu được chuyển đổi trở lại thành dạng có thể sử dụng được và chuyển đến ứng dụng hoặc hệ thống tương ứng.

Cường độ của tín hiệu RF và khoảng cách mà nó có thể truyền đi bị ảnh hưởng bởi các yếu tố như công suất của bộ phát, sự hiện diện của các vật cản, và mật độ nhiễu RF trong môi trường. Vì vậy, để đảm bảo giao tiếp đáng tin cậy, các mạng WiFi sử dụng các kỹ thuật như truyền phổ trải rộng (spread spectrum transmission) và sửa lỗi (error correction) để vượt qua những thách thức này.

## Kết Nối WiFi

Thiết bị cũng phải được cấu hình với các cài đặt mạng chính xác, chẳng hạn như tên mạng / [Service Set Identifier](https://www.geeksforgeeks.org/service-set-identifier-ssid-in-computer-network/) (**SSID**) và **mật khẩu**. Vì vậy, để kết nối với router, laptop sử dụng một giao thức mạng không dây gọi là [IEEE 802.11](https://en.wikipedia.org/wiki/IEEE_802.11). Giao thức này định nghĩa các chi tiết kỹ thuật về cách các thiết bị không dây giao tiếp với nhau và với các WAP. Khi một thiết bị muốn tham gia vào một mạng WiFi, nó sẽ gửi một yêu cầu đến WAP để bắt đầu quá trình kết nối. Yêu cầu này được gọi là **connection request frame** (khung yêu cầu kết nối) hoặc **association request** (yêu cầu liên kết) và được gửi bằng giao thức mạng không dây **IEEE 802.11**. Khung yêu cầu kết nối chứa nhiều trường thông tin khác nhau, bao gồm nhưng không giới hạn ở các thông tin sau:

![image](https://github.com/user-attachments/assets/5f5492c6-790c-4adb-ae54-c5c026103f87)

Sau đó, thiết bị sử dụng thông tin này để cấu hình bộ chuyển đổi không dây của nó và kết nối với WAP. Sau khi kết nối được thiết lập, thiết bị có thể giao tiếp với WAP và các thiết bị mạng khác. Nó cũng có thể truy cập Internet và các tài nguyên trực tuyến khác thông qua WAP, đơn vị đóng vai trò như một cổng (gateway) vào mạng có dây. Tuy nhiên, **SSID** có thể được ẩn đi bằng cách vô hiệu hóa việc phát quảng bá (broadcasting). Điều đó có nghĩa là các thiết bị tìm kiếm WAP cụ thể đó sẽ không thể xác định được **SSID** của nó. Tuy nhiên, **SSID** vẫn có thể được tìm thấy trong gói tin xác thực (authentication packet).

Bên cạnh giao thức **IEEE 802.11**, các giao thức và công nghệ mạng khác cũng có thể được sử dụng, như TCP/IP, DHCP, và WPA2, trong một mạng WiFi để thực hiện các nhiệm vụ như gán địa chỉ IP cho các thiết bị, định tuyến lưu lượng giữa các thiết bị, và cung cấp bảo mật.

## Bắt Tay Thách Thức-Phản Hồi WEP (WEP Challenge-Response Handshake)

Bắt tay thách thức-phản hồi là một quy trình thiết lập kết nối an toàn giữa một WAP và một thiết bị khách trong một mạng không dây sử dụng giao thức bảo mật WEP. Quy trình này liên quan đến việc trao đổi các gói tin giữa WAP và thiết bị khách để xác thực thiết bị và thiết lập một kết nối an toàn.

![image](https://github.com/user-attachments/assets/e1d717f0-43df-4cf9-af22-261c93f5e741)

Tuy nhiên, một số gói tin có thể bị mất, vì vậy cái gọi là checksum **CRC** đã được tích hợp vào. [Cyclic Redundancy Check](https://en.wikipedia.org/wiki/Cyclic_redundancy_check) (**CRC**) là một cơ chế phát hiện lỗi được sử dụng trong giao thức WEP để bảo vệ chống lại việc hỏng dữ liệu trong các giao tiếp không dây. Một giá trị CRC được tính toán cho mỗi gói tin được truyền qua mạng không dây dựa trên dữ liệu của gói tin đó. Nó được sử dụng để xác minh tính toàn vẹn của dữ liệu. Khi thiết bị đích nhận được gói tin, giá trị CRC sẽ được tính toán lại và so sánh với giá trị ban đầu. Nếu các giá trị trùng khớp, dữ liệu đã được truyền thành công mà không có bất kỳ lỗi nào. Tuy nhiên, nếu các giá trị không trùng khớp, dữ liệu đã bị hỏng và cần phải được truyền lại.

Thiết kế của cơ chế **CRC** có một khiếm khuyết cho phép chúng ta giải mã một gói tin duy nhất mà **không cần** biết **khóa mã hóa (encryption key)**. Điều này là vì giá trị **CRC** được tính toán dựa trên dữ liệu **văn bản gốc (plaintext)** trong gói tin thay vì dữ liệu đã được mã hóa. Trong WEP, giá trị **CRC** được đưa vào header của gói tin cùng với dữ liệu đã mã hóa. Khi thiết bị đích nhận được gói tin, giá trị CRC sẽ được tính toán lại và so sánh với giá trị ban đầu để đảm bảo rằng dữ liệu đã được truyền thành công mà không có lỗi nào. Tuy nhiên, chúng ta có thể sử dụng **CRC** để xác định dữ liệu văn bản gốc trong gói tin, ngay cả khi dữ liệu đó đã được mã hóa.

## Các Tính Năng Bảo Mật

Các mạng WiFi có một số tính năng bảo mật để bảo vệ chống lại truy cập trái phép và đảm bảo tính riêng tư cũng như tính toàn vẹn của dữ liệu được truyền qua mạng. Một số tính năng bảo mật hàng đầu bao gồm nhưng không giới hạn ở:

- Mã Hóa (Encryption)
- Kiểm Soát Truy Cập (Access Control)
- Tường Lửa (Firewall)

### Mã Hóa (Encryption)

Chúng ta có thể sử dụng nhiều thuật toán mã hóa khác nhau để bảo vệ tính bảo mật của dữ liệu được truyền qua các mạng không dây. Các thuật toán mã hóa phổ biến nhất trong các mạng WiFi là [Wired Equivalent Privacy](https://en.wikipedia.org/wiki/Wired_Equivalent_Privacy) (**WEP**), [WiFi Protected Access 2](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access#WPA2) (**WPA2**), và [WiFi Protected Access 3](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access#WPA3) (**WPA3**).

### Kiểm Soát Truy Cập (Access Control)

Các mạng WiFi được cấu hình theo mặc định để cho phép các thiết bị được ủy quyền tham gia vào mạng bằng các phương thức xác thực cụ thể. Tuy nhiên, các phương thức này có thể được thay đổi bằng cách yêu cầu một mật khẩu hoặc một mã định danh duy nhất (chẳng hạn như địa chỉ MAC) để xác định các thiết bị được ủy quyền.

### Tường Lửa (Firewall)

Tường lửa là một hệ thống bảo mật kiểm soát lưu lượng mạng đi vào và đi ra dựa trên các quy tắc bảo mật được xác định trước. Ví dụ, các router WiFi thường có tường lửa được tích hợp sẵn, có thể chặn lưu lượng đến từ Internet và bảo vệ chống lại nhiều loại mối đe dọa mạng khác nhau.

## Các Giao Thức Mã Hóa

[Wired Equivalent Privacy](https://en.wikipedia.org/wiki/Wired_Equivalent_Privacy) (**WEP**) và [WiFi Protected Access](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access) (**WPA**) là các giao thức mã hóa bảo mật dữ liệu được truyền qua một mạng WiFi. WPA có thể sử dụng nhiều thuật toán mã hóa khác nhau, bao gồm [Advanced Encryption Standard](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) (**AES**).

### WEP

**WEP** sử dụng một khóa **40-bit** hoặc **104-bit** để mã hóa dữ liệu, trong khi **WPA sử dụng AES** sử dụng một khóa **128-bit**. Các khóa dài hơn cung cấp khả năng mã hóa mạnh mẽ hơn và có khả năng chống lại các cuộc tấn công tốt hơn. Tuy nhiên, WEP dễ bị tổn thương trước nhiều loại tấn công khác nhau, có thể cho phép kẻ tấn công giải mã dữ liệu được truyền qua mạng. Ngoài ra, WEP không tương thích với các thiết bị và hệ điều hành mới hơn và nhìn chung không còn được coi là an toàn nữa. Cuối cùng, **WEP** sử dụng thuật toán mã hóa **RC4 cipher**, khiến nó dễ bị tấn công.

Tuy nhiên, WEP sử dụng một **khóa dùng chung (shared key)** để xác thực, có nghĩa là cùng một khóa được sử dụng cho cả mã hóa và xác thực. Có hai phiên bản của giao thức WEP:

- WEP-40/WEP-64
- WEP-104

**WEP-40**, còn được gọi là **WEP-64**, sử dụng một khóa (bí mật) **40-bit**, trong khi **WEP-104** sử dụng một khóa **104-bit**. Khóa này được chia thành một [Vector Khởi Tạo (Initialization Vector)](https://en.wikipedia.org/wiki/Initialization_vector) (**IV**) và một **khóa bí mật**.

**IV** là một giá trị nhỏ được đưa vào header của gói tin cùng với dữ liệu đã mã hóa, và được sử dụng để tạo ra khóa cho cả **WEP-40** và **WEP-104**, đồng thời được đưa vào để đảm bảo rằng mỗi khóa là duy nhất. Khóa bí mật là một chuỗi bit ngẫu nhiên được sử dụng để mã hóa dữ liệu. Tuy nhiên, **WEP-104** có một **khóa bí mật** dài **80-bit**. Hãy xem bảng sau đây để thấy rõ sự khác biệt:

![image](https://github.com/user-attachments/assets/1adbe58d-0746-4499-90da-0b841c0b6af0)

Tuy nhiên, vì IV trong WEP tương đối nhỏ, chúng ta có thể sử dụng phương pháp brute force để thử mọi tổ hợp ký tự có thể có cho nó, và xác định được giá trị chính xác. Sau đó, chúng ta có thể sử dụng nó để giải mã dữ liệu trong gói tin. Điều này cho phép chúng ta truy cập vào dữ liệu được truyền qua mạng không dây và có khả năng làm tổn hại đến tính bảo mật của mạng.

### WPA

**WPA** cung cấp mức độ bảo mật cao nhất và không dễ bị tổn thương trước các loại tấn công tương tự như WEP. Ngoài ra, WPA sử dụng các phương thức xác thực an toàn hơn, chẳng hạn như [Khóa Chia Sẻ Trước (Pre-Shared Key)](https://en.wikipedia.org/wiki/Pre-shared_key) (**PSK**) hoặc một máy chủ xác thực 802.1X, cung cấp khả năng bảo vệ mạnh mẽ hơn chống lại truy cập trái phép. Mặc dù các thiết bị cũ hơn có thể không hỗ trợ, WPA vẫn tương thích với hầu hết các thiết bị và hệ điều hành. Tất cả các mạng không dây, đặc biệt là trong hạ tầng quan trọng như văn phòng, nói chung nên triển khai ít nhất mã hóa **WPA2** hoặc thậm chí **WPA3**.

## Các Giao Thức Xác Thực

[Lightweight Extensible Authentication Protocol](https://en.wikipedia.org/wiki/Lightweight_Extensible_Authentication_Protocol) (**LEAP**) và [Protected Extensible Authentication Protocol](https://en.wikipedia.org/wiki/Protected_Extensible_Authentication_Protocol) (**PEAP**) là các giao thức xác thực được sử dụng để bảo mật các mạng không dây, cung cấp một phương thức an toàn để xác thực các thiết bị trên một mạng không dây, và thường được sử dụng cùng với WEP hoặc WPA để cung cấp thêm một lớp bảo mật bổ sung.

Cả LEAP và PEAP đều dựa trên [Extensible Authentication Protocol](https://en.wikipedia.org/wiki/Extensible_Authentication_Protocol) (**EAP**), một khung xác thực được sử dụng trong nhiều bối cảnh mạng khác nhau. Tuy nhiên, một điểm khác biệt quan trọng giữa **LEAP** và **PEAP** là cách chúng bảo mật quá trình xác thực.

- **LEAP** sử dụng một **khóa dùng chung (shared key)** để xác thực, có nghĩa là **cùng một khóa** được sử dụng cho cả **mã hóa và xác thực**.

Điều này có thể khiến chúng ta tương đối dễ dàng chiếm được quyền truy cập vào mạng nếu khóa đó bị lộ.

Tuy nhiên, **PEAP** sử dụng một phương thức xác thực an toàn hơn được gọi là [Transport Layer Security](https://en.wikipedia.org/wiki/Transport_Layer_Security) (**TLS**) qua đường hầm (tunneled). Phương thức này thiết lập một kết nối an toàn giữa thiết bị và WAP bằng cách sử dụng một **chứng chỉ số (digital certificate)**, và một đường hầm được mã hóa bảo vệ quá trình xác thực. Điều này cung cấp khả năng bảo vệ mạnh mẽ hơn chống lại truy cập trái phép và có khả năng chống chịu tốt hơn trước các cuộc tấn công.

#### _Giải thích đơn giản (Các Giao Thức Xác Thực)_

LEAP và PEAP là hai phương pháp bảo mật các mạng không dây, giúp các thiết bị kết nối với WiFi một cách an toàn.

🔹 LEAP sử dụng một khóa dùng chung để xác thực, có nghĩa là cùng một khóa được sử dụng cho cả mã hóa và xác thực. Phương pháp này có mức độ bảo mật thấp hơn vì nếu khóa đó bị lộ, hacker có thể dễ dàng truy cập vào mạng.

🔹 PEAP sử dụng một phương pháp gọi là TLS, tạo ra một đường hầm được mã hóa giữa thiết bị và modem (WAP). Phương pháp này cung cấp mức độ bảo mật cao hơn vì nó sử dụng chứng chỉ số và mang lại khả năng bảo vệ tốt hơn trước các nỗ lực xâm nhập.

Nói một cách đơn giản, LEAP giống như một ổ khóa đơn giản với một chiếc chìa khóa dùng chung, vì vậy nếu ai đó tìm thấy chiếc chìa khóa đó, họ có thể dễ dàng đột nhập vào. Nhưng PEAP giống như một cánh cửa bảo mật cao với mã hóa mạnh mẽ, khiến việc đột nhập trở nên khó khăn hơn nhiều. 🚀🔐

## TACACS+

Trong một mạng không dây, khi một điểm truy cập không dây (WAP) gửi một yêu cầu xác thực đến một máy chủ [Terminal Access Controller Access-Control System Plus](https://www.ciscopress.com/articles/article.asp?p=422947&seqNum=4) (**TACACS+**), rất có thể **toàn bộ gói tin yêu cầu** sẽ được mã hóa để bảo vệ tính bảo mật và tính toàn vẹn của yêu cầu đó.

**TACACS+** là một giao thức được sử dụng để xác thực và ủy quyền cho người dùng truy cập vào các thiết bị mạng, chẳng hạn như router và switch. Khi một WAP gửi một yêu cầu xác thực đến một máy chủ **TACACS+**, yêu cầu đó thường bao gồm thông tin đăng nhập của người dùng và các thông tin khác về phiên làm việc (session).

Việc mã hóa yêu cầu xác thực giúp đảm bảo rằng thông tin nhạy cảm này không hiển thị đối với các bên trái phép có thể chặn được yêu cầu đó. Đồng thời, nó cũng giúp bảo vệ trong khi yêu cầu đang được truyền qua mạng. Nó cũng giúp ngăn chặn việc can thiệp vào yêu cầu hoặc thay thế nó bằng một yêu cầu độc hại của riêng kẻ tấn công.

Nhiều phương pháp mã hóa có thể được sử dụng để mã hóa yêu cầu xác thực, chẳng hạn như **SSL**/**TLS** hoặc **IPSec**. Phương pháp mã hóa cụ thể được sử dụng có thể phụ thuộc vào cấu hình của máy chủ **TACACS+** và khả năng của WAP.

#### _Giải thích đơn giản (TACACS+)_

TACACS+ là một giao thức bảo mật được sử dụng để xác thực và kiểm soát truy cập vào các thiết bị mạng như router và switch.

Trong một mạng không dây, khi một Điểm Truy Cập Không Dây (WAP) gửi một yêu cầu xác thực đến một máy chủ TACACS+, toàn bộ yêu cầu thường được mã hóa. Điều này đảm bảo rằng thông tin nhạy cảm, chẳng hạn như tên người dùng và mật khẩu, được bảo vệ và không thể bị đánh cắp hoặc thay đổi.

Việc mã hóa này được thực hiện bằng các phương pháp như SSL/TLS hoặc IPSec, tăng cường tính bảo mật cho việc giao tiếp giữa WAP và máy chủ TACACS+. Phương pháp mã hóa cụ thể được sử dụng phụ thuộc vào cấu hình máy chủ và khả năng của WAP.

Nói một cách đơn giản, TACACS+ giống như một két sắt an toàn, mã hóa và bảo vệ thông tin đăng nhập của người dùng, ngăn không cho hacker truy cập vào nó trong quá trình truyền tải. 🔐🚀

## Tấn Công Ngắt Kết Nối (Disassociation Attack)

![image](https://github.com/user-attachments/assets/478ad53f-4709-4568-8849-443a9c765439)

[Tấn Công Ngắt Kết Nối (Disassociation Attack)](https://www.makeuseof.com/what-are-disassociation-attacks/) là một loại tấn công mạng không dây nhắm vào việc làm gián đoạn giao tiếp giữa một WAP và các thiết bị khách của nó bằng cách gửi các khung ngắt kết nối (disassociation frame) đến một hoặc nhiều thiết bị khách.

WAP sử dụng các khung ngắt kết nối để ngắt kết nối một thiết bị khách khỏi mạng. Khi một WAP gửi một khung ngắt kết nối đến một thiết bị khách, thiết bị đó sẽ bị ngắt kết nối khỏi mạng và phải kết nối lại để tiếp tục sử dụng mạng.

Chúng ta có thể thực hiện cuộc tấn công này từ **bên trong** hoặc **bên ngoài** mạng tùy thuộc vào vị trí của chúng ta và các biện pháp bảo mật của mạng. Mục đích của cuộc tấn công này là làm gián đoạn giao tiếp giữa WAP và các thiết bị khách của nó, khiến các thiết bị khách bị ngắt kết nối và có thể gây bất tiện hoặc gián đoạn cho người dùng. Chúng ta cũng có thể sử dụng nó như một bước chuẩn bị cho các cuộc tấn công khác, chẳng hạn như tấn công MITM, bằng cách buộc các thiết bị khách phải kết nối lại với mạng và có khả năng khiến chúng bị lộ trước các cuộc tấn công tiếp theo.

#### _Giải thích đơn giản (Tấn Công Ngắt Kết Nối)_

**Tấn Công Ngắt Kết Nối (Disassociation Attack)** là một loại tấn công vào các mạng không dây nhằm mục đích **ngắt kết nối các thiết bị khỏi Wi-Fi**.

Trong cuộc tấn công này, hacker gửi các khung ngắt kết nối đến các thiết bị đã kết nối. Các khung này buộc các thiết bị phải ngắt kết nối khỏi mạng, yêu cầu chúng phải kết nối lại để tiếp tục sử dụng Wi-Fi.

🔹 Tại sao cuộc tấn công này lại được sử dụng?

Để làm gián đoạn và gây bất tiện cho người dùng bằng cách ngắt kết nối họ khỏi mạng
Như một bước chuẩn bị cho các cuộc tấn công khác, chẳng hạn như tấn công Man-in-the-Middle (MITM), trong đó hacker lừa người dùng kết nối vào một mạng giả để đánh cắp dữ liệu của họ
🔹 Cuộc tấn công này có thể đến từ đâu?

Nó có thể được thực hiện từ bên trong mạng (ví dụ: từ một thiết bị đã kết nối) hoặc từ bên ngoài mạng (ví dụ: bởi một kẻ tấn công ở gần đó).
Nói một cách đơn giản, một Tấn Công Ngắt Kết Nối giống như việc ai đó liên tục rút phích cắm và cắm lại dây internet của bạn, khiến bạn không thể duy trì kết nối! 😡🔌

## Tăng Cường Bảo Mật Mạng Không Dây (Wireless Hardening)

Có rất nhiều cách khác nhau để bảo vệ các mạng không dây. Tuy nhiên, một số ví dụ sau đây nên được xem xét để tăng cường đáng kể tính bảo mật của các mạng không dây. Đây là những cách sau, nhưng không giới hạn ở:

- Vô hiệu hóa việc phát quảng bá (Disabling broadcasting)
- WiFi Protected Access
- Lọc theo địa chỉ MAC (MAC filtering)
- Triển khai EAP-TLS

### Vô Hiệu Hóa Việc Phát Quảng Bá (Disabling Broadcasting)

Việc vô hiệu hóa phát quảng bá SSID là một biện pháp bảo mật có thể giúp tăng cường bảo mật cho một WAP bằng cách khiến việc phát hiện và kết nối với mạng trở nên khó khăn hơn. Khi SSID được phát quảng bá, nó được đưa vào các khung hiệu lệnh (beacon frame) được WAP truyền đi thường xuyên để thông báo về sự sẵn có của mạng. Bằng cách vô hiệu hóa việc phát quảng bá SSID, WAP sẽ không truyền các khung hiệu lệnh, và mạng sẽ không hiển thị đối với các thiết bị chưa từng kết nối với mạng đó trước đây.

#### _Giải thích đơn giản (Vô Hiệu Hóa Việc Phát Quảng Bá)_

Việc vô hiệu hóa phát quảng bá SSID là một biện pháp bảo mật giúp ẩn một mạng Wi-Fi, khiến việc hacker phát hiện và kết nối với nó trở nên khó khăn hơn.

Thông thường, một WAP sẽ phát quảng bá SSID trong các khung hiệu lệnh thường xuyên để các thiết bị có thể phát hiện và kết nối với mạng. Tuy nhiên, nếu việc phát quảng bá SSID bị vô hiệu hóa:

Mạng sẽ không xuất hiện trong danh sách các mạng Wi-Fi khả dụng.
Chỉ những thiết bị đã từng kết nối với mạng trước đây mới có thể kết nối lại được.
🔹 Tại sao điều này lại hữu ích?

Nó khiến việc tìm ra mạng trở nên khó khăn hơn đối với hacker và những người dùng trái phép.
Nó tăng cường tính bảo mật, nhưng bản thân nó là không đủ—nó nên được kết hợp với mã hóa mạnh (chẳng hạn như WPA2/WPA3).
Nói một cách đơn giản, việc vô hiệu hóa phát quảng bá SSID giống như việc gỡ bỏ biển tên của một ngôi nhà để người lạ khó tìm thấy nó hơn! 🏠🔒

### WPA

Một lần nữa, WPA cung cấp khả năng mã hóa và xác thực mạnh mẽ cho các giao tiếp không dây, giúp bảo vệ chống lại truy cập trái phép vào mạng và việc chặn dữ liệu nhạy cảm. WPA bao gồm hai phiên bản chính:

1. WPA-Personal
2. WPA-Enterprise

WPA-Personal, được thiết kế cho các mạng gia đình và doanh nghiệp nhỏ, và WPA-Enterprise, được thiết kế cho các tổ chức lớn hơn và sử dụng một máy chủ xác thực tập trung (ví dụ: RADIUS hoặc TACACS+) để xác minh danh tính của các thiết bị khách.

### Lọc Theo Địa Chỉ MAC (MAC Filtering)

Lọc theo địa chỉ MAC là một biện pháp bảo mật cho phép một WAP chấp nhận hoặc từ chối các kết nối từ các thiết bị cụ thể dựa trên địa chỉ MAC của chúng. Bằng cách cấu hình WAP chỉ chấp nhận kết nối từ các thiết bị có địa chỉ MAC đã được phê duyệt, chúng ta có thể ngăn chặn các thiết bị trái phép kết nối vào mạng.

### Triển Khai EAP-TLS

EAP-TLS là một giao thức bảo mật được sử dụng để xác thực và mã hóa các giao tiếp không dây. Nó sử dụng chứng chỉ số và PKI để xác minh danh tính của các thiết bị khách và thiết lập các kết nối an toàn. Việc triển khai EAP-TLS có thể giúp tăng cường bảo mật cho một WAP bằng cách cung cấp khả năng xác thực và mã hóa mạnh mẽ cho các giao tiếp không dây, giúp bảo vệ chống lại truy cập trái phép vào mạng và việc chặn dữ liệu nhạy cảm.

#### _Giải thích đơn giản (Triển Khai EAP-TLS)_

EAP-TLS là một giao thức bảo mật được sử dụng để xác thực và mã hóa các giao tiếp không dây. Nó sử dụng chứng chỉ số và Hạ Tầng Khóa Công Khai (Public Key Infrastructure - PKI) để xác minh danh tính người dùng và thiết lập các kết nối an toàn.

🔹 Tại sao EAP-TLS lại quan trọng?

Cung cấp khả năng xác thực mạnh mẽ, ngăn chặn truy cập trái phép.
Mã hóa các giao tiếp để bảo vệ dữ liệu nhạy cảm khỏi bị chặn.
Tăng cường tính bảo mật của các Điểm Truy Cập Không Dây (WAP) và bảo vệ chống lại các mối đe dọa mạng.
Nói một cách đơn giản, EAP-TLS hoạt động giống như một thẻ căn cước kỹ thuật số an toàn, chỉ cho phép những người dùng đáng tin cậy kết nối trong khi mã hóa các giao tiếp để ngăn chặn hacker. 🔐📡
