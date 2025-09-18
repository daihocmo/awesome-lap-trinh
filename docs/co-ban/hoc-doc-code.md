# Hướng dẫn đọc code

Nạn sẽ phải **đọc code nhiều hơn viết code**. Có thể trong lớp học hay tutorial, bạn quen với việc chỉ viết vài chục dòng code rồi chạy được ngay. Nhưng trong thế giới thực, đặc biệt là khi bước vào dự án thật (trên GitHub hay trong công việc), codebase có thể lên tới **hàng ngàn file, hàng trăm ngàn dòng**.

Câu hỏi thường gặp: *“Làm sao để mình đọc nổi chỗ đó?”*

Câu trả lời ngắn gọn: **từng bước một, và có chiến lược**. Dưới đây là những kinh nghiệm và cách tiếp cận thực tế mà mình rút ra (cộng với nhiều chia sẻ từ lập trình viên khác), hi vọng giúp bạn đỡ hoang mang khi mở một repo lạ.


## 1. Đừng lao vào code ngay lập tức

Giống như đọc một cuốn sách, bạn không thể nhảy thẳng vào chương 10 mà bỏ qua lời mở đầu. Trước khi “đào bới” từng dòng, hãy:

* Đọc **README**: đây là bản đồ chỉ đường, thường có giới thiệu, hướng dẫn cài đặt, và cách chạy thử.
* Xem **cấu trúc thư mục**: thư mục `src/`, `tests/`, `docs/`... sẽ gợi ý cho bạn dự án được chia thành những phần nào.
* Chạy thử dự án nếu có thể: thấy chương trình chạy được sẽ giúp bạn có **khung tham chiếu** khi bắt đầu đọc code.

## 2. Xác định “điểm vào”

Một dự án thường có một “cửa ngõ” – file `main`, `index.js`, hay một hàm khởi chạy server. Hãy bắt đầu từ đây, rồi lần theo dòng chảy của chương trình.
Khi gặp một hàm hoặc class được gọi nhiều lần, bạn có thể “đánh dấu” nó là trung tâm để tìm hiểu sâu hơn.

Mẹo: đừng cố hiểu tất cả ngay lần đầu. Chỉ cần nắm được “dòng chảy chính” trước đã.

## 3. Học cách **đọc lướt**

Không phải dòng nào bạn cũng cần hiểu chi tiết. Khi gặp một đoạn code chưa quen (ví dụ: một hàm xử lý toán học phức tạp, hoặc một thư viện ngoài), hãy tạm coi nó như một **hộp đen** (blackbox): biết nó nhận gì vào, trả gì ra là đủ. Sau này, nếu thật sự cần, bạn mới mở hộp ra.

Cách này giúp bạn tránh **ngộp thông tin** – kẻ thù lớn nhất của người mới khi đọc code.

## 4. Dùng debugger hoặc in ra log

Một trong những cách hiểu code nhanh nhất là **chạy từng bước**.

* Với debugger, bạn có thể step into (đi sâu vào chi tiết) hoặc step over (bỏ qua phần chưa cần).
* Nếu debugger phức tạp, cứ `print` (hoặc `console.log`) ra biến để xem giá trị thay đổi thế nào.

Việc thấy tận mắt code chạy giúp bạn hiểu nhanh hơn gấp nhiều lần.


## 5. Tìm pattern, không học vẹt

Bạn không cần nhớ từng dòng, nhưng nên chú ý đến **mẫu lặp lại**: cách viết vòng lặp, cách xử lý request, cách chia module. Đọc nhiều code sẽ giúp bạn dần “nhìn ra” pattern – đó chính là chìa khóa để học lập trình nhanh.

Hãy thử:

* Viết lại đoạn code bạn vừa hiểu, với cách viết của riêng mình.
* Thay đổi vài chỗ, chạy lại, xem có khác biệt gì.

Kinh nghiệm cho thấy, “nghịch phá” code người khác là cách học nhanh nhất.


## 6. Chọn dự án phù hợp

Đừng nhảy ngay vào những con quái vật như **Linux kernel** hay framework to như **React**. Bạn sẽ sớm nản.

Thay vào đó:

* Bắt đầu với những dự án nhỏ: một thư viện xử lý ngày tháng, một game mini, một clone app đơn giản.
* Ưu tiên repo có ít contributor và commit history gọn.
* Nếu có test đi kèm, đọc test trước: nó mô tả chương trình được mong đợi chạy như thế nào.

GitHub có tính năng tìm kiếm repo theo topic, rất tiện để lọc ra dự án nhỏ phù hợp.


## 7. Đừng ngại không hiểu

Bạn sẽ luôn gặp code mà mình không hiểu nổi, nhất là khi đụng phải kiến thức chưa học. Điều này hoàn toàn bình thường.
Quan trọng là:

* Biết chọn cái cần học trước, cái nào để sau.
* Có thể tra Google, hỏi bạn bè, hoặc đọc docs để lấp lỗ hổng.
* Biết dừng lại khi thấy quá tải – ép mình quá chỉ làm mất động lực.


## 8. Luyện tập như đọc sách

Đọc code cũng giống đọc sách: càng đọc nhiều, bạn càng nhanh nhạy hơn.

Gợi ý nhỏ:

* Mỗi tuần chọn một repo nhỏ để đọc.
* Ghi chú lại những đoạn hay hoặc kỹ thuật mới.
* Sau vài tháng, bạn sẽ bất ngờ với vốn “pattern” mình tích lũy được.