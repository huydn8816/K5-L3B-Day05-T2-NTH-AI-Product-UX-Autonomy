# Bài nộp LAB5 — T2 · Nhóm NTH

**Lớp:** L3B · **Bàn / zone:** ____ · **Track:** T2

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| Đặng Nhật Huy | 2A202603822 | Chặng 1: Lát cắt & phạm vi (§1) · Chặng 2: Kịch bản rủi ro (§2) |
| Chu Văn Nhật | 2A202603848 | Chặng 4: Mức tự chủ (§4 · Bảng phân mức 4 tools, lập luận cost-of-error, tool khó xếp nhất, guardrails) |
| [Chờ cập nhật - Trình] | ... | Chặng 3: Khi AI sai (§3) & Hỗ trợ demo |

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
*(Phần của thành viên phụ trách Chặng 3)*
Với mỗi kịch bản đắt nhất:
- AI nói gì (nguyên văn) · người dùng thấy gì · làm gì tiếp · ai được báo, sau bao lâu.
- Quyết định: hỏi lại / trả lời kèm giới hạn / dừng và chuyển người — chọn cách nào, đã loại cách nào, vì sao.
- Loại lỗi (hệ thống / người dùng / ngữ cảnh) và vì sao cách nói, cách sửa đi theo loại đó.
- 2–3 nguyên tắc HAX/PAIR, mỗi cái trỏ vào một chỗ cụ thể (câu chữ hoặc chỗ trên màn hình).
- Lỗi nào sửa câu chữ không cứu được (nếu có), và thiết kế cứu nó thế nào.

## §4. Mức tự chủ  (chặng 4)
*Người phụ trách: Chu Văn Nhật*

### 1. Phân loại mức tự chủ cho 4 Tools theo Cost-of-error

| Tool | Mức tự chủ | Người duyệt & Giao diện (nếu có) | Lập luận theo Cái giá khi sai (Cost-of-Error) | Phương án đã cân nhắc & Lý do loại |
|---|---|---|---|---|
| `tra_cuu_tai_lieu` | **Tự làm** | Không cần duyệt. AI tự động truy xuất tài liệu Buổi 3 và trích dẫn theo mã mục (§3.1 – §3.5). | - **Sai thì rẻ:** Đây là tác vụ chỉ đọc (read-only), không làm thay đổi trạng thái hệ thống.<br>- **Đảo ngược được:** Học viên nhìn thấy trích dẫn nguồn ngay cạnh câu trả lời. Nếu AI trích nhầm, học viên đọc thấy lạc đề sẽ hỏi lại ngay.<br>- **Nếu chờ người duyệt:** Mất hoàn toàn giá trị của trợ lý đêm muộn; học viên bị gián đoạn việc học lúc 23h đêm. | - **Cân nhắc:** Bắt TA duyệt trước khi gửi đoạn trích.<br>- **Loại vì:** Quá tải cho TA và học viên phải chờ đến sáng hôm sau chỉ để đọc lại một mục lý thuyết. |
| `goi_y_bai_tap` | **Tự làm (kèm Rào chắn / Guardrails)** | Không cần TA duyệt từng câu, nhưng áp dụng luật kiểm tra điều kiện tự động: Cấm đưa công thức thế số và kết quả cho bài tập đang mở. | - **Sai thì cực đắt nếu lộ đáp án:** Đối với bài tập đang mở tính điểm (Bài tập 3 - hạn 13/11 23:59), nếu AI đưa đáp án thì học viên chép ngay. Lỗi này **không thể đảo ngược** (học viên đã nhìn thấy đáp số thì không thể thu hồi trí nhớ).<br>- **Nếu cấm hoặc chờ TA duyệt:** Học viên bị bế tắc hoàn toàn khi làm bài tối muộn.<br>- **Giải pháp tối ưu:** Cho AI tự động trả lời nhưng ép chạy ở chế độ Socratic (chỉ đặt câu hỏi gợi mở, gợi ý đọc lại mục lý thuyết liên quan). | - **Cân nhắc:** Cho AI tự do giải bài tập để hỗ trợ tối đa.<br>- **Loại vì:** Biến trợ lý học tập thành công cụ làm bài hộ, phá vỡ tính liêm chính học thuật. |
| `chuyen_TA` | **Tự làm** | AI tự động gom ngữ cảnh (câu hỏi, đoạn hội thoại, lý do chuyển) và tạo vé (ticket) vào hàng đợi của TA lúc 08:00 sáng. | - **Sai thì rẻ & dễ đảo ngược:** Việc tạo vé chỉ là thông báo nội bộ. Nếu AI chuyển nhầm câu hỏi đơn giản, TA chỉ mất 5 giây bấm đóng vé.<br>- **Không tạo gánh nặng cho học viên:** Giúp học viên an tâm đi ngủ vì biết chắc thắc mắc của mình đã được ghi nhận và có lịch phản hồi cụ thể (08:00 sáng hôm sau). | - **Cân nhắc:** Bắt học viên phải bấm xác nhận "Bạn có muốn chuyển TA không?".<br>- **Loại vì:** Tạo thêm bước cản trở không cần thiết khi học viên đã gặp khó khăn bế tắc. |
| `dang_FAQ` | **Cần người duyệt** | **Ai duyệt:** TA trực tiếp bấm duyệt trên Dashboard quản trị.<br>**Người duyệt thấy gì:** Câu hỏi của học viên + Câu trả lời đề xuất của AI + Đoạn trích đối chiếu giáo trình.<br>**Nếu quá hạn (sau 24h):** Bản ghi tự động lưu ở trạng thái nháp (Draft), tuyệt đối không tự ý xuất bản. | - **Sai thì đắt và lây lan diện rộng:** FAQ là nơi toàn bộ lớp học (hàng chục/hàng trăm người) cùng truy cập. Nếu AI đăng câu trả lời sai (do tài liệu §3.3 có lỗi) hoặc đăng cách giải Bài tập 3 đang mở, lỗi sẽ phát tán ra cả lớp.<br>- **Khó đảo ngược:** Dù sau đó có gỡ bài thì học viên đã đọc hoặc chụp màn hình lưu lại, gây mất uy tín học thuật nghiêm trọng. | - **Cân nhắc:** Cho AI tự động đăng lên FAQ nếu câu hỏi được hỏi lại nhiều lần trong đêm.<br>- **Loại vì:** Cái giá của việc lan truyền kiến thức sai cho cả lớp lớn hơn rất nhiều so với sự tiện lợi tức thì. |

---

### 2. Tool khó xếp nhất trong nhóm: `dang_FAQ`

- **Tranh luận nội bộ:**
  - *Phương án 1 (Tự làm):* Có ý kiến muốn để `dang_FAQ` tự động xuất bản vì vào ban đêm, nhiều học viên cùng vấp ở một câu hỏi; nếu đăng ngay thì các bạn khác không phải hỏi lại, giảm tải cho hệ thống.
  - *Phương án 2 (Cấm hoàn toàn):* AI không phải giảng viên, không có thẩm quyền phát ngôn kiến thức chính thức cho khóa học.
- **Cái giá của mỗi phía (chiếu theo kịch bản ở §2):**
  - Nếu chọn *Tự làm*: Gặp ngay **Kịch bản đắt 1 (KB6)** (§3.3 tài liệu sai toán học). AI tin tài liệu sai nên đăng bài giải thích sai lên FAQ -> Cả lớp học sai theo -> Thảm họa về chất lượng đào tạo.
  - Nếu chọn *Cấm*: Lãng phí khả năng tổng hợp câu hỏi hay của AI, TA sáng hôm sau phải tự lọc lại hàng trăm tin nhắn thủ công.
- **Cách nhóm chốt:**
  - Nhóm chọn giải pháp **Cần người duyệt (TA duyệt)**. AI đóng vai trò "người soạn thảo nội dung", TA giữ vai trò "người biên tập xuất bản". Việc này giữ trọn cả hai giá trị: AI giúp chuẩn bị sẵn bài viết, còn TA đảm bảo tính chính xác 100% trước khi truyền thông ra toàn khóa học.

---

### 3. Thử nghiệm mức tự chủ trên 3 kịch bản

1. **Kịch bản đắt 1 (KB6): Tài liệu §3.3 bị sai toán học ("độ lệch chuẩn luôn nhỏ hơn phương sai"):**
   - *Cái sai có bị chặn không?* **CÓ.** Khi học viên thắc mắc về điểm mâu thuẫn này, `tra_cuu_tai_lieu` trích nguyên văn để học viên đối chiếu, AI không bịa thêm mà gọi `chuyen_TA` (Tự làm) để báo giảng viên. Hành động `dang_FAQ` bị chặn lại ở trạng thái Chờ duyệt, lỗi sai được cô lập hoàn toàn, không lây lan ra lớp học.
2. **Kịch bản đắt 2 (KB4 + KB5): Học viên hỏi xin đáp số Bài tập 3 (bài đang mở tính điểm):**
   - *AI có làm việc khi lẽ ra phải hỏi không?* **KHÔNG.** Rào chắn của `goi_y_bai_tap` kích hoạt ngay lập tức: Chặn đứng hành vi tính toán hộ tiền lương điển hình, chuyển thành câu hỏi gợi ý ôn tập mục §3.2 (so sánh trung bình và trung vị khi có giá trị ngoại lai 45).
3. **Kịch bản bình thường: Học viên hỏi lý thuyết lúc 23h "Trung vị khác trung bình ở chỗ nào?" (KB1):**
   - *Người dùng bình thường có phải chờ vô ích không?* **KHÔNG.** AI tự động gọi `tra_cuu_tai_lieu` và trả lời ngay trong 3 giây kèm trích đoạn §3.1 và §3.2. Người dùng tiếp tục học bình thường mà không cần đợi TA phê duyệt.

---

### 4. Luật bổ sung & Tách bước công cụ (Guardrails)

- **Tách bước cho `goi_y_bai_tap`:**
  - **Bước 1 — Phân loại trạng thái bài tập (Status Check):**
    - Nếu là bài tập đã hết hạn (Bài tập 2 - hạn 06/11): Cho phép hiển thị giải thích chi tiết và đối chiếu đáp số chính thức (Đáp án: 6).
    - Nếu là bài tập đang mở (Bài tập 3 - hạn 13/11 23:59): Kích hoạt chế độ Socratic: Chỉ đưa câu hỏi định hướng tư duy, ẩn toàn bộ nút giải hộ hoặc công thức tính sẵn.
  - **Bước 2 — Giới hạn độ dài gợi ý:** Mỗi lần gợi ý không quá 3 câu để tránh việc AI vô tình viết thành bài giải hoàn chỉnh.

---

### 5. Mức tự chủ đã thay đổi Lời hứa sản phẩm như thế nào?

- **Khi chưa có kiểm soát (AI tự do):** Lời hứa là *"Trợ lý vạn năng giải quyết mọi thắc mắc ngay lập tức"* -> Lời hứa này dễ vỡ trận khi gặp bài kiểm tra hoặc tài liệu sai sót, biến trợ lý thành công cụ gian lận hoặc phát tán tin sai.
- **Khi áp dụng mức tự chủ có kiểm soát của nhóm:** Lời hứa đổi thành:
  > *"Người bạn đồng hành học tập ban đêm, giúp bạn tự thông suốt tư duy, đảm bảo học đúng chuẩn giáo trình và cam kết mọi vấn đề phức tạp luôn được Trợ giảng giải đáp vào đầu giờ sáng hôm sau."*

---

## §5. Prototype (Chặng 5)
*(Phần của thành viên phụ trách Prototype)*

- Link hoặc file · công cụ · phần nào mock · có lời gọi AI thật không.
- 1–2 ảnh có đánh số; mỗi số: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào.
- Quyết định: cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ — đã nghĩ tới cách nào khác, vì sao chọn cách này.

---

## §6. Tốt là gì (Chặng 6 — nhẹ, bỏ được nếu thiếu giờ)
- 3 tiêu chí Pass/Fail chấm được; thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất; lỗi còn lại.

---

## §7. Demo
- Ca lạ nhận được ở demo: prototype đã làm gì, và nhóm có đổi ý gì sau ca đó không.
