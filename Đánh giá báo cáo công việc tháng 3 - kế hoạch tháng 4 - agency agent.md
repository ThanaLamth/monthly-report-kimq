# Đánh giá báo cáo công việc tháng 3 - kế hoạch tháng 4

Ngày rà soát: 2026-05-04

## 1. Phạm vi đánh giá

Bản làm lại này không chỉ dựa trên snapshot local của `news-workflow-main` mà còn đối chiếu thêm các repo public trên GitHub profile `ThanaLamth`.

Nguồn evidence chính:
- `news-workflow-main`
- `news-flow`
- `writing-qc`
- `integrate-capture-v2`
- `new-category`
- `screaming-frow`
- `cmc-author-dashboard`
- `author-news`
- `cmc-chart-capture`

Nguyên tắc đánh giá:
- Repo/spec/tooling chỉ dùng để chứng minh `đã có hệ thống`, `đã có workflow`, `đã có module`, `đã có file xử lý`.
- Không dùng repo public để suy ra `đã rollout production`, `đã áp live toàn bộ`, hoặc `đã đạt KPI SEO`.

## 2. Điều chỉnh chính so với bản đánh giá cũ

- Phần `taxonomy/category` nay có bằng chứng mạnh hơn rất nhiều nhờ `new-category` và `screaming-frow`.
- Phần `capture ảnh unique` không còn nên mô tả như một helper nhỏ. Thực tế đã phát triển thành một `article-evidence capture engine`.
- Phần `audit` không chỉ nằm ở QC logic trong repo chính, mà đã tách thành cả một lớp `writing-qc` và cụm file audit/decision/implementation theo site.
- Phần `policy/trust` có bằng chứng live URL mạnh hơn trước, nhưng vẫn chưa đủ để xác nhận toàn bộ claim về quá trình tạo nội dung hoặc rollout đồng loạt.
- Các claim kiểu `14 sites`, `Semrush traffic`, `season/location`, `evergreen full chain` vẫn chưa có bằng chứng đủ chắc để nâng trạng thái.

## 3. Công việc/sáng kiến mới trong tháng và giá trị tạo ra

### 3.1 Chuẩn hóa QA/SEO thành skill riêng

`writing-qc` cho thấy QA bài viết đã được đóng gói thành skill portable, có knowledge base và workflow audit riêng.

Giá trị tạo ra:
- chuẩn hóa khâu review bài viết
- giảm phụ thuộc vào review cảm tính
- tăng khả năng tái sử dụng cùng một chuẩn review giữa nhiều workflow

Repo:
- https://github.com/ThanaLamth/writing-qc

### 3.2 Formal hóa kiến trúc đa repo cho news workflow

`news-flow` mô tả lại workflow theo phase rõ ràng:

`SITE IDENTITY -> RESEARCH -> DATA VISUALS PLAN -> SEO & OUTLINE -> WRITING -> WRITING-QC LOOP -> DATA VISUALS EXECUTION -> FINAL ARTICLE PATCH-UP -> THUMBNAIL -> PUBLISHING`

Giá trị tạo ra:
- giảm chồng chéo giữa viết bài, QC, capture, publish
- dễ audit artifact hơn theo từng phase
- dễ mở rộng sang worker/dashboard hoặc repo phụ trợ

Repo:
- https://github.com/ThanaLamth/news-flow

### 3.3 Xây hệ capture ảnh unique thành article-evidence engine

`integrate-capture-v2` không chỉ chụp ảnh minh họa. Repo này đã có:
- platform recommendation theo ngữ cảnh bài
- draft planning với `Required Evidence`, `Visual Needs`, `Capture Plan`, `Data Notes`
- platform health checks
- page validation
- persistent browser profile cho site có challenge
- capture metadata và caption profile theo site

`cmc-chart-capture` bổ sung utility chụp riêng chart CMC/TradingView.

Giá trị tạo ra:
- bài viết có visual riêng theo claim/dữ liệu thật
- tăng độ tin cậy và tính khác biệt của bài
- giảm phụ thuộc vào ảnh minh họa chung

Repo:
- https://github.com/ThanaLamth/integrate-capture-v2
- https://github.com/ThanaLamth/cmc-chart-capture

### 3.4 Làm full taxonomy cleanup và full SEO audit theo site

`new-category` chứng minh đã có:
- decision/remap summary
- manual review queue
- script build manual review

`screaming-frow` chứng minh đã đi xa hơn:
- full SEO audit
- url decision full
- priority 301 batch
- noindex batch
- internal-link cut batch
- next actions

Đặc biệt mạnh trên:
- Coinlineup
- Tokentopnews
- TheCCPress

Giá trị tạo ra:
- taxonomy cleanup có hệ thống
- audit không còn ở mức ghi chú rời rạc
- dễ chuyển từ phân tích sang batch triển khai

Repo:
- https://github.com/ThanaLamth/new-category
- https://github.com/ThanaLamth/screaming-frow

### 3.5 Xây workflow riêng cho CoinMarketCap coin-page

`cmc-author-dashboard` + `author-news` cho thấy đã có một nhánh vận hành riêng:
- submit CoinMarketCap coin page URL
- tạo 4 variants
- chọn variant tốt nhất
- schedule 4 bài WordPress
- log Google Sheets
- notify Telegram
- dùng `top-cmc-writer` để giữ heuristic viết bài theo coin-page

Giá trị tạo ra:
- chuẩn hóa output cho nhánh CMC
- giảm khâu thao tác tay khi craft và schedule bài
- tạo nền cho workflow theo từng coin page thay vì chỉ viết bài news chung

Repo:
- https://github.com/ThanaLamth/cmc-author-dashboard
- https://github.com/ThanaLamth/author-news

## 4. Repo ngoài phạm vi core report nhưng vẫn đáng ghi nhận

Các repo dưới đây có thật trên profile nhưng không nên cộng thẳng vào core report tháng 3/tháng 4 nếu đang đánh giá riêng workflow SEO/news system:

- `web-crawler-tool`
  Mạnh về crawl docs/blog/help center cho RAG hoặc extraction.
- `translator`
  Là skill dịch thuật có QA và kiểm soát meaning drift.
- `deep-research-coin`
  Nghiêng về deep research + on-chain verification cho coin-specific analysis.
- `x-automation`
  Nghiêng về social automation và thêm cả nhánh thử nghiệm prediction.
- `telegram-rss-art`
  Là bot RSS -> Telegram.
- `power-bank-topical-map`
  Thuộc nhánh topical map non-crypto.

Kết luận: đây là các nhánh phụ hoặc nhánh mở rộng, có thể ghi ở mục `các thử nghiệm/công việc song song`, nhưng không nên dùng để nâng KPI core report nếu không có yêu cầu riêng.

## 5. Kết luận ngắn

Nếu chỉ nhìn repo public và artifact local, điểm mạnh nhất không phải là `rollout breadth`, mà là:
- systemization
- modularization
- capture evidence
- QA/SEO gating
- taxonomy cleanup
- site-level audit batching

Phần còn yếu về bằng chứng là:
- KPI SEO kết quả
- rollout đủ 14 site
- season/location
- evergreen full chain
- bằng chứng live production trên toàn hệ
