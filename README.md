# Track 1 · Day 17 — Problem Interview Practice

> Case A: **AI Tutor – Diagnostic Refresher**

## 1. Thông tin cá nhân và nhóm

| Mục | Nội dung |
|---|---|
| MHV | 2A202602491 |
| Họ tên | Đỗ Lê Việt Anh |
| Tên nhóm | Tung Tung Tung Sahur |
| Thành viên | Đỗ Lê Việt Anh (2A202602491), Nguyễn Thị Minh Khánh (2A202602546), Nguyễn Quang Huy (2A020262421), Lại Bá Quân (2A202602495) |
| Case đã chọn | **A. AI Tutor – Diagnostic Refresher**: nút "Tôi vẫn chưa hiểu", AI chẩn đoán lỗ hổng rồi cho ôn lại khái niệm nền |
| Đối tượng phỏng vấn | Người từng bị kẹt khi học trong 7 ngày gần đây |

Cấu trúc repo:

```
├── README.md
└── interview/
    ├── notes.md          # Interview Record, lượt mình làm interviewer
    └── recording.m4a     # bản ghi đã được người được phỏng vấn đồng ý
```

---

## 2. Problem Hypothesis Brief (Chặng 1)

Nhóm chỉ được cung cấp solution. Phần dưới là chuỗi giả thuyết nhóm dựng ngược từ solution, để đi kiểm chứng. Đây chưa phải sự thật.

| Mắt xích | Giả thuyết |
|---|---|
| **Solution** | Khi người học bấm "Tôi vẫn chưa hiểu", AI hỏi vài câu để chẩn đoán khái niệm nền đang hổng, rồi đưa phần ôn ngắn cho đúng khái niệm đó. |
| **Change** | Người học tự gỡ được chỗ kẹt trong một buổi học, thay vì bỏ qua phần đó, chép đáp án hoặc bỏ dở bài. |
| **Actor** | Người tự học online (sinh viên, hoặc người đi làm học thêm), học một mình ngoài giờ, không có người để hỏi ngay lúc đó. |
| **Situation & Job** | *Khi* đã đọc hoặc xem lại một khái niệm mới 2–3 lần mà vẫn không hiểu, *tôi muốn* biết chính xác mình đang thiếu gì, *để* học tiếp được mà không mất cả buổi. |
| **Pain** | (1) Không biết mình thiếu gì, nên không biết tìm cái gì. (2) Xem lại cùng một lời giải thích không giúp được. (3) Tự tra Google/YouTube/ChatGPT tốn thời gian và lan man. (4) Ngại hỏi bạn hoặc giảng viên. (5) Bỏ qua thì lỗ hổng dồn sang bài sau. |
| **Evidence cần tìm** | Một lần kẹt cụ thể gần đây: đang học gì, đã thử những gì theo thứ tự, mất bao lâu, cuối cùng có gỡ được không và nhờ cái gì. Workaround đang dùng. Họ có từng tự quay lại học phần kiến thức cũ không. |

**Hai cách giải thích cạnh tranh (nhóm giữ cả hai khi phỏng vấn):**

- **H1, giả thuyết đứng sau solution:** Người học kẹt chủ yếu vì **thiếu kiến thức nền** (prerequisite).
- **H2, giải thích thay thế:** Nền đủ, nhưng **cách trình bày hiện tại khó hiểu** (trừu tượng, thiếu ví dụ, nhảy bước). Một nhánh khác của H2: kẹt vì **trạng thái** như mệt, mất tập trung, bị áp lực thời gian, tức là không phải vấn đề kiến thức.

**Giả thuyết bị bác bỏ khi:** Phần lớn người được phỏng vấn gỡ được chỗ kẹt nhờ *một cách giải thích khác hoặc một ví dụ* chứ không nhờ học lại kiến thức cũ, hoặc họ không thấy chỗ kẹt đủ tốn kém để phải xử lý.

---

## 3. Conversation Guide — phiên bản cuối (sau khi luyện)

### Big 3 — ba điều cần học

| # | Điều cần học | Nối với giả thuyết |
|---|---|---|
| 1 | Lần kẹt gần nhất diễn ra thế nào, và người học đã thực sự làm gì để xử lý (workaround thật) | Situation & Job, Pain |
| 2 | Điều cuối cùng giúp họ hiểu ra (hoặc thứ còn thiếu) là kiến thức nền hay cách giải thích/trạng thái | H1 và H2 |
| 3 | Chỗ kẹt đó tốn gì của họ: thời gian, cảm xúc, có bỏ dở không | Pain có đủ lớn không |

### Kịch bản (~15 phút)

**Mở đầu (1–2 phút)**
- "Mình đang tìm hiểu cách mọi người tự học, không bán hay giới thiệu sản phẩm nào. Không có câu trả lời đúng sai."
- "Mình xin phép ghi âm để xem lại sau, chỉ dùng cho bài học. Bạn đồng ý không?" → **chờ đồng ý rồi mới bật ghi âm, và hỏi lại câu đồng ý khi đã ghi.**

**Sàng lọc (1 phút)**
- "Trong 7 ngày vừa rồi bạn có học gì không? Có chỗ nào bạn đọc hoặc xem mãi mà chưa hiểu không?"

**Kể chuyện — Big 3 #1 (5–6 phút)**
- "Kể mình nghe lần gần nhất đó. Bạn đang học gì, ở đâu, khoảng mấy giờ?"
- "Lúc nhận ra mình không hiểu, việc đầu tiên bạn làm là gì?"
- "Rồi sau đó?" (hỏi lại cho đến hết chuỗi hành động)
- "Bạn đã thử ở đâu? Có mở công cụ, trang web hay hỏi ai không?"

**Đào nguyên nhân — Big 3 #2 (3–4 phút)**
- "Cuối cùng bạn có hiểu không? Cái gì làm bạn hiểu ra?"
- "Lúc hiểu ra rồi, bạn thấy lúc trước mình thiếu cái gì?"
- Nếu chưa hiểu: "Nếu phải đoán, bạn nghĩ vì sao phần đó khó với bạn?"

**Chi phí — Big 3 #3 (2 phút)**
- "Việc đó mất của bạn khoảng bao lâu?"
- "Sau đó bạn làm gì với phần đó? Học tiếp, bỏ qua hay quay lại sau?"
- "Lần gần nhất bạn bỏ qua một phần như thế là khi nào? Chuyện gì xảy ra sau đó?"

**Kết (1 phút)**
- "Có điều gì về lần đó mà mình chưa hỏi nhưng bạn thấy quan trọng không?"
- "Mình có thể liên hệ lại nếu cần hỏi thêm không?"

### Follow-up dùng khi cần
- Người kia nói chung chung ("thường thì mình…") → "Cụ thể lần đó thì sao?"
- Câu trả lời ngắn → im lặng 3–5 giây, hoặc "Rồi sao nữa?"
- Nghe thấy cảm xúc ("bực lắm", "nản") → "Lúc đó bạn bực vì điều gì?"

### Những câu đã bỏ / viết lại sau khi luyện

| Bản trước | Bản cuối | Vì sao sửa |
|---|---|---|
| "Bạn có dùng các công cụ nào để hỗ trợ không?" | "Lúc đó bạn đã mở gì ra để tìm hiểu?" | Khi luyện, câu cũ là câu có/không và nhắc sẵn "công cụ", nên chỉ gợi ra câu trả lời chung; câu mới kéo về hành động cụ thể của lần đó. |
| "Bạn có thấy thiếu kiến thức nền là vấn đề lớn không?" | "Lúc hiểu ra rồi, bạn thấy lúc trước mình thiếu cái gì?" | Câu cũ gợi ý sẵn H1; câu mới để người học tự gọi tên nguyên nhân. |
| "Bạn thường xử lý thế nào khi bị kẹt?" | "Lúc nhận ra mình không hiểu, việc đầu tiên bạn làm là gì?" | Câu cũ hỏi thói quen chung nên nhận câu trả lời chung; câu mới kéo về một lần cụ thể. |

**Quy tắc guide tuân thủ:** chỉ hỏi về một lần cụ thể trong quá khứ, không hỏi "bạn có muốn / có dùng…", không nhắc đến AI, chẩn đoán hay ôn lại khái niệm nền trước khi người kia tự nói ra.

---

## 4. Practice Reflection (Chặng 4)

**1. Câu hỏi nào đã giúp user kể một tình huống cụ thể?**

Câu "Lúc nhận ra mình không hiểu, việc đầu tiên bạn làm là gì?" đã giúp người được phỏng vấn (một học viên khoá 3) kể một tình huống cụ thể: anh đang ôn lại bài trên Vlearn, gặp nhiều keyword chuyên ngành và khái niệm trên lớp không nói rõ, rồi tra Google, đọc bài báo, xem YouTube và hỏi AI (ChatGPT, Gemini) để giải thích lại. Anh nói mất 30 phút đến 1 tiếng cho một khái niệm và thấy nản.

**2. Chỗ nào mình cần làm tốt hơn ở lần phỏng vấn thật?**

Mình đã hỏi "Bạn có dùng các công cụ nào để hỗ trợ không?", là câu có/không và nhắc sẵn "công cụ", nên gợi ý đáp án thay vì để họ tự kể. Ở lần thật mình sẽ hỏi "Lúc đó bạn đã mở gì ra để tìm hiểu?". Ngoài ra bản ghi chỉ dài khoảng 1,5 phút, ngắn hơn nhiều so với kịch bản 15 phút: mình chưa đào sâu được việc "thiếu nền hay cách trình bày" (ví dụ hỏi thêm "viết tắt nào cụ thể?") và chưa hỏi lần gần nhất bỏ qua một phần là khi nào.

**3. Sau khi luyện, nhóm đã sửa Conversation Guide ở đâu và vì sao?**

Nhóm đã sửa ba câu trong bảng "Những câu đã bỏ / viết lại" ở mục 3. Cả ba đều bỏ câu gợi ý sẵn đáp án hoặc hỏi thói quen chung, thay bằng câu kéo người học về một lần cụ thể và để họ tự gọi tên nguyên nhân: (1) "thiếu kiến thức nền là vấn đề lớn không?" → "Lúc hiểu ra rồi, bạn thấy lúc trước mình thiếu cái gì?"; (2) "Bạn thường xử lý thế nào khi bị kẹt?" → "Lúc nhận ra mình không hiểu, việc đầu tiên bạn làm là gì?"; (3) "Bạn có dùng các công cụ nào để hỗ trợ không?" → "Lúc đó bạn đã mở gì ra để tìm hiểu?".

---

## 5. AI Support Log

| Bước | AI đã giúp gì | Điểm sai / hời hợt | Mình đã tự sửa thế nào |
|---|---|---|---|
| Chặng 1 | Gợi ý khung chuỗi Solution → Evidence và hai giả thuyết cạnh tranh H1/H2 | Actor ban đầu quá rộng ("người tự học online"); Pain có nguy cơ viết theo hướng solution ("không có công cụ chẩn đoán") | Thu hẹp actor thành người đang ôn lại bài sau buổi học và bị kẹt ở một khái niệm cụ thể; viết lại pain theo hành vi đã quan sát (tra nhiều nguồn, mất thời gian) thay vì theo thứ solution đang thiếu |
| Chặng 2 | Gợi ý Big 3, khung guide và bảng đổi câu dẫn dắt sang câu trung lập | Một số câu mẫu vẫn còn gợi ý H1 (nhắc "kiến thức nền") | Viết lại để người học tự nêu nguyên nhân (xem mục 3) |
| Chặng 4 | Dựng cấu trúc repo, README và mẫu Interview Record | AI không nghe được bản ghi nên không viết được notes và reflection | Tự điền notes, reflection từ trải nghiệm phỏng vấn thật |
| Điền README | Đối chiếu `notes.md` với các mục còn trống và soạn nội dung cho Practice Reflection, bảng câu đã sửa | AI không nghe được bản ghi nên chỉ dựa vào notes mình ghi | Tự nghe lại bản ghi, ghi notes và quote có mốc thời gian, rồi kiểm tra lại nội dung AI soạn |
