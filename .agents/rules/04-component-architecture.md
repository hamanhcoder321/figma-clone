---
trigger: always_on
---

# Component Architecture

## Stack

Project sử dụng:

- Astro
- React
- TypeScript

Astro chịu trách nhiệm:

- page
- layout
- static content
- page composition

React chịu trách nhiệm:

- interactive component
- client-side state
- UI cần JavaScript

Không dùng React cho mọi thứ nếu không cần thiết.

---

## Structure

src/
├── assets/
│   └── images/
├── components/
│   ├── common/
│   ├── layout/
│   └── sections/
├── constants/
│   └── images.ts
├── layouts/
├── pages/
├── styles/
└── types/

---

## Naming

Component:

PascalCase

Ví dụ:

Header
HeroSection
CourseCard

File component:

PascalCase.tsx hoặc PascalCase.astro

Constants:

camelCase hoặc UPPER_SNAKE_CASE tùy loại dữ liệu.

---

## Section

Mỗi section của landing page nên có component riêng khi:

- section có UI phức tạp
- section có nhiều element
- section cần responsive riêng
- section có khả năng tái sử dụng

Không chia nhỏ quá mức.

---

## Images

Image source tập trung tại:

src/constants/images.ts

Không tạo nhiều object image rải rác trong component nếu cùng thuộc hệ thống image của project.

---

## Layout

Layout chung phải được xử lý tập trung.

Không copy:

header
footer
container
navigation

vào từng page.

---

## Data

Nếu UI render từ danh sách:

Ưu tiên dữ liệu dạng array/object và map khi hợp lý.

Không lặp markup thủ công nếu các item có cùng cấu trúc.