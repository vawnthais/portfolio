# Refactor Lesson Pages and Layout

Mục tiêu: Tóm tắt, tinh gọn nội dung của 6 bài thực hành (bai1.html -> bai6.html) để tập trung duy nhất vào các yêu cầu cốt lõi được giao. Đồng thời, thiết kế lại bố cục (loại bỏ kiểu chia 2 cột bị thừa) để trang web trông gọn gàng, chuyên nghiệp và dễ đọc hơn.

## User Review Required

> [!IMPORTANT]
> - Nội dung hiện tại của các bài đang rất dài (dạng copy-paste toàn bộ các bước thực hành từ PDF). Việc tóm tắt sẽ **xóa bỏ các chi tiết thừa** (ví dụ: các bước bấm nút nào, tạo thư mục ra sao trong Bài 1) và chỉ giữ lại đúng trọng tâm yêu cầu (ví dụ: Cấu trúc thư mục cuối cùng và quy tắc đặt tên).
> - Bạn có đồng ý với việc loại bỏ hoàn toàn phần cột phụ bên phải (phần "Sản phẩm & Dữ liệu Minh họa" - `.detail-assets`) vốn đang bị lặp lại và thừa thãi không? Thay vào đó, mình sẽ đưa thẻ (tags) và kỹ năng lên đầu trang ngay dưới tiêu đề, phần còn lại dành không gian 1 cột rộng rãi, dễ đọc cho nội dung chính.

## Proposed Changes

### 1. Cập nhật CSS chung cho 6 trang chi tiết
- Sửa lại class `.detail-grid` thành `grid-template-columns: 1fr; max-width: 900px; margin: 2rem auto;` (tập trung thành 1 cột chính giữa, chuẩn phong cách blog/portfolio hiện đại).
- Di chuyển phần "Kỹ năng rèn luyện" (tags) lên ngay dưới tiêu đề (header) của từng bài.
- Xóa bỏ khối `.detail-assets` thừa thãi.

### 2. Tóm tắt nội dung từng bài (bai1.html -> bai6.html)

---

#### [MODIFY] `bai1.html`
- **Nội dung mới:** Trình bày cấu trúc thư mục tối ưu và quy tắc đặt tên tệp đã thiết lập, kèm ảnh chụp minh họa.
- **Cách làm:** Loại bỏ các bước 1-12 dài dòng. Chỉ tạo 2 phần: "1. Cấu trúc thư mục tối ưu" (kèm 1-2 ảnh đẹp nhất về thư mục) và "2. Quy tắc đặt tên tệp" (giải thích quy tắc không dấu, viết hoa chữ cái đầu...).

#### [MODIFY] `bai2.html`
- **Nội dung mới:** Trình bày kết quả tìm kiếm học thuật bằng các toán tử nâng cao và bảng đánh giá nguồn tin đã thực hiện.
- **Cách làm:** Trình bày rõ ràng các cú pháp tìm kiếm nâng cao (AND, OR, site:, filetype:). Trình bày lại Bảng đánh giá nguồn tin một cách gọn gàng bằng thẻ `<table>` đẹp mắt. Xóa các đoạn diễn giải lan man.

#### [MODIFY] `bai3.html`
- **Nội dung mới:** Trình bày sự so sánh giữa Prompt ban đầu và Prompt cải tiến cùng kết quả đầu ra từ AI.
- **Cách làm:** Sử dụng thiết kế 2 cột (hoặc box so sánh) dành riêng cho "Prompt Trước" vs "Prompt Sau" để làm nổi bật sự cải tiến. Hiển thị kết quả AI trả về bên dưới một cách rõ ràng.

#### [MODIFY] `bai4.html`
- **Nội dung mới:** Trình bày minh chứng về việc sử dụng công cụ quản lý dự án nhóm và cách thức phối hợp trực tuyến.
- **Cách làm:** Hiển thị ảnh chụp màn hình công cụ (ví dụ Trello/Google Drive) và tóm tắt ngắn gọn quy trình làm việc nhóm (giao việc, tiến độ, nhận xét).

#### [MODIFY] `bai5.html`
- **Nội dung mới:** Trưng bày sản phẩm nội dung số hoàn thiện (hình ảnh, video hoặc bài viết) được hỗ trợ bởi AI.
- **Cách làm:** Dành toàn bộ không gian để làm nổi bật sản phẩm số. Loại bỏ các bước tạo prompt dài dòng không cần thiết nếu không có trong yêu cầu.

#### [MODIFY] `bai6.html`
- **Nội dung mới:** Trình bày bộ nguyên tắc cá nhân về sử dụng AI có trách nhiệm dựa trên các nghiên cứu đã thực hiện.
- **Cách làm:** Biến 6 nguyên tắc thành 6 thẻ (cards) hoặc một danh sách được thiết kế ấn tượng (icon + text), kèm theo Infographic minh họa ở cuối trang. Xóa bỏ các lý thuyết đạo đức học thuật dài dòng ở đầu trang.

## Verification Plan
- Chạy thử (Preview) các trang HTML để đảm bảo bố cục 1 cột hiển thị hoàn hảo trên cả Desktop và Mobile.
- Đối chiếu lại nội dung của từng file HTML xem đã khớp 100% với bức ảnh yêu cầu của người dùng hay chưa.
