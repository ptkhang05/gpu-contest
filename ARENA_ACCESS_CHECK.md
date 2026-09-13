# Kiểm tra quyền FuriosaAI Arena

> Kiểm tra read-only ngày **2026-09-09** qua phiên trình duyệt người dùng đã đăng nhập.
> Các quan sát UI bên dưới là bản ghi lịch sử, không phải trạng thái Arena hiện tại.
> Không gửi, sửa hoặc hủy job; không tải file lên.

## Kết quả xác nhận

- URL: <https://arena.furiosa.ai/>
- Trang tải thành công với tiêu đề **RNGD Job Scheduler**.
- Phiên đang đăng nhập bằng GitHub account **`ptkhang05`**, role hiển thị **`user`**.
- Phiên bản giao diện scheduler: **v0.8.0**.
- Queue thay đổi trong lúc quan sát từ **0 waiting · 0/1 NPUs running** sang
  **0 waiting · 1/1 NPUs running** dù tài khoản không có job nào. Điều này là bằng chứng
  mạnh rằng chỉ số NPU phản ánh scheduler dùng chung, không chỉ job của tài khoản này.
- Storage thay đổi từ **64.63 GB** lên **64.65 GB / 487.43 GB** trong lúc quan sát.
  Đây là số giao diện báo; chưa rõ là storage dùng chung hay cách tính quota nào khác.
- Danh sách job hiện tại: **no jobs**.

## Chức năng nhìn thấy trên tài khoản

- Chọn file cho job.
- `Name`.
- `Entrypoint`.
- `Timeout (s)`.
- `Args`.
- `Env (KEY=VALUE per line)`.
- Nút `Submit`.
- Bộ lọc job theo `status`: `any`, `QUEUED`, `RUNNING`, `SUCCEEDED`, `FAILED`, `CANCELED`.
- Bộ lọc ngày `submitted` và `to`.
- Bảng job có các cột: `ID`, `Name`, `Owner`, `Status`, `Ahead`, `Size`, `Submitted`,
  `Dur`, `Why`, `Actions`.

## Điều đã xác nhận từ email

- Registration đã được ban tổ chức xác nhận.
- Quyền Arena đã được phê duyệt.
- Người tham gia đăng nhập Arena bằng GitHub account đã khai trong form.
- Arena là scheduler cho máy chủ RNGD dùng chung, nơi submission được chạy và đánh giá.
- Vào 09/09 tutorial vẫn đang chuẩn bị; thông tin này đã lỗi thời. Xem
  `YEU_CAU_CUOC_THI.md` để biết lịch được công bố sau đó.
- Câu hỏi toolchain/RNGD: FuriosaAI Forum.
- Vấn đề registration/account: `moa2026.competition@gmail.com`.

## Điều chưa thể kết luận từ giao diện

- Không có tên competition/namespace riêng hiển thị trên trang chính.
- Chưa thấy quota số job/submission mỗi ngày hoặc mỗi đội.
- Giao diện Arena ngày 09/09 không hiển thị submission format hoặc score formula;
  chúng đã được công bố sau đó ở baseline repository mới và `moa-submitter-cli`.
- Chưa thể xác nhận ý nghĩa chính xác của chỉ số storage nếu không có tài liệu server.
- Chưa chạy job thử, nên chưa xác nhận toolchain upload, entrypoint, log hoặc cycle output.

## Trạng thái nguồn ngày 09/09

- Baseline remote vẫn ở commit
  `4bf1bac714d8bb9e3b8639e450a0c69d5aee93ba`; bản cục bộ đang mới nhất.
- Website đã cập nhật lên commit
  `00d6217de3701e6a6eb59780ca2f2ddc5c6a47f1`; bản cục bộ đã fast-forward.
- FAQ mới thêm hướng dẫn đổi leaderboard display name và bỏ hướng dẫn đội cũ qua email.
- Form hiện có các trường `Team Participation`, `Team Members` và `Leaderboard Name`.
