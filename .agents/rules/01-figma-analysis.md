---
trigger: always_on
---

# Figma Analysis Rules

## Mục tiêu

Khi nhận thiết kế Figma, AI phải giúp Developer phân tích trước khi code.

Không chuyển máy móc thông số Figma thành CSS.

---

## Thông tin cần phân tích

Khi đọc Figma, phân tích:

- Page
- Section
- Container
- Layout
- Grid
- Flex
- Alignment
- Spacing
- Typography
- Image
- Background
- Border
- Border radius
- Shadow
- Gradient
- Overlay
- Animation hoặc effect nếu có
- Responsive behavior

---

## Container

Thiết kế chuẩn của project:

- Desktop section mặc định: 1440px.
- Màn hình lớn hơn: nội dung có thể mở rộng tới 1920px tùy thiết kế.
- Không mặc định biến 1440px thành width cố định cho mọi thành phần.
- Phân biệt rõ:
  - section width
  - container width
  - content width
  - element width

Không hard-code width chỉ vì Figma đang hiển thị một kích thước cụ thể.

---

## Responsive

Không giả định rằng:

Desktop = Mobile thu nhỏ.

Phải phân tích:

- element nào giữ nguyên
- element nào co giãn
- element nào thay đổi layout
- element nào đổi thứ tự
- element nào ẩn
- typography nào thay đổi
- spacing nào thay đổi
- image nào thay đổi tỷ lệ

Nếu Figma chỉ cung cấp desktop:

AI phải đưa ra giả thuyết responsive và nói rõ đó là giả thuyết.

Không khẳng định đó là yêu cầu thiết kế nếu không có bằng chứng.

---

## Khi Developer hỏi "phần này code thế nào?"

Trả lời theo thứ tự:

1. Cấu trúc HTML/component.
2. Layout nên dùng.
3. Các breakpoint cần quan tâm.
4. Các thuộc tính CSS/Tailwind cần dùng.
5. Những điểm cần tự quyết định.

Không viết code hoàn chỉnh trừ khi Developer yêu cầu.

---

## Khi thông số Figma mâu thuẫn với nhau

Không tự chọn một giá trị.

Phải chỉ ra:

- thông số A
- thông số B
- điểm mâu thuẫn
- ảnh hưởng
- đề xuất cách kiểm tra

Sau đó chờ Developer quyết định.