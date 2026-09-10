# NPU Model Optimization Competition — hồ sơ yêu cầu

> Bản chụp thông tin được kiểm tra ngày **2026-09-09** (Asia/Saigon).
> Website chính thức được lưu tại commit `00d6217de3701e6a6eb59780ca2f2ddc5c6a47f1`.
> Repository baseline được lưu tại commit `4bf1bac714d8bb9e3b8639e450a0c69d5aee93ba`
> (commit time `2026-09-08T05:45:54Z`). Các mục được ban tổ chức ghi **TBD/TBA**
> bên dưới chưa phải quy định hoàn chỉnh và cần kiểm tra lại khi có thông báo mới.

## 1. Thông tin tổng quan

- Tên: **NPU Model Optimization Competition**.
- Thuộc workshop **MOA — Measuring and Optimizing Heterogeneous AI Architectures**,
  tại **MICRO 2026 (59th IEEE/ACM International Symposium on Microarchitecture)**.
- Đơn vị đồng tổ chức: **Seoul National University** và **FuriosaAI**.
- Mục tiêu: tối ưu suy luận **Gemma-4-12B-it / Gemma 4 12B**, một mô hình ngôn ngữ
  lớn đa phương thức, trên NPU **FuriosaAI RNGD**, dùng toolchain `furiosa-opt`.
- Người tham gia bắt đầu từ implementation baseline do ban tổ chức cung cấp và phải
  giữ nguyên public interface cũng như hành vi số của mô hình trong phạm vi hợp đồng chấm.
- Không cần tự sở hữu phần cứng RNGD. Chương trình được chạy trên máy chủ RNGD dùng chung
  qua **FuriosaAI Arena**; quyền truy cập được cấp cho người đã đăng ký.
- Cuộc thi có 2 vòng/stage: **Kernel Optimization** và **Model Optimization (E2E)**.
- Trong cả hai vòng, correctness là điều kiện bắt buộc trước khi được tính hiệu năng.
- Ba đội đứng đầu có cơ hội trình bày công việc tại MOA Workshop ở Athens.

## 2. Điều kiện tham gia và đăng ký

### 2.1. Điều kiện tư cách

- Cuộc thi chỉ dành cho người **đang có tư cách sinh viên** (undergraduate hoặc graduate).
- Người vừa đi làm vừa đang theo học vẫn đủ điều kiện (FAQ nêu ví dụ degree dispatch program).
- Người đã tốt nghiệp và không còn là sinh viên **không đủ điều kiện**.
- Form đăng ký mô tả cuộc thi là mở cho sinh viên trên toàn thế giới.

### 2.2. Cá nhân và đội

- Có thể thi cá nhân hoặc theo đội.
- **Không giới hạn số thành viên tối đa** trong đội.
- Mỗi thành viên đội phải tự điền form đăng ký riêng.
- Trên form hiện hành, mỗi thành viên phải liệt kê toàn bộ thành viên (bao gồm chính mình),
  chỉ rõ **đại diện đội**, và mọi thành viên phải cung cấp cùng một danh sách.
- Mọi thành viên trong cùng đội phải nhập cùng một `Leaderboard Name` nếu muốn hiển thị
  tên đội thống nhất.
- FAQ ngày 09/09 đã bỏ hướng dẫn cũ yêu cầu gửi danh sách đội qua email. Vì vậy quy trình
  hiện hành là khai trực tiếp trên form; chỉ liên hệ email nếu cần sửa tên leaderboard
  hoặc xử lý vấn đề tài khoản/đăng ký.

### 2.3. Thời hạn và dữ liệu form đăng ký

- Thời gian đăng ký: **2026-09-01 đến 2026-09-15**.
- Form yêu cầu các trường sau (dấu “bắt buộc” theo form tại thời điểm chụp):
  - `Name` — bắt buộc.
  - `University Email Address` — bắt buộc; phải dùng email chính thức của trường để xác
    minh tư cách sinh viên; form kiểm tra định dạng email.
  - `GitHub ID` — bắt buộc; dùng để cấp quyền truy cập máy chủ đánh giá RNGD.
  - `LinkedIn / Homepage` — không bắt buộc.
  - `Team Participation` — bắt buộc; chọn `Yes` hoặc `No`. Mỗi thành viên đội vẫn phải
    tự nộp form riêng.
  - `Team Members` — không bắt buộc; nếu thi đội, liệt kê tất cả thành viên, bao gồm chính
    mình, chỉ rõ đại diện đội; tất cả thành viên cung cấp cùng danh sách.
  - `Leaderboard Name` — không bắt buộc; nếu thi đội, tất cả thành viên phải nhập cùng
    tên. Nếu để trống sẽ hiển thị dạng `Participant #XXX`.
  - `School` — bắt buộc; form ghi nếu không đang theo học thì nhập `N/A` (tuy nhiên FAQ
    đồng thời quy định người không còn là sinh viên không đủ điều kiện).
  - `Department` — bắt buộc; nếu không đang theo học thì nhập `N/A`.
  - `Current Degree Program` — bắt buộc; lựa chọn gồm `Undergraduate`, `Master's`,
    `Ph.D.`, hoặc lựa chọn tự điền.
  - `Expected Graduation Date` — bắt buộc; ví dụ `May 2027`.
  - Câu hỏi mở về hiểu biết/câu hỏi đối với FuriosaAI — không bắt buộc.
  - Đồng ý thu thập và sử dụng thông tin cá nhân — bắt buộc, chọn
    `I have read and agree.`
- Mục đích sử dụng dữ liệu theo form: vận hành cuộc thi, cấp quyền evaluation server,
  gửi thông báo, trao giải, và có thể liên hệ về cuộc thi/các cơ hội liên quan.
- Sau đăng ký, ban tổ chức sẽ liên hệ qua email về bước tiếp theo và quyền truy cập RNGD.

## 3. Vòng 1 — Kernel Optimization

### 3.1. Phạm vi tối ưu

Ba kernel decoder-layer khai báo trong `src/ops.rs`; mỗi kernel được đo như **một lần gọi**:

1. `ops::sliding_project_qkv`
   - RMSNorm;
   - Q/K/V projection;
   - Q/K RMSNorm;
   - RoPE;
   - ghi K/V vào ring cache.
2. `ops::sliding_attention_output`
   - head broadcast;
   - O projection;
   - post-attention RMSNorm;
   - residual add.
3. `ops::decoder_feedforward`
   - RMSNorm;
   - GeGLU MLP;
   - post-feed-forward RMSNorm;
   - residual add;
   - layer gate.

Các kernel dùng trọng số lượng tử hóa và tensor layout hiện có của mô hình.

### 3.2. Nguồn chấm chính thức

- Grading server chuyên dụng chạy `tests/test_kernels.rs` của skeleton trên mỗi submission.
- File test này là **source of truth** cho correctness và hiệu năng kernel của Stage 1.
- Test kiểm tra theo thứ tự:
  1. **Buildability:** phần code được phép sửa phải compile với toolchain cuộc thi.
  2. **Correctness:** cả ba kernel phải đạt tolerance công bố.
  3. **Performance:** báo số cycle thực trên RNGD cho từng kernel.
- Correctness là hard gate: nếu fail một kiểm tra correctness bắt buộc thì submission
  không nhận performance credit, dù chạy nhanh hơn.

### 3.3. Tolerance correctness

| Kernel | Absolute tolerance (`atol`) | Relative tolerance (`rtol`) |
|---|---:|---:|
| `sliding_project_qkv` | `0.04` | `1e-2` |
| `sliding_attention_output` | `0.05` | `1e-2` |
| `decoder_feedforward` | `0.01` | `1e-2` |

### 3.4. Hợp đồng skeleton — bắt buộc

1. **Không đổi tên hoặc signature của bất kỳ hàm `#[device]` nào.** Tên, tham số, kiểu
   tham số và kiểu trả về đều thuộc hợp đồng evaluator.
2. Chỉ các thay đổi sau được đưa vào đánh giá:
   - mọi thay đổi trong `src/device/`;
   - phần thân hàm trong `src/ops.rs`, `src/ops_vision.rs`, `src/ops_audio.rs`.
3. Các thay đổi trong những nơi sau **bị bỏ qua khi chấm**:
   - `src/axes.rs`;
   - `src/host/`;
   - `src/api/`;
   - `src/bin/`;
   - `src/lib.rs`;
   - `tests/`.
4. Phải giữ `src/ops.rs`, `src/ops_vision.rs`, `src/ops_audio.rs` ở crate root. Tên kernel
   đã compile chứa `module_path!()`, nên di chuyển các module này sẽ đổi tên kernel và phá
   công cụ chấm.
5. Code dùng chung có thể tác động nhiều đường chạy. Đặc biệt
   `device/shared/rmsnorm.rs` và `device/shared/mlp.rs` còn được dùng bởi full attention,
   vision và audio; phải kiểm tra tác động của thay đổi shared trước khi đo kết quả.

### 3.5. Các quy định Stage 1 chưa được công bố (TBD)

- URL grading server và cách xác thực.
- Định dạng submission archive và lệnh submission.
- Deadline submission và số submission tối đa cho mỗi đội.
- Công thức kết hợp cycle count của ba kernel.

Lưu ý: trang chính hiện ghi thời gian vòng Kernel Optimization là 01–25/09/2026, nhưng
README vẫn đánh dấu **submission deadline** chi tiết là TBD. Không tự suy diễn rằng 25/09
là deadline kỹ thuật cuối cùng cho tới khi ban tổ chức xác nhận.

## 4. Vòng 2 — Model Optimization / End-to-End

- Người có kết quả cao nhất ở vòng Kernel Optimization được vào vòng Model Optimization.
- Phạm vi: toàn bộ đường phục vụ **Gemma-4-12B-it E2E**, ngoại trừ public API endpoint
  trong `src/api/`.
- Phạm vi bao gồm:
  - thực thi mô hình;
  - host orchestration;
  - tokenization;
  - tiền xử lý ảnh và âm thanh;
  - tích hợp runtime.
- Các thông số Stage 2 vẫn **TBD**:
  - số lượng benchmark input, độ dài prompt và độ dài output;
  - số lần lặp benchmark và cấu hình RNGD;
  - ngưỡng correctness và metric hiệu năng E2E;
  - deadline submission, công thức điểm và quy tắc tie-break.

## 5. Chính sách chấm và xếp hạng chung

- Mọi submission phải pass correctness trước khi được xếp hạng hiệu năng.
- Stage 1 đo cycle count thực trên RNGD cho từng kernel bằng official evaluation.
- Stage 2 E2E metric hiện chưa công bố.
- **Schedule makespan chỉ là metric hỗ trợ phát triển**, không thay thế kết quả chấm chính thức.
- Các giá trị sau vẫn TBD:
  - performance metric và weighting;
  - cách xử lý run fail hoặc timeout;
  - yêu cầu/tác động của reproducibility và code review.
- README chưa công bố score formula và tie-break rule hoàn chỉnh.

## 6. Quy trình chuẩn bị, kiểm tra và nộp

### 6.1. Tạo public fixture

Nếu thiếu `ref/fixtures.safetensors`, chạy một lần:

```sh
python3 scripts/generate_references.py
```

- Fixture chứa expected outputs và checksums.
- Input được sinh deterministic từ PRNG dùng chung ở Python và Rust.

### 6.2. Kiểm tra trên RNGD công khai

```sh
./scripts/rngd_test.sh
```

- Script build test binary, gửi qua RNGD scheduler, rồi báo accuracy và cycle count thực.
- `--no-build`: dùng lại binary mới nhất.
- `--no-wait`: gửi job và thoát mà không chờ kết quả.
- Cần cấu hình Arena CLI và chạy `rngd login` trước.
- Với RNGD cục bộ có thể dùng:

```sh
./scripts/local_test.sh
```

### 6.3. Nộp bài

- Trang chính yêu cầu nộp theo hướng dẫn trong README baseline.
- Tuy nhiên tại commit đã chụp, định dạng archive, submission command, URL/auth server,
  deadline kỹ thuật và quota submission đều đang TBD; vì vậy chưa có quy trình nộp hoàn chỉnh.
- Submission pass correctness sẽ được xếp theo performance trên leaderboard.

## 7. Môi trường và toolchain được hỗ trợ

- Môi trường phát triển: **x86_64 Ubuntu 22.04 hoặc mới hơn**.
- Yêu cầu **GLIBC 2.34 hoặc mới hơn**.
- Các lệnh cài đặt được baseline công bố:

```sh
sudo apt install build-essential libclang-dev
sudo apt install gcc-aarch64-linux-gnu

rustup toolchain install nightly-2026-05-01
cargo +nightly-2026-05-01 install cargo-binstall
cargo +nightly-2026-05-01 binstall cargo-furiosa-opt
cargo install furiosa-schedule-viewer

cargo binstall furiosa-arena-cli
rngd login
```

- Lệnh scheduler phục vụ troubleshooting:

| Lệnh | Mục đích |
|---|---|
| `rngd submit <file>` | Gửi script hoặc binary |
| `rngd status <id>` | Xem trạng thái job |
| `rngd logs <id> --follow` | Theo dõi log job |
| `rngd list` | Liệt kê job |
| `rngd cancel <id>` | Hủy job đang chờ hoặc đang chạy |

## 8. Workflow tối ưu được ban tổ chức hướng dẫn

1. Dump schedule riêng từng kernel, ví dụ:

   ```sh
   mkdir -p target/schedules
   cargo furiosa-opt compile ops::sliding_project_qkv --exact \
       --dump-schedule target/schedules/sliding_project_qkv.json
   ```

   - Các cờ `--dump-*` là single-kernel; dump từng kernel một.
   - Phải dùng `--exact` vì positional filter mặc định là substring. Ví dụ
     `ops::sliding_attention` cũng match `ops::sliding_attention_output` nếu không exact.
   - Các dump khác: `--dump-visa`, `--dump-ir`, `--dump-dfg`, `--dump-graph`,
     `--dump-summary` (nhận directory thay vì file).
2. Mở `furiosa-schedule-viewer` (mặc định `127.0.0.1:9254`), nạp JSON và xem node,
   lifetime, context, source location, cycle range hoặc brush theo địa chỉ bộ nhớ.
3. Tìm bottleneck theo context:
   - `DmaEngine`: di chuyển weight/activation;
   - `SubContext`: staging/preload register file;
   - `MainContext` / `VectorEngine`: vector compute như softmax, RMSNorm, cast.
   - `MainContext` và `SubContext` tranh chấp Tensor Unit pipeline, nên overlap có giới hạn.
   - Với DMA cần xem cả `util`; truy cập phân vùng, strided, không liên tục, alignment và
     HBM bank conflict có thể gây tốn kém.
4. Chọn đòn bẩy phù hợp: execution-engine path; tile/split shape; hoặc mapping, padding,
   transfer boundary.
5. Dump lại, giữ các JSON cũ để tái lập so sánh, ghi nhận context thống trị mới, rồi xác
   nhận thay đổi có triển vọng bằng `./scripts/rngd_test.sh`.
- Không được báo cải thiện cycle nếu không có schedule comparison tái lập được hoặc bằng
  chứng RNGD được ghi riêng.

## 9. Lịch chính thức đang hiển thị

| Hạng mục | Thời gian |
|---|---|
| Registration Period | **2026-09-01 – 2026-09-15** |
| Kernel Optimization Round | **2026-09-01 – 2026-09-25** |
| Finalists Announcement | **2026-09-30** |
| Model Optimization Round | **2026-10-01 – 2026-10-25** |
| Award Ceremony | **2026-11-01**; giờ và địa điểm cụ thể TBA |

- Lễ trao giải diễn ra tại MOA Workshop, MICRO 2026, Athens, Greece.

## 10. Giải thưởng và nghĩa vụ hiện diện

| Hạng | Giải thưởng |
|---|---:|
| 1 | **€5,000** |
| 2 | **€3,000** |
| 3 | **€2,000** |

- Người thắng cuộc **phải tham dự trực tiếp** lễ trao giải tại Athens.
- Trang chưa nêu chi tiết thuế, chi phí đi lại/lưu trú, cách chia giải cho đội hoặc điều
  kiện chi trả; không nên tự giả định các khoản này được tài trợ.

## 11. Tutorial, hỗ trợ và liên hệ

- Ban tổ chức đang chuẩn bị tutorial session; ngày và chi tiết chưa công bố.
- Câu hỏi kỹ thuật: dùng **FuriosaAI forums** để câu trả lời được chia sẻ với mọi người.
- Câu hỏi cá nhân: `moa2026.competition@gmail.com`.

## 12. Nguồn chính thức đã kiểm tra

- Trang cuộc thi: <https://micro2026-moa.github.io/>
- Bản source website đã khóa theo commit nằm trong `official-site-snapshot/`.
- FAQ (last modified hiển thị: `2026-09-09`):
  <https://micro2026-moa.github.io/faq.html>
- Form đăng ký:
  <https://docs.google.com/forms/d/e/1FAIpQLScOBksLrh4AW5ApaWLEEAdY1pXb4nwV6N1_DFuDWO8kCRc_4A/viewform>
- Baseline/competition guide:
  <https://github.com/HoseongLee/furiosa-opt-gemma4-12B>
- Bản repository baseline đã khóa theo commit nằm trong `baseline/`.
- Tài liệu `furiosa-opt`: <https://developer.furiosa.ai/furiosa-opt/book/>
- FuriosaAI Arena: <https://arena.furiosa.ai/>
- FuriosaAI forums: <https://forums.furiosa.ai/>

## 13. Những điểm bắt buộc phải theo dõi cập nhật

Danh sách này không phải suy đoán; đây là các mục chính nguồn hiện ghi TBD/TBA hoặc chưa nêu:

- tutorial date/details;
- grading server URL và authentication;
- submission archive format và submission command;
- deadline submission kỹ thuật và quota submission mỗi đội;
- công thức gộp cycle count Stage 1;
- toàn bộ benchmark configuration, correctness threshold, metric và repetitions Stage 2;
- Stage 2 deadline submission, score formula và tie-break;
- policy cho fail/timeout;
- reproducibility/code-review rule;
- giờ và venue cụ thể của lễ trao giải;
- số lượng finalist/đội được vào vòng 2 (nguồn chỉ nói “top performers/highest results”);
- chính sách tài trợ đi lại/lưu trú, thuế và chia giải theo đội.

Khi ban tổ chức cập nhật website hoặc repository, cần đối chiếu lại hồ sơ này với commit và
ngày chụp ở đầu tệp trước khi dùng làm căn cứ cuối cùng.
