# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Lê Mạnh Cường
- Mã học viên: 2A202602604
- Nhóm: AIBC-ZoneB
- Candidate problem nhóm chọn:
Vinhomes Resident Amenity Booking Bot / Script Exploit: Cư dân phản ánh rằng các slot tiện ích thể thao khan hiếm trên Vinhomes Resident có thể bị công cụ tự động chiếm trước người dùng thông thường và được bán lại, tạo ra bài toán công bằng trong phân bổ slot; root cause kỹ thuật thực tế vẫn cần được xác minh bằng booking logs.

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Tôi đã scan 5 problem từ các bối cảnh CSKH, thuê xe đạp, sinh hoạt trong phòng, ra vào khuôn viên và thanh toán tại quầy. Tôi chọn top 3 dựa trên actor, workflow, bottleneck và số đo, đồng thời ghi rõ các số liệu nào mới là quan sát/ước tính cần kiểm chứng. | Cung cấp cho nhóm các candidate có actor và cách đo tương đối cụ thể; card mạnh nhất của tôi là bài thanh toán nội bộ tại Samsung. |
| Pitch Problem Card | Tôi pitch Card #3 về việc nhập số tài khoản và xác nhận thanh toán tại quầy, với thời gian 35–45 giây/lượt và hàng đợi trên 10 người vào giờ ăn trưa. Tôi đề xuất process fix bằng thẻ hoặc QR thay vì mặc định dùng AI. | Nhóm có thêm một case có số đo trực tiếp và thấy rõ rằng một problem có thể giải bằng process fix, không cần Agent. |
| Challenge bài của bạn khác | Tôi tập trung hỏi về nguồn của các con số, cách phân biệt pain thật với giả định và liệu giải pháp có thực sự cần AI hay không. Với bài Vinhomes, điểm tôi lưu ý là chưa thể coi bot/script là root cause nếu chưa có server-side logs. | Nhóm hạ mức khẳng định từ “bot exploit đã xác định” xuống hypothesis cần kiểm chứng, đồng thời bổ sung các khả năng race condition, stale state và allocation policy. |
| Gom trùng / cluster | Tôi tham gia gom các candidate vào các nhóm Customer/Operations, Resource/Transaction Fairness, Finance/Back-office và Personal/Knowledge Assistance. | Việc cluster giúp nhóm so sánh các bài theo pattern chung thay vì chỉ chọn theo cảm nhận cá nhân. |
| Chọn candidate problem |Tôi đã tham gia vào việc chọn candidate problem | Nhóm tôi đã nhất trí đồng ý với candidate problem đó |
| Validation / research | Tôi cùng nhóm đọc resident reports trên App Store và đối chiếu với các giải pháp chính thức như AWS WAF Rate-based Rules, AWS WAF Bot Control và Google Play Integrity API. Tôi chú ý ghi rõ rằng review chỉ là tín hiệu từ người dùng, không phải bằng chứng backend. | Nhóm chọn hướng layered defense và không phụ thuộc duy nhất vào AI; các nguồn research được đưa vào phần research của báo cáo nhóm. |
| Workflow nhóm | Tôi tham gia mô tả current workflow từ mở app, chọn slot, gửi request đến backend commit/reject. Ở future workflow, tôi cùng nhóm đặt Rule ở eligibility, rate limit, nonce, integrity và atomic reservation; AI chỉ chấm risk cho case chưa rõ. | Workflow có bottleneck, handoff App → Backend, AI intervention point, human boundary và fallback rule-only rõ hơn. |
| Problem Statement | Tôi góp phần làm rõ bottleneck không chỉ là “bot chiếm slot” mà còn có thể là race condition, stale state hoặc allocation policy. Tôi cũng kiểm tra boundary để không mở rộng thành việc xây lại toàn bộ ứng dụng. | Problem Statement v0/v1 giữ được tính thận trọng, có metric target nhưng ghi rõ cần baseline từ production logs. |
| Rule / Workflow / Agent | Tôi đồng ý với kết luận Workflow là kiến trúc chính, Rule là nền tảng và AI chỉ hỗ trợ phân loại rủi ro. Tôi không chọn Agent vì booking control có điều kiện và trạng thái rõ, không cần planning tự chủ. | Nhóm có lập luận hạ cấp được từ AI về Rule + challenge nếu AI không tạo thêm giá trị hoặc gây false positive. |
| Decision | Tôi ủng hộ quyết định Not Yet: chạy pilot telemetry và shadow scoring trước khi block người dùng. | Quyết định cuối không biến resident reports thành kết luận kỹ thuật, đồng thời xác định rõ dữ liệu cần lấy và điều kiện rollback. |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Hai phần có dấu tay rõ nhất của tôi là current/future workflow và cách nhóm đặt boundary cho AI. Tôi góp phần giữ cho bài toán không bị đóng khung sớm là “bot exploit”, mà chuyển thành bài toán fair access cần kiểm chứng bằng request, booking và slot-state telemetry.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Không dùng AI để tạo danh sách ban đầu; tôi tự quan sát và ghi 5 problem trước. | Giúp tôi kiểm tra lại cách nhìn theo actor, workflow và metric khi rà soát bài. | AI có thể gợi ý các ý tưởng nghe hợp lý nhưng không phải pain tôi đã trải nghiệm. | Tôi giữ các problem có dấu hiệu cụ thể như 35–45 giây/lượt, hàng đợi trên 10 người hoặc số lần thao tác; đánh dấu các số ước tính cần đo thêm. |
| Problem Card | Không dùng AI để viết thay card hoặc pitch. | Việc tự viết giúp tôi xác định non-AI alternative rõ hơn. | Nếu chỉ nhìn vào “có thể dùng AI”, tôi dễ bỏ qua khả năng process fix là đủ. | Tôi chọn bài thanh toán Samsung để pitch và nêu rõ giải pháp thẻ/QR, không ép dùng AI. |
| Workflow | Không dùng AI để quyết định workflow; nhóm tự vẽ và kiểm tra từng bước. | Có thể dùng cách trình bày dạng ASCII để làm flow dễ đọc hơn. | Một workflow do AI gợi ý có thể tự giả định API, telemetry hoặc quyền backend mà nhóm chưa có. | Tôi giữ các nhãn “TBD”, “hypothesis” và yêu cầu kiểm tra request/booking logs trước khi kết luận. |
| Research | Tôi dùng các link chính thức trong báo cáo nhóm để kiểm tra pattern rate limiting, bot control và app/device integrity. | Research giúp nhóm biết Rule và transaction controls nên đứng trước AI. | Không thể lấy claim của công cụ thành bằng chứng rằng Vinhomes đang có đúng kiến trúc đó. | Tôi tách rõ “bài học có thể áp dụng” khỏi “sự thật production của Vinhomes”, và giữ nguồn chính thức. |
| Problem Statement | Không dùng AI viết thay phần kết luận cá nhân; tôi cùng nhóm rà lại actor, bottleneck, metric và boundary. | Cách hỏi phản biện giúp nhận ra root cause và baseline còn mơ hồ. | Câu “bot/script exploit” dễ nghe như một fact dù mới chỉ có resident reports. | Tôi ủng hộ wording “automation/exploit hypothesis” và bổ sung race condition, stale state, allocation policy. |
| Rule / Workflow / Agent | Tôi không để AI chọn mức công nghệ thay nhóm. | Việc so sánh ba mức giúp nhìn thấy Rule xử lý case rõ, Workflow điều phối nhánh và Agent không cần thiết. | Gắn AI vào mọi bài sẽ làm tăng complexity, khó audit và có thể tạo false positive. | Tôi chọn Workflow với Rule làm nền tảng, AI chỉ tạo risk score và không được commit/cancel slot. |
| Decision | Không dùng AI để chốt Go/Not Yet/No-Go. | Khung câu hỏi giúp nhóm kiểm tra baseline, owner, hậu quả khi AI sai và rollback. | Chưa có production logs nên không thể kết luận Go hoặc khẳng định hiệu quả của AI. | Tôi đồng ý với Not Yet, pilot shadow scoring và fallback về deterministic controls trước khi block người dùng. |

> Nếu phase nào không dùng AI, ghi `Không dùng` và vì sao tự làm.

---

## 3. Reflection câu hỏi mở

Chọn 3-4 câu trong 6 câu dưới để viết thành đoạn 8-12 câu (không trả lời bullet 1 dòng):
- Tôi học được gì khi nghe top 3 problems của các bạn khác?
- Nhóm có lúc nào bị solution-first, đòi làm Agent cho ngầu không?
- Tôi có thay đổi ý kiến sau khi bị challenge không, vì sao đổi?
- Tôi đóng góp gì thật sự vào artifact cuối, phần nào có dấu tay của tôi?
- Điều khó nhất khi viết Problem Statement là gì, metric hay boundary?
- Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?

**Reflection:**

```text
Khi nghe top 3 problems của các bạn, tôi nhận ra cùng một tiêu chí “có thể dùng AI” chưa đủ để chọn problem; actor, workflow và cách đo mới quyết định bài có đáng làm hay không. Card tôi pitch là bài thanh toán tại Samsung vì có số đo 35–45 giây/lượt và hàng đợi trên 10 người, nhưng nhóm lại chọn Vinhomes vì bài đó có câu hỏi fairness và adversarial behavior đáng đào sâu hơn. Tôi học được rằng một resident report về việc “hack” sân là tín hiệu pain, nhưng chưa đủ để kết luận bot là nguyên nhân kỹ thuật. Trong lúc thảo luận, tôi thay đổi cách nhìn từ chống bot đơn thuần sang fair access, trong đó race condition, stale state và allocation policy cũng phải được kiểm tra. Dấu tay của tôi trong artifact cuối nằm ở phần workflow và research: tôi giúp làm rõ handoff App → Backend, vị trí của atomic reservation và việc AI chỉ được can thiệp sau các pre-check. Nhóm có lúc dễ bị solution-first khi nói đến behavioral risk scoring, nhưng sau đó đã đưa Rule, transaction safety và fallback lên trước AI. Điều khó nhất khi viết Problem Statement là đặt metric mà không giả vờ rằng nhóm đã có baseline production; vì vậy các target như false-positive dưới 1% hay p95 risk decision 500 ms được ghi là mục tiêu cần kiểm chứng. Tôi cũng thấy boundary quan trọng không kém solution, vì AI không được trực tiếp commit hoặc hủy slot và phải có challenge cho case trung gian. Nếu làm lại, tôi sẽ challenge sớm hơn về tính đại diện của hai interview và yêu cầu bổ sung survey cư dân, BQL hoặc IT trước khi chấm điểm impact. Bài học lớn nhất của tôi là một quyết định “Not Yet” vẫn có chất lượng nếu nó chỉ rõ dữ liệu cần lấy, pilot chạy thế nào và điều kiện rollback ra sao.
```

---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [x] [12đ] Cá nhân có 5+ problems + top 3 Problem Cards
- [x] [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1)
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài
- [x] [15đ] Nhóm có workflow trước/sau
- [x] [20đ] Nhóm có PS v0/v1 với metric + boundary rõ
- [x] [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent
- [x] [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ
- [x] [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì
- [x] [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI

