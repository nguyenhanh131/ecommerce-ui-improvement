# ecommerce-ui-improvement
PTUD-BTVNcanhan-Buoi1

## 1. Giới thiệu
Dự án là bài tập cải tiến giao diện website thương mại điện tử văn phòng phẩm. Khu vực được cải tiến là **trang Giỏ hàng**, được xây dựng lại bằng HTML5 và CSS3 thuần dưới dạng một trang minh họa tĩnh. Trang này không liên quan đến hệ thống của website thật.

## 2. Website tham khảo
- Tên website: Văn phòng phẩm Hồng Hà Online
- URL: https://vpphonghaonline.com.vn/
- Khu vực đã khảo sát: Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng
- Khu vực được cải tiến: Giỏ hàng

## 3. Chức năng
- Hiển thị danh sách sản phẩm trong giỏ (hình ảnh, tên, mã, đơn giá, số lượng, thành tiền).
- Hiển thị tên và giá sản phẩm, cả ở danh sách giỏ hàng và khu gợi ý mua kèm (7 sản phẩm).
- Thanh tiến trình miễn phí vận chuyển ("Mua thêm 78.400 ₫ để được miễn phí vận chuyển") và dòng "Hôm qua có N người đã mua".
- Ô nhập mã giảm giá trong phần tóm tắt đơn hàng, có thông báo thành công và thông báo lỗi.
- Bố cục hỗ trợ nhiều kích thước màn hình: 2 cột trên máy tính, 1 cột trên điện thoại kèm thanh thanh toán cố định ở đáy.

## 4. Công nghệ
- HTML5
- CSS3 (không dùng JavaScript, thư viện hay backend)

## 5. Cách chạy
Mở file `index.html` bằng trình duyệt, hoặc mở thư mục bằng VS Code và dùng Live Server. Giữ đúng cấu trúc thư mục:

```
ecommerce-uui-improvement/
├── css/
│   └── style.css
├── images/
│   ├── vo.jpg
    ├── but-gel.jpg
    ├── so-a5.jpg
    ├── boc-decal.jpg
    ├── but-chi.jpg
    ├── giay-kiem-tra.jpg
    └── but-da-quang.jpg
├── ai_usage.md
├── index.html
└── README.md
```

## 6. Cải tiến đã thực hiện
**Vấn đề ban đầu (giỏ hàng của website tham khảo):**
1. Thiếu thông điệp thúc đẩy mua hàng (ví dụ "Mua thêm X đồng để freeship", "Đã có xx người mua sản phẩm này hôm qua").
2. Chưa có ô nhập mã giảm giá / voucher ngay tại màn hình giỏ hàng.
3. Thiếu đề xuất sản phẩm liên quan.

**Thay đổi đã thực hiện:**
1. Thêm khối freeship ở đầu trang, gồm thanh tiến trình kẻ ô ly và dòng thông báo số tiền còn thiếu; mỗi sản phẩm có nhãn "Hôm qua có N người đã mua".
2. Thêm khối "Mã giảm giá" trong cột tóm tắt đơn hàng, cạnh tổng tiền.
3. Thêm khu "Mua kèm cho đủ bộ" gồm 4 sản phẩm giá thấp (bọc vở, bút chì, giấy kiểm tra, bút dạ quang).

**Lỗi tự phát hiện và đã sửa:**
- Ảnh sản phẩm không hiển thị: tên ảnh trong thư mục `images/` và tên ảnh trong `index.html` không trùng khớp. Đã sửa cho khớp.
- Thanh tiêu đề trên điện thoại sai tỷ lệ: trang bị tràn ngang (rộng khoảng 686px so với màn hình 320–430px) nên trình duyệt thu nhỏ cả trang. Đã sửa bằng cách đổi các cột grid sang `minmax(0, 1fr)` và giảm cỡ chữ header ở màn hình ≤ 360px.

**Giới hạn:**
- Đây là bản minh họa tĩnh. Các nút (Áp dụng, Thêm vào giỏ, Xóa, Thanh toán) chưa có chức năng, ô số lượng chưa cập nhật tổng tiền.
- Số liệu "người đã mua", mức freeship 300.000 ₫, phí vận chuyển 30.000 ₫ và mã GIAM10K là **dữ liệu mẫu**, không phải chính sách của website thật.
- Thông báo mã giảm giá thành công và thông báo lỗi cùng hiển thị để minh họa hai trạng thái.

## 7. Hỗ trợ từ AI
**AI hỗ trợ (Claude):** phân tích và kiểm chứng website tham khảo, đề xuất phương án thiết kế giỏ hàng, tạo mã HTML/CSS ban đầu và hỗ trợ tìm nguyên nhân lỗi responsive.

**Phần tôi thực hiện:**
- Tự khảo sát website và lập bảng khảo sát ban đầu, rồi điều chỉnh lại sau khi đối chiếu với kết quả kiểm chứng của AI.
- Chạy trang bằng Live Server, kiểm tra ở kích thước máy tính và điện thoại, tự phát hiện lỗi ảnh và lỗi header.
- Sửa lỗi đường dẫn ảnh và chạy lại prompt để sửa lỗi responsive.

Chi tiết xem trong file [AI_USAGE.md](AI_USAGE.md).