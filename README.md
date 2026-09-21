# KTE311 - Lịch trả nợ dự án

Trang luyện tập tương tác cho học phần **KTE311 Kinh tế đầu tư**, Trường Đại học Ngoại thương.

**Mở trang: https://dongkien.github.io/kte311/**

## Bài toán

Một dự án có 1 năm đầu tư và 8 năm vận hành. Chủ đầu tư chỉ bỏ được một phần vốn chủ sở hữu,
phần còn lại đi vay, và vì năm đầu chưa có doanh thu nên còn phải vay thêm để trả lãi và chuẩn bị
vốn lưu động. Dư nợ cuối năm 1 vì thế là một con số cố định.

Việc của người học là chia đúng số dư nợ đó thành các khoản trả gốc cho những năm còn lại, sao cho
không năm nào trả gốc âm, không năm nào tổng dòng tiền âm, mà NPV cùng IRR của dự án cao nhất có thể.

Thêm một điều kiện nữa: **doanh thu là con số ngẫu nhiên**, phân phối chuẩn hoặc không chuẩn. Vì vậy
còn phải trả lời xác suất dự án đạt kỳ vọng tài chính, tính bằng cả mô phỏng lẫn cách chính xác.

Kết luận của bài đi ngược trực giác, nên trang được thiết kế để người học tự mò ra trước khi nghe giảng.

## Cách dùng

1. Gõ mã sinh viên rồi bấm **Lấy đề**. Mỗi mã cho một đề riêng trong 200 đề, mở lại lúc nào cũng ra
   đúng đề đó. Không nhập gì thì trang chạy đề mẫu đã chữa trên lớp.
2. Nhập lịch trả gốc. Bảng lưu chuyển tiền tệ, NPV, IRR, ba đèn ràng buộc và hai biểu đồ cập nhật
   ngay khi gõ.
3. Mức NPV và IRR tối ưu hiện sẵn ngay dưới hai ô kết quả, kèm khoảng cách còn lại, nên bạn luôn
   biết mình còn cách đích bao xa. Thanh đo cho biết bạn đang ở đâu trên quãng đường từ phương án
   trả đều tới mức đó. Điểm chỉ được tính khi cả ba ràng buộc đều xanh.
4. Mục **Dựng lịch theo phương pháp** không giải hộ bạn. Bạn nói cho nó biết ân hạn gốc tới hết
   năm nào, nó dựng phần còn lại theo đúng ba bước của phương pháp rồi báo NPV. Thử lần lượt các
   mức ân hạn, sổ thử ghi lại từng lần, và chỗ NPV cao nhất ngay trước khi gặp "không khả thi"
   chính là nghiệm.
5. Mục **Doanh thu không chắc chắn** mô phỏng Monte Carlo cho doanh thu dao động quanh đường kỳ vọng,
   với năm dạng phân phối: chuẩn, tam giác, đều, loga chuẩn, beta PERT. Con số đáng đọc nhất ở đó là
   xác suất lịch trả nợ của bạn vỡ ràng buộc dòng tiền.
6. Bốn gợi ý ở cuối trang, mở theo thứ tự. Gợi ý cuối là cách giải bằng tay, không cần trang này.

## Ghi chú kỹ thuật

Trang là một tệp HTML tĩnh, không cần máy chủ, không gọi mạng ngoài hai tệp phông của Google.
Toàn bộ mô hình dòng tiền chạy bằng JavaScript ngay trên trình duyệt, kèm 35 ca kiểm thử tự chạy
lúc tải trang để bảo đảm khớp với bản mô hình gốc viết bằng Python; kết quả kiểm thử hiện ở chân trang.

Trang hiện sẵn mức NPV và IRR tối ưu để người học biết đích ở đâu, nhưng **không chứa lịch trả gốc
tối ưu**: biết đích mà vẫn phải tự tìm đường. Bộ sinh đề và bộ giải được giữ riêng.

## Giấy phép

Tài liệu giảng dạy. Đỗ Ngọc Kiên, Trường Đại học Ngoại thương.
