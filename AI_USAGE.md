# AI Usage Log

## 1. Công cụ AI
Tên công cụ: Claude (Anthropic).

## 2. Mục đích sử dụng
- Phân tích giao diện website tham khảo (Văn phòng phẩm Hồng Hà) 
- Đề xuất bố cục, thẻ HTML, cách tổ chức CSS và cách hiển thị đa thiết bị cho khu vực Giỏ hàng.
- Tạo mã nguồn HTML/CSS ban đầu theo cấu trúc thư mục GitHub.
- Hỗ trợ tìm nguyên nhân và sửa lỗi responsive.

## 3. Prompt đã sử dụng
Các prompt chính (đã rút gọn, nội dung đầy đủ nằm trong bài tập):

**Prompt 1 – Phân tích website.** "Bạn là chuyên gia phân tích nghiệp vụ và thiết kế trải nghiệm người dùng cho website thương mại điện tử. Tôi đang khảo sát https://vpphonghaonline.com.vn/. Hãy lập bảng phân tích 5 khu vực (Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng): mục đích, thành phần giao diện cần có, điểm thuận tiện, một vấn đề, một đề xuất. Không khẳng định những tính năng chưa được kiểm chứng. Phân biệt rõ nhận xét dựa trên quan sát và đề xuất của AI."

**Prompt 2 – Đề xuất giao diện.** "Tôi đang thực hiện bài tập phát triển giao diện website thương mại điện tử bằng HTML5 và CSS3. Tôi muốn cải tiến khu vực giỏ hàng. Đối tượng: khách hàng mua sắm trực tuyến tại Việt Nam. Hãy đề xuất: bố cục, thành phần HTML, cách tổ chức CSS, cách hiển thị trên máy tính và điện thoại, điểm cần kiểm tra về khả năng sử dụng. Trước tiên hãy giải thích phương án thiết kế, chưa tạo mã nguồn cho đến khi tôi yêu cầu."

**Prompt 3 – Tạo mã nguồn (Phương án A, HTML/CSS thuần).** "Hãy tạo một trang giao diện thương mại điện tử bằng HTML và CSS: có tiêu đề và khu vực sản phẩm, tối thiểu 4 sản phẩm mẫu (hình ảnh, tên, giá, nút thao tác), bố cục cho máy tính và điện thoại, CSS tách file riêng, không backend, không thư viện không cần thiết. Giải thích cách chạy và những phần cần kiểm tra. Làm theo cấu trúc thư mục ecommerce-uui-improvement/ (css/style.css, images/product-demo.jpg, ai_usage.md, index.html, README.md)."

**Prompt 4 – Sửa lỗi responsive.** "Kiểm tra và sửa lỗi 1: thanh tiêu đề trên mobile sai kích thước và bố cục; lỗi 2: ảnh sản phẩm không hiển thị đúng. Giữ nguyên thiết kế, màu sắc, nội dung, chức năng và bố cục desktop; không dùng transform: scale() hay zoom để che lỗi; kiểm tra ở 320px, 375px, 390px, 430px; giải thích vai trò của các thành phần HTML/CSS đã sửa."

## 4. Kết quả AI đề xuất
- **Kiểm chứng website:** AI đọc mã nguồn của trang chủ, một trang sản phẩm và một trang danh mục. AI không kiểm tra được trang giỏ hàng, tìm kiếm và thanh toán thật, nên các điểm này được ghi là chưa xác nhận và do tôi kiểm chứng.
- **Phương án thiết kế giỏ hàng:** bố cục 2 cột trên máy tính (danh sách hàng và cột tóm tắt đơn), 1 cột trên điện thoại kèm thanh thanh toán cố định ở đáy. Gồm 3 cải tiến: thanh freeship và thông điệp "người đã mua", ô mã giảm giá trong phần tóm tắt, khu gợi ý mua kèm.
- **Mã nguồn:** `index.html` (thẻ ngữ nghĩa), `css/style.css` (biến CSS, grid/flex, mobile-first), ảnh minh họa, README và ai_usage.
- **Sửa lỗi:** AI xác định trang bị tràn ngang (khoảng 686px) khiến trình duyệt điện thoại thu nhỏ trang, nên header trông sai tỷ lệ. Nguyên nhân nằm ở khu cuộn ngang "Mua kèm cho đủ bộ" và cột tóm tắt đơn hàng.

## 5. Kiểm tra và điều chỉnh
**Đã kiểm tra:**
- Đối chiếu bảng khảo sát với website thật qua kết quả kiểm chứng của AI, sau đó tự điều chỉnh nội dung. Ví dụ: sản phẩm đã có điểm "5/5 (5 đánh giá)", nút "Mua ngay" có tồn tại, chính sách đổi trả là 2 ngày đầu (không phải 7 ngày).
- Chạy trang bằng Live Server, xem ở kích thước máy tính và điện thoại mô phỏng.
- Phát hiện lỗi header trên điện thoại bị sai kích thước.
- Phát hiện lỗi ảnh sản phẩm không hiển thị.

**Đã sửa:**
- Lỗi ảnh: tên ảnh trong thư mục `images/` và tên ảnh trong `index.html` không trùng khớp, tôi tự sửa cho khớp.
- Lỗi header: áp dụng bản sửa CSS của AI (đổi cột grid sang `minmax(0, 1fr)`, giảm cỡ chữ header ở màn hình ≤ 360px). AI cũng đổi `object-fit` của ảnh sang `contain` để ảnh không bị cắt.
- Sau khi sửa, AI đo bằng trình duyệt không giao diện ở các độ rộng 320, 375, 390, 430, 768 và 1280px: không còn thanh cuộn ngang và ảnh tải thành công.

**Không sử dụng / giới hạn:**
- Không dùng JavaScript, nên các nút và ô số lượng chưa có chức năng và các con số tính sẵn bằng tay.
- Không dùng đồng hồ đếm ngược hay "chỉ còn N sản phẩm", vì không có dữ liệu thật.
- Số liệu "người đã mua", mức freeship 300.000 ₫, phí ship 30.000 ₫ và mã GIAM10K là dữ liệu mẫu do AI tạo, không phải chính sách của website thật.
- Tất cả ảnh sản phẩm dùng chung một ảnh minh họa.

## 6. Phần tôi hiểu và có thể giải thích
**HTML (`index.html`):**
- `<meta name="viewport" content="width=device-width, initial-scale=1">`: để điện thoại hiển thị trang theo chiều rộng thật của màn hình.
- `<ul>/<li>`: danh sách sản phẩm trong giỏ và danh sách gợi ý mua kèm.
- `<dl>`: các cặp nhãn–giá trị trong phần tóm tắt (Tạm tính, Phí vận chuyển, Giảm giá, Tổng cộng).
- `<form>`, `<label>`, `<input>`: ô nhập mã giảm giá; `role="status"` cho thông báo kết quả.
- `<img>` có `alt`, `width`, `height`: mô tả ảnh và giữ chỗ cho ảnh khi tải.

**CSS (`css/style.css`):**
- `display: grid` với `minmax(0, 1fr)`: cột co được theo màn hình, không bị nội dung bên trong làm giãn ra (nguyên nhân gây lỗi header).
- `.upsell__list` với `overflow-x: auto` và `scroll-snap`: cho khu gợi ý cuộn ngang trên điện thoại.
- `.freeship__track` dùng `linear-gradient` làm nền kẻ ô ly cho thanh tiến trình.
- `object-fit: contain` và `aspect-ratio`: giữ tỷ lệ ảnh và hiện đủ ảnh trong khung.
- `:focus-visible` và `min-height: 44px` cho nút: hỗ trợ bàn phím và dễ bấm trên điện thoại.