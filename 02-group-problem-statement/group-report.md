# 02 — Group Problem Statement (Bản nộp nhóm)

> Làm chung 1 bản, mỗi thành viên copy vào repo cá nhân. Đi theo Phase 3 → 6 trong `01-worksheet.md`. Nhóm chọn candidate problem ở Phase 3 và tiếp tục validate + vẽ workflow trước khi chốt Problem Statement cuối.

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm (VD: facilitator, workflow, research, writer) |
|-----|-----------|-------------|---------------------------------------------------------------|
| 1   | Nguyễn Trọng Minh | 2A202602496 | Team Lead, Research, Writer, Presenter |
| 2   | Lê Mạnh Cường | 2A202602604 | Research, Workflow |
| 3   | Lại Bá Quân | 2A202602495 | Facilitator, Research |
| 4   | Trần Quốc Khánh | 2A202602824 | Facilitator, Workflow |
| 5   | Nguyễn Trần Nhựt Nam | 2A202602981 | Facilitator, Research, Writer |

**Candidate problem nhóm chọn (1 câu):**

```text
Vinhomes Resident Amenity Booking Bot / Script Exploit: Cư dân phản ánh rằng các slot tiện ích thể thao khan hiếm trên Vinhomes Resident có thể bị công cụ tự động chiếm trước người dùng thông thường và được bán lại, tạo ra bài toán công bằng trong phân bổ slot; root cause kỹ thuật thực tế vẫn cần được xác minh bằng booking logs.
```

---

## Phase 3 — Group Convergence: từ 9-12 candidates về 1

### 3.1. Trình bày top 3 mỗi người (mỗi candidate 1-2 phút)

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh của nhóm |
|---|---|---|---|---|---|
| 1 | Nguyễn Trọng Minh | VinFast EV 12V Battery & Software Diagnostic Delay | Chủ xe VinFast & kỹ thuật viên xưởng dịch vụ | Kỹ thuật viên phải đọc DTC và đối soát thủ công lỗi phần mềm với tình trạng sụt áp ắc quy 12V, kéo dài thời gian chẩn đoán | Tác động trực tiếp đến sản phẩm cốt lõi, impact tài chính rõ và workflow dễ đo lường |
| 2 | Nguyễn Trọng Minh | Vinhomes Resident Amenity Booking Bot Exploit & Slot Scalping | Cư dân Vinhomes & Bộ phận IT/BQL Vinhomes | Hệ thống booking có thể chưa phân biệt tốt request tự động với người dùng thật, tạo điều kiện cho automation chiếm slot | Pain trực tiếp, liên quan tính công bằng, CSAT và niềm tin; có thể đo bằng booking logs |
| 3 | Nguyễn Trọng Minh | Vinmec Private Insurance Guarantee Waiting Queue | Bệnh nhân có bảo hiểm tư nhân & nhân viên bảo hiểm/thu ngân Vinmec | Nhập liệu, kiểm tra điều kiện bảo hiểm và chờ phản hồi khiến thời gian xử lý kéo dài 15–45 phút | Bottleneck rõ, có số đo thời gian cụ thể và tiềm năng tự động hóa |
| 4 | Lê Mạnh Cường | Nhân viên CSKH phải tiếp nhận và xử lý số lượng lớn tin nhắn, cuộc gọi | Nhân viên CSKH | Khối lượng tin nhắn/cuộc gọi lớn; phân loại và trả lời lặp lại | Actor và tần suất có thể đo bằng log; cần thêm dữ liệu về thời gian xử lý và tỷ lệ câu hỏi lặp lại |
| 5 | Lê Mạnh Cường | Người sử dụng xe đạp phải dừng xe, tìm trạm khóa và quét mã để gia hạn lượt thuê | Người thuê xe đạp | Thao tác gia hạn buộc người dùng dừng chuyến, tìm trạm và quét mã | Bối cảnh cụ thể, có thể đo số lần dừng và thời gian; dữ liệu hiện tại chưa đủ để xác định root cause |
| 6 | Lê Mạnh Cường | Nhân viên tại Samsung phải nhập số tài khoản và xác nhận khi thanh toán tại quầy | Nhân viên/khách hàng tại quầy Samsung | Quy trình xác nhận thủ công mất khoảng 35–45 giây/lượt và có hàng đợi | Có số đo trực tiếp, dễ vẽ flow; nhưng có thể giải quyết bằng process fix hơn là AI |
| 7 | Lại Bá Quân | Tự động hóa đối soát & tính lương thưởng team livestream | Leader livestream | Đối chiếu lịch live trên Sheets với file giải ngân đối tác mất khoảng 45 phút/lần và dễ nhầm số liệu | Nghiệp vụ rõ nhưng thiên về Rule/Script; không nhất thiết cần AI |
| 8 | Lại Bá Quân | Chatbot AI ghi chép và tra cứu thu chi cá nhân tức thì qua tin nhắn | Bản thân / sinh viên năm cuối | Ma sát mở Google Sheets và nhập liệu thủ công khoảng 15 phút/ngày | Pain thật; AI có vai trò rõ ở việc bóc tách ngôn ngữ tự nhiên nhưng phạm vi nhỏ |
| 9 | Lại Bá Quân | Trợ lý AI giải đáp thắc mắc tài liệu và quy trình khóa học AI in Action | Học viên 50+ & trợ giảng | Học viên tìm docs rời rạc, TA mất 2–3 giờ/ngày trả lời FAQ lặp lại | Impact rộng nhưng khóa học đã có giải pháp riêng |
| 10 | Trần Quốc Khánh | Phân loại và gán ticket hỗ trợ khách hàng cho đúng phòng ban | Nhân viên Customer Support / các phòng ban nhận ticket | Điểm nghẽn tập trung ở khâu đọc hiểu mô tả ticket | Workflow 4 bước rõ, có metric định lượng và dễ so sánh Rule vs Workflow AI |
| 11 | Trần Quốc Khánh | Nhập liệu và đối soát hóa đơn đầu vào (PDF/ảnh) với sổ phụ ngân hàng và phần mềm kế toán | Nhân viên kế toán | Trích xuất và đối soát thủ công cuối tháng trên 500+ hóa đơn | Impact lớn, workflow rõ, có human boundary tự nhiên; cần kiểm chứng chất lượng OCR với chứng từ khó |
| 12 | Trần Quốc Khánh | Nhân viên mới liên tục hỏi lại câu hỏi về SOP, mẫu biểu hoặc phúc lợi trong nhóm chat chung | Nhân viên mới & HR/đồng nghiệp cũ | Câu hỏi lặp lại 15–20 lần/tuần, làm gián đoạn HR/nhân viên cũ | Pain lặp lại và RAG phù hợp, nhưng chất lượng phụ thuộc độ chuẩn hóa/cập nhật của knowledge base |
| 13 | Nguyễn Trần Nhựt Nam | Quá tải Review Pull Request do lập trình viên dùng AI sinh code quá nhanh | Senior Developer / Tech Lead | PR tạo nhanh hơn khả năng review, có nguy cơ tăng review/rework burden | Có evidence ngành và workflow rõ; cần dữ liệu nội bộ để lượng hóa tỷ lệ AI-generated PR cần rework |
| 14 | Nguyễn Trần Nhựt Nam | PM giao task thiếu ngữ cảnh → developer phải hỏi lại nhiều lần | PM & Developer | Bottleneck ở handoff PM → Dev, nhiều vòng hỏi lại làm task delay/rework | Handoff rõ, dễ đo số vòng trao đổi và tỷ lệ task trễ |
| 15 | Nguyễn Trần Nhựt Nam | Nhân viên văn phòng phải đọc, phân loại email/tin nhắn rồi thủ công tạo TODO | Nhân viên văn phòng | Phân loại và chuyển thông tin thành TODO còn thủ công, lặp lại hàng ngày | Pain có tần suất cao; cần xác định tỷ lệ email thực sự cần phân loại phức tạp |

> **Ghi chú:** File Top3P có tổng cộng 15 candidate (3 của mỗi 5 thành viên), dù template ban đầu chỉ có 12 dòng. Nhóm giữ toàn bộ candidate để không làm mất thông tin đầu vào.

### 3.2. Gom trùng / cluster (gom ý thành 4 cụm)

| Cluster | Candidates included | Pattern chung | Ghi chú |
|---|---|---|---|
| **A — Customer / Operations Automation** | #1, #3, #4, #10, #12, #13 | Khối lượng thao tác/triage/review lặp lại, có thể chuẩn hóa bằng workflow | Phù hợp để so sánh Rule và Workflow/AI |
| **B — Resource / Transaction Fairness** | #2, #5, #6 | Người dùng gặp ma sát hoặc cạnh tranh khi thực hiện một giao dịch/dịch vụ có giới hạn | #2 nổi bật vì pain liên quan tài nguyên khan hiếm và fairness |
| **C — Finance / Back-office Automation** | #7, #11 | Đối soát, nhập liệu và xử lý dữ liệu bán cấu trúc | Nhiều case có thể giải bằng Rule/Script trước AI |
| **D — Personal / Knowledge Assistance** | #8, #9, #14, #15 | Tìm kiếm, hỏi-đáp hoặc chuyển thông tin thành hành động | AI có lợi thế ở NLP/RAG/context nhưng phạm vi từng case khác nhau |

### 3.3. Shortlist (giữ 3 bài để so sánh)

| Candidate | Vì sao vào shortlist (2-3 ý) | Rủi ro / điều chưa rõ |
|---|---|---|
| **Vinhomes Resident Amenity Booking Bot / Script Exploit** | 1. Pain trực tiếp về fairness của tài nguyên khan hiếm.<br>2. Có review công khai từ cư dân về “hack” sân và bán lại.<br>3. Có thể xây solution nhiều lớp và đo bằng request/booking logs. | Chưa xác minh root cause là automation, race condition hay allocation logic; chưa có baseline server-side. |
| **Customer Support Ticket Classification & Routing** | 1. Workflow rõ, bottleneck tập trung ở đọc hiểu ticket.<br>2. Có metric định lượng trong candidate report.<br>3. Có human boundary và fallback rõ. | Cần dữ liệu ticket thực để xác nhận distribution và độ khó của case mơ hồ. |
| **Invoice Extraction & Reconciliation** | 1. Impact định lượng lớn.<br>2. Workflow tuần tự và human check rõ.<br>3. Multimodal extraction + deterministic reconciliation là hướng triển khai cụ thể. | Cần kiểm chứng chất lượng trên hóa đơn scan mờ/không chuẩn và dữ liệu sao kê thực tế. |

### 3.4. Score để đồng thuận (chấm 1-5; điểm dưới đây là working score của nhóm)

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **Vinhomes Resident Booking Defense** | 5 | 4 | 4 | 4 | 5 | 5 | 4 | **31/35** |
| **Customer Support Ticket Classification** | 5 | 5 | 4 | 5 | 5 | 5 | 4 | **33/35** |
| **Invoice Extraction & Reconciliation** | 5 | 5 | 4 | 5 | 4 | 5 | 4 | **32/35** |

> *Mặc dù ticket classification có tổng điểm cao hơn, nhóm chọn Vinhomes vì đây là bài toán có tín hiệu pain trực tiếp về fair access, có yếu tố adversarial/automation rõ để test layered defense, và tạo được câu hỏi quan trọng về việc AI có thực sự cần thiết hay không. Điểm số không thay thế quyết định của nhóm; nó là công cụ ép nhóm nói rõ trade-off.*

**Candidate nhóm chọn (1 bài duy nhất):**

```text
Vinhomes Resident Amenity Booking Bot / Script Exploit & Slot Scalping
```

**Vì sao chọn (4-5 câu):**

```text
Đây là bài toán ảnh hưởng trực tiếp đến tính công bằng khi cư dân cạnh tranh để sử dụng một tài nguyên có số lượng slot hữu hạn. App Store có phản ánh trực tiếp từ cư dân về việc sân thể thao bị “hack” và bán lại, đồng thời phía phát triển ứng dụng ghi nhận phản ánh để kiểm tra/xử lý. Bài toán có thể kiểm chứng bằng booking/request logs và có nhiều phương án từ Rule, Workflow đến AI-assisted behavioral risk scoring. Quan trọng hơn, nhóm có thể kiểm tra giả thuyết một cách nghiêm túc: nếu automation không phải nguyên nhân chính thì solution phải chuyển sang allocation/race-condition hoặc policy fix thay vì cố ép AI vào bài toán.
```

**Vì sao KHÔNG chọn các candidate còn lại (mỗi bài 2-3 câu):**

```text
Nhóm không chọn các bài toán VinFast/Vinmec của Nguyễn Trọng Minh vì trong bối cảnh nhóm, hai bài toán này cần access sâu vào dữ liệu kỹ thuật/quy trình nội bộ để validate; Vinhomes có tín hiệu người dùng công khai và dễ thiết kế pilot log-based hơn. Các bài toán CSKH/ticket classification, invoice và onboarding đều có workflow tốt nhưng ít thể hiện được bài toán fairness/adversarial behavior mà nhóm muốn khảo sát; một số còn có thể giải quyết tốt bằng Rule/Script/RAG mà không cần AI phức tạp. Các bài toán vận hành của Lê Mạnh Cường và Lại Bá Quân cũng có feasibility tốt, nhưng nhóm đánh giá Vinhomes phù hợp hơn để chứng minh việc lựa chọn đúng mức công nghệ thay vì mặc định dùng Agent.
```

**Disagreement (nếu có — ai lo gì, chốt ra sao):**

```text
Điểm cần thống nhất lớn nhất là mức độ chắc chắn của claim “bot/script là nguyên nhân”. Nhóm thống nhất không trình bày đây là một fact đã được xác minh server-side; thay vào đó coi đó là hypothesis dựa trên resident reports. Cách chốt là chọn bài toán ở cấp độ “fair access to scarce amenities” và dùng telemetry/booking logs để xác minh root cause trước khi quyết định mức AI.
```

---

## Phase 4 — Quick Validation + Research

### 4.1. Quick validation (ít nhất 1 cách: interview 2-3 người hoặc survey 5-10 người)

| Nguồn | Số người / mẫu | Tín hiệu xác nhận (kèm quote nguyên văn) | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| **Interview** | 2 | "Cảm giác như không thể Book sân trong cả tuần mặc cho khung giờ" | Chưa có | Cần interview thêm cư dân/BQL/IT trước pilot để xác nhận tần suất và root cause |
| **Survey / poll** | Chưa thực hiện | Chưa có dữ liệu survey thật | Chưa có | Sẽ hỏi tần suất gặp “slot biến mất”, mức chấp nhận CAPTCHA và trải nghiệm UI |
| **Log / ticket / review (nếu có)** | App Store reviews, mẫu review không chuẩn hóa | Review ghi nhận việc sân thể thao bị “hack” và bán lại; review khác phản ánh trạng thái còn chỗ ở danh sách nhưng hết khi vào detail. Đây là resident reports, không phải backend proof. [1] | Chưa có server-side evidence để phân biệt bot, race condition, stale state hoặc allocation bug | Hạ mức khẳng định từ “bot exploit đã xác định” xuống “automation/exploit hypothesis cần kiểm chứng bằng logs” |

**Insight sau validation (1-2 câu — pain thật nằm ở đâu):**

```text
Pain đã có tín hiệu từ người dùng: cư dân cảm nhận việc tiếp cận slot không công bằng và có phản ánh về việc slot bị lấy/bán lại. Tuy nhiên, validation hiện tại chưa đủ để kết luận bot là root cause; bước tiếp theo phải là đối chiếu review với request/booking logs để xác định liệu vấn đề nằm ở automation, race condition, trạng thái slot không nhất quán hay allocation policy.
```

Bằng chứng đính kèm (nếu có): App Store review source [1]. Mock survey/interview chưa triển khai.

### 4.2. Research giải pháp đã có (ít nhất 2-3 tools/patterns + 1-2 link kiểm được)

| Nguồn / tool / case | Link | Họ giải quyết bước nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| **AWS WAF Rate-based Rules** | [AWS WAF Rate-based Rules](https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-rate-based.html) | Bảo vệ endpoint khỏi burst/request volume bất thường | Deterministic, dễ audit, latency thấp | Không tự hiểu được hành vi tinh vi nếu attacker phân tán request | Rate limiting phải là lớp nền, không đợi AI |
| **AWS WAF Bot Control** | [AWS WAF Bot Control](https://docs.aws.amazon.com/waf/latest/developerguide/waf-bot-control-use-cases.html) | Bot management, behavioral/fingerprint signals, challenge | Layered mitigation và có thể challenge thay vì block ngay | Có false positive; phụ thuộc tín hiệu và threshold | Dùng behavioral risk scoring như lớp bổ sung cho rules |
| **Google Play Integrity API** | [Google Play Integrity API](https://developer.android.com/google/play/integrity/verdicts) | App/device/request integrity trước khi server xử lý | Cho server thêm context về integrity của app/device | Không phải bot detector hoàn chỉnh và không phủ mọi client/platform | Client/device integrity có thể giảm attack surface trước behavioral model |

**Research takeaway (2-3 câu — nên build gì / không build gì):**

```text
Nên build theo layered defense: eligibility/quota + rate limiting + request/session integrity + transaction-safe slot allocation trước; AI behavioral risk scoring chỉ xử lý các request khó phân loại. Không nên build một AI Agent tự quyết định booking hoặc phụ thuộc duy nhất vào CAPTCHA/AI classifier, vì phần lớn bài toán có thể giải quyết bằng deterministic workflow và server-side transaction controls.
```

> **Lưu ý:** Các metric cụ thể trong solution là target của nhóm, không phải số liệu production đã đo. Các claim kỹ thuật về kiến trúc Vinhomes vẫn là hypothesis cho tới khi có API/server logs.

---

## Phase 5 — Workflow + Problem Statement

### 5.1. Current workflow bản nhóm

Dán workflow hoặc link file: `02-group-problem-statement-workflow.png/pdf/md`

```text
[1. Mở Vinhomes Resident - cư dân] → [2. Chọn tiện ích + slot - cư dân] → [3. Submit booking request - cư dân/app] → [4. Backend kiểm tra/commit slot - hệ thống - BOTTLENECK CẦN XÁC MINH] → [5. Trả kết quả booking - hệ thống] → [6. Cư dân nhận thành công hoặc hết chỗ]
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú (handoff? bottleneck?) |
|---|---|---|---|---|---|
| 1 | Cư dân | Tài khoản + giờ mở booking | Màn hình tiện ích | Theo giờ mở booking; TBD | Không có handoff |
| 2 | Cư dân | Sân + khung giờ | Booking selection | TBD | Không có handoff |
| 3 | Cư dân / App | Booking payload | Server request | TBD | Handoff App → Backend |
| 4 | Backend | Request + slot state | Commit / reject | Chưa có baseline | Bottleneck cần xác minh: anti-automation, integrity, quota, race-condition/atomic commit |
| 5 | Backend/App | Booking decision | Confirmation/error | TBD | Handoff Backend → App |
| 6 | Cư dân | Result | Successful booking / sold out | TBD | Pain xuất hiện ở đây nếu request hợp lệ mất cơ hội |

**Bottleneck chính (2-3 câu):**

```text
Điểm nghẽn cần điều tra là bước server tiếp nhận và phân bổ slot, nơi request tự động và request từ cư dân có thể cùng cạnh tranh cho tài nguyên khan hiếm. Hiện chưa có đủ dữ liệu công khai để khẳng định thiếu rate limiting là root cause; cần log request, booking transaction, slot-state changes và device/session telemetry để tách automation khỏi race condition hoặc allocation bug.
```

### 5.2. Future workflow bản nhóm

Phải nhìn ra 5 thứ: bước nào máy (Rule), bước nào AI, bước nào người, boundary ở đâu, fallback khi AI sai.

```text
[1. Kiểm tra account/quota/session - RULE] →
[2. Rate limit + nonce + integrity check - RULE] →
[3. Behavioral Risk Score - AI, chỉ với case chưa rõ] →
[4. Low risk → allow / Medium → CAPTCHA / High → rate-limit hoặc block] →
[5. Atomic slot reservation + idempotency - RULE/BACKEND] →
[6. Payment/confirmation - hệ thống] →
[7. Monitoring + appeal - người vận hành]

Fallback: Nếu AI không đủ tự tin hoặc unavailable, quay về deterministic controls + step-up verification; không để AI outage làm gián đoạn toàn bộ booking flow.
```

**Before/after impact:**

| Metric | Trước | Sau kỳ vọng | Cách đo |
|---|---:|---:|---|
| **Tổng thời gian** | Chưa có baseline production | p95 decision latency ≤500 ms; không đặt target tổng journey trước khi đo | App/server telemetry |
| **Số bước** | 6 bước logic chính | 7 bước logic do thêm lớp kiểm soát, nhưng low-risk đi thẳng | Workflow instrumentation |
| **Số bước thủ công** | Chưa xác định; low-risk hiện tại không yêu cầu challenge | 0 cho low-risk; 1 challenge cho medium-risk | Challenge logs |
| **Bottleneck chính** | Request admission + slot allocation (hypothesis) | Risk-based admission + atomic reservation | Request/booking traces |
| **Risk mới** | Chưa quantifiable | False positive <1%; model unavailable phải fallback | Risk dashboard + incident logs |

### 5.3. Problem Statement v0 (mỗi field 2-3 câu)

| Field | Nội dung |
|---|---|
| **Actor** | Cư dân Vinhomes sử dụng tiện ích khan hiếm là người chịu pain trực tiếp; BQL/CSKH và IT/Product là owner của trải nghiệm và hệ thống booking. |
| **Workflow** | Cư dân mở app, chọn tiện ích/slot, submit booking và nhận kết quả từ backend. Vấn đề xuất hiện tại thời điểm request cạnh tranh để commit một slot có nguồn cung hữu hạn. |
| **Bottleneck** | Request admission và slot allocation là điểm cần kiểm chứng: hệ thống có thể chưa đủ khả năng phân biệt automation, request bất thường và người dùng hợp lệ, hoặc có vấn đề race condition/stale state. Đây là hypothesis chứ chưa phải kết luận kiến trúc. |
| **Impact** | Cư dân có thể mất cơ hội booking và cảm nhận thiếu công bằng; phản ánh trên App Store còn cho thấy nguy cơ slot bị bán lại. Về vận hành, issue có thể làm tăng ticket khiếu nại và giảm niềm tin vào tính năng booking. [1], [4] |
| **Success Metric** | Pilot mục tiêu: giảm ≥95% automation requests được nhận diện; false-positive rate <1%; booking success rate của resident hợp lệ >90% ở peak window; giảm ≥80% khiếu nại liên quan “bot/hack sân”; p95 risk decision ≤500 ms. Các mục tiêu này cần baseline thực tế trước khi kết luận hiệu quả. |
| **Boundary** | **Làm:** booking endpoint, anti-automation, eligibility, integrity, risk scoring, slot transaction safety và monitoring.<br>**Không làm:** thay đổi toàn bộ chính sách tiện ích, xử lý tranh chấp ngoài hệ thống, xây lại toàn bộ app, hay mặc định dùng AI nếu Rule/Workflow đã đủ. |

**Câu hỏi AI phản biện v0 (nếu có):**
- **Field nào mơ hồ:** Root cause “bot exploit” chưa có server-side proof; time/volume baseline chưa có.
- **Tôi sửa gì:** Đổi framing thành “fair access / booking abuse hypothesis”, bổ sung race-condition/allocation hypothesis và thiết kế pilot đo request/booking telemetry.

---

## Phase 6 — Rule / Workflow / Agent + Decision

### 6.0. Ma trận độ phù hợp (suy nghĩ nhanh, không thay quyết định cuối)

- Độ mơ hồ: [x] Cao (có nhiều root cause có thể đúng) / [ ] Thấp — Vì sao: cùng một triệu chứng “slot biến mất rất nhanh” có thể do automation, concurrency/race condition, stale UI state hoặc allocation policy.
- Độ phức tạp: [x] Cao (3+ bước/nguồn, phụ thuộc nhau) / [ ] Thấp — Vì sao: request admission, risk scoring, challenge, transaction locking và monitoring phụ thuộc nhau.

**Bài toán nhóm nằm ở ô nào:**

```text
Độ mơ hồ cao + Độ phức tạp cao → Workflow + Rule là nền tảng; AI chỉ là lớp hỗ trợ phân loại rủi ro.
```

**Vì sao (2-3 câu):**

```text
Phần lớn quyết định là deterministic: quota, rate limit, integrity, idempotency và atomic slot commit có điều kiện rõ ràng. AI chỉ hữu ích khi tín hiệu hành vi có nhiều chiều và không có ngưỡng rule đơn giản đủ tốt để phân biệt người thật với automation.
```

### 6.1. So sánh Rule / Workflow / Agent (so trên cùng 1 bài)

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? (Dùng cho bước nào?) |
|---|---|---|---|---|
| **Rule** | Quota, rate limiting, cooldown, duplicate detection, request nonce, integrity check, atomic slot locking | Đủ cho phần lớn case rõ ràng | False positive/false negative nếu chỉ dùng tín hiệu đơn lẻ | Có — lớp nền |
| **Workflow** | Rule → risk scoring → allow/challenge/block → slot commit → monitoring/appeal | Đủ để điều phối nhiều bước và nhánh xử lý | Nhiều integration point hơn, cần observability | **Chọn — kiến trúc chính** |
| **Agent** | Agent tự lập kế hoạch, gọi nhiều tool và tự quyết định enforcement | Chỉ hợp lý nếu bài toán cần planning/open-ended tool use | Complexity, khó audit, không cần thiết | Không chọn |

**5 câu hỏi chốt (trả lời câu đầy đủ):**
1. **Rule có giải được 70-80% case không?** Có khả năng cao; các case rõ như vượt quota, burst quá mức, request trùng lặp và integrity fail nên được xử lý bằng rule trước. Cần logs để xác nhận tỷ lệ thực tế.
2. **Các bước có đi thẳng một đường không hay phải rẽ nhánh?** Có rẽ nhánh ở bước risk score: low-risk đi thẳng, medium-risk challenge, high-risk rate-limit/block.
3. **Có thật sự cần Agent tự lập kế hoạch + gọi tool không?** Không. Booking control là workflow có trạng thái và điều kiện rõ, không cần planning tự chủ.
4. **Nếu AI sai, ai phát hiện đầu tiên và sửa trong bao lâu?** Monitoring/CSKH/BQL có thể phát hiện qua spike false positives, complaint và booking-failure rate; threshold/rule phải có owner IT/Product để rollback nhanh. Thời gian xử lý cụ thể cần xác lập trong SLA pilot.
5. **Có hạ được từ Agent → Workflow → Rule không?** Có. Nếu risk scoring không tạo thêm giá trị hoặc gây false positive cao, có thể tắt AI và giữ Rule + Workflow + challenge.

**Mức chọn:**

```text
[Workflow — với Rule là nền tảng và AI là lớp hỗ trợ rủi ro]
```

**Vì sao chọn (3-4 câu):**

```text
Workflow phù hợp vì bài toán có nhiều bước và nhánh nhưng vẫn có logic rõ ràng. Rule xử lý các trường hợp chắc chắn; AI xử lý trường hợp mơ hồ; người dùng được challenge khi risk ở mức trung gian. Kiến trúc này giảm sự phụ thuộc vào AI và giữ được human-safe fallback.
```

**Vì sao không chọn mức đơn giản hơn (2-3 câu):**

```text
Rule-only có thể giải quyết phần lớn abuse đơn giản nhưng có nguy cơ nhầm người dùng thao tác nhanh với automation hoặc bị bypass khi attacker thay đổi hành vi. Cần Workflow để kết hợp nhiều lớp kiểm soát và đưa case mơ hồ sang challenge/AI risk scoring thay vì block thẳng.
```

### 6.2. Problem Statement v1 (v0 sửa chặt hơn + 3 field cuối)

| Field | Nội dung |
|---|---|
| **Actor** | Cư dân Vinhomes là user chính; BQL/CSKH và IT/Product là system/process owner. |
| **Workflow** | Resident selection → eligibility → rate/integrity checks → behavioral risk scoring → allow/challenge/block → atomic slot reservation → confirmation → monitoring/appeal. |
| **Bottleneck** | Booking request admission và slot allocation; root cause thực tế phải được phân biệt giữa automation, race condition, stale state và policy. |
| **Impact** | Mất cơ hội sử dụng tiện ích, giảm cảm nhận công bằng và có thể tăng khiếu nại; App Store đã có resident reports về “hack”/resale của sports slots. [1] |
| **Success Metric** | Automation reaching allocation ≤1%; false-positive challenge <1%; legitimate peak booking success >90%; complaint volume −80%; p95 risk decision ≤500 ms. Tất cả target phải được đo từ baseline server/app logs. |
| **Boundary** (làm / không làm) | **Làm:** booking endpoint controls, behavior risk scoring, challenge, transaction-safe allocation, monitoring.<br>**Không làm:** redesign toàn bộ Vinhomes Resident, đổi policy tiện ích, xử lý tranh chấp ngoài app, hay dùng Agent. |
| **AI intervention point** (can thiệp sau bước nào, trước bước nào) | Sau eligibility/rate/integrity pre-check và trước bước atomic slot reservation. AI chỉ tạo risk score; nó không trực tiếp commit/cancel slot. |
| **Mức chọn** (Rule / Workflow / Agent + 1 câu vì sao) | **Workflow** — Rule xử lý case rõ, AI hỗ trợ case mơ hồ, challenge xử lý uncertainty và backend transaction bảo đảm fairness. |
| **Rủi ro & người thật kiểm tra** (rủi ro lớn nhất + ai kiểm tra bằng cách nào) | Rủi ro lớn nhất là false positive làm mất booking của cư dân hợp lệ. IT/Product owner kiểm tra qua false-positive dashboard, complaint signals và rollback/fallback sang rule + challenge khi threshold/model có vấn đề. |

### 6.3. Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú (câu đầy đủ) |
|---|---|---|
| **Actor + workflow rõ chưa?** | Yes | Actor, request flow, bottleneck và future decision points đã được xác định rõ. |
| **Baseline + metric đo được chưa?** | Not Yet | Target metrics đã có, nhưng baseline request/booking/complaint phải lấy từ production logs. |
| **Data/input đủ dùng chưa?** | Not Yet | Có resident reviews nhưng chưa có server-side request/booking telemetry để xác minh root cause. |
| **AI sai, hậu quả chấp nhận được không?** | Yes, có điều kiện | Không block trực tiếp case borderline; dùng challenge và có fallback rule-only. |
| **Có người review/owner không?** | Yes | IT/Product/BQL là owner của threshold, policy và rollback; CSKH/BQL nhận tín hiệu complaint. |
| **Có cách non-AI đơn giản hơn không?** | Yes | Rule + transaction controls giải quyết phần lớn case; AI chỉ nên thêm sau khi đo được residual ambiguity. |

**Decision:**

```text
[Not Yet — nhưng đủ cơ sở để chạy pilot validation nhỏ]
```

**Lý do (3-4 câu dựa trên bằng chứng):**

```text
Pain của cư dân đã có tín hiệu trực tiếp từ App Store và phù hợp với bài toán tài nguyên khan hiếm, nhưng bằng chứng công khai chưa đủ để xác định bot là root cause. Vì vậy nhóm chưa coi AI anti-bot là một production-ready answer. Quyết định hợp lý là chạy pilot thu thập request/booking telemetry, kiểm tra race condition và allocation behavior, sau đó chỉ bật behavioral risk scoring nếu dữ liệu cho thấy residual automation đủ lớn để biện minh cho AI.
```

**Nếu Go — pilot nhỏ nhất (data nào, chạy tay ra sao, đo 3 số nào):**

```text
Pilot nhỏ nhất: lấy một khung giờ booking có nhu cầu cao và instrument booking endpoint. Thu các trường tối thiểu: account/session ID đã ẩn danh, timestamp/request velocity, slot requested, success/fail result, device/app integrity signals, challenge outcome và duplicate/retry pattern. Chạy rule-based shadow scoring trước khi block bất kỳ ai; đo 3 số: (1) tỷ lệ request nghi automation, (2) false-positive rate của rule/challenge trên cohort người dùng hợp lệ, và (3) booking success rate của người dùng hợp lệ trong peak window. Nếu automation không đáng kể, dừng AI và giữ rule/transaction fix.
```

**Nếu Not Yet — cần validate gì trước:**

```text
1. Lấy booking/server logs để xác định request burst, duplicate/replay, device/session reuse và slot-state transitions.
2. Kiểm tra transaction/locking để loại trừ race condition.
3. Thực hiện survey/interview cư dân và BQL/IT để xác nhận tần suất pain và quy trình xử lý hiện tại.
4. Đo baseline legitimate booking success và complaint volume trước khi thay đổi workflow.
```

**Nếu No-Go — làm gì thay AI:**

```text
Giữ Rule + Workflow: strict rate limiting, quota/cooldown, request nonce/idempotency, app/device integrity check, CAPTCHA step-up và atomic slot reservation. Nếu vấn đề chính là scarcity policy chứ không phải automation, cân nhắc waiting room/lottery/randomized allocation cho peak slots.
```

**Exit / rollback (khi nào dừng AI, quay về cách cũ):**

```text
Dừng behavioral scoring nếu false-positive rate vượt ngưỡng pilot, challenge failure của user hợp lệ tăng bất thường, risk engine gây latency vượt SLA, hoặc log không cho thấy automation đáng kể. Khi đó hệ thống rollback về deterministic rules + step-up verification + transaction-safe booking; không để AI outage làm dừng toàn bộ booking.
```

---

### Self-check nộp phần 02 (nhóm)
- [x] Có nhật ký hội tụ 15 candidates → cluster + shortlist + score
- [x] Có validation interview/survey với quote thật — chưa thực hiện; mới có App Store review evidence và bộ câu hỏi validation
- [x] Có research giải pháp với link kiểm được và không trình bày root cause chưa xác minh như fact
- [x] Có workflow trước/sau, bottleneck, boundary và fallback
- [x] Có PS v0 → v1, metric target + cách đo và boundary làm/không làm
- [x] Có so sánh Rule/Workflow/Agent + Decision Not Yet / pilot validation có lý do

### Nguồn chính dùng cho candidate và solution
- [1] Vinhomes Resident — Apple App Store reviews: [https://apps.apple.com/vn/app/vinhomes-resident/id6450522818?see-all=reviews](https://apps.apple.com/vn/app/vinhomes-resident/id6450522818?see-all=reviews)
- [2] Vinhomes — Kết nối tiện ích với cư dân: [https://vinhomes.vn/vi/cong-dong-vinhomes-center-park](https://vinhomes.vn/vi/cong-dong-vinhomes-center-park)
- [3] Vinhomes Resident — App Store overview: [https://apps.apple.com/vn/app/vinhomes-resident/id6450522818](https://apps.apple.com/vn/app/vinhomes-resident/id6450522818)
- [4] Vinhomes — Quy định xử lý khiếu nại/yêu cầu của khách hàng: [https://gcp-cdn.vinhomes.vn/cms-data/3_VHM_Quy%20dinh%20xu%20ly%20khieu%20nai%20yeu%20cau%20cua%20KH.pdf](https://gcp-cdn.vinhomes.vn/cms-data/3_VHM_Quy%20dinh%20xu%20ly%20khieu%20nai%20yeu%20cau%20cua%20KH.pdf)
- [5] AWS WAF — Rate-based rules: [https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-rate-based.html](https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-rate-based.html)
- [6] AWS WAF Bot Control: [https://docs.aws.amazon.com/waf/latest/developerguide/waf-bot-control-use-cases.html](https://docs.aws.amazon.com/waf/latest/developerguide/waf-bot-control-use-cases.html)
- [7] Google Play Integrity API: [https://developer.android.com/google/play/integrity/verdicts](https://developer.android.com/google/play/integrity/verdicts)
