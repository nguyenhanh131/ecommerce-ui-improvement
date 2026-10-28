
# ecommerce-ui-improvement
PTUD-BTVNcanhan-Buoi2

## 1. Giới thiệu
Bài tập Buổi 2 tiếp tục phát triển website minh họa giao diện giỏ hàng văn phòng phẩm từ Buổi 1. Mục tiêu là thực hành HTML5 và CSS3, cải thiện cấu trúc nội dung, cách bố trí sản phẩm và phản hồi trực quan của giao diện.

Website được xây dựng bằng HTML5 và CSS3 thuần, không kết nối với hệ thống của website tham khảo.

## 2. Website tham khảo và khu vực cải tiến
- **Website tham khảo:** Văn phòng phẩm Hồng Hà Online
- **URL:** https://vpphonghaonline.com.vn/
- **Khu vực thực hiện:** Trang giỏ hàng, bao gồm danh sách sản phẩm, tóm tắt đơn hàng và khu vực mua kèm.

## 3. Kỹ thuật HTML5/CSS3 đã thực hành
- **HTML5:** Sử dụng các phần tử ngữ nghĩa như `header`, `main`, `section`, `aside`, cùng các phần tử biểu mẫu và danh sách phù hợp.
- **CSS selector:** Thực hành element selector, class selector và descendant selector.
- **Box Model:** Điều chỉnh `margin`, `padding`, `border` và `border-radius`.
- **Flexbox:** Căn chỉnh các thành phần theo hàng hoặc cột bằng `display: flex`, `justify-content`, `align-items` và `gap`.
- **CSS Grid:** Bố trí khu vực sản phẩm mua kèm theo hàng và cột bằng `display: grid`, `grid-template-columns`, `repeat()` và `gap`.
- **Hình ảnh:** Sử dụng `alt` cho hình ảnh và `object-fit` để kiểm soát cách hiển thị.
- **Pseudo-class và transition:** Bổ sung hiệu ứng `:hover`, `:focus-visible` và chuyển đổi trạng thái nhẹ cho nút bấm.

## 4. Hướng dẫn chạy website
1. Tải hoặc clone repository về máy.
2. Mở thư mục dự án bằng VS Code.
3. Mở file `index.html` trực tiếp bằng trình duyệt hoặc sử dụng tiện ích Live Server.
4. Đảm bảo thư mục `css/` và `images/` được giữ nguyên để các tệp CSS và hình ảnh hiển thị chính xác.

## 5. Những thay đổi đã thực hiện
- Cải thiện cấu trúc HTML và nhãn cho các trường nhập số lượng sản phẩm.
- Điều chỉnh khu vực mua kèm bằng CSS selector và Box Model.
- Áp dụng Flexbox để căn chỉnh thông tin trong phần tóm tắt đơn hàng.
- Chuyển khu vực mua kèm sang CSS Grid, giúp các thẻ sản phẩm hiển thị theo nhiều cột tùy kích thước màn hình.
- Bổ sung hiệu ứng hover, transition và focus-visible cho nút “Thêm vào giỏ”.
- Thay chữ thương hiệu mẫu bằng logo và tên “Văn phòng phẩm HH” trong header.

## 6. Công cụ AI và cách kiểm tra kết quả
**Công cụ AI sử dụng:** ChatGPT và Claude.

AI hỗ trợ giải thích kiến thức HTML5/CSS3, đề xuất cách cải tiến giao diện, viết và điều chỉnh mã nguồn.

**Cách kiểm tra và điều chỉnh:**
- Đối chiếu mã được đề xuất với cấu trúc HTML và CSS hiện có.
- Chạy website bằng trình duyệt hoặc Live Server để kiểm tra giao diện thực tế.
- Quan sát cách bố trí sản phẩm ở các kích thước màn hình khác nhau.
- Kiểm tra hiệu ứng hover bằng chuột và focus-visible bằng bàn phím.
- Điều chỉnh các đề xuất chưa phù hợp với trải nghiệm người dùng, chẳng hạn giữ hình ảnh sản phẩm hiển thị đầy đủ bằng `object-fit: contain` thay vì cắt ảnh bằng `cover`.

Chi tiết quá trình sử dụng AI được trình bày trong file [AI_USAGE.md](AI_USAGE.md).

## 7. Giới hạn
- Website là bản minh họa tĩnh; các nút thao tác chưa thực sự cập nhật dữ liệu giỏ hàng nếu chưa có JavaScript xử lý.
- Giá sản phẩm, phí vận chuyển, mã giảm giá và các số liệu hiển thị là dữ liệu mẫu.
- Giao diện được xây dựng phục vụ mục đích học tập, không đại diện cho hệ thống chính thức của website tham khảo.
