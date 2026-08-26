# 🎓 VinUniversity AI Talent Program — Track 1: AI Product Management
## Day 24: AI Product Financial Model & Unit Economics Lab!

> **Brief (Triết lý bài học):** Một sản phẩm AI có RAG/Agent chạy mượt ở Day 23 mới chỉ là thành công về kỹ thuật. Để sản phẩm sống sót và tăng trưởng thương mại, PM/Founder bắt buộc phải giải bài toán tài chính: Tính đúng chi phí biến đổi COGS (đặc biệt là AI Hidden Costs), làm chủ Unit Economics (CAC, LTV, Gross Margin), và thực hiện stress-test dòng tiền 3 kịch bản (Optimistic, Base, Pessimistic) để chứng minh khả năng sinh tồn (Runway ≥ 12 tháng).

---

## 🎯 1. Tiêu Đề & Mục Tiêu Tổng Quan (Header & Objectives)

### Mục Tiêu Đầu Ra (Outcomes & Objectives):
Sau khi hoàn thành bài lab này, học viên sẽ đạt được:
- [x] **Cost Architecture:** Xác định đủ 5 cấu phần chi phí sản phẩm AI, đặc biệt là **AI Hidden Costs** (Data Labeling, Model Retraining ~20%/năm, Human QA, Compliance).
- [x] **Unit Economics Mastery:** Tính toán chính xác **LTV dựa trên Gross Profit** (không lấy Revenue thô), tỷ lệ **LTV/CAC > 3.0** và **CAC Payback Period < 12 tháng**.
- [x] **Scenario Stress-Testing:** Thiết lập giả định 3 kịch bản (Optimistic, Base, Pessimistic với shock factor ≥ 1.5x Churn & CAC) trên Excel 3-Tab để đảm bảo **Pessimistic Runway ≥ 12 tháng**.
- [x] **Investor Decision Note:** Viết báo cáo lập luận 200–300 từ bảo vệ logic chọn ARPU, CAC và phương án ứng phó rủi ro tài chính trước hội đồng đầu tư.

---

## ⚙️ 2. Hướng Dẫn Thiết Lập & Môi Trường (Setup & Prerequisites)

### Yêu cầu Công cụ & Môi trường:
* **Phần mềm xử lý bảng tính:** Microsoft Excel 2016+ (khuyên dùng) hoặc Google Sheets.
* **Trình duyệt Web:** Chrome, Edge, Safari (để xem Slide Deck tương tác 90 phút tại `slides/index.html`).
* **Quản lý mã nguồn:** Git & Tài khoản GitHub cá nhân.

### Clone Starter Repo bài tập:
```bash
git clone https://github.com/VinUni-AI20k/Day24-Track1-AI-Product-Financial-Model-Lab.git
cd Day24-Track1-AI-Product-Financial-Model-Lab
```

### Quy tắc Sử dụng AI Assistance (AI Ethics Policy):
* **ĐƯỢC DÙNG AI (Cursor/Claude/ChatGPT):** Để hỏi khái niệm, tra cứu benchmark ARPU/CAC/Churn ngành SaaS/AI tương đương, hoặc nhờ AI gợi ý khung câu hỏi tư duy.
* **KHÔNG ĐƯỢC DÙNG AI:** Để nhờ AI điền thay 100% số liệu tài chính hoặc bịa số ảo để vượt qua các checkpoint kiểm tra.

---

## 📂 3. Sơ Đồ Cấu Trúc Thư Mục (Repository Structure)

```text
Day24-Track1-AI-Product-Financial-Model-Lab/
├── README.md                              # ★ BẠN VIẾT DECISION NOTE & GHI THÔNG TIN BÀI NỘP
├── Day24-AI-Product-Finance-Model.xlsx    # ★ BẠN IMPLEMENT (Điền giả định 3-Tab Excel)
├── Day24-AI-Product-Handbook.pdf          # Tài liệu Handbook tra cứu Benchmark tài chính AI
├── .gitignore                             # Cấu hình ẩn file tạm & dotfiles hệ thống
└── slides/                                # THƯ MỤC SLIDE DECK TƯƠNG TÁC (90 PHÚT)
    ├── index.html                         # Mở trình duyệt xem Slide hướng dẫn từng Phase
    ├── css/
    │   └── styles.css                     # Hiệu ứng Glassmorphic Dark Mode UI
    └── js/
        ├── data.js                        # Dữ liệu 5 Phase bài Lab
        ├── timer.js                       # Bộ đếm thời gian thực tế
        └── slides.js                      # Điều hướng Slide & Dynamic Island
```

---

## ⏳ 4. Khung Lộ Trình Thực Hiện (Phases & Checkpoints)

Thời lượng thực hành: **90 phút (14h00 – 15h30)**. Bài học chia thành 5 Phase nối tiếp:

```text
Phase 0: Phạm vi & Pricing (10') ➔ Phase 1: Giả định Tab 1 (20') ➔ Phase 2: Unit Economics Tab 2 (15')
➔ Phase 3: Stress-test P&L Tab 3 (20') ➔ Phase 4: Decision Note & Nộp bài (25')
```

| Phase | Thời lượng | Công việc chính | Checkpoint / Điều kiện qua Gate |
|---|---:|---|---|
| **Phase 0** | 10 phút | Khai báo dự án (nhóm Build Phase hoặc cá nhân), Persona & Chọn mô hình **Hybrid Pricing**. | **Gate 0:** Chốt rõ mô hình thu tiền có phí cố định + phí usage. |
| **Phase 1** | 20 phút | Mở Tab 1 Excel, điền 100% ô màu vàng cả 3 kịch bản. | **Gate 1:** `AI Hidden Costs >= 30% API Cost`; Pessimistic Churn/CAC ≥ 1.5x Base. |
| **Phase 2** | 15 phút | Mở Tab 2, kiểm tra 4 chỉ số Unit Economics ở cột Base. | **Gate 2:** Base `LTV/CAC > 3.0` (tính trên Gross Margin %) & `Payback < 12m`. |
| **Phase 3** | 20 phút | Mở Tab 3, đổi ô C4 sang `Pessimistic`, soi dòng Cash Position. | **Gate 3:** Base `NPV > 0`, `IRR >= 20%`; `Pessimistic Runway >= 12 tháng`. |
| **Phase 4** | 25 phút | Viết **Decision Note (200–300 từ)** bảo vệ giả định vào README.md. | **Gate 4:** Quyết định tài chính có benchmark dẫn chứng & Plan B rõ ràng. |

---

## 📊 5. Tiêu Chí Đánh Giá & Bảng Điểm (Grading Rubric)

Bài làm được đánh giá trên thang điểm **100** phân bổ theo 5 Gates:

| Hạng mục đánh giá | Trọng số | Tiêu chí đạt điểm tối đa (100%) | Dấu hiệu bị trừ điểm / 0 điểm |
|---|---:|---|---|
| **1. Giả định Tab 1** | 30 điểm | Điền 100% ô màu vàng cả 3 kịch bản. `AI Hidden Costs >= 30% API Cost`. | Bỏ trống ô màu vàng, hoặc điền Hidden Costs = 0. |
| **2. AI Cost Awareness** | 25 điểm | Tính đủ 5 cấu phần chi phí: Labeling, Retraining (~20%), QA, Server, API. | Chỉ tính API cost OpenAI mà quên chi phí retrain/QA. |
| **3. Unit Economics (Tab 2)** | 20 điểm | LTV tính đúng bằng Gross Profit. Base `LTV/CAC > 3.0` và `Payback < 12m`. | LTV tính bằng Revenue thô, hoặc `LTV/CAC < 3.0`. |
| **4. Stress-testing (Tab 3)** | 15 điểm | Kịch bản Pessimistic có shock ≥ 1.5x, `Pessimistic Runway >= 12 tháng`. | Pessimistic copy nguyên từ Base, hoặc Tiền mặt bị âm. |
| **5. Decision Note & Format** | 10 điểm | Decision Note có căn cứ/benchmark rõ ràng, nộp đúng quy chuẩn repo cá nhân. | Viết mơ hồ, không có căn cứ, nộp sai tên file. |
| **⭐ BONUS POINTS** | **+10 điểm** | Bổ sung bảng Phân tích độ nhạy (Sensitivity Analysis) giữa ARPU và Churn. | Không bắt buộc. |

---

## 📌 6. Quy Chuẩn Nộp Bài & Bàn Giao (Submission Guidelines & Deliverables)

### Danh sách sản phẩm bàn giao (Deliverables):
1. File Excel `[MSSV]_[HoVaTen]_Day24.xlsx` hoàn thiện 3-Tab.
2. File `README.md` điền đầy đủ Họ tên, MSSV, Tên dự án (nhóm Build Phase hoặc cá nhân) và đoạn văn **Decision Note**.

### Quy ước Đặt tên Repo & File:

Mỗi học viên tạo một **Repository Cá Nhân trên GitHub** và nộp link vào hệ thống VLearn:

* **Tên GitHub Repository cá nhân:** `Track1-Day24-MHV-[MSSV]-[HoVaTen]`  
  *(Ví dụ: `Track1-Day24-MHV-20261234-NguyenVanA`)*
* **Tên file Excel nộp bài:** `[MSSV]_[HoVaTen]_Day24.xlsx`  
  *(Ví dụ: `20261234_NguyenVanA_Day24.xlsx`)*

```text
Track1-Day24-MHV-[MSSV]-[HoVaTen]/
├── README.md               # Họ tên, MSSV, Tên dự án (Build Phase / cá nhân) & Decision Note
└── [MSSV]_[HoVaTen]_Day24.xlsx # File Excel tài chính 3 Tabs đã hoàn thành
```

### Pre-submission Checklist (Rà soát 6 bước trước khi nộp):
- [x] 1. Khai báo rõ Họ tên, MSSV và Tên dự án (nhóm Build Phase hoặc cá nhân) trong `README.md`.
- [x] 2. File Excel đã điền 100% ô màu vàng cả 3 kịch bản tại Tab 1.
- [x] 3. Đã đảm bảo `AI Hidden Costs >= 30% API Cost` (không để bằng 0).
- [x] 4. Tab 2 Base LTV/CAC > 3.0 và CAC Payback < 12 tháng (tính trên Gross Margin).
- [x] 5. Tab 3 khi đổi sang `Pessimistic` đảm bảo Runway ≥ 12 tháng (Cash Position không bị âm).
- [x] 6. Viết xong đoạn văn **Decision Note (200–300 từ)** bảo vệ mô hình trong `README.md`.

---

### 🏛️ VinUniversity Codelab
* **Program:** AI Talent Incubation (Cohort 2026)
* **Track:** Track 1 — AI Product Management

### 📝 5. Thông tin người thực hiện & Khai báo Phase 0
* **Họ và tên:** Phạm Bá Huy
* **MSSV:** 2A202601132
* **Tên dự án:** HPTravelAI — Trợ lý AI du lịch & Hướng dẫn viên văn hóa bản địa thông minh
* **Target Persona (Khách hàng mục tiêu):** 
  * Khách du lịch tự túc (Free Independent Travelers - FIT), giới trẻ và người yêu thích du lịch trải nghiệm, khám phá sâu sắc văn hóa, ẩm thực, lịch sử Việt Nam.
  * Sẵn sàng chi trả cho trải nghiệm cá nhân hóa, tiết kiệm thời gian lên lịch trình và cần trợ lý ảo hướng dẫn thời gian thực tại điểm đến.
* **TAM (Total Addressable Market - Quy mô thị trường):**
  * Ước tính **500.000** người dùng du lịch tự túc có thói quen sử dụng ứng dụng số và chi trả cho dịch vụ du lịch thông minh tại Việt Nam.
* **Mô hình định giá (Pricing Model):** **Hybrid Pricing** (Bảo vệ biên lợi nhuận, chống bẫy lỗ do Power Users)
  * **Phí cố định (Base Subscription):** `149.000 VND / tháng` (bao gồm: Tạo lịch trình AI không giới hạn, 50 lượt hỏi đáp Audio Tour tại các di tích văn hóa).
  * **Phí sử dụng bổ sung (Usage Overage):** `2.000 VND / lượt` truy vấn Audio Guide / RAG thời gian thực vượt hạn mức.
  * **ARPU trung bình kỳ vọng (Base):** `159.000 VND / khách / tháng` (đã gồm Base Subscription + Usage trung bình).

---

### 📊 6. Investor Decision Note (Báo cáo Lập luận & Bảo vệ Mô hình Tài chính)

**1. Căn cứ lựa chọn ARPU & CAC:**
Mức ARPU kỳ vọng ở kịch bản Base (159.000 VND/tháng) được xây dựng theo mô hình **Hybrid Pricing** (gói cơ bản 149.000 VND + phí overage 2.000 VND/lượt truy vấn mở rộng). Mức giá này chỉ bằng 1/5 chi phí thuê hướng dẫn viên du lịch truyền thống, tạo rào cản chuyển đổi thấp cho tệp khách du lịch tự túc (FIT) nhưng vẫn bảo vệ biên lợi nhuận gộp ở mức an toàn **66.2%**. Mức CAC 320.000 VND được tối ưu hóa thông qua chiến lược Product-Led Growth (cho phép người dùng tạo miễn phí 1 lịch trình đầu tiên) kết hợp kênh liên kết đối tác Homestay/OTA, mang lại tỷ lệ **LTV/CAC đạt 4.11x** (vượt chuẩn vàng 3.0x của VC) và thời gian thu hồi vốn **CAC Payback cực nhanh chỉ 3.04 tháng** (< 12 tháng).

**2. Giải trình cơ cấu Chi phí ẩn (AI Hidden Costs):**
Nhận thức rõ cạm bẫy chi phí của các sản phẩm GenAI, dự án trích lập **40.000 VND/khách/tháng** cho AI Hidden Costs (chiếm 454.5% chi phí API), phân bổ vào 3 trụ cột: (i) *Data Labeling:* Chuẩn hóa dữ liệu điểm đến, di tích lịch sử và ẩm thực địa phương; (ii) *Model Retraining (~20%/năm):* Cập nhật định kỳ thông tin giá vé, tuyến điểm mới và sự kiện mùa lễ hội; (iii) *Human QA & Guardrails:* Kiểm duyệt thủ công để loại bỏ hoàn toàn hiện tượng "ảo giác" (hallucination) về kiến thức văn hóa và lịch sử.

**3. Đánh giá sức khỏe tài chính & Kế hoạch ứng phó (Plan B):**
Ở kịch bản Base, dự án tạo ra giá trị bền vững với **NPV dương 301.4 triệu VND** và IRR > 20%. Trong trường hợp thị trường gặp khủng hoảng (kịch bản Pessimistic: Churn tăng vọt lên 15%, CAC đắt đỏ 480.000 VND), quỹ tiền mặt dự trữ 1.2 tỷ VND vẫn đảm bảo **Runway an toàn đạt 15 tháng** (vượt tiêu chuẩn ≥ 12 tháng). Để ứng phó, team kích hoạt **Plan B**: (1) Cắt giảm chi phí cố định (lương và vận hành) từ 75 triệu xuống 35 triệu/tháng; (2) Tối ưu hóa hạ tầng AI bằng cách áp dụng Semantic Caching cho các câu hỏi phổ biến và chuyển các tác vụ đơn giản sang mô hình Small LLM (như GPT-4o-mini / Gemini Flash) để giảm thêm 40% chi phí biến đổi COGS.



