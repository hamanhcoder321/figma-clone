---
trigger: always_on
---

# Frontend Code Rules

## Mục tiêu

Code phải:

- sạch
- dễ đọc
- dễ bảo trì
- dễ mở rộng
- đúng TypeScript
- đúng kiến trúc project
- hạn chế lặp code

---

## Nguyên tắc

Ưu tiên:

- semantic HTML
- component rõ trách nhiệm
- tên biến rõ nghĩa
- class rõ mục đích
- TypeScript type rõ ràng
- cấu trúc thư mục nhất quán

Không viết code chỉ để "chạy được".

---

## Component

Một component nên có một trách nhiệm chính.

Không tạo component chỉ để tách một vài dòng code nếu việc tách làm cấu trúc khó hiểu hơn.

Không tạo component quá lớn nếu nó chứa nhiều phần UI độc lập.

---

## Shared components

Các thành phần dùng nhiều nơi nên đặt trong:

src/components/common/

Ví dụ:

- Button
- Container
- SectionTitle
- Icon
- Badge

Layout dùng chung đặt trong:

src/components/layout/

Page-specific sections đặt trong:

src/components/sections/

---

## Images

Không hard-code đường dẫn ảnh lặp lại trong nhiều component.

Thông tin ảnh dùng chung đặt trong:

src/constants/images.ts

Component chỉ lấy ảnh từ constants.

---

## TypeScript

Không sử dụng `any` nếu có thể xác định type.

Không tạo type phức tạp nếu dữ liệu đơn giản.

Type phải phản ánh dữ liệu thực tế.

---

## CSS / Tailwind

Không biến mọi thông số Figma thành giá trị fixed.

Phải xác định trước:

- fixed
- fluid
- max-width
- min-width
- responsive

Ưu tiên layout bằng:

- flex
- grid
- max-width
- margin auto
- gap
- padding

hơn là position tuyệt đối.

---

## Absolute positioning

Chỉ dùng khi element thực sự cần nằm theo vị trí tương đối với một element khác.

Không dùng absolute để "ép" layout giống Figma.

---

## Code duplication

Nếu cùng một logic hoặc UI xuất hiện nhiều lần:

Phân tích xem có nên tạo:

- component
- constant
- utility

Không copy/paste một cách máy móc.