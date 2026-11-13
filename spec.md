# Bài nộp LAB5 — Track T2: Giáo dục · Nhóm NTH

## Thành viên nhóm

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| Chu Văn Nhật | 2A202603848 | **Chặng 4: Mức tự chủ** (§4 · Bảng phân mức 4 tools, lập luận cost-of-error, tool khó xếp nhất, thử nghiệm kịch bản & guardrails) |
| [Đang cập nhật - Trình] | ... | [Chặng 1, 2, 3: Lát cắt, kịch bản rủi ro & ứng xử khi AI sai] |
| [Đang cập nhật - Huy] | ... | [Chặng 5, 6, 7: Thiết kế Prototype, tiêu chí nghiệm thu & Demo] |

---

## §1. Lát cắt & phạm vi
*(Phần của thành viên phụ trách Chặng 1)*

- **Lát cắt:** Trong trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode), khi học viên đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên", để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.
- **3 việc tính năng KHÔNG làm:**
  1. ...
  2. ...
  3. ...

---

## §2. Kịch bản rủi ro (Chặng 2)
*(Phần của thành viên phụ trách Chặng 2)*

- Bảng kịch bản rủi ro (≥8 kịch bản đủ 4 lớp ①②③④)...
- 2 kịch bản đắt nhất:
  - **Kịch bản đắt 1:** Lỗi mâu thuẫn tài liệu buổi 3 (§3.3 viết sai toán học "độ lệch chuẩn luôn nhỏ hơn phương sai").
  - **Kịch bản đắt 2:** Học viên đòi giải Bài tập 3 (đang mở hạn đến 23:59 ngày 13/11).

---

## §3. Khi AI sai (Chặng 3)
*(Phần của thành viên phụ trách Chặng 3)*

- Xử lý 2 kịch bản đắt nhất...

---

## §4. Mức tự chủ (Chặng 4)
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
  - Nếu chọn *Tự làm*: Gặp ngay **Kịch bản đắt 1** (§3.3 tài liệu sai toán học). AI tin tài liệu sai nên đăng bài giải thích sai lên FAQ -> Cả lớp học sai theo -> Thảm họa về chất lượng đào tạo.
  - Nếu chọn *Cấm*: Lãng phí khả năng tổng hợp câu hỏi hay của AI, TA sáng hôm sau phải tự lọc lại hàng trăm tin nhắn thủ công.
- **Cách nhóm chốt:**
  - Nhóm chọn giải pháp **Cần người duyệt (TA duyệt)**. AI đóng vai trò "người soạn thảo nội dung", TA giữ vai trò "người biên tập xuất bản". Việc này giữ trọn cả hai giá trị: AI giúp chuẩn bị sẵn bài viết, còn TA đảm bảo tính chính xác 100% trước khi truyền thông ra toàn khóa học.

---

### 3. Thử nghiệm mức tự chủ trên 3 kịch bản

1. **Kịch bản đắt 1: Tài liệu §3.3 bị sai toán học ("độ lệch chuẩn luôn nhỏ hơn phương sai"):**
   - *Cái sai có bị chặn không?* **CÓ.** Khi học viên thắc mắc về điểm mâu thuẫn này, `tra_cuu_tai_lieu` trích nguyên văn để học viên đối chiếu, AI không bịa thêm mà gọi `chuyen_TA` (Tự làm) để báo giảng viên. Hành động `dang_FAQ` bị chặn lại ở trạng thái Chờ duyệt, lỗi sai được cô lập hoàn toàn, không lây lan ra lớp học.
2. **Kịch bản đắt 2: Học viên hỏi xin đáp số Bài tập 3 (bài đang mở tính điểm):**
   - *AI có làm việc khi lẽ ra phải hỏi không?* **KHÔNG.** Rào chắn của `goi_y_bai_tap` kích hoạt ngay lập tức: Chặn đứng hành vi tính toán hộ tiền lương điển hình, chuyển thành câu hỏi gợi ý ôn tập mục §3.2 (so sánh trung bình và trung vị khi có giá trị ngoại lai 45).
3. **Kịch bản bình thường: Học viên hỏi lý thuyết lúc 23h "Trung vị khác trung bình ở chỗ nào?":**
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

- Link / File: `prototype/index.html`
- Mô tả màn hình & các số đánh dấu tương ứng HAX/PAIR...

---

## §6. Tốt là gì (Chặng 6)
*(Tiêu chí Pass/Fail)*

1. Tiêu chí 1: ...
2. Tiêu chí 2: ...
3. Tiêu chí 3: ...

---

## §7. Demo
*(Kịch bản demo và xử lý ca lạ)*
