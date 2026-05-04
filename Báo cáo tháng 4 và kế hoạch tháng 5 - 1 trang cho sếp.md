# Báo cáo tháng 4 và kế hoạch tháng 5 - 1 trang cho sếp

## 1. Situation Overview

Tháng 4 xác nhận rõ một điểm: phần mạnh nhất hiện tại không phải `rollout breadth`, mà là `năng lực xây hệ thống`. Các trục đã có bằng chứng tốt gồm `news workflow`, `QC loop`, `article-evidence capture`, `taxonomy cleanup` và `SEO audit batching`. Tuy nhiên, trạng thái mong muốn cho giai đoạn tiếp theo không còn là “đã có repo/tool”, mà phải là `đã chạy thật`, `đã sửa thật`, `đã có KPI tối thiểu` và `đã nhân rộng được theo site`.

## 2. Key Findings

**Workflow nền đã hình thành tương đối hoàn chỉnh.** Hệ hiện có các lớp `news-flow`, `writing-qc`, `integrate-capture-v2`, `author-news`, `cmc-author-dashboard`. **Hàm ý chiến lược: nền vận hành đã đủ tốt để chuyển trọng tâm từ build sang rollout và closure.**

**Technical SEO là phần tiến xa nhất trong tháng 4.** Đã có full decision/remap/manual review và audit sâu cho `3 site`: `Coinlineup`, `Tokentopnews`, `TheCCPress`. **Hàm ý chiến lược: đây là cụm việc đã chứng minh được năng lực xử lý ở mức site-level, phù hợp dùng làm mẫu để nhân rộng.**

**Capture đã vượt mức utility rời rạc.** Hệ capture hiện đi theo hướng `article-evidence engine`, cộng thêm utility chụp chart riêng. **Hàm ý chiến lược: đây là lợi thế khác biệt cho content quality, trust và mức độ khó sao chép.**

**Nhiều việc ngoài report có giá trị thật nhưng chưa nên cộng vào KPI core.** Có `216` dòng dry-run ở `bulk hulk`; `deep-research-coin` có `38` file trong `research-output` gồm `32 md`, `6 pdf`, cộng thêm `8` file bài/report ở root. **Hàm ý chiến lược: có chiều sâu thử nghiệm, nhưng tháng 5 phải ưu tiên core system trước.**

**Gap lớn nhất vẫn là bằng chứng vận hành và outcome.** Chưa xác nhận được `14/14 site rollout`; chưa có bằng chứng đủ chắc cho `season/location`, `evergreen full chain`, và `KPI SEO outcome`. **Hàm ý chiến lược: nếu không khóa scope tháng 5, hệ sẽ tiếp tục mạnh về kiến trúc nhưng yếu về chứng minh hiệu quả.**

## 3. Business Impact

Nếu giữ đúng trọng tâm tháng 5, hệ có cơ sở nâng từ `7.2/10` lên khoảng `8.0/10` mà không cần overclaim. Cửa thắng nằm ở `closure`, không nằm ở mở thêm nhánh mới: verify xong `3 site` đã xử lý trước, rollout indexation sang site còn lại, đạt tối thiểu `6 site` ready cho push sale tháng 6, và đưa mỗi site mục tiêu lên `3 bài evergreen`. Nếu làm trượt các mốc này, tháng 6 sẽ thiếu nền để đẩy `hubpage` và scale sale.

## 4. Recommendations

**[Critical]** Khóa trọng tâm tháng 5 vào `runtime evidence` và `indexation closure`  
Chủ trì: `Thana` | Hạn: `Tuần 1` khóa scope, `Tuần 2-4` thực thi | Kết quả mong đợi: toàn bộ backlog `Đã thu thập dữ liệu – hiện chưa được lập chỉ mục` được phân nhóm rõ theo site, trong đó `Coinlineup / Tokentopnews / TheCCPress` được verify lại thay vì làm lại từ đầu.

**[Critical]** Dùng `3 site` đã xử lý trước làm benchmark và nhân rộng  
Chủ trì: `Thana` | Hạn: `Tuần 2` | Kết quả mong đợi: có biên bản verify closure cho `Coinlineup`, `Tokentopnews`, `TheCCPress`, kèm rule giữ / gộp / `301` / `410` / sửa inlinks để rollout sang site còn lại.

**[High]** Chốt output evergreen theo tuần thay vì theo ý tưởng  
Chủ trì: `Thana` | Hạn: `Tuần 3-4` | Kết quả mong đợi: ít nhất `3 case` `news cũ -> evergreen` trên nhóm `Tokentopnews / Trusts / Bitcoininfonews / TheCCPress`, và mỗi site mục tiêu đạt tối thiểu `3 bài evergreen`.

**[High]** Chuẩn bị sale tháng 6 từ cuối tháng 5  
Chủ trì: `Thana` | Hạn: `trước khi hết Sell in May` | Kết quả mong đợi: tối thiểu `6 site` update `UI/UX signature + trending`, đồng thời giữ ngưỡng tháng 6 là chỉ dựng `hubpage` khi site vượt `30 bài cluster evergreen`.

## 5. Next Steps

1. Khóa ngay danh sách site theo 3 nhóm: `đã xử lý`, `cần verify`, `cần rollout` trong `Tuần 1`.
2. Chốt bảng KPI tháng 5 theo site: `pipeline chạy thật`, `URL chưa index đã xử lý`, `số evergreen`, `UI/UX + trending`.
3. Ra quyết định quản lý trước cuối `Tuần 1`: tháng 5 ưu tiên `closure core system`, không mở thêm nhánh lớn mới nếu không phục vụ trực tiếp cho rollout tháng 6.
