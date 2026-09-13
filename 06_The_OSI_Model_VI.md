# Mô Hình OSI

Mục tiêu khi định nghĩa tiêu chuẩn **ISO/OSI** là tạo ra một mô hình tham chiếu cho phép các hệ thống kỹ thuật khác nhau giao tiếp với nhau thông qua nhiều thiết bị và công nghệ khác nhau, đồng thời đảm bảo khả năng tương thích. Mô hình **OSI** sử dụng **bảy** tầng khác nhau, được sắp xếp theo thứ bậc dựa trên nhau để đạt được mục tiêu này. Các tầng này đại diện cho các giai đoạn trong quá trình thiết lập mỗi kết nối mà các gói tin được gửi phải đi qua. Bằng cách này, tiêu chuẩn được tạo ra nhằm mô tả trực quan cách một kết nối được cấu trúc và thiết lập.

![image](https://github.com/user-attachments/assets/7d69710d-9f4e-428e-b962-769636c02578)

Các tầng **2-4** là các tầng **hướng vận chuyển (transport oriented)**, và các tầng **5-7** là các tầng **hướng ứng dụng (application oriented)**. Ở mỗi tầng, các nhiệm vụ được xác định chính xác, và các giao diện với các tầng lân cận cũng được mô tả một cách chính xác. Mỗi tầng cung cấp các dịch vụ để tầng ngay phía trên sử dụng. Để cung cấp các dịch vụ này, một tầng sẽ sử dụng các dịch vụ của tầng bên dưới nó và thực hiện các nhiệm vụ riêng của tầng mình.

Nếu hai hệ thống giao tiếp với nhau, tất cả bảy tầng của mô hình **OSI** sẽ được thực hiện ít nhất **hai lần**, vì cả bên gửi và bên nhận đều phải tuân theo mô hình phân tầng này. Do đó, một số lượng lớn các nhiệm vụ khác nhau phải được thực hiện ở từng tầng riêng lẻ để đảm bảo tính bảo mật, độ tin cậy, và hiệu suất của việc giao tiếp.

Khi một ứng dụng gửi một gói tin đến hệ thống khác, hệ thống đó sẽ xử lý qua các tầng được thể hiện ở trên, từ tầng **7** xuống đến tầng **1**, và hệ thống nhận sẽ giải nén gói tin nhận được từ tầng **1** lên đến tầng **7**.

![image](https://github.com/user-attachments/assets/c309b73e-ef42-403a-822b-240e381fd93a)

## Mô Tả Đơn Giản Hóa

**Mô hình OSI** giống như một hướng dẫn từng bước để các máy tính giao tiếp với nhau. Nó có **7 tầng**, và mỗi tầng có một nhiệm vụ cụ thể. Các tầng này được chia thành hai nhóm:

- **Tầng 2-4 (hướng vận chuyển):** Xử lý việc di chuyển dữ liệu giữa các thiết bị.
- **Tầng 5-7 (hướng ứng dụng):** Tập trung vào cách các ứng dụng tương tác với dữ liệu.

Cách hoạt động như sau:

1. **Mỗi tầng thực hiện nhiệm vụ riêng của mình** và làm việc với các tầng phía trên và phía dưới nó.
2. Tầng đó **sử dụng các dịch vụ từ tầng bên dưới** và cung cấp dịch vụ cho tầng bên trên. Hãy hình dung nó giống như một đội đang chuyền bóng từ người chơi này sang người chơi khác.

Khi hai hệ thống giao tiếp với nhau:

1. **Hệ thống bên gửi** bắt đầu từ **Tầng 7 (tầng ứng dụng)** và đi dần **xuống Tầng 1**, thêm các thông tin cần thiết ở mỗi bước.
2. **Hệ thống bên nhận** bắt đầu từ **Tầng 1** và đi dần **lên Tầng 7**, giải nén các thông tin đã được thêm vào ở mỗi tầng.

Quá trình này diễn ra hai lần: một lần cho việc gửi và một lần cho việc nhận. Các tầng này đảm bảo việc giao tiếp diễn ra an toàn, đáng tin cậy, và hiệu quả.
