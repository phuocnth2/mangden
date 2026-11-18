# Măng Đen 3 ngày 2 đêm — GitHub Pages

Trang web HTML tĩnh, không cần npm, build, API key hay tài khoản hosting trả phí.

## 1. Deploy qua giao diện GitHub (máy tính dễ nhất)

1. Đăng nhập https://github.com và chọn **New repository**.
2. Đặt tên repo, ví dụ `mang-den-2026`; chọn **Public** (GitHub Free yêu cầu repo public để dùng Pages).
3. Chọn **Create repository**.
4. Tại trang repo, bấm **Add file → Upload files**, chọn **index.html** từ thư mục này và **README.md** nếu muốn.
5. Bấm **Commit changes**.
6. Mở **Settings → Pages**.
7. Trong **Build and deployment**, chọn **Source: Deploy from a branch**, **Branch: main**, **Folder: /(root)** và **Save**.
8. Sau khi Pages hoàn tất triển khai, mở `https://TEN_USER.github.io/mang-den-2026/` hoặc URL hiển thị trong Pages.
9. Gửi link HTTPS cho bạn bè qua Messenger. Trên iPhone, nếu mở trong trình duyệt của Messenger mà GPS lỗi, chọn mở ngoài bằng Safari/Chrome.

## 2. Cập nhật trang

Sửa file `index.html` rồi thay file đó trong repo (Commit changes). GitHub Pages sẽ xuất bản phiên bản mới.

## 3. GPS & an toàn

- Nút **Lấy GPS / Làm mới GPS** chỉ yêu cầu vị trí sau khi người dùng bấm.
- Mỗi lần bấm dùng `getCurrentPosition(..., {enableHighAccuracy:true,maximumAge:0})` để lấy một lần mới.
- Khoảng cách số km hiển thị là đường chim bay; quãng đường lái xe chính xác cần xem bằng **Chỉ đường** trong Google Maps.
- Với các địa điểm chưa có ghim chính xác, số km chỉ là **ước lượng tới khu vực**, không phải địa chỉ thực.
- Tọa độ hiện tại không được lưu lên server hoặc localStorage. Liên kết chỉ đường có thể đưa vị trí đó sang Google Maps theo hành động người dùng.
- GitHub Pages cấp HTTPS. GPS có thể bị hạn chế trong `file://` hay trình xem nhúng của Messenger/iPhone.

## 4. Chú ý khi public

- Repo **Public** và nội dung `index.html` có thể được người khác xem. Không đưa số điện thoại cá nhân, vị trí trực tiếp của bạn hay thông tin vé/booking lên repo.
- `17 Hoàng Thị Loan` là địa chỉ lưu trú được người dùng cung cấp, đang hiển thị trong trang làm mốc xuất phát. Hãy cân nhắc nếu không muốn công khai nơi đang lưu trú.
- Nút GPS không tự chạy khi vừa mở trang.

Nguồn GitHub: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
Nguồn GPS: https://developer.mozilla.org/en-US/docs/Web/API/Navigator/geolocation