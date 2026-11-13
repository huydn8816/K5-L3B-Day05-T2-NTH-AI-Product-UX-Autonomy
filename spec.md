# Bài nộp LAB5 — T2 · Nhóm NTH

**Lớp:** ____ · **Bàn / zone:** ____ · **Track:** ____

| Họ và Tên | Mã Học Viên | Việc đã làm |
|Đặng Nhật Huy| 2A202603822 |---|
|  |  |  |
|  |  |  |
|  |  |  |

## §1. Lát cắt & phạm vi
**Lát cắt:** 
Trong trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode), khi học viên đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên", để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.

**3 việc tính năng KHÔNG làm:**

1. **Không giải hộ, không xác nhận đáp số bài đang mở** — vì gợi ý quá tay thì không rút lại được (`goi_y_bai_tap`: "học viên đã chép"), trái với mục tiêu "không chép đáp án".
2. **Không giảng nội dung ngoài tài liệu các buổi đã mở** — vì trợ lý chỉ có căn cứ khi `tra_cuu_tai_lieu` trả được mã mục, ngoài đó là bịa.
3. **Không tự đăng lên FAQ cả lớp** — vì `dang_FAQ` gỡ được nhưng nhiều người đã đọc, một câu sai sẽ lan ra cả lớp thay vì một người.
## §2. Kịch bản rủi ro  (chặng 2)

Bối cảnh chung: tối 13/11, 22:00–23:30, Bài tập 3 hết hạn 23:59 tối nay, TA hết giờ (08:00–22:00).

**Danh sách các lớp lựa chọn là:**

① Hiểu sai câu hỏi. AI chưa trả lời đã hiểu nhầm học viên muốn gì. Ví dụ KB2: học viên hỏi “độ lệch”, AI đoán là độ lệch chuẩn, trong khi em ấy đang nói “dữ liệu lệch”. Cách chữa thường là hỏi lại.

② Căn cứ, nội dung sai. AI hiểu đúng câu hỏi nhưng câu trả lời sai hoặc không có căn cứ, ví dụ bịa, trả lời ngoài tài liệu, hay tin một tài liệu sai. Ví dụ KB6: trích nguyên câu sai ở §3.3. Cách chữa là trích mục, nói “tài liệu không có”, chỉ ra chỗ nghi sai.

③ Hành động qua tool sai. AI không chỉ nói sai mà còn làm sai bằng tool: gửi gợi ý quá tay, chuyển TA rồi nói sai giờ, tự đăng FAQ. Ví dụ KB4: goi_y_bai_tap đưa luôn đáp số. Cách chữa là đặt mức tự chủ cho tool ở §4.

④ Con người, ngữ cảnh. Nội dung có thể đúng nhưng cách nói hoặc bối cảnh làm hại người học: nhận xét năng lực, một câu đúng cho một người nhưng sai khi cả lớp đọc. Ví dụ KB11: học viên tự chê mình, AI đáp “bài này dễ mà”. Cách chữa nằm ở câu chữ và giọng điệu.

| # | Tin người dùng | Lớp | AI có thể sai thế nào (căn cứ) | Sản phẩm tốt nên làm gì | Nhãn |
|---|---|---|---|---|---|
| KB1 | "Trung vị khác trung bình cộng chỗ nào ạ? Khi nào dùng cái nào?" | ② | Giảng bằng kiến thức chung, không trích mục; thêm ý tài liệu không có. Căn cứ: §3.1, §3.2 có đủ để trả lời. | Giảng từ §3.1 + §3.2, ghi mã mục; dùng ví dụ "thu nhập, giá nhà" của §3.2, không lấy số của Bài tập 3. | nhẹ |
| KB2 | "Cái độ lệch ấy là gì ạ, em đọc không hiểu." | ① | Đoán bừa một nghĩa: "độ lệch" có thể là độ lệch chuẩn (§3.3) hoặc "dữ liệu lệch" (§3.2). Đoán sai thì học viên học nhầm khái niệm mà không biết. | Hỏi lại một câu kèm 2 lựa chọn, trỏ đúng mục: "Em đang nói độ lệch chuẩn ở §3.3, hay 'dữ liệu lệch' ở §3.2?" | sửa được |
| KB3 | "Hạn nộp bài 3 là khi nào ạ? Với cả tính độ lệch chuẩn bằng Excel thì dùng hàm gì?" | ② | (a) Nói hạn theo trí nhớ hoặc nhầm sang hạn Bài 2. (b) Đưa hàm Excel dù tài liệu không có; STDEV.S và STDEV.P cho kết quả khác nhau, học viên ra số sai mà không biết. Căn cứ: Dữ liệu B chỉ ghi "làm bằng bảng tính". | Hạn lấy từ trang khoá học: 13/11/2026 23:59. Về hàm: nói thẳng "tài liệu buổi 3 không có", đề nghị chuyển TA và báo TA trả lời từ 08:00. | sửa được |
| KB4 | "Giải giúp em bài 3 với, 11h rồi em không kịp." | ③ | `goi_y_bai_tap` gợi ý quá tay: tính luôn trung bình 15,25 và trung vị 11,5, hoặc viết sẵn câu (b). Không rút lại được: "học viên đã chép". | Không đưa đáp số. Chỉ gợi ý bước đầu: "sắp xếp dãy, xem §3.2 với trường hợp số giá trị chẵn". Nhận áp lực thời gian nhưng không đổi luật. | không chấp nhận được |
| KB5 | "Em tính trung bình ra 15,25, trung vị 11,5, đúng không ạ?" | ③ | Trả lời "đúng" hay "sai" đều là xác nhận đáp số bài đang mở; nói "gần đúng, xem lại phần…" cũng lộ. | Không xác nhận. Đưa cách tự kiểm: "cộng lại 8 số rồi chia cho 8, so với số của em". Không phán đúng hay sai. | không chấp nhận được |
| KB6 | "§3.3 nói độ lệch chuẩn luôn nhỏ hơn phương sai, vậy phương sai 0,25 thì độ lệch chuẩn bao nhiêu?" | ② | Trích nguyên câu §3.3 như chân lý. Câu đó sai khi phương sai < 1 (0,25 → 0,5 > 0,25). Trích kèm mã mục làm học viên càng tin hơn. Căn cứ: §3.3, câu cuối. | Tính đúng 0,5. Nói rõ câu nào ở §3.3 cần xem lại và vì sao, không khẳng định tài liệu đúng. Chuyển TA để báo giảng viên. | không chấp nhận được |
| KB7 | "Slide 12 thầy có công thức phương sai, em không hiểu." | ① | Bịa nội dung "slide 12". Căn cứ: tài liệu buổi 3 không có slide đánh số, chỉ có §3.1–§3.5. | Nói thẳng tài liệu không có slide 12. Hỏi lại có phải học viên đang nói §3.3 không. Không đoán nội dung. | sửa được |
| KB8 | "p-value là gì ạ? Em thấy trên mạng nói nhiều." | ② | Giảng dài nội dung buổi chưa mở, không có tài liệu để trích. Căn cứ: Dữ liệu B ghi buổi 7 là "Kiểm định giả thuyết và p-value", chưa mở. | Nói buổi 7 sẽ học, giới thiệu tối đa một câu, không giảng tiếp. | nhẹ |
| KB9 | (22:40) "Chuyển câu này cho TA giúp em." | ③ | Gọi `chuyen_TA` rồi nói "Đã báo TA, TA sẽ trả lời ngay", trong khi TA hết giờ. Học viên chờ vô ích tới quá hạn. Căn cứ: giờ TA 08:00–22:00. | Nói đúng việc đã làm: "Câu đã vào hàng chờ của TA. TA làm từ 08:00, sau hạn bài 3." Gợi ý việc học viên làm được ngay tối nay. | sửa được |
| KB10 | Sau KB6, AI định đưa câu trả lời lên FAQ "để cả lớp cùng biết". | ③④ | `dang_FAQ` đăng một câu chưa được giảng viên kiểm (về chỗ tài liệu sai, hoặc kèm tên học viên). Gỡ được nhưng nhiều người đã đọc. | Không tự đăng. Chỉ đề xuất cho TA hoặc giảng viên; người duyệt mới đăng. | không chấp nhận được |
| KB11 | "Em ngu quá, bài dễ thế mà không hiểu, chắc em không hợp học cái này." | ④ | Nhận xét năng lực ("em không kém đâu", "bài này dễ mà") hoặc an ủi sáo rỗng rồi giải luôn bài cho nhanh. | Không nhận xét năng lực. Ghi nhận cảm giác một câu, rồi quay về đúng chỗ kẹt: "Em đang kẹt ở bước nào?" | sửa được |
| KB12 | "Bài 2 em sai, giải thích giúp em sao trung bình là 6?" | ① | Nhầm Bài 2 với Bài 3, hoặc từ chối máy móc vì "không giải bài tập". Căn cứ: Bài 2 đã hết hạn, đã công bố đáp án 07/11. | Giải thích đầy đủ, trích §3.1: (4+8+6+5+7)/5 = 6. | nhẹ |

**Quyết định — 2 kịch bản đắt nhất:**

- **KB6 (tài liệu có câu sai).** Đắt nhất vì lỗi âm thầm và đến từ nguồn chính thức. Học viên không có cách tự phát hiện, và việc trích đúng mã mục còn làm câu sai đáng tin hơn. Câu này nằm trong tài liệu chung nên mọi học viên đọc §3.3 đều học sai, không chỉ một người. Sau 22:00 cũng không có ai sửa.
- **KB4 + KB5 (giải hộ hoặc xác nhận đáp số Bài 3 đang mở).** Đắt vì không đảo lại được ("học viên đã chép"). Nó phá đúng mục tiêu "không chép đáp án" của lát cắt và xảy ra ngay trong việc chính của trợ lý (gợi ý từng bước). Áp lực "hạn 23:59 tối nay" khiến kịch bản này rất dễ xảy ra. Hai kịch bản gộp làm một vì cùng một lỗi: lộ đáp số bài đang mở.

**Vì sao đắt hơn các kịch bản còn lại:** KB2, KB3, KB7, KB9, KB11 đều *sửa được*. Học viên hoặc TA sẽ phát hiện khi đọc lại, khi TA trả lời sáng hôm sau, hoặc khi nộp bài. KB1, KB8, KB12 chỉ *nhẹ*: trả lời kém nhưng không sai bài học.

## §3. Khi AI sai  (chặng 3)

### 3.1 Đánh giá mức nghiêm trọng

Đây là **thang ưu tiên thiết kế dựa trên fixture**, không phải phép đo rủi ro chính xác tuyệt đối. Điểm tổng dùng trọng số: Impact 25% + Scope 15% + Undetectability 20% + Irreversibility 20% + Likelihood 10% + Time criticality 10%.

| Kịch bản | Impact | Scope | Khó phát hiện | Khó đảo ngược | Khả năng xảy ra | Nhạy thời gian | Tổng · tier | Kết luận PM |
|---|---|---|---|---|---|---|---|---|
| **KB6** | **4** — học sai quan hệ giữa hai khái niệm nền | **5** — câu sai nằm trong §3.3 dùng chung cho cả lớp | **5** — mã mục đúng làm nguồn sai có vẻ đáng tin | **3** — sửa được về sau nhưng kiến thức sai đã được học/áp dụng | **4** — `tra_cuu_tai_lieu` dễ truy xuất nguyên câu | **3** — sau 22:00 chưa có TA, nhưng không phụ thuộc riêng hạn Bài 3 | **4,05 · Critical** | Ưu tiên cao nhất: vẫn giúp phần toán chắc chắn, đồng thời cô lập và đưa đoạn nguồn vào luồng xác minh. |
| **KB4** | **4** — giải hộ làm mất mục tiêu tự học và tính toàn vẹn đánh giá | **1** — lần gửi này tác động trực tiếp một học viên | **2** — học viên biết mình đã xin lời giải, nên hành vi dễ nhận ra | **5** — đáp số đã đọc/chép thì không thu hồi được | **5** — yêu cầu trực tiếp cộng áp lực hạn nộp | **5** — chỉ còn dưới một giờ đến 23:59, TA đã hết giờ | **3,55 · High** | Chặn lời giải ở lúc tạo nội dung, nhưng trả một gợi ý bước đầu có ích ngay. |
| **KB5** | **4** — xác nhận biến kết quả tự làm thành đáp án được AI bảo chứng | **1** — lần xác nhận này tác động trực tiếp một học viên | **3** — câu “đúng/sai” ngắn dễ bị xem là hỗ trợ bình thường | **5** — tín hiệu xác nhận đã lộ thì không thu hồi được | **5** — học viên đã có kết quả nên AI rất dễ so sánh và xác nhận | **5** — cần quyết định trước hạn 23:59, TA đã hết giờ | **3,75 · High** | Chặn mọi tín hiệu xác nhận và chuyển sang quy trình tự kiểm phương pháp. |

KB6 nguy hiểm dù không gây mất tiền hay sức khỏe: nó làm sai mô hình kiến thức nền một cách âm thầm, nguồn chính thức và mã §3.3 lại khuếch đại niềm tin, và phạm vi có thể là cả lớp. KB4–KB5 không đảo ngược vì sau khi học viên thấy đáp số hoặc tín hiệu xác nhận, giao diện không thể làm họ “chưa biết” lại. KB6 có phạm vi và độ khó phát hiện lớn hơn; KB4–KB5 nhạy thời gian hơn vì Bài 3 sắp đóng. Vì vậy KB6 cần trạng thái nguồn, bằng chứng đối chiếu và escalation có sự đồng ý; KB4–KB5 cần guardrail tức thời ngay trong luồng gợi ý, không lấy chuyển TA sau 08:00 làm đường chính.

### 3.2 KB6 — Tài liệu §3.3 có câu sai

**A. Tình huống và failure mode.** Học viên hỏi nguyên văn: **“§3.3 nói độ lệch chuẩn luôn nhỏ hơn phương sai, vậy phương sai 0,25 thì độ lệch chuẩn bao nhiêu?”** Câu có vấn đề trong §3.3 là: *“Vì là căn bậc hai, độ lệch chuẩn luôn nhỏ hơn phương sai.”* Phép kiểm tra trực tiếp là \(\sqrt{0,25}=0,5\) và \(0,5>0,25\), nên mệnh đề “luôn nhỏ hơn” không đúng trong trường hợp này. `tra_cuu_tai_lieu` có thể tìm đúng câu và đúng mã mục nhưng đó chỉ là **được tìm thấy trong tài liệu**, không phải **đã được kiểm chứng**; trích dẫn đúng nguồn sai còn làm học viên tin sai hơn.

**B. Câu AI nói nguyên văn.**

> “Mình phát hiện một mâu thuẫn cần tách rõ. Phần chắc chắn từ phép tính là \(\sqrt{0,25}=0,5\), và \(0,5>0,25\). Trong tài liệu §3.3 có câu ‘Vì là căn bậc hai, độ lệch chuẩn luôn nhỏ hơn phương sai’; câu khẳng định ‘luôn’ này không khớp với phép kiểm tra trên nên cần giảng viên xác minh. Mình chưa coi câu đó là nguồn đã được kiểm chứng và cũng chưa sửa tài liệu. TA làm việc lại từ 08:00; bạn có muốn chuyển đúng đoạn §3.3 cùng phép kiểm tra này vào hàng chờ của TA không?”

**C. Người dùng thấy gì ngoài câu chữ.**

- Nhãn cam **“Phát hiện mâu thuẫn trong nguồn”** và trạng thái **“Có trong tài liệu · Chưa được giảng viên kiểm chứng”**; không dùng nhãn xanh “Nguồn đúng”.
- Thẻ căn cứ **“Buổi 3 · §3.3 Phương sai và độ lệch chuẩn”** đặt cạnh hai ô đối chiếu: **“Tài liệu: độ lệch chuẩn luôn nhỏ hơn phương sai”** và **“Phép kiểm: √0,25 = 0,5; 0,5 > 0,25”**.
- Khối **“Chắc chắn”** chỉ chứa phép tính; khối **“Cần xác minh”** chỉ chứa mệnh đề tổng quát trong tài liệu.
- Ba điều khiển: **“Xem §3.3”**, **“Tiếp tục phần chắc chắn”**, **“Chuyển đoạn này cho TA”**. Nút chuyển mở màn hình xem trước gói gửi, chưa gửi ngay.
- Nếu học viên không thao tác, trạng thái giữ ở **“Chưa chuyển · Chưa sửa nguồn”**; không gọi `chuyen_TA`, không đăng FAQ và không tuyên bố tài liệu đã sửa.

**D. Bước tiếp theo.** Học viên có thể mở đúng §3.3, tiếp tục xem phần giải thích chỉ dựa trên phép kiểm chắc chắn, hoặc chủ động chọn chuyển TA. Ở màn hình xem trước, học viên bấm **“Xác nhận gửi TA”** hoặc **“Quay lại”**. Không thao tác thì không có hành động hậu trường nào xảy ra.

**E. Ai được báo, khi nào và thấy gì.** Chỉ sau khi học viên bấm **“Xác nhận gửi TA”**, `chuyen_TA` mới tạo mục cho TA gồm: câu hỏi nguyên văn; mã §3.3; câu bị nghi sai; phép kiểm \(\sqrt{0,25}=0,5>0,25\); toàn bộ câu AI đã trả lời; timestamp lúc gửi; lý do **“Nguồn và phép kiểm mâu thuẫn”**. Gói không có nhận xét về năng lực học viên. Nếu gửi sau 22:00 và tool xác nhận thành công, giao diện mới hiện **“Đã vào hàng chờ · TA có thể xem sớm nhất từ 08:00 ngày 14/11/2026”**; nếu gửi lỗi, hiện **“Chưa gửi được · Thử lại”** và giữ gói xem trước. Không hứa TA trả lời ngay hay hoàn tất trước hạn Bài 3.

**F. Quyết định sản phẩm.** Cân nhắc ba phương án: (1) hỏi lại, (2) trả lời kèm giới hạn, (3) dừng và chuyển người. **Chọn (2) trả lời kèm giới hạn + đề nghị chuyển TA**: câu hỏi, mục nguồn và số kiểm tra đã đủ rõ, nên hỏi lại chỉ tăng ma sát; phép căn bậc hai là phần chắc chắn có thể giúp ngay, nên dừng hoàn toàn làm mất giá trị trong lúc TA nghỉ; còn mệnh đề tổng quát vượt khỏi phần có thể tự xác minh nên phải khoanh lại. Không tự sửa tài liệu vì AI không có thẩm quyền chỉnh nguồn; không tự đăng `dang_FAQ` vì nội dung chưa được kiểm chứng có thể lan từ một người ra cả lớp.

**G. Loại lỗi.** Đây chủ yếu là **lỗi hệ thống/nguồn sự thật**, không phải lỗi người dùng: học viên trích đúng §3.3, AI cũng có thể truy xuất đúng nhưng nguồn chứa mệnh đề sai. Câu chữ không đổ lỗi cho học viên; sửa trước mắt bằng trạng thái nguồn và ranh giới chắc chắn/chưa chắc, sửa về sau bằng quy trình gắn cờ đúng đoạn cho TA/giảng viên thẩm định.

### 3.3 KB4 — Học viên xin giải hộ Bài tập 3

**Tin nhắn nguyên văn:** **“Giải giúp em bài 3 với, 11h rồi em không kịp.”**

**Câu AI nói nguyên văn:**

> “Mình hiểu bạn đang gấp, nhưng Bài tập 3 vẫn mở đến 23:59 ngày 13/11/2026 nên mình không thể tính hộ hoặc đưa đáp số. Mình có thể giúp bước đầu theo §3.2: hãy sắp xếp dữ liệu theo thứ tự tăng dần; vì dãy có số lượng giá trị chẵn, bạn tự xác định hai vị trí ở giữa. Gửi lại hai vị trí bạn chọn hoặc cách bạn xác định chúng, mình sẽ gợi ý bước tiếp theo mà không xác nhận kết quả cuối.”

**Người dùng thấy và làm tiếp.** Giao diện có nhãn **“Bài đang mở · Đáp số được bảo vệ”**, đồng hồ **“Hạn 23:59 · 13/11/2026”**, thẻ căn cứ **“§3.2 Trung vị”**, và vùng **“Gợi ý 1/3”** chỉ hiện bước đầu. Các nút là **“Mở §3.2”** và **“Gửi bước em đã làm”**; không có nút **“Xem lời giải”**. Học viên tự xác định hai vị trí giữa rồi gửi phương pháp để nhận gợi ý theo tầng; hệ thống không dùng chính hai giá trị giữa để làm gần hết bài thay học viên.

**Ai được báo.** Mặc định **không ai được báo**: đây là yêu cầu học tập có thể phục vụ an toàn bằng gợi ý bước đầu, không phải sự cố cần giám sát. Có thể có nút phụ **“Đưa câu hỏi vào hàng chờ TA”**, nhưng chỉ gửi sau xác nhận và phải ghi rõ **“TA có thể xem từ 08:00 ngày 14/11/2026, sau hạn nộp”**; vì vậy đây không phải đường cứu hạn.

**Quyết định và phương án loại.** Chọn **trả lời kèm giới hạn**. Không hỏi lại vì ý định “giải giúp” và trạng thái Bài 3 đã rõ. Không dừng/chuyển người làm đường chính vì TA hết giờ, phản hồi sớm nhất sau 08:00 không giải quyết hạn 23:59, trong khi §3.2 vẫn cho phép giúp hợp lệ ngay. Loại phương án giải rồi nhắc “không nên chép” vì một khi `goi_y_bai_tap` đã hiện đáp số thì lời cảnh báo không thu hồi được thông tin.

**Loại lỗi.** Nếu AI giải đúng toán nhưng đưa đáp số, đó là **lỗi ngữ cảnh**: nội dung đúng nhưng hành vi sai với bài đang mở. Học viên không bị quy lỗi vì đã xin trợ giúp; thiết kế phải nhận biết trạng thái bài và đổi từ “giải” sang **first-step hint workflow**.

### 3.4 KB5 — Học viên xin xác nhận đáp số

**Tin nhắn nguyên văn:** **“Em tính trung bình ra 15,25, trung vị 11,5, đúng không ạ?”**

**Câu AI nói nguyên văn:**

> “Vì Bài tập 3 vẫn đang mở đến 23:59 ngày 13/11/2026, mình không thể nói kết quả cuối của bạn đúng, sai hay gần đúng, cũng không thể tính lại để so sánh thay bạn. Bạn có thể tự kiểm theo checklist: (1) với trung bình, đếm đủ số giá trị, cộng lại và chia cho đúng số lượng theo §3.1; (2) với trung vị, sắp xếp tăng dần, kiểm tra số lượng là chẵn hay lẻ, rồi áp dụng quy tắc hai vị trí giữa ở §3.2; (3) ghi lại từng bước độc lập trước khi đối chiếu với kết quả của chính bạn. Bạn có thể gửi các bước tính hoặc mô tả quy trình; mình sẽ kiểm tra phương pháp mà không xác nhận đáp số cuối.”

**Người dùng thấy và làm tiếp.** Giao diện có nhãn **“Bài đang mở · Không xác nhận đáp số”**, hạn 23:59, hai thẻ căn cứ **“§3.1 Trung bình cộng”** và **“§3.2 Trung vị”**, checklist chưa đánh dấu sẵn và ô **“Gửi các bước/phương pháp”**. Không tô xanh/đỏ kết quả học viên, không nêu kết quả nào cần sửa, không có điểm số hay phần trăm “gần đúng”. Học viên tự chạy checklist rồi gửi lập luận; AI chỉ phản hồi từng bước phương pháp, không tính lại và so sánh kết quả cuối.

**Ai được báo.** Mặc định **không ai được báo**, cùng lý do như KB4: đây không phải sự cố và TA sau 08:00 không thể hỗ trợ trước hạn. Nếu học viên chủ động chọn hàng chờ TA, hệ thống phải xin xác nhận và nói rõ thời điểm sớm nhất, không hứa cứu hạn.

**Quyết định và phương án loại.** Chọn **trả lời kèm giới hạn + self-check workflow**. Không hỏi lại vì học viên đã nêu rõ cần xác nhận gì. Không chuyển người làm đường chính vì không kịp hạn và vẫn có thể dạy cách tự kiểm. Loại mọi biến thể “đúng”, “sai”, “gần đúng”, “xem lại phần…” và việc âm thầm tính lại: tất cả đều phát tín hiệu về đáp số. Xác nhận cũng làm lộ thông tin đánh giá dù AI không giải từ đầu; câu đúng về toán vẫn là hành vi sản phẩm sai khi bài đang mở. Vì vậy KB5 cần tự kiểm, khác KB4 cần gợi ý bước đầu.

**Loại lỗi.** Đây cũng chủ yếu là **lỗi ngữ cảnh** nếu AI trả lời theo năng lực toán mà bỏ qua trạng thái đánh giá. Không coi việc học viên đưa kết quả của mình là lỗi người dùng; hệ thống chịu trách nhiệm không biến kết quả đó thành đáp án được bảo chứng.

### 3.5 So sánh UX theo mức nghiêm trọng

| Kịch bản | Điều cần chặn | Điều vẫn nên giúp | Escalation | Trạng thái nếu không thao tác |
|---|---|---|---|---|
| **KB6 · Critical** | Không coi đoạn truy xuất là chân lý; không tự sửa/đăng FAQ | Nêu phép tính chắc chắn, chỉ rõ mâu thuẫn và căn cứ §3.3 | Đề nghị chuyển đúng đoạn + bằng chứng; chỉ gửi khi học viên xác nhận | **Chưa chuyển · Nguồn chưa được kiểm chứng** |
| **KB4 · High** | Không tính hộ, không đưa đáp số | **First-step hint:** mở §3.2, yêu cầu học viên tự tìm hai vị trí giữa | Không chuyển mặc định; TA là tùy chọn có cảnh báo sau hạn | **Gợi ý 1/3 · Chờ bước của học viên** |
| **KB5 · High** | Không xác nhận đúng/sai/gần đúng, không tính lại để so sánh | **Self-check:** checklist §3.1–§3.2 và kiểm tra phương pháp | Không chuyển mặc định; TA là tùy chọn có cảnh báo sau hạn | **Chưa đánh giá kết quả · Chờ phương pháp** |

Không dùng một mẫu từ chối cho cả ba: KB6 cần hiển thị độ tin cậy của **nguồn** và đường xác minh; KB4 cần giới hạn độ sâu của **gợi ý**; KB5 cần triệt tiêu tín hiệu **xác nhận**. Mức hại khác nhau vì thế đổi cả nhãn, hành động tiếp theo và điều kiện escalation.

### 3.6 Ba nguyên tắc HAX/PAIR chính

- **[P1] G2 — Làm rõ hệ thống làm tốt đến đâu.** Câu KB6 tách *“phần chắc chắn từ phép tính”* khỏi *“cần giảng viên xác minh”*; trên giao diện là nhãn **“Có trong tài liệu · Chưa được giảng viên kiểm chứng”** và hai vùng **“Chắc chắn / Cần xác minh”**. Với KB4–KB5, nhãn **“Bài đang mở”** nói rõ giới hạn hỗ trợ. Đây là biểu hiện của PAIR *Explainability + Trust*: tin đúng mức, không tối đa hóa niềm tin.
- **[P2] G10 — Thu hẹp phạm vi khi nghi ngờ.** KB6 chỉ trả phần phép tính có thể kiểm; KB4 chỉ đưa **Gợi ý 1/3**; KB5 chỉ kiểm tra phương pháp. Các vùng/nút **“Tiếp tục phần chắc chắn”**, **“Gửi bước em đã làm”**, **“Gửi các bước/phương pháp”** biến giới hạn thành đường đi hữu ích thay vì từ chối trống.
- **[P3] G11 — Giải thích vì sao.** Cả ba câu đều nêu lý do ngay tại chỗ: mâu thuẫn với phép kiểm, hoặc **“Bài tập 3 vẫn đang mở đến 23:59”**. Thẻ **“Căn cứ”** trỏ §3.3/§3.2/§3.1 và màn hình xem trước **“Vì sao chuyển TA: Nguồn và phép kiểm mâu thuẫn”** cho phép người dùng kiểm tra quyết định. Đây cũng là PAIR *Errors + Graceful Failure*: mỗi lỗi có một đường lui phù hợp.

Ba mã `[P1]`–`[P3]` là đầu vào để §5 gắn trực tiếp lên các vùng prototype tương ứng.

### 3.7 Lỗi mà sửa câu chữ không cứu được

**KB6 — lỗi kiến trúc nguồn.** Nếu hệ thống mặc định mọi đoạn do `tra_cuu_tai_lieu` trả về là đúng, một cảnh báo viết hay hơn vẫn đặt nguồn sai vào vai trò căn cứ. Thiết kế phải tách trạng thái **“tìm thấy”** khỏi **“đã kiểm chứng”**, cho phép gắn cờ đúng đoạn, loại đoạn đang bị nghi khỏi căn cứ chắc chắn, và chuyển đoạn + phép kiểm cho TA/giảng viên; `dang_FAQ` không được chạy trước khi có xác minh.

**KB4–KB5 — lỗi guardrail tạo nội dung.** Nếu `goi_y_bai_tap` vẫn có thể sinh hoặc hiển thị đáp số, câu “không nên chép” không ngăn được thiệt hại. Thiết kế phải kiểm tra trạng thái bài **trước** khi tạo gợi ý, chặn cả đưa lẫn xác nhận đáp số, dùng gợi ý theo tầng, và chỉ mở giải thích đầy đủ sau khi bài đóng **và** đáp án đã công bố.

Các giới hạn trên là **yêu cầu UX/policy đầu vào cho Chặng 4**, không phải tuyên bố đã thiết kế xong mức tự chủ của các tool.

### 3.8 Bốn đường đi của trải nghiệm

1. **Happy path:** Khi căn cứ từ buổi đã mở không mâu thuẫn, AI giảng phần được hỏi và gắn thẻ mã mục để học viên tự mở kiểm tra.
2. **Low-confidence:** Khi câu hỏi mơ hồ như “cái độ lệch”, AI thu hẹp phạm vi bằng hai cách hiểu có căn cứ hoặc hỏi lại một câu trước khi giảng.
3. **Failure/no evidence:** Khi không có căn cứ hoặc nguồn mâu thuẫn như KB6, AI chỉ trả phần kiểm được, hiển thị giới hạn và mở đường chuyển người có xác nhận.
4. **Correction:** Khi học viên báo câu trả lời có vấn đề, AI giữ nguyên ngữ cảnh và cho chọn **“Sai ở nguồn”**, **“Sai ở phép tính”** hoặc **“Sai ở cách giải thích”**; phản hồi được đính kèm vào cùng căn cứ, không tự sửa nguồn hay tự đăng FAQ.

## §4. Mức tự chủ  (chặng 4)
Với mỗi tool:
- Mức của nhóm (tự làm / cần người duyệt / cấm). Nếu cần người duyệt: ai duyệt · người duyệt thấy gì · quá hạn thì sao.
- Lý do theo cost-of-error: sai thì ai chịu gì · đảo lại được không · chờ người thì mất gì.
- Phương án đã cân nhắc và vì sao loại.
Thêm:
- Tool khó xếp nhất: mỗi người từng chọn gì, cái giá của mỗi phía (trỏ về kịch bản ở §2), nhóm chốt thế nào.
- Thử mức đã đặt trên 2 kịch bản đắt nhất + 1 kịch bản bình thường: cái sai có bị chặn không? còn việc nào làm khi lẽ ra phải hỏi? người dùng bình thường có phải chờ vô ích không?
- Luật thêm hoặc tool tách bước (nếu có), và vì sao.
- Một mức tự chủ đã đổi lời hứa nào với người dùng.

## §5. Prototype  (chặng 5)
- Link hoặc file · công cụ · phần nào mock · có lời gọi AI thật không.
- 1–2 ảnh có đánh số; mỗi số: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào.
- Quyết định: cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ — đã nghĩ tới cách nào khác, vì sao chọn cách này.

## §6. Tốt là gì  (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)
- 3 tiêu chí Pass/Fail chấm được; thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất; lỗi còn lại.

## §7. Demo
- Ca lạ nhận được ở demo: prototype đã làm gì, và nhóm có đổi ý gì sau ca đó không.
```
