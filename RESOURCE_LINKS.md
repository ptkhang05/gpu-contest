# Kiểm tra các resource chính thức

> Kiểm tra ngày 2026-09-08 (Asia/Saigon). Trạng thái website và nội dung “latest” có thể
> thay đổi; luôn đối chiếu lại trước khi chốt kế hoạch hoặc nộp bài.

## Resource chính trên trang cuộc thi

| Resource | Trạng thái truy cập | Nội dung và giá trị sử dụng |
|---|---|---|
| [Baseline repository](https://github.com/HoseongLee/furiosa-opt-gemma4-12B) | HTTP 200; đã clone | Competition skeleton và competition guide. README là nguồn chính cho scope, code được phép sửa, tolerance, test và toolchain. Bản cục bộ nằm trong `baseline/`, commit `4bf1bac714d8bb9e3b8639e450a0c69d5aee93ba`. |
| [Programming Tensor Contraction Processors](https://developer.furiosa.ai/furiosa-opt/book/) | HTTP 200 | Sách lập trình `furiosa-opt`/vISA: setup, mapping, moving tensors, compute engines, scheduling, tuning và tools. Tài liệu tự ghi đây là alpha/experimental build; `furiosa_opt_std` rustdoc là API source có thẩm quyền cho release đã xuất bản. |
| [FuriosaAI Arena](https://arena.furiosa.ai/) | HTTP 200 | Trang SPA có tiêu đề `RNGD Job Scheduler`. Nội dung công khai không hiển thị workflow nếu chưa có quyền/phiên đăng nhập. Quyền Arena được ban tổ chức cấp cho người đã đăng ký; thao tác CLI dùng `rngd`. |

## Các link kỹ thuật được baseline dẫn tới

| Link | Trạng thái | Ghi chú |
|---|---|---|
| [`furiosa_opt_std` API](https://docs.rs/furiosa-opt-std/latest/furiosa_opt_std/) | HTTP 200 | Rust API docs cho tensor types, mapping expressions và engine modules. Dùng để xác minh signature/API thay vì suy đoán từ ví dụ. |
| [`furiosa-arena-cli`](https://github.com/kreatinj/furiosa-arena-cli#installation) | HTTP 200 | Hướng dẫn cài CLI Arena. Baseline chỉ dẫn `cargo binstall furiosa-arena-cli`, sau đó `rngd login`. |
| [Kernel Optimizer](https://developer.furiosa.ai/furiosa-opt/book/tools/kernel-optimizer.html) | HTTP 200 | Tham chiếu đầy đủ cho `cargo furiosa-opt`, compile trực tiếp và các cờ dump schedule/vISA/IR/DFG/graph/summary. |
| [Kernel Validation](https://developer.furiosa.ai/furiosa-opt/book/quick-start/kernel-validation.html) | HTTP 200 | Phân biệt compile validity, correctness bằng oracle, chạy NPU thật và schedule tĩnh. Schedule makespan không tự nó là throughput measurement. |
| [Contraction Engine](https://developer.furiosa.ai/furiosa-opt/book/computing-tensors/contraction-engine/index.html) | HTTP 200 | Giải thích Broadcast–Multiply–Reduce, TRF, main/sub context và giới hạn mapping liên quan contraction. |

## Link hỗ trợ và bối cảnh

| Link | Trạng thái | Ghi chú |
|---|---|---|
| [FuriosaAI forums](https://forums.furiosa.ai/) | HTTP 200 | Discourse công khai; có các chủ đề `rngd`, `sdk`, `furiosa-opt`, profiling và lỗi compiler. Đây là kênh ban tổ chức khuyến nghị cho câu hỏi kỹ thuật để câu trả lời được chia sẻ chung. |
| [RNGD product page](https://furiosa.ai/rngd) | HTTP 200 | Trang giới thiệu phần cứng RNGD. Dùng làm bối cảnh sản phẩm; không thay thế competition guide hoặc evaluator. |
| [MOA Workshop overview](https://www.ai-bmt.com/micro2026-MOA/overview) | HTTP 200 | Trang workshop xác nhận MOA lần thứ 2, chủ đề heterogeneous AI architectures, benchmarking và optimization; có danh sách ban tổ chức và bối cảnh workshop. |
| [Registration form](https://docs.google.com/forms/d/e/1FAIpQLScOBksLrh4AW5ApaWLEEAdY1pXb4nwV6N1_DFuDWO8kCRc_4A/viewform) | HTTP 200 | Form đăng ký đang hoạt động. Các trường và consent đã được chép đầy đủ trong `YEU_CAU_CUOC_THI.md`. |

## Thứ tự nên đọc khi bắt đầu

1. `YEU_CAU_CUOC_THI.md` — hợp đồng và các mục TBD/TBA đã tổng hợp.
2. `baseline/README.md` — nguồn chấm và giới hạn thay đổi.
3. `baseline/OPTIMIZATION.md` — workflow dump schedule, chẩn đoán và đo lại.
4. `baseline/tests/test_kernels.rs` — source of truth Stage 1 cho fixture và tolerance.
5. Sách `furiosa-opt`, ưu tiên Quick Start → Mapping/Moving/Computing → Scheduling → Tools.
6. `furiosa_opt_std` API docs khi cần xác minh API cụ thể.
7. Arena CLI và forum khi tài khoản thi đã được cấp.

## Giới hạn truy cập hiện tại

- Arena chỉ trả về shell của ứng dụng scheduler khi chưa có tài khoản/phiên đăng nhập;
  chưa thể xác nhận queue, quota hoặc endpoint riêng của cuộc thi.
- Những thông số submission và scoring được README đánh dấu TBD vẫn chưa xuất hiện trong
  các resource công khai đã kiểm tra.
- Không có bằng chứng công khai trong các link trên về tài trợ chuyến đi, quota submission,
  số finalist hoặc công thức tính điểm cuối cùng.
