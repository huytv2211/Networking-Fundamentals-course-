# Các Cấu Trúc Liên Kết Mạng (Networking Topologies)
![image](https://github.com/user-attachments/assets/b7d81315-bee8-453b-869c-2d5a377113c6)


## Cấu Trúc Liên Kết Mạng Là Gì?

Cấu trúc liên kết mạng (network topology) là cách sắp xếp điển hình và kết nối vật lý hoặc logic của các thiết bị trong một mạng. Máy tính là các host, chẳng hạn như máy khách (client) và máy chủ (server), chủ động sử dụng mạng. Chúng cũng bao gồm các thành phần mạng như switch, bridge, và router, mà chúng ta sẽ thảo luận chi tiết hơn ở các phần sau, có chức năng phân phối và đảm bảo tất cả các host trong mạng có thể thiết lập kết nối logic với nhau. Cấu trúc liên kết mạng xác định các thành phần sẽ được sử dụng và phương thức truy cập vào phương tiện truyền dẫn.

---
Cấu trúc liên kết vật lý (physical topology) và cấu trúc liên kết logic (logical topology) là hai khái niệm quan trọng trong mạng máy tính, đề cập đến cách các thiết bị được kết nối và cách dữ liệu được truyền tải trong một mạng:

### Cấu Trúc Liên Kết Vật Lý
Cấu trúc liên kết vật lý đề cập đến cách sắp xếp và kết nối vật lý của các thiết bị trong một mạng, bao gồm:
- Sơ đồ đi dây: Các tuyến đường mà dây cáp đi qua để kết nối các thiết bị với nhau.
- Vị trí các node: Vị trí chính xác của các thiết bị (như máy tính, máy chủ, router) trong mạng.
- Các kết nối: Cách các thiết bị được kết nối với dây cáp và thiết bị mạng.
Nói một cách đơn giản, cấu trúc liên kết vật lý là bản đồ hữu hình của các kết nối thực tế giữa các thiết bị. Ví dụ về cấu trúc liên kết vật lý bao gồm:
- Cấu trúc hình sao (Star topology): Các thiết bị được kết nối với một switch hoặc hub trung tâm.
- Cấu trúc hình vòng (Ring topology): Mỗi thiết bị được kết nối với thiết bị tiếp theo, tạo thành một vòng.
- Cấu trúc hình tuyến tính (Bus topology): Tất cả các thiết bị được kết nối thông qua một dây cáp dùng chung.

### Cấu Trúc Liên Kết Logic
Cấu trúc liên kết logic đề cập đến cách dữ liệu được truyền giữa các thiết bị trong một mạng, có thể khác với cấu trúc liên kết vật lý. Nó bao gồm:
- Cách tín hiệu di chuyển trên phương tiện truyền dẫn: Ví dụ, các đường đi mà dữ liệu thực hiện để được gửi và nhận.
- Cơ chế truyền dữ liệu: Cách thức và trình tự dữ liệu được gửi từ thiết bị này sang thiết bị khác.

### **Ví dụ:**
- Trong mạng Ethernet, cấu trúc liên kết vật lý có thể là hình sao, nhưng cấu trúc liên kết logic có thể hoạt động giống như hình tuyến tính vì dữ liệu được phát quảng bá (broadcast) theo cách logic đến tất cả các thiết bị.
- Trong một mạng không dây, có thể không tồn tại cấu trúc liên kết vật lý, nhưng cấu trúc liên kết logic xác định cách các thiết bị giao tiếp và trao đổi dữ liệu với nhau.

### Khác Biệt Chính
- Cấu trúc liên kết vật lý: Cấu trúc thực tế và cách sắp xếp phần cứng của mạng.
- Cấu trúc liên kết logic: Hoạt động chức năng và việc truyền dữ liệu trong mạng.

---
Chúng ta có thể chia toàn bộ lĩnh vực cấu trúc liên kết mạng thành ba khu vực:
1. Kết nối (Connections):
![image](https://github.com/user-attachments/assets/bd047e21-d28f-4208-9bf9-4946e330d9f1)
2. Node - Bộ Điều Khiển Giao Diện Mạng (Network Interface Controller - NIC):
![image](https://github.com/user-attachments/assets/5e79aabf-d44d-471c-be8a-aa89a190697f)
Các node mạng là các điểm kết nối của phương tiện truyền dẫn với bộ phát và bộ thu tín hiệu điện, quang, hoặc vô tuyến trong phương tiện đó. Một node có thể được kết nối với một máy tính, nhưng một số loại có thể chỉ có một bộ vi điều khiển trên một node hoặc thậm chí không có bất kỳ thiết bị lập trình được nào.
3. Phân Loại (Classifications)

Chúng ta có thể hình dung một cấu trúc liên kết như một hình dạng hoặc cấu trúc ảo của một mạng. Hình dạng này không nhất thiết phải tương ứng với cách sắp xếp vật lý thực tế của các thiết bị trong mạng. Do đó, các cấu trúc liên kết này có thể là vật lý hoặc logic. Ví dụ, các máy tính trong một mạng LAN có thể được sắp xếp thành một vòng tròn trong một căn phòng ngủ, nhưng rất khó có khả năng đó thực sự là một cấu trúc liên kết hình vòng thực sự.

---
Cấu trúc liên kết mạng được chia thành tám loại cơ bản sau:

![image](https://github.com/user-attachments/assets/b7dea406-694a-4539-8fd2-88020138a10c)

Các mạng phức tạp hơn có thể được xây dựng dưới dạng lai (hybrid) của hai hoặc nhiều cấu trúc liên kết cơ bản nêu trên.

---
## Điểm-Nối-Điểm (Point-to-Point)
Cấu trúc liên kết mạng đơn giản nhất với một kết nối chuyên dụng giữa hai host là cấu trúc liên kết điểm-nối-điểm. Trong cấu trúc liên kết này, chỉ tồn tại một liên kết vật lý trực tiếp và đơn giản giữa hai host. Hai thiết bị này có thể sử dụng kết nối này để giao tiếp qua lại với nhau.

Cấu trúc liên kết điểm-nối-điểm là mô hình cơ bản của điện thoại truyền thống và không được nhầm lẫn với P2P (kiến trúc ngang hàng - Peer-to-Peer).

![image](https://github.com/user-attachments/assets/d1ac750c-cf54-4bb1-9b1c-109aac3a7216)

## Hình Tuyến Tính (Bus)
Trong cấu trúc liên kết bus, tất cả các host được kết nối thông qua một phương tiện truyền dẫn. Mỗi host đều có quyền truy cập vào phương tiện truyền dẫn và các tín hiệu được truyền qua đó. Không có thành phần mạng trung tâm nào kiểm soát các quá trình diễn ra trên đó. Phương tiện truyền dẫn cho loại này có thể là, ví dụ, một dây cáp đồng trục.

Vì phương tiện truyền dẫn được chia sẻ với tất cả các thiết bị khác, chỉ có một host có thể gửi dữ liệu tại một thời điểm, và tất cả các host khác chỉ có thể nhận và đánh giá dữ liệu để xem liệu nó có dành cho mình hay không.

![image](https://github.com/user-attachments/assets/ce0efd49-3620-4aea-bdb5-64c19aa7bc2a)

## Hình Sao (Star)
Cấu trúc liên kết hình sao có một thành phần mạng duy trì kết nối với tất cả các host. Mỗi host được kết nối với thành phần mạng trung tâm thông qua một liên kết riêng biệt. Đây thường là một router, hub, hoặc switch. Các thiết bị này đảm nhận chức năng chuyển tiếp các gói dữ liệu. Để làm điều này, các gói dữ liệu được nhận và chuyển tiếp đến đích. Lưu lượng dữ liệu trên thành phần mạng trung tâm có thể rất cao vì tất cả dữ liệu và kết nối đều đi qua nó.

![image](https://github.com/user-attachments/assets/fcc75627-21e7-4420-8a4c-d15bc137440e)

## Hình Vòng (Ring)

Cấu trúc liên kết vòng vật lý được thiết kế sao cho mỗi host hoặc node được kết nối vào vòng bằng hai dây cáp:

- Một dây cho tín hiệu đến, và
- Một dây cho tín hiệu đi.

Điều này có nghĩa là một dây cáp đi vào mỗi host và một dây cáp đi ra. Cấu trúc liên kết vòng thường không yêu cầu một thành phần mạng chủ động (active). Việc kiểm soát và truy cập vào phương tiện truyền dẫn được quy định bởi một giao thức mà tất cả các trạm phải tuân theo.

Một cấu trúc liên kết vòng logic được xây dựng dựa trên cấu trúc liên kết hình sao vật lý, trong đó một bộ phân phối tại node mô phỏng vòng bằng cách chuyển tiếp từ cổng này sang cổng tiếp theo.

Thông tin được truyền theo một hướng truyền được xác định trước. Thông thường, phương tiện truyền dẫn được truy cập tuần tự từ trạm này sang trạm khác bằng cách sử dụng hệ thống truy xuất từ trạm trung tâm hoặc thông qua token. Token là một mẫu bit liên tục di chuyển qua mạng hình vòng theo một hướng, hoạt động theo quy trình "claim token" (giành quyền token).

![image](https://github.com/user-attachments/assets/9ec76d15-4057-4d76-b55c-8fd6dc35606f)

## Hình Lưới (Mesh)

Trong các mạng dạng lưới (meshed networks), nhiều node quyết định về các kết nối ở cấp độ vật lý và định tuyến (routing) ở cấp độ logic. Do đó, các cấu trúc dạng lưới không có một cấu trúc liên kết cố định. Có hai cấu trúc cơ bản xuất phát từ khái niệm nền tảng này: cấu trúc lưới đầy đủ (fully meshed) và cấu trúc lưới một phần (partially meshed).

Trong cấu trúc lưới đầy đủ, mỗi host được kết nối với mọi host khác trong mạng. Điều này có nghĩa là các host được liên kết chặt chẽ với nhau. Kỹ thuật này chủ yếu được sử dụng trong WAN hoặc MAN để đảm bảo độ tin cậy cao và băng thông lớn.

Trong thiết lập này, các node mạng quan trọng như router có thể được kết nối với nhau. Nếu một router gặp sự cố, các router khác có thể tiếp tục hoạt động bình thường, và mạng có thể chịu được sự cố nhờ vào rất nhiều kết nối sẵn có.

Trong cấu trúc lưới một phần, các điểm cuối chỉ được kết nối bằng một kết nối duy nhất. Trong loại cấu trúc liên kết mạng này, một số node cụ thể được kết nối với chính xác một node khác, trong khi một số node khác được kết nối với hai hoặc nhiều node khác thông qua kết nối điểm-nối-điểm.

![image](https://github.com/user-attachments/assets/ea2cd3c6-0cf8-41f0-8d82-3115a4d234e5)

## Hình Cây (Tree)

Cấu trúc liên kết hình cây là một cấu trúc liên kết hình sao mở rộng mà các mạng cục bộ quy mô lớn hơn thường có. Điều này đặc biệt hữu ích khi kết hợp nhiều cấu trúc liên kết với nhau. Cấu trúc liên kết này thường được sử dụng, chẳng hạn, trong các tòa nhà công ty lớn.

Có cả cấu trúc cây logic theo mô hình spanning tree và cấu trúc cây vật lý. Các mạng hiện đại theo mô-đun, dựa trên hệ thống cáp có cấu trúc với phân cấp hub, cũng có cấu trúc hình cây. Cấu trúc liên kết hình cây cũng được sử dụng cho các mạng băng thông rộng và mạng đô thị (MAN).

![image](https://github.com/user-attachments/assets/dbcec4ed-973b-402e-9b62-b19912e10bd1)

## Lai (Hybrid)

Mạng lai kết hợp hai hoặc nhiều cấu trúc liên kết sao cho mạng kết quả không thể hiện bất kỳ cấu trúc liên kết tiêu chuẩn nào. Ví dụ, một mạng hình cây có thể là một cấu trúc liên kết lai, trong đó các mạng hình sao được kết nối thông qua các mạng hình tuyến tính liên kết với nhau. Tuy nhiên, một mạng hình cây được liên kết với một mạng hình cây khác vẫn được xem là một mạng hình cây về mặt cấu trúc liên kết. Một cấu trúc liên kết lai luôn được tạo ra khi hai cấu trúc liên kết mạng cơ bản khác nhau được kết nối với nhau.

![image](https://github.com/user-attachments/assets/97e5132a-40eb-4375-847d-7e466599d64f)

## Chuỗi Nối Tiếp (Daisy Chain)

Trong cấu trúc liên kết daisy chain, nhiều host được kết nối bằng cách đặt một dây cáp từ node này sang node khác.

Vì điều này tạo ra một chuỗi các kết nối, nó còn được gọi là cấu hình daisy-chain, trong đó nhiều thành phần phần cứng được kết nối theo kiểu nối tiếp. Loại kết nối mạng này thường thấy trong công nghệ tự động hóa (CAN).

Daisy chaining dựa trên cách sắp xếp vật lý của các node, trái ngược với các quy trình sử dụng token, vốn mang tính cấu trúc nhưng có thể được thiết kế độc lập với cách bố trí vật lý. Tín hiệu được gửi đến và đi từ một thành phần thông qua các node trước đó của nó đến hệ thống máy tính.

![image](https://github.com/user-attachments/assets/62c0d058-fdc1-4486-b1f6-b2b984afd4a3)
