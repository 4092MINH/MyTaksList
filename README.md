# MyStudyApp - Ứng dụng SwiftUI Demo

Đây là một dự án demo được xây dựng hoàn toàn bằng SwiftUI, mô phỏng lại giao diện người dùng từ một bản thiết kế (mockup) được cung cấp. Ứng dụng bao gồm các luồng chức năng cơ bản như đăng nhập, xem báo cáo học tập, quản lý nhắc nhở và một trung tâm hỗ trợ dạng chat.

## Giao diện ứng dụng

Dưới đây là bản thiết kế gốc mà dự án này mô phỏng theo:


*(Lưu ý: Bạn có thể thay thế link trên bằng link đến hình ảnh của bạn hoặc lưu hình ảnh vào dự án và dẫn link tương đối)*

## Tính năng chính & Checklist

Dưới đây là danh sách các tính năng đã được triển khai và các tính năng dự kiến trong tương lai.

### Đã hoàn thành (Implemented)
- [x] **Màn hình Đăng nhập (Login)**
  - [x] Giao diện nhập Username và Password.
  - [x] Nút "Login" để chuyển sang màn hình chính.
  - [x] Giả lập trạng thái đăng nhập thành công.
- [x] **Giao diện chính (Main App)**
  - [x] Sử dụng `TabView` để điều hướng giữa các màn hình.
  - [x] Ba tab chính: Report, Reminder, và Help.
- [x] **Tab Báo cáo (Report)**
  - [x] Hiển thị danh sách các môn học.
  - [x] Sử dụng `ProgressBar` tùy chỉnh để biểu diễn điểm số.
  - [x] Hiển thị xếp hạng tổng quan.
- [x] **Tab Nhắc nhở (Reminder)**
  - [x] Hiển thị danh sách các thông báo/nhắc nhở.
  - [x] Giao diện `List` gọn gàng, sạch sẽ.
- [x] **Tab Trung tâm Hỗ trợ (Helping Center)**
  - [x] Giao diện chat cơ bản.
  - [x] Phân biệt tin nhắn của người dùng và người gửi bằng bong bóng chat (message bubble).
  - [x] Vùng nhập liệu tin nhắn.

### Kế hoạch phát triển (To-Do)
- [ ] **Xác thực người dùng**
  - [ ] Tích hợp logic xác thực thực tế (thay vì giả lập).
  - [ ] Xử lý các trường hợp đăng nhập thất bại (sai mật khẩu, tài khoản không tồn tại).
  - [ ] Thêm chức năng "Đăng ký" (Sign up).
- [ ] **Tương tác với Backend**
  - [ ] Kết nối API để lấy dữ liệu động cho các màn hình (điểm số, nhắc nhở, tin nhắn).
  - [ ] Gửi tin nhắn trong Trung tâm Hỗ trợ lên server.
- [ ] **Cải tiến giao diện người dùng**
  - [ ] Thêm hiệu ứng chuyển cảnh (animations) mượt mà hơn.
  - [ ] Hoàn thiện màn hình chi tiết cho từng mục (ví dụ: khi nhấn vào một nhắc nhở).
  - [ ] Hỗ trợ Chế độ Tối (Dark Mode).
- [ ] **Lưu trữ dữ liệu**
  - [ ] Lưu trữ token đăng nhập cục bộ (sử dụng `UserDefaults` hoặc `Keychain`).
  - [ ] Cache dữ liệu để có thể sử dụng offline.
- [ ] **Testing**
  - [ ] Viết Unit Tests cho các logic nghiệp vụ.
  - [ ] Viết UI Tests để đảm bảo giao diện hoạt động đúng.

## Công nghệ sử dụng
*   **Framework:** SwiftUI
*   **Ngôn ngữ:** Swift
*   **Kiến trúc:** MVVM (Model-View-ViewModel) cơ bản
*   **Môi trường:** Xcode 14+
*   **Nền tảng:** iOS 15.0+

## Cấu trúc thư mục
Dự án được tổ chức theo cấu trúc rõ ràng để dễ dàng quản lý và mở rộng:
```
MyStudyApp/
├── MyStudyAppApp.swift   // Entry point
├── ContentView.swift      // View chính, điều hướng Login/MainApp
│
├── Views/                 // Chứa các màn hình giao diện chính
│   ├── LoginView.swift
│   ├── MainAppView.swift
│   ├── ReportView.swift
│   ├── ReminderView.swift
│   └── HelpingCenterView.swift
│
├── Components/            // Chứa các View nhỏ, tái sử dụng
│   ├── ProgressBarView.swift
│   └── MessageBubble.swift (trong HelpingCenterView)
│
└── Models/                // Chứa các cấu trúc dữ liệu
    └── DataModels.swift
```

## Hướng dẫn cài đặt và chạy dự án
1.  **Clone repository:**
    ```bash
    git clone [link-repository-cua-ban]
    ```
2.  **Mở dự án:**
    Mở file `MyStudyApp.xcodeproj` bằng Xcode.
3.  **Chọn Simulator:**
    Chọn một máy ảo iOS (ví dụ: iPhone 14 Pro).
4.  **Chạy ứng dụng:**
    Nhấn nút **Run** (phím tắt `Cmd + R`) để biên dịch và chạy ứng dụng trên máy ảo.

## Giấy phép
Dự án này được cấp phép theo Giấy phép MIT - xem chi tiết trong file `LICENSE`.

