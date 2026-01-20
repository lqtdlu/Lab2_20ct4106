# Bài thực hành 2: Shopping List Manager (Ionic + Angular)

Chào mừng các bạn đến với bài thực hành xây dựng ứng dụng quản lý mua sắm bằng Ionic Framework và Angular.

## 🎯 Mục tiêu bài thực hành
Dựa trên kiến thức đã học, sinh viên xây dựng ứng dụng **"Shopping List Manager"** với các chức năng:
1.  Hiển thị danh sách vật phẩm cần mua.
2.  Thêm vật phẩm mới (có Validation).
3.  Xóa vật phẩm khỏi danh sách.
4.  Đánh dấu đã mua (Checkbox & CSS).
5.  Xem thông tin giới thiệu (About Page) và điều hướng.

## 🛠 Hướng dẫn Cài đặt & Chạy dự án

1.  **Cài đặt thư viện:**
    Mở Terminal tại thư mục dự án và chạy lệnh:
    ```bash
    npm install
    ```

2.  **Khởi chạy ứng dụng (Xem trước):**
    ```bash
    ionic serve
    ```
    Trình duyệt sẽ tự động mở tại địa chỉ `http://localhost:8100`.

3.  **Tạo trang mới (Yêu cầu bắt buộc):**
    Bạn cần chạy lệnh sau để tạo trang About chuẩn theo cấu trúc đề bài:
    ```bash
    ionic generate page items/about
    ```

---

## 💯 Tiêu chí chấm điểm (Autograding)

Hệ thống GitHub Classroom sẽ tự động chấm điểm bài làm của bạn mỗi khi bạn **Push** code lên.
Tổng điểm tối đa: **10/10**.

| STT | Tên Test Case | Yêu cầu chi tiết | Điểm |
|:---:|:--- |:--- |:---:|
| **1** | **Cấu trúc & Standalone** | - Component phải cấu hình `standalone: true`.<br>- Import đầy đủ các UI component (`IonList`, `IonItem`, `IonInput`...) trong mảng `imports: []`. | **2.0** |
| **2** | **Hiển thị & Nhập liệu** | - Import `FormsModule`.<br>- Sử dụng `*ngFor` để hiển thị danh sách.<br>- Sử dụng `[(ngModel)]` cho ô nhập liệu để binding dữ liệu 2 chiều. | **1.0** |
| **3** | **Điều hướng (Navigation)** | - Có trang `items/about`.<br>- Nút "About" tại trang chủ sử dụng `routerLink` để chuyển trang. | **1.0** |
| **4** | **Validation (Cảnh báo)** | - Sử dụng `AlertController` để hiển thị thông báo lỗi.<br>- Cảnh báo xuất hiện khi người dùng bấm "Thêm" mà ô nhập liệu bị rỗng hoặc chỉ chứa khoảng trắng. | **1.0** |
| **5** | **Chức năng Xóa** | - Sử dụng `ion-item-sliding` và `ion-item-options` để tạo nút xóa trượt.<br>- Hàm xóa phải dùng `.splice()` để thực sự loại bỏ phần tử khỏi mảng dữ liệu. | **1.0** |
| **6** | **Tuân thủ UI & Danh tính** | - **UI:** `ion-input` phải dùng thuộc tính `labelPlacement="floating"` (Ionic 7+).<br>- **About Page:** Phải dùng cấu trúc `ion-card` và nút `ion-back-button` có `defaultHref="/home"`.<br>- **Danh tính:** Bắt buộc thay thế placeholder `[Tên Sinh Viên]` và `[MSSV]` bằng thông tin thật của bạn. | **2.0** |
| **7** | **Nâng cao (OOP & Logic)** | - **OOP:** Mảng `items` phải chứa các **đối tượng** (Object: `{ name, isBought }`) thay vì mảng chuỗi đơn thuần.<br>- **Tương tác:** Khi click vào `ion-checkbox`, trạng thái `isBought` phải cập nhật và tên sản phẩm phải được gạch ngang (CSS). | **2.0** |

---

## ⚠️ CẢNH BÁO QUAN TRỌNG (Quy chế thi)

Hệ thống chấm điểm đã kích hoạt chế độ **Protected Files** (Bảo vệ tệp tin).

1.  **NGHIÊM CẤM SỬA ĐỔI** các file/thư mục hệ thống sau:
    * 🚫 Thư mục `.github/` (Chứa workflows chấm điểm)
    * 🚫 File `package.json`
    * 🚫 File `angular.json`
    
2.  **Hậu quả:**
    Nếu bạn cố tình sửa đổi các file trên để gian lận hoặc can thiệp vào quá trình chấm điểm, hệ thống sẽ gắn nhãn **"Protected file(s) modified"**. Bài làm của bạn sẽ bị hủy kết quả và nhận **0 điểm** ngay lập tức.

3.  **Phạm vi làm bài:**
    Sinh viên chỉ thực hiện viết code và chỉnh sửa trong thư mục `src/app/` và `src/theme/`.

---

## 🧪 Cách kiểm tra điểm

### Cách 1: Kiểm tra trên GitHub (Khuyên dùng)
Sau khi hoàn thành một chức năng, hãy thực hiện:
```bash
git add .
git commit -m "Hoàn thành chức năng X"
git push origin main
