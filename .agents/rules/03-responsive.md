---
trigger: always_on
---

# Responsive Rules

## Nguyên tắc

Responsive phải được xây dựng từ layout logic, không phải bằng cách sửa từng pixel cho từng màn hình.

---

## Desktop

Thiết kế Figma sử dụng:

- 1440px cho section chuẩn.
- 1920px cho màn hình lớn hơn khi thiết kế yêu cầu.

Không mặc định:

width: 1440px;

cho mọi section.

Phải xác định:

section có full width hay không,
container có max-width hay không,
content có giới hạn width hay không.

---

## Breakpoints

Không tạo breakpoint chỉ vì một kích thước xuất hiện trong Figma.

Breakpoint phải xuất hiện khi layout thực sự cần thay đổi.

---

## Mobile

Phải kiểm tra:

- horizontal overflow
- text wrapping
- image scaling
- button width
- spacing
- grid columns
- flex direction
- navigation
- font size
- line height

---

## Tablet

Không mặc định tablet = desktop hoặc mobile.

Phải kiểm tra layout tại khoảng giữa hai trạng thái.

---

## Validation

Sau khi hoàn thành một section:

Kiểm tra tối thiểu:

- desktop
- tablet
- mobile

Nếu chỉ có Figma desktop:

Phải kiểm tra khả năng responsive thực tế và ghi rõ các quyết định do Developer tự thiết kế.