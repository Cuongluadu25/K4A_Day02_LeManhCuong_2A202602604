# 01 — Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước, dùng AI sau để phản biện. Không copy ví dụ Weekly Report.

## Thông tin cá nhân

- Họ và tên: Lê Mạnh Cường
- Mã học viên: 2A202602604
- Vai trò / bối cảnh (VD: sinh viên năm X, intern PM, ...): Sinh viên mới tốt nghiệp
- Công việc hằng tuần (3-5 gạch đầu dòng để soi problem):
   + Học thêm kiến thức mới
   + Học thêm môn thể thao mới
   + Đi những chỗ mới
---

## Phase 1 — Scan 5+ problems (tối thiểu 5, khuyến khích 8-10)

**Cách điền:** mỗi dòng = việc gì + ai chịu + đo bằng gì. Cột `Dấu hiệu thật` bắt buộc có số: mất bao lâu (bấm giờ mấy lần), mấy lần/tuần, bao nhiêu người gặp, log/ticket/quote nào.

| # | Lăng kính (Lặp lại / Tốn thời gian / AI có thể tốt hơn / Pain từ người khác) | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật (số + bằng chứng) |
|---|---|---|---|---|
| 1 | Lặp lại | Nhân viên CSKH phải tiếp nhận và xử lý số lượng lớn tin nhắn, cuộc gọi | Nhân viên CSKH | Ước tính khoảng 500 tin nhắn/cuộc gọi mỗi ngày, tương đương khoảng 3.000-3.500 lượt mỗi tuần nếu hoạt động 6-7 ngày; cần đối chiếu bằng log hệ thống.|
| 2 | Tốn thời gian | Người sử dụng xe đạp phải dừng xe, tìm trạm khóa và quét mã để gia hạn lượt thuê | Người sử dụng xe đạp | Phải quét QR mỗi 30 phút; chuyến đi 2 giờ cần khoảng 4 lần quét và theo ước tính mất 4-5 phút tổng cộng; cần bấm giờ thêm vài lượt để xác nhận. |
| 3 | AI có thể tốt hơn | Người ở ngoài không biết phòng đang có người ngủ nên gõ cửa nhiều lần | Người ngủ trong phòng và người cần vào phòng | Quan sát thực tế: trong 1 đêm, cô chủ nhà gõ cửa 2 lần khi người bên trong đang ngủ; ghi nhận 5 lần người bên trong bị thức giấc. Cần làm rõ 5 lần này xảy ra trong bao nhiêu đêm. |
| 4 | Tốn thời gian | Người học và nhân viên phải mang thẻ và quẹt thẻ mỗi lần ra vào khuôn viên | Sinh viên, nhân viên thường xuyên ra vào | Một người có thể phải quẹt khoảng 10-20 lần mỗi ngày; cần bổ sung thời gian mỗi lần và số ngày quan sát. |
| 5 | Lặp lại | Nhân viên tại Samsung phải nhập số tài khoản và xác nhận khi thanh toán tại quầy theo yêu cầu bảo mật | Nhân viên mua hàng tại nhà ăn/quầy thanh toán | Bấm giờ tại quầy: mất 35-45 giây/lượt nhập số và xác nhận; giờ ăn trưa hàng đợi kéo dài trên 10 người/quầy. |

> Gợi ý tự soi: tuần trước mất nhiều thời gian nhất vào việc gì? Việc gì hay trì hoãn? Người khác hay hỏi lại câu gì? Workflow nào ai cũng biết là chậm?

**AI đã dùng ở Phase 1 (nếu có):**
- Prompt đã hỏi:
- Ý dùng được:
- Ý bỏ vì không phải pain thật:

**Self-check Phase 1:**
- [ ] Đủ 5+ dòng, mỗi dòng có actor + số đo cụ thể
- [ ] Dùng ít nhất 3/4 lăng kính
- [ ] Không có dòng chung chung kiểu "mất nhiều thời gian"

---

## Phase 2 — Top 3 Problem Cards

### 2.1. Chọn top 3

Giữ bài nào: actor cụ thể, workflow vẽ được 3-7 bước, bottleneck ở 1 bước, impact đo được. Loại bài quá rộng.

| Rank | Problem (copy từ bảng scan) | Vì sao chọn (2-3 ý) | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Nhân viên CSKH phải tiếp nhận và xử lý số lượng lớn tin nhắn, cuộc gọi | Actor rõ, tần suất lớn và có thể đo bằng log; workflow phân loại và trả lời lặp lại, phù hợp để so sánh process/rule/workflow. | Chưa có dữ liệu tách riêng tin nhắn, cuộc gọi, thời gian xử lý và tỷ lệ câu hỏi lặp lại.|
| 2 | Người sử dụng xe đạp phải dừng xe, tìm trạm khóa và quét mã để gia hạn lượt thuê | Bối cảnh và hành động cụ thể; có thể đo số lần dừng, thời gian quét và thời gian chuyến đi; bottleneck nằm ở thao tác gia hạn. | Chưa biết hệ thống có cho phép tự động gia hạn hay không và 4-5 phút đã được bấm giờ chính xác chưa. |
| 3 | Nhân viên tại Samsung phải nhập số tài khoản và xác nhận khi thanh toán tại quầy theo yêu cầu bảo mật | Có số đo trực tiếp 35-45 giây/lượt và hàng đợi trên 10 người; dễ vẽ flow và có phương án process fix không cần AI. | Chưa biết quy định bảo mật bắt buộc đến mức nào và thời gian chờ trung bình của cả hàng đợi. |

### 2.2. Problem Cards chi tiết (lặp lại cho cả 3 cards)

---

#### Problem Card #1 — Xử lý lượng lớn yêu cầu CSKH

```text
Problem 1 câu: Nhân viên CSKH mất nhiều công sức tiếp nhận, phân loại và trả lời khoảng 500 tin nhắn/cuộc gọi mỗi ngày.

Actor: Nhân viên CSKH.

Thời điểm / bối cảnh: Trong mỗi ca trực, đặc biệt khi lượng yêu cầu tăng cao.

Current workflow 3-7 bước:
1. Nhận tin nhắn hoặc cuộc gọi.
2. Đọc/nghe và xác định nhu cầu.
3. Tra cứu thông tin hoặc chính sách.
4. Soạn câu trả lời và gửi hoặc chuyển ca khó.
5. Ghi nhận kết quả xử lý.

Bottleneck: Đọc, phân loại và tra cứu lại thông tin cho các yêu cầu lặp lại.

Impact: Khoảng 500 lượt mỗi ngày tạo tải xử lý lớn và có thể làm tăng thời gian phản hồi.

Success metric: Giảm thời gian xử lý trung vị mỗi lượt và giảm tỷ lệ yêu cầu chờ quá SLA, nhưng cần lấy số liệu nền từ log.

Non-AI alternative: Chuẩn hóa FAQ, macro trả lời và menu phân loại cố định.

AI hypothesis: AI phân loại yêu cầu và gợi ý câu trả lời từ FAQ; nhân viên vẫn duyệt trước khi gửi.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #1** (ASCII / Mermaid / ảnh đính kèm):

```text
CURRENT STATE — chưa có số đo tổng thời gian

[1 nhận yêu cầu] → [2 đọc/nghe] → [3 phân loại + tra cứu: bottleneck] → [4 trả lời] → [5 ghi nhận]

FUTURE STATE — cần đo thử nghiệm trước/sau

[1 AI phân loại] → [2 AI gợi ý từ FAQ] → [3 nhân viên review và gửi]  <-- human boundary

Fallback: nếu AI không chắc hoặc không tìm thấy FAQ, chuyển toàn bộ yêu cầu cho nhân viên xử lý thủ công.
```

File đính kèm (nếu vẽ riêng): `01-individual-problem-scan-workflow-card-1.png`

---

#### Problem Card #2 — Gia hạn lượt thuê xe đạp

```text
Problem 1 câu: Người thuê xe phải dừng lại nhiều lần để quét QR gia hạn, làm gián đoạn chuyến đi.

Actor: Người sử dụng xe đạp.


Thời điểm / bối cảnh: Chuyến đi kéo dài khoảng 2 giờ, trong đó lượt thuê cần gia hạn mỗi 30 phút.


Current workflow 3-7 bước:
1. Đang di chuyển gần hết thời hạn thuê.
2. Tìm nơi có thể dừng và trạm khóa phù hợp.
3. Dừng xe và mở ứng dụng.
4. Quét QR để gia hạn.
5. Tiếp tục hành trình.


Bottleneck: Dừng xe và quét QR lặp lại mỗi 30 phút.


Impact: Chuyến đi 2 giờ cần khoảng 4 lần gia hạn, ước tính mất 4-5 phút và làm gián đoạn hành trình.


Success metric: Giảm số lần dừng và thời gian thao tác gia hạn trên mỗi chuyến; không phát sinh phí quá hạn.

Non-AI alternative: Cho phép bật tự động gia hạn hoặc gia hạn một lần cho toàn bộ chuyến trong giới hạn ngân sách.

AI hypothesis: Workflow tự động nhận biết thời điểm sắp hết hạn, gửi nhắc đúng lúc và thực hiện gia hạn sau khi người dùng xác nhận.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #2:**

```text
CURRENT STATE — khoảng 4-5 phút thao tác trong chuyến 2 giờ

[1 di chuyển] → [2 tìm chỗ/trạm dừng] → [3 mở app + quét QR: bottleneck] → [4 tiếp tục]

FUTURE STATE — mục tiêu giảm còn dưới 1 phút thao tác

[1 nhận nhắc sắp hết hạn] → [2 xác nhận gia hạn] → [3 hệ thống gia hạn + ghi nhận]  <-- human boundary

Fallback: nếu không xác nhận hoặc mạng lỗi, ứng dụng cảnh báo trước hạn để người dùng gia hạn thủ công tại trạm gần nhất.
```

File đính kèm: `01-individual-problem-scan-workflow-card-2.png`

---

#### Problem Card #3 — Nhập thông tin khi thanh toán nội bộ

```text
Problem 1 câu: Nhân viên mất 35-45 giây mỗi lượt để nhập số tài khoản và xác nhận khi thanh toán tại quầy.

Actor: Nhân viên mua hàng tại nhà ăn/quầy thanh toán trong Samsung.

Thời điểm / bối cảnh: Giờ ăn trưa, khi nhiều nhân viên thanh toán liên tiếp và quy định bảo mật vẫn được áp dụng.

Current workflow 3-7 bước:
1. Chọn món và đến quầy.
2. Cung cấp hoặc nhập số tài khoản.
3. Xác nhận thông tin.
4. Chờ giao dịch hoàn tất.
5. Nhận hàng và rời quầy.

Bottleneck: Nhập số tài khoản và xác nhận thủ công ở mỗi giao dịch.

Impact: Mỗi giao dịch mất 35-45 giây; giờ ăn trưa hàng đợi có trên 10 người mỗi quầy.

Success metric: Giảm thời gian thanh toán trung vị xuống dưới 15 giây mà vẫn giữ yêu cầu xác thực; giảm độ dài hàng đợi giờ trưa.

Non-AI alternative: Dùng thẻ nhân viên, QR cá nhân hoặc đăng nhập một lần thay cho nhập số thủ công.

AI hypothesis: Không cần AI; tối ưu quy trình và xác thực bằng token/QR là phù hợp hơn.

Quick gut:
[x] No AI / process fix
[ ] Rule
[ ] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #3:**

```text
CURRENT STATE — 35-45 giây mỗi lượt nhập và xác nhận

[1 chọn món] → [2 nhập số tài khoản: bottleneck] → [3 xác nhận] → [4 chờ giao dịch] → [5 nhận hàng]

FUTURE STATE — mục tiêu dưới 15 giây mỗi lượt

[1 quét thẻ/QR] → [2 xác thực tự động] → [3 nhân viên nhận kết quả]  <-- human boundary: hệ thống không tự giao hàng khi xác thực lỗi

Fallback: nếu thẻ/QR lỗi, nhân viên nhập số tài khoản thủ công và xác nhận như quy trình hiện tại.
```

File đính kèm: `01-individual-problem-scan-workflow-card-3.png`

---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card tôi muốn pitch nhất:**

```text
Card #3 — Nhập thông tin khi thanh toán nội bộ
```

**Vì sao (2-3 câu: workflow gì, số đo gì, impact gì):**

```text
Workflow ngắn, số đo trực tiếp và giải pháp process fix rõ ràng: thay nhập số bằng thẻ hoặc QR có thể giảm 35-45 giây mỗi giao dịch mà không cần AI. Đây là bài dễ kiểm chứng bằng bấm giờ và đo hàng đợi trước/sau.
```

**Câu hỏi tôi muốn nhóm challenge (1-2 câu hỏi đúng chỗ yếu):**

```text
Quy định bảo mật có cho phép dùng thẻ hoặc QR thay nhập số tài khoản không? 35-45 giây là thời gian nhập và xác nhận hay đã bao gồm toàn bộ thời gian thanh toán?
```

**AI phản biện Card (nếu có):**
- Điểm yếu AI chỉ ra: Bằng chứng của một số problem mới là quan sát/ước tính; chưa đủ log hoặc nhiều lần bấm giờ để khẳng định quy mô.
- Tôi sửa gì: Ghi rõ nguồn của từng con số, đánh dấu giả định cần kiểm chứng và không ép dùng AI cho bài thanh toán.

### Đánh giá và chỉnh sửa Phase 1

Phase 1 **đạt yêu cầu tối thiểu về hình thức**: có 5 problems và dùng 4 lăng kính, trong đó có ít nhất 3 lăng kính khác nhau. Tuy nhiên, để được xem là chuẩn xác hơn, cần lưu ý:

- Dòng #1 đang trộn “tin nhắn” và “cuộc gọi”; cần lấy log để xác nhận 500 lượt/ngày và số ngày hoạt động.
- Dòng #2 có số lần quét và tổng thời gian nhưng câu bằng chứng bị dang dở; cần bấm giờ thêm vài chuyến.
- Dòng #3 ghi 2 lần gõ cửa nhưng 5 lần bị thức giấc; cần ghi rõ 5 lần xảy ra trong bao nhiêu đêm và ai là actor chính.
- Dòng #4 có ước tính 10-20 lần/ngày nhưng chưa có thời gian mỗi lần và số ngày quan sát.
- Dòng #5 là dòng mạnh nhất vì có bấm giờ và số người trong hàng đợi; nên gọi là vấn đề quy trình/bảo mật, không mặc định là bài toán AI.

### Self-check nộp phần 01
- [x] Có 5+ problems + top 3 Cards đủ field
- [x] Mỗi Card có workflow trước/sau + bottleneck + metric + fallback
- [x] Đã chọn 1 card pitch + câu hỏi challenge
