# Candidate Problem Card để pitch — #11

## Tài liệu kỹ thuật thu thập từ nhiều nguồn nhưng không được hệ thống hóa

![Workflow candidate #11 — Hệ thống hóa tài liệu kỹ thuật](02-group-problem-statement-workflow-candidate-11.png)

```text
Problem 1 câu:
Trong quá trình học tập và làm việc, một cá nhân thu thập tài liệu kỹ thuật từ note,
website, Discord, Teams và email nhưng không lưu theo cấu trúc thống nhất, nên khi cần
dùng lại một chủ đề đã đọc, họ phải tìm kiếm hoặc đọc lại nhiều nguồn rời rạc.

Actor:
Nguyễn Danh Gia Mình — người trực tiếp thu thập và tái sử dụng tài liệu kỹ thuật cho
mục đích học tập, nghiên cứu và xử lý task. Đây là actor chính của pilot; chưa khái quát
pain cho mọi sinh viên hoặc nhân viên khi chưa validation thêm.

Thời điểm / bối cảnh:
Khi một task học tập hoặc công việc cần dùng lại kiến thức kỹ thuật đã đọc trước đó.
Tình huống xảy ra không cố định, hiện được ước tính khoảng 2–3 lần/tuần.

Current workflow (cần bấm giờ trên 5–10 lần tra cứu thật):
1. Phát sinh nhu cầu dùng kiến thức/tài liệu cũ cho task hiện tại.
2. Nhớ lại mình từng đọc chủ đề đó ở nguồn nào.
3. Tìm trong note, file, browser history, Discord, Teams hoặc email.
4. Đối chiếu các đoạn rời rạc; nếu không đủ thì đọc/tìm hiểu lại một phần.
5. Áp dụng vào task hiện tại.
6. Thường không lưu lại kết quả tra cứu theo cấu trúc thống nhất nên vòng lặp tái diễn.

Bottleneck:
Bước 3 — tìm đúng nội dung trong nhiều nguồn không có taxonomy, tag và index thống
nhất — là bottleneck giả thuyết. Bước 4 “đọc hiểu lại” được đo riêng để xác định đó là
hậu quả của retrieval kém hay một bottleneck độc lập.

Impact:
Ước tính phải tìm/đọc lại chủ đề cũ 2–3 lần/tuần. Breakdown được cung cấp là
2 + 2 + 20 + 15 + 3 = 42 phút/lần, không khớp với mô tả “25 phút/lần”; do đó 42 phút
được dùng làm tổng ước tính tạm thời và cần bấm giờ 5–10 lần để lấy baseline đáng tin.
Ngoài thời gian, việc chỉ tìm thấy một phần tài liệu có thể dẫn tới áp dụng thiếu ngữ cảnh.

Success metric:
- Baseline: trung vị thời gian từ lúc phát sinh nhu cầu đến khi tìm thấy nội dung đủ dùng,
  đo trên 5–10 lần tra cứu thật.
- Giảm thời gian tìm lại từ baseline xuống dưới 10 phút ở ít nhất 80% lượt pilot.
- Ít nhất 90% câu trả lời từ knowledge base có trích dẫn mở được tới tài liệu nguồn.
- Giảm số lần phải đọc/tìm hiểu lại từ đầu cùng một chủ đề xuống dưới 2 lần/tuần.
- Không dùng “số lần query” làm metric chính vì vẫn có thể query thường xuyên nhưng nhanh hơn.

Non-AI alternative:
Chọn một kho kiến thức tập trung như Notion; dùng template cố định gồm title, topic,
source URL, ngày đọc, tóm tắt, use case và tag; duy trì taxonomy/tag thủ công và link
tới nguồn gốc. Pilot phương án này trước để kiểm tra process fix có giải quyết đủ không.

AI hypothesis:
Một workflow ingestion có thể nhận tài liệu do người dùng chủ động đưa vào, trích text,
tạo bản tóm tắt/tag đề xuất và index vào knowledge base. Khi truy vấn, RAG chỉ tìm trên
kho đã được cho phép, trả lời kèm trích dẫn; người dùng mở nguồn, review và quyết định
cách áp dụng. AI không tự thu thập dữ liệu riêng tư từ Discord/Teams/email và không tự
áp dụng câu trả lời vào task.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

## Draft workflow candidate #11

```text
CURRENT STATE — 42 phút/lần theo breakdown ước tính, cần đo lại

[Phát sinh nhu cầu: 2'] → [Nhớ nguồn đã đọc: 2']
→ [Lục note/file/chat/email: 20']  <-- bottleneck giả thuyết
→ [Đọc lại phần còn thiếu: 15'] → [Áp dụng: 3']

FUTURE STATE — mục tiêu dưới 10 phút/lượt

[Query knowledge base: 1'] → [RAG trả lời + trích nguồn: 1']
→ [Người dùng mở nguồn, review + áp dụng: mục tiêu 5–8']  <-- human boundary

Ingestion trước đó:
[Người dùng chọn tài liệu] → [Trích text] → [AI đề xuất summary/tag]
→ [Người dùng duyệt] → [Index vào knowledge base]

Fallback:
Nếu tài liệu chưa được index, RAG không tìm thấy hoặc citation không mở được thì hệ
thống báo “không đủ nguồn”; người dùng tra cứu thủ công và bổ sung tài liệu sau khi kiểm tra.
```

File đính kèm: `02-group-problem-statement-workflow-candidate-11.png`

---

# Phase 4 — Quick Validation + Research

## 4.1. Quick validation — dữ liệu minh họa cho 3 người

> **CẢNH BÁO:** Toàn bộ câu trả lời và quote trong mục 4.1 dưới đây là **dữ liệu giả lập để minh họa cách trình bày**, không phải kết quả phỏng vấn thật và không được dùng làm bằng chứng khi nộp. Nhóm cần phỏng vấn ba người thật, thay nội dung trong bảng và lưu ngày phỏng vấn/ghi chú gốc.

### Đối tượng và kịch bản khảo sát minh họa

| Người | Persona giả lập | Bối cảnh tra cứu | Nguồn thường dùng |
|---|---|---|---|
| Người A | Sinh viên năm 4 CNTT đang làm khóa luận | Tìm lại paper, đoạn code và cách cấu hình từng đọc trước đó | Google Drive, bookmark trình duyệt, GitHub, note cá nhân |
| Người B | Lập trình viên backend có khoảng 1–2 năm kinh nghiệm | Tìm lại tài liệu API, cách xử lý lỗi và quyết định kỹ thuật cũ | Documentation website, Slack/Teams, GitHub issue, email |
| Người C | Học viên đang học thêm AI và làm việc toàn thời gian | Ôn lại khái niệm hoặc hướng dẫn để hoàn thành lab/task | Slide, Discord, website, file PDF và Notion |

### Kết quả minh họa

| Nguồn | Số người / mẫu | Tín hiệu xác nhận (quote minh họa, không phải quote thật) | Tín hiệu phản bác | Nhóm sẽ sửa problem thế nào nếu dữ liệu thật cho kết quả tương tự |
|---|---:|---|---|---|
| Phỏng vấn giả lập — Người A | 1 | “Tôi nhớ đã đọc cách đánh giá mô hình ở một paper hoặc notebook cũ, nhưng thường mất khoảng 25–35 phút để tìm đúng đoạn và kiểm tra lại ngữ cảnh.” Persona ước tính gặp 2 lần/tuần; pain tập trung ở bước tìm đúng đoạn trong Drive/bookmark. | Không phải mọi tài liệu đều cần đưa vào một kho; paper quan trọng đã được lưu theo thư mục nên đôi khi tìm trong dưới 5 phút. | Thu hẹp input pilot vào paper, notebook và bookmark đã được người dùng chủ động chọn; đo riêng trường hợp tìm nhanh nhờ folder hiện có để so sánh với RAG. |
| Phỏng vấn giả lập — Người B | 1 | “Search theo từ khóa thường trả về quá nhiều kết quả. Tôi tìm được đoạn chat cũ nhưng vẫn phải mở documentation chính thức để biết thông tin còn đúng không.” Persona ước tính gặp 3 lần/tuần, khoảng 15–25 phút/lần. | Vấn đề không chỉ là thiếu index; tài liệu có thể hết hạn. Một câu trả lời tổng hợp không có ngày cập nhật và link nguồn có thể làm tăng rủi ro áp dụng sai. | Bổ sung metadata `source`, `captured_at`, `updated_at` nếu có; bắt buộc citation mở được và yêu cầu người dùng review nguồn trước khi áp dụng. Không index tự động toàn bộ chat riêng tư. |
| Phỏng vấn giả lập — Người C | 1 | “Tôi lưu link ở nhiều nơi nhưng ít khi ghi vì sao link đó hữu ích. Khi làm lab, tôi phải đọc lại gần như từ đầu để biết phần nào liên quan.” Persona ước tính gặp 2–3 lần/tuần, khoảng 30–40 phút/lần. | Persona thừa nhận nguyên nhân một phần là không duy trì thói quen ghi chú. Một template Notion đơn giản có thể giải quyết phần lớn pain mà chưa cần AI. | Pilot process fix trước: một nơi lưu tập trung với topic, use case, source URL và tóm tắt ngắn. Chỉ thử AI ingestion/RAG nếu sau pilot thủ công, thời gian tìm lại vẫn trên 10 phút. |

### Tổng hợp giả lập

| Chỉ số | Người A | Người B | Người C | Cách đo thật cần dùng |
|---|---:|---:|---:|---|
| Tần suất ước tính | 2 lần/tuần | 3 lần/tuần | 2–3 lần/tuần | Nhật ký tra cứu liên tục trong 2 tuần |
| Thời gian một lượt | 25–35 phút | 15–25 phút | 30–40 phút | Bấm giờ từ lúc phát sinh nhu cầu đến khi tìm thấy nguồn đủ dùng |
| Pain chính | Tìm đúng đoạn | Kết quả thiếu ngữ cảnh/có thể hết hạn | Không nhớ lý do đã lưu tài liệu | Ghi loại failure sau từng lượt |
| Process fix có thể đủ? | Một phần | Không đủ nếu thiếu kiểm tra độ mới | Có khả năng cao | Pilot template trước khi thử AI |

### Insight tạm thời từ mô phỏng

```text
Dữ liệu minh họa gợi ý pain không chỉ là “tài liệu nằm nhiều nơi”. Ba failure mode cần
đo riêng là: không tìm thấy đúng đoạn, tìm thấy nhưng thiếu/nguy cơ hết hạn ngữ cảnh,
và không nhớ vì sao tài liệu từng được lưu. Vì đây chưa phải dữ liệu thật, nhóm chưa được
kết luận Go; bước tiếp theo là phỏng vấn ba người và ghi nhật ký 5–10 lượt tra cứu.
```

### Bộ câu hỏi để thay dữ liệu giả lập bằng khảo sát thật

1. Lần gần nhất bạn cần tìm lại một kiến thức kỹ thuật đã từng đọc là khi nào và để làm task gì?
2. Bạn đã tìm qua những nguồn nào, theo thứ tự nào? Hãy mô tả từng bước thực tế.
3. Từ lúc bắt đầu đến khi tìm thấy nội dung đủ dùng mất bao nhiêu phút?
4. Bước nào tốn thời gian nhất: nhớ nguồn, search, đọc lại hay xác minh thông tin còn đúng?
5. Trong hai tuần gần nhất việc này xảy ra bao nhiêu lần?
6. Có lần nào bạn không tìm thấy, tìm thiếu ngữ cảnh hoặc áp dụng thông tin đã cũ không?
7. Bạn hiện dùng folder, bookmark, Notion hay tag nào? Cách đó giải quyết được phần nào?
8. Bạn có chấp nhận chủ động lưu tài liệu vào một kho không? Nguồn nào không được phép index?

**Trạng thái validation:** `Chưa hoàn thành — đang dùng dữ liệu minh họa, cần thay bằng 3 phỏng vấn thật.`

---

## 4.2. Research giải pháp đã có

Quy ước các bước để so sánh cùng một workflow:

1. **Capture/Ingestion:** đưa tài liệu được phép vào kho.
2. **Chuẩn hóa/Index:** trích text, thêm metadata, tag và lập chỉ mục.
3. **Retrieval/Q&A:** tìm kiếm hoặc hỏi đáp trên kho kiến thức.
4. **Review:** mở citation, kiểm tra nguồn và quyết định cách áp dụng.

| Nguồn / tool / case | Link | Họ giải quyết bước nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Google NotebookLM | https://notebooklm.google.com/ | **Bước 2–4:** tổ chức/index tập nguồn người dùng cung cấp, tổng hợp, hỏi đáp và dẫn người dùng trở lại nguồn để review. | Pattern source-grounded: câu trả lời/tóm tắt bám theo tập tài liệu đã chọn và có citation để đối soát, phù hợp với yêu cầu giảm hallucination khi tái sử dụng kiến thức kỹ thuật. | **Bước 1 chưa hoàn toàn tự động:** người dùng vẫn phải lựa chọn, thêm và quản lý nguồn. Nhóm chưa xác minh được claim giới hạn `50–100 nguồn` từ link chính thức này, nên không dùng con số đó làm căn cứ thiết kế. | Áp dụng pattern RAG bám nguồn và bắt buộc trả citation mở được tới tài liệu/đoạn gốc; không coi câu trả lời AI là nguồn sự thật độc lập. |
| Notion AI | https://www.notion.so/product/ai | **Bước 1–4:** lưu nội dung có cấu trúc trong workspace, hỗ trợ tạo summary/thuộc tính, tìm kiếm trên workspace và connected apps, sau đó hiển thị nguồn để review. | Nằm ngay trong docs/database hằng ngày; hỗ trợ Enterprise Search trên các nguồn được kết nối như Slack, Google Drive và GitHub, cùng AI citations. Phù hợp làm knowledge base và process fix ban đầu. | Garbage in, garbage out: note sơ sài, thiếu metadata hoặc sai quyền truy cập vẫn cho kết quả kém. Connected apps, Enterprise Search và mức sử dụng AI phụ thuộc plan; không mặc định truy cập được mọi Discord, email hay bookmark cá nhân. | Chuẩn hóa ngay lúc ingestion bằng template tối thiểu: topic, source URL, ngày, use case, summary và tag đã được người dùng duyệt; không chỉ trông chờ AI search ở cuối. |
| Onyx — Open Source AI Platform | https://github.com/onyx-dot-app/onyx | **Bước 1–4:** connector/background worker đồng bộ knowledge; vector + keyword index hỗ trợ RAG/search tập trung; kết quả được dùng trong giao diện AI để tra cứu nguồn. | Open source và có thể self-host; Standard hỗ trợ connector sync, vector + keyword index và nhiều LLM. Pattern hybrid retrieval phù hợp khi dữ liệu nằm ở nhiều hệ thống. | Full deployment cần nhiều thành phần vận hành như worker, indexing/inference, Redis và MinIO; cấu hình connector còn phụ thuộc API key và permission từng nguồn. Bản Lite nhẹ hơn nhưng không có RAG index và connector-sync workers của Standard, nên giải pháp đầy đủ quá nặng cho pilot một cá nhân. | Không xây lại Onyx hay đồng bộ file thủ công. Chỉ học pattern connector/webhook → kho trung gian → hybrid retrieval; pilot nên dùng một nguồn capture nhỏ và stack/dịch vụ có sẵn. |

### Research takeaway

```text
Không nên build lại giao diện ghi chú, hệ thống chat hoặc hạ tầng Enterprise Search như
Onyx vì quá cồng kềnh cho nhu cầu của một cá nhân. Nếu validation thật cho thấy template
Notion/Markdown chưa đủ, nhóm nên pilot Workflow RAG tinh gọn: 1-click capture tài liệu
được phép → AI đề xuất summary/tag → người dùng duyệt → index → semantic search luôn
trả citation theo pattern NotebookLM. Không tự đọc toàn bộ Discord/Teams/email và không
dùng Agent tự chọn nguồn hoặc áp dụng kiến thức vào task.
```

### Quyết định sau research (tạm thời)

```text
Not Yet. Research cho thấy giải pháp kỹ thuật đã tồn tại và Workflow phù hợp hơn Agent,
nhưng nhóm chưa có validation thật để chứng minh process fix thủ công không đủ. Cần
phỏng vấn 3 người và pilot template trước khi quyết định build RAG.
```

---

# Trả lời theo tiêu chí đánh giá

## Hạng mục 1 — Chất lượng bài toán và pain point

**Actor cụ thể:** Nguyễn Danh Gia Mình, người trực tiếp thu thập và tái sử dụng tài liệu kỹ thuật phục vụ học tập, nghiên cứu và xử lý task, là actor chính của pilot. Nhóm chưa khái quát pain này cho mọi sinh viên hoặc nhân sự kỹ thuật khi chưa có validation thật với các actor khác.

**Workflow và bottleneck:** Khi cần dùng lại kiến thức đã đọc, actor phải nhớ nguồn, tìm thủ công trong note, file, browser history, Discord, Teams hoặc email, đối chiếu các phần rời rạc, đọc lại phần thiếu rồi mới áp dụng vào task. Bottleneck giả thuyết là **bước 3 — tìm đúng nội dung trên nhiều nguồn không có taxonomy, metadata, tag và index chung**, hiện ước tính mất 20 phút trong tổng số 42 phút/lượt; bước đọc lại 10 phút được đo riêng để xác định đây là hậu quả của retrieval kém hay một bottleneck độc lập.

**Impact và bằng chứng hiện có:** Tình huống được ước tính xảy ra 2–3 lần/tuần, tương đương khoảng 84–126 phút/tuần cho việc tìm và đọc lại. Tuy nhiên, các persona, quote và khoảng thời gian 15–40 phút trong phần validation hiện chỉ là **dữ liệu minh họa**, không phải phỏng vấn thật. Vì vậy, bằng chứng hiện tại mới đủ để hình thành giả thuyết pain, chưa đủ để kết luận pain đã được xác nhận.

**Cách bổ sung bằng chứng thật:** Phỏng vấn 3 người thuộc đúng nhóm người dùng mục tiêu và yêu cầu mỗi người ghi nhật ký tra cứu trong 2 tuần. Với 5–10 lượt tra cứu thật, ghi thời điểm, task, nguồn đã tìm, thời gian từng bước, có/không tìm thấy, tình trạng thiếu ngữ cảnh hoặc tài liệu hết hạn và link/ảnh chụp log gốc. Nếu dữ liệu không cho thấy bước tìm kiếm là bước tốn thời gian nhất hoặc tần suất thấp hơn đáng kể, nhóm sẽ thu hẹp hoặc đổi problem thay vì giữ giả thuyết ban đầu.

**Tự đánh giá hiện tại:** Mức **3/5** vì actor, workflow, bottleneck và impact dự kiến đã cụ thể, nhưng chưa có interview/survey/log thật. Bài có thể đạt mức 5/5 sau khi thay dữ liệu minh họa bằng bằng chứng thật và xác nhận được baseline.

## Hạng mục 2 — Cách phân tích và hướng giải quyết

| Mức giải pháp | Phương án | Khi nào đủ | Lý do chọn/không chọn |
|---|---|---|---|
| **Rule** | Dùng một kho Notion/Markdown, template cố định gồm `title`, `topic`, `source URL`, ngày đọc, `use case`, tóm tắt và tag; tìm bằng taxonomy/từ khóa. | Đủ nếu tài liệu ít, taxonomy ổn định và sau pilot thủ công ít nhất 80% lượt tra cứu dưới 10 phút. | Đây là phương án đơn giản nhất và phải thử trước. Điểm yếu là người dùng phải tự tóm tắt/gắn tag đều đặn; rule từ khóa khó xử lý cách diễn đạt khác nhau, đoạn liên quan nằm sâu trong tài liệu và câu hỏi cần tổng hợp nhiều nguồn. |
| **Workflow** | Người dùng chọn tài liệu → máy trích text → AI đề xuất summary/tag → người dùng duyệt → hệ thống index; khi tra cứu, RAG tìm trong kho được phép, trả lời kèm citation → người dùng mở nguồn, kiểm tra và áp dụng. | Phù hợp khi template thủ công chưa đạt mục tiêu nhưng dữ liệu đầu vào, các bước và điểm kiểm soát vẫn xác định trước. | **Mức được đề xuất** vì bài toán gồm chuỗi bước ổn định, cần semantic retrieval/tổng hợp nhưng không cần hệ thống tự lập kế hoạch. Workflow giữ được human review và dễ đo từng bước. |
| **Agent** | Agent tự chọn nguồn, tự truy cập nhiều hệ thống, lập kế hoạch tìm kiếm, đánh giá và áp dụng thông tin. | Chỉ phù hợp nếu nhiệm vụ có nhiều nhánh khó dự đoán và thực sự cần tự chọn tool/chiến lược theo từng tình huống. | Không chọn vì scope pilot không cần tự chủ như vậy; quyền truy cập Discord/Teams/email, tài liệu cũ, hallucination và hành động sai làm rủi ro tăng mạnh. Chi phí xây dựng, kiểm thử và vận hành cũng vượt quá nhu cầu của một pilot cá nhân. |

**Research giải pháp đã có:** NotebookLM cho thấy pattern hỏi đáp bám tập nguồn và citation; Notion AI kết hợp kho dữ liệu có cấu trúc với tìm kiếm và connected apps; Onyx cho thấy mô hình connector → index → hybrid retrieval nhưng hạ tầng đầy đủ quá nặng cho pilot một người. Do đó nhóm không xây lại hệ thống ghi chú hoặc Enterprise Search, mà tận dụng kho có sẵn và chỉ thử Workflow RAG tinh gọn nếu Rule/process fix chưa đủ.

**Boundary và workflow trước/sau:** Hệ thống chỉ index tài liệu do người dùng chủ động chọn và được phép sử dụng; không tự đọc toàn bộ chat hoặc email riêng tư. AI chỉ đề xuất metadata và trả lời dựa trên kho đã index, luôn kèm citation; người dùng chịu trách nhiệm duyệt metadata, kiểm tra độ chính xác/độ mới của nguồn và quyết định cách áp dụng. Workflow hiện tại có 6 bước, mục tiêu 42 phút/lượt; workflow sau có 4 bước, mục tiêu 7 phút/lượt, trong đó review nguồn 4 phút là human boundary bắt buộc.

**Kết luận:** Chọn **Workflow**, chưa chọn Agent. Chỉ nâng từ Rule lên Workflow nếu pilot kho tập trung và tagging thủ công vẫn không đưa ít nhất 80% lượt tra cứu xuống dưới 10 phút.

## Hạng mục 3 — Độ thiết thực và khả thi

**Success metric:**

| Chỉ số | Hiện trạng | Mục tiêu | Cách đo |
|---|---:|---:|---|
| Thời gian hoàn thành một lượt tra cứu | 42 phút/lượt (ước tính, cần xác nhận) | 7 phút/lượt và dưới 10 phút ở ít nhất 80% lượt pilot | Bấm giờ từ khi phát sinh nhu cầu đến khi tìm được nguồn đủ dùng và áp dụng; so sánh 5–10 lượt trước với 5–10 lượt sau. |
| Thời gian ở bottleneck tìm kiếm | Khoảng 20 phút/lượt (ước tính) | Không quá 2 phút cho query và nhận kết quả | Ghi thời gian theo từng bước trong nhật ký tra cứu. |
| Khả năng kiểm chứng kết quả | Chưa có baseline | Ít nhất 90% câu trả lời có citation mở được tới đúng tài liệu nguồn | Mở và kiểm tra citation trong từng lượt; ghi số citation lỗi hoặc sai nguồn. |
| Kết quả không sử dụng được | Chưa có baseline | Không quá 10% câu trả lời phải bỏ và tra cứu lại hoàn toàn | Người dùng đánh dấu `dùng được / thiếu nguồn / sai / hết hạn` sau mỗi lượt. |

**Pilot nhỏ nhất, khả thi:**

1. Trong 2 tuần đầu, Nguyễn Danh Gia Mình ghi log 5–10 lượt tra cứu thật để xác nhận baseline và bottleneck.
2. Chọn 20–30 tài liệu không nhạy cảm thuộc 1–2 chủ đề thường dùng; đưa vào một kho Notion/Markdown bằng template thống nhất.
3. Chạy pilot Rule trong 1 tuần. Nếu ít nhất 80% lượt đã dưới 10 phút thì dừng ở Rule, không xây AI.
4. Nếu Rule chưa đạt, chạy Workflow RAG trên đúng tập dữ liệu đó trong 1 tuần; thực hiện 5–10 truy vấn thật, luôn bắt buộc citation và người dùng review.
5. So sánh ba số chính: trung vị thời gian/lượt, tỷ lệ lượt dưới 10 phút và tỷ lệ câu trả lời có citation đúng, mở được.

**Rủi ro và fallback:**

- Nếu RAG thiếu nguồn, trả lời sai hoặc citation không mở được, hệ thống báo “không đủ nguồn”; người dùng quay về tìm thủ công, không áp dụng câu trả lời AI.
- Nếu tài liệu cũ hoặc thiếu ngữ cảnh, người dùng kiểm tra ngày cập nhật và nguồn chính thức trước khi áp dụng; metadata lưu `source`, `captured_at` và `updated_at` nếu có.
- Nếu có dữ liệu riêng tư hoặc thiếu quyền truy cập, không index tự động; pilot chỉ dùng tài liệu không nhạy cảm do người dùng chủ động chọn.
- Nếu việc nhập và duyệt metadata tốn nhiều thời gian hơn phần tiết kiệm được, dừng Workflow và quay về template tối giản hoặc cấu trúc folder hiện tại.

**Quyết định:** **Not Yet**. Bài toán và pilot có tính khả thi, nhưng nhóm chưa có bằng chứng người dùng thật và baseline đo được để chứng minh pain cũng như việc Rule không đủ. Chỉ **Go** với Workflow RAG khi log thật xác nhận pain xảy ra thường xuyên, bottleneck nằm ở bước tìm kiếm và pilot Rule không đạt mục tiêu; chọn **No-Go cho AI** nếu Rule đã đạt mục tiêu hoặc chi phí ingestion/review lớn hơn lợi ích tiết kiệm.

**Điều kiện dừng/rollback:** Dừng thử AI nếu dưới 90% kết quả có citation đúng và mở được, trên 10% kết quả phải bỏ để tra lại, không đạt tỷ lệ 80% lượt dưới 10 phút, xảy ra sự cố quyền riêng tư, hoặc sau pilot không tiết kiệm thời gian ròng. Khi đó quay về kho tập trung với template/tag thủ công và tra cứu nguồn gốc.

**Tự đánh giá hiện tại:** Mức **3/5** vì metric, pilot, rủi ro, fallback và quyết định đã cụ thể nhưng baseline vẫn là ước tính. Có thể đạt mức 5/5 sau khi hoàn thành log trước/sau và ra quyết định dựa trên số liệu thật.
