# Báo cáo tháng 4 và kế hoạch tháng 5 - 1 trang cho sếp

## 1. Tóm tắt điều hành

- Tháng báo cáo: `Tháng 4/2026`
- Người thực hiện: `Thana`
- Điểm tổng quan: `7.2/10`
- Kết luận ngắn: `Đúng hướng nhưng cần chuyển mạnh từ repo/tooling sang vận hành thật và KPI có bằng chứng`

Trong tháng 4, trọng tâm chính là:

- chuẩn hóa `news workflow` và `QC loop`
- mở rộng `capture ảnh unique / article-evidence`
- làm sâu `technical SEO / taxonomy / audit batching`

## 2. Kết quả nổi bật

- Đã hình thành hệ `workflow` khá rõ giữa `news-flow`, `writing-qc`, `integrate-capture-v2`, `author-news`, `cmc-author-dashboard`.
- Đã làm sâu phần `taxonomy cleanup` và `SEO audit` cho `Coinlineup`, `Tokentopnews`, `TheCCPress`, bao gồm decision/remap/manual review và các batch triển khai ưu tiên.
- Đã nâng `capture ảnh unique` từ utility chụp ảnh thành `article-evidence engine`, có planning, health check, persistent profile và utility chụp chart riêng.

Giá trị tạo ra:

- tăng mức hệ thống hóa và khả năng scale
- giảm phụ thuộc vào xử lý tay rời rạc
- tăng độ tin cậy của bài viết, audit và artifact

## 3. Phần đã làm được theo kế hoạch

- Đã đi rất xa ở trục `workflow`, `QC`, `capture`, `taxonomy`, `audit`.
- Đã có thêm nhánh `CoinMarketCap author workflow` với dashboard, multi-variant article craft, WordPress scheduling, Google Sheets và Telegram notify.
- Đã có thêm một số công việc ngoài report nhưng có giá trị thật như `bulk hulk`, `deep-research-coin`, `cmc-chart-capture`, `telegram-rss-art`.

## 4. Phần chưa làm được hoặc chưa có bằng chứng đủ chắc

- Chưa xác nhận được `14/14 site rollout`.
- Chưa có bằng chứng đủ chắc cho `season/location`.
- Chưa chốt được `evergreen full chain` ở mức chạy thật có artifact đầy đủ.
- Chưa có lớp KPI đủ chắc để xác nhận `Semrush traffic`, `indexation` hay outcome SEO thực tế.

## 5. Đánh giá hướng đi

Nhận định:

- `Đúng hướng`

Lý do:

- đang ưu tiên đúng vào các lớp nền tảng có thể tái sử dụng: workflow, QC, capture, taxonomy, audit
- các repo và artifact đã nối thành một hệ tương đối logic
- điểm yếu hiện tại chủ yếu là closure runtime và data proof, không phải thiếu năng lực xây hệ thống

## 6. Công việc ngoài kế hoạch nhưng đáng ghi nhận

- đóng gói `writing-qc` thành skill QA/SEO review riêng
- làm `full decision/remap/manual review` và `full SEO audit` cho 3 site ưu tiên
- triển khai `deep-research-coin` với `38` file trong `research-output` và thêm `8` file bài/report ở root repo
- dựng `bulk hulk` cho bulk scheduling/publishing từ Google Sheet

## 7. Trọng tâm tháng 5

- chuyển từ `đã có repo/tool` sang `đã chạy thật có log và artifact`
- chốt `evergreen MVP` trên 1-2 site thay vì giữ ở mức ý tưởng
- đi hết chuỗi `audit -> decision -> implementation -> verification` cho 3 site ưu tiên
- dựng lớp KPI tối thiểu: site active, job thành công, bài publish, lỗi capture, batch audit/taxonomy đã xử lý
- mở rộng xử lý toàn bộ nhóm URL `Đã thu thập dữ liệu – hiện chưa được lập chỉ mục` theo từng site; riêng `Coinlineup / Tokentopnews / TheCCPress` là 3 site đã xử lý trước, tháng 5 cần verify và rollout sang site còn lại, kèm `301/410/sửa inlinks` nếu có
- đến tuần 4, mỗi site mục tiêu phải có ít nhất `3 bài evergreen`
- tuần 3 phải có ít nhất `3 case` gộp `news cũ -> 1 bài evergreen cùng sector` trên nhóm `Tokentopnews / Trusts / Bitcoininfonews / TheCCPress`
- trước khi hết nhịp `Sell in May`, tối thiểu `6 site` được update `UI/UX signature + trending` để sẵn sàng push sale tháng 6
- scale format bài `review / research / why pump / why dump` đã thắng ở `Coincu` sang các site khác với topic khác

Định hướng tháng 6:

- site nào có trên `30 bài cluster evergreen` thì bắt đầu dựng `hubpage`

## 8. Hỗ trợ / quyết định cần từ quản lý

- chốt rõ danh sách site ưu tiên trong tháng 5: `production active`, `ready but not active`, `blocked`
- thống nhất không mở thêm quá nhiều nhánh mới nếu chưa đóng vòng vận hành core system
- nếu cần báo cáo KPI outcome, phải cấp hoặc chốt luôn nguồn dữ liệu đo đủ tin cậy
