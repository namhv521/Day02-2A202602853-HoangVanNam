# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Hoàng Văn Nam
- Mã học viên: 2A202602853
- Nhóm: Pennity
- Candidate problem nhóm chọn: Người thu thập tài liệu kỹ thuật từ nhiều nguồn chưa có quy trình thống nhất để phân loại, gắn ngữ cảnh và tìm lại đúng tài liệu khi cần sử dụng.

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Scan các vấn đề trong quá trình vừa đi làm vừa hoàn thành khóa luận, gồm đồng bộ báo cáo trên GitHub/Drive/DOCX, chuyển feedback của GVHD thành task và xếp lịch review | Nhóm có thêm 3 candidate có actor, workflow và cách đo sơ bộ để đưa vào bước hội tụ |
| Pitch Problem Card | Pitch bài chuyển feedback sau buổi review thành task có vị trí cần sửa và acceptance criteria rõ | Candidate được đưa vào cụm báo cáo, ghi chú và chuyển thông tin thành đầu việc; nhóm nhận ra cần ưu tiên template/process fix trước AI |
| Challenge bài của bạn khác | Tôi cùng nhóm đặt câu hỏi liệu việc hệ thống hóa tài liệu có thể được giải quyết đủ tốt bằng một kho tập trung, metadata, tag và keyword search hay không | Nhóm giữ Rule làm kill-test và không mặc định RAG tốt hơn phương án non-AI |
| Gom trùng / cluster | Đối chiếu 15 candidate và gom các bài của mình vào cụm báo cáo/đầu việc và cụm scheduling | Các vấn đề gần nhau được nhìn theo pattern chung, giúp nhóm tránh so sánh các mô tả bị trùng |
| Chọn candidate problem | Tham gia vào việc so sánh actor, workflow, evidence, impact và khả năng thử nghiệm của các candidate | Nhóm chọn bài hệ thống hóa tài liệu kỹ thuật vì pain tìm kiếm có workflow rõ và có thể so sánh Rule với Workflow |
| Validation / research | Rà soát phần validation,sinh dữ liệu minh họa, chưa phải phỏng vấn thật | Báo cáo ghi rõ cần phỏng vấn 3 người và đo 5–10 lượt tra cứu thay vì dùng số giả lập làm baseline |
| Workflow nhóm | Góp ý tách bước tìm tài liệu khỏi bước đọc hiểu và giữ bước mở nguồn kiểm tra sau kết quả RAG | Bottleneck được đặt ở bước tìm thủ công nhiều nguồn; human boundary nằm ở bước review citation trước khi áp dụng |
| Problem Statement | Hỗ trợ rà soát metric và boundary | Problem Statement nêu rõ actor pilot, cách đo, nguồn được phép index và những việc AI không được tự làm. |
| Rule / Workflow / Agent | Tham gia so sánh kho có cấu trúc + keyword search, Workflow | Nhóm chọn Workflow: Rule xử lý ingestion/index, AI semantic retrieval, con người review; Agent bị loại vì không cần tự lập kế hoạch |
| Decision | Quyết định Go ở phạm vi pilot nhỏ, chưa Go xây hệ thống hoàn chỉnh | Pilot sẽ so sánh keyword search và RAG trên cùng tập 20–30 tài liệu, có điều kiện dừng và rollback rõ |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Đóng góp rõ nhất ở việc cung cấp 3 vấn đề thực tế trong lúc làm khoá luận, quyết định được các giải pháp và chia role, vai trò, nhiệm vụ cho từng người trong quá trình tìm hiểu bài tập nhóm
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Tôi dùng AI để gợi ý thêm vấn đề theo 4 lăng kính sau khi đã tự nêu 3 pain thực tế. | AI giúp mở rộng góc nhìn sang việc tìm feedback cũ, chuẩn bị checklist và quản lý kết quả thử nghiệm. | Một số gợi ý quá rộng hoặc tự đưa ra số liệu chưa được đo. | Tôi chỉ giữ các vấn đề gắn với workflow mình thực sự trải qua và ghi các con số là ước tính cần kiểm chứng. |
| Problem Card | Tôi dùng AI để phản biện actor, bottleneck, metric và non-AI alternative cho 3 card cá nhân. | AI giúp tôi thu hẹp bài “feedback chung chung” thành bước chuyển feedback sang task có acceptance criteria. | AI có xu hướng đề xuất tự động hóa trước khi chứng minh nguyên nhân và baseline. | Tôi ưu tiên template/process fix, bổ sung cách đo trong 3–5 buổi và giữ GVHD ở bước xác nhận cách hiểu. |
| Workflow | Tôi dùng AI hỗ trợ diễn đạt current/future workflow và rà soát các bước của bài nhóm. | AI giúp tách retrieval, review và apply thành các bước có actor rõ. | AI dễ gộp tìm kiếm với đọc hiểu hoặc bỏ qua bước kiểm chứng nguồn. | Tôi giữ bước mở citation và kiểm tra độ mới làm human boundary bắt buộc. |
| Research | Tôi dùng AI hỗ trợ tổng hợp pattern từ NotebookLM, Notion AI và Onyx. | AI giúp so sánh source-grounded Q&A, metadata và connector/RAG. | Một số claim về giới hạn sản phẩm hoặc hiệu quả không có nguồn chính thức rõ ràng. | Nhóm chỉ giữ các nhận xét kiểm tra được qua link sản phẩm và loại số liệu chưa xác minh khỏi lập luận. |
| Problem Statement | Tôi dùng AI phản biện phạm vi, metric và boundary của bản v0. | AI chỉ ra “tài liệu kỹ thuật” còn rộng và baseline 42 phút chưa phải dữ liệu thật. | AI không thể tự xác nhận tần suất, quyền truy cập hay pain của actor. | Nhóm giới hạn actor pilot, nêu cách đo 5–10 lượt và chỉ index tài liệu người dùng chủ động cung cấp. |
| Rule / Workflow / Agent | Tôi dùng AI để lập bảng so sánh ba mức giải pháp trên cùng một problem. | AI giúp làm rõ Workflow đủ cho luồng tuyến tính và Agent là thừa. | AI có thể thiên về RAG dù Rule/keyword search chưa được thử. | Nhóm giữ Rule làm kill-test: nếu đạt metric dưới 10 phút ở ít nhất 80% lượt thì không dùng AI. |
| Decision | Tôi dùng AI để rà soát điều kiện Go, pilot và rollback. | AI giúp hệ thống hóa ba metric đo và các điều kiện dừng. | AI không biến dữ liệu minh họa thành validation thật và không thể kết luận RAG chắc chắn tốt hơn. | Tôi đồng ý Go chỉ cho pilot so sánh, đồng thời ghi rõ chưa Go xây hệ thống hoàn chỉnh và phải fallback khi citation lỗi. |

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
Khi nghe các candidate của nhóm, tôi nhận ra một problem nghe phù hợp với AI chưa chắc đã là bài nên chọn nếu actor, workflow và bằng chứng còn mơ hồ. Ba bài tôi đưa ra đều xuất phát từ việc làm khóa luận, nhưng phần lớn có thể bắt đầu bằng template hoặc rule đơn giản. Bài nhóm chọn về tìm lại tài liệu kỹ thuật có điểm nghẽn cụ thể hơn ở bước tìm thủ công trên nhiều nguồn. Tôi học được rằng cần tách retrieval khỏi đọc hiểu để biết AI đang giải đúng bottleneck nào. Nhóm cũng không chọn Agent dù bài toán có độ mơ hồ và phức tạp cao, vì luồng truy vấn vẫn tuyến tính và không cần hệ thống tự lập kế hoạch. Tôi đồng ý chọn Workflow RAG nhưng chỉ khi Rule bằng kho tập trung, metadata và keyword search không đạt metric. Boundary quan trọng nhất là AI chỉ trả kết quả kèm citation, còn người dùng phải mở nguồn, kiểm tra độ chính xác và độ mới trước khi áp dụng. Phần validation hiện vẫn chưa hoàn thành vì dữ liệu trong báo cáo mới là minh họa, nên quyết định Go chỉ có nghĩa là Go với pilot nhỏ để đo. Dấu tay của tôi trong bài là đưa các pain thực tế vào vòng hội tụ và nhắc nhóm phân biệt giả định với bằng chứng. Nếu làm lại, tôi sẽ challenge sớm hơn về nguồn nào thực sự được phép index và yêu cầu ghi nhật ký 5–10 lượt tìm kiếm trước khi đặt target. Tôi cũng sẽ tham gia phỏng vấn người dùng thật để kiểm tra xem pain nằm ở khâu tìm tài liệu, đọc hiểu hay thói quen lưu tài liệu.
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

