# Kế hoạch tháng 5 - agency agent

Ngày lập kế hoạch: 2026-05-04

## 1. Cơ sở lập kế hoạch

Kế hoạch tháng 5 này được rút ra từ:

- [Báo cáo công việc tháng 3 - Kế hoạch tháng 4 - Trang tính1.csv](/root/report-monthly/Báo%20cáo%20công%20việc%20tháng%203%20-%20Kế%20hoạch%20tháng%204%20-%20Trang%20tính1.csv)
- [Đánh giá báo cáo công việc tháng 3 - kế hoạch tháng 4.csv](/root/report-monthly/Đánh%20giá%20báo%20cáo%20công%20việc%20tháng%203%20-%20kế%20hoạch%20tháng%204.csv)
- [Đánh giá báo cáo công việc tháng 3 - kế hoạch tháng 4 - agency agent.md](/root/report-monthly/Đánh%20giá%20báo%20cáo%20công%20việc%20tháng%203%20-%20kế%20hoạch%20tháng%204%20-%20agency%20agent.md)

Kết luận chính từ tháng 4:

- Đã làm mạnh ở `workflow`, `QC`, `capture`, `taxonomy`, `audit batching`.
- Chưa đủ bằng chứng cho `14/14 rollout`, `KPI SEO`, `evergreen full chain`, `season/location`, và `runtime proof` trên toàn hệ.
- Hướng đi đúng, nhưng tháng 5 phải ưu tiên `đóng vòng vận hành thật` thay vì mở thêm nhiều nhánh mới.

## 2. Mục tiêu tháng 5

### Mục tiêu chính

1. Chuyển từ `repo/spec/tooling` sang `runtime evidence`.
2. Đưa nhiều site hơn vào vận hành thật có log, artifact và trạng thái đo được.
3. Chốt một phiên bản `evergreen MVP` khả dụng thay vì tiếp tục để ở mức ý tưởng.
4. Hoàn tất một cụm `audit -> decision -> implementation -> verification` cho các site ưu tiên.
5. Bắt đầu có lớp theo dõi KPI tối thiểu đủ để chứng minh tiến độ thật.

### Mục tiêu phụ

- Giữ `deep-research-coin`, `telegram-rss-art`, `cmc-chart-capture`, `x-automation` ở vai trò nhánh phụ trợ.
- Không dùng các nhánh phụ này để thay thế KPI core của news/SEO system.

## 3. Định hướng tháng 5

### 3.1 Làm ít hơn nhưng đóng vòng hơn

Tháng 5 không nên mở thêm quá nhiều repo hoặc nhánh thử nghiệm mới.

Ưu tiên:
- rollout thật
- kiểm chứng thật
- log thật
- báo cáo thật

Thay vì:
- thêm spec mới
- thêm repo mới
- thêm hệ thống lớn chưa có người vận hành

### 3.2 Giảm scope của season/location

`season/location` chưa có bằng chứng implementation đủ mạnh.

Trong tháng 5 nên hạ scope:
- không đặt mục tiêu hoàn thiện full system
- chỉ chốt `spec + data schema + 1 proof-of-concept nhỏ` nếu còn thời gian

### 3.3 Evergreen phải đi theo hướng MVP

Không cố gắng hoàn thành full chuỗi hoàn hảo.

Mục tiêu hợp lý hơn:
- keyword input
- topic grouping cơ bản
- outline generation
- article generation
- publish thử nghiệm có log/artifact

Nếu làm được chuỗi này cho một nhóm site nhỏ, đó đã là đủ giá trị cho tháng 5.

## 4. Ưu tiên công việc tháng 5

### Priority A - Vận hành thật và evidence

- Mở rộng số site chạy pipeline thật có `job`, `artifact`, `publish result`.
- Chốt dashboard hoặc bảng theo dõi trạng thái chạy theo site.
- Ghi nhận rõ site nào:
  - đã setup
  - đã chạy pipeline
  - đã publish
  - đang lỗi
  - đang chờ review

### Priority B - Audit và implementation closure

- Chọn 3 site ưu tiên:
  - Coinlineup
  - Tokentopnews
  - TheCCPress
- Với từng site, đi hết chuỗi:
  - audit
  - decision sheet
  - implementation batch
  - verify lại sau fix

### Priority C - Evergreen MVP

- Chạy được một workflow evergreen mức tối thiểu trên 1-2 site.
- Không yêu cầu full season/location.
- Có artifact và output thật để chứng minh.

### Priority D - KPI tối thiểu

- Thiết lập lớp theo dõi KPI đủ tối thiểu:
  - số site chạy thật
  - số job thành công
  - số bài publish
  - số bài cần review
  - số lỗi capture
  - số batch taxonomy/audit đã hoàn tất

Nếu có thể:
- thêm snapshot indexation / GSC / crawl health đơn giản
- chưa cần hứa Semrush traffic nếu chưa có dữ liệu rõ

## 5. Timeline tháng 5

### Tuần 1

- Chốt danh sách site theo 3 trạng thái:
  - production active
  - ready but not active
  - blocked
- Chốt format tracking chung cho tất cả site.
- Chốt bộ KPI vận hành tối thiểu.
- Chọn 1-2 site để chạy evergreen MVP.

Deliverables:
- bảng trạng thái site
- bảng KPI tối thiểu
- danh sách blocker theo site

### Tuần 2

- Mở rộng news pipeline thật sang thêm site có thể chạy ngay.
- Chạy xác minh lại 3 site audit priority:
  - Coinlineup
  - Tokentopnews
  - TheCCPress
- Bắt đầu chạy evergreen MVP trên 1 site.

Deliverables:
- logs/job artifacts mới
- verify batch sau audit
- output evergreen đầu tiên

### Tuần 3

- Mở evergreen MVP sang site thứ 2 nếu site đầu chạy ổn.
- Chốt cơ chế report tuần tự động hoặc bán tự động.
- Chốt lớp tổng hợp lỗi:
  - capture
  - publish
  - QC
  - taxonomy/manual review

Deliverables:
- 1 report tuần mẫu
- 1 bảng lỗi tổng hợp
- 1 bảng so sánh site active vs blocked

### Tuần 4

- Tổng kết hiệu quả vận hành thực tế.
- Đánh giá có đủ cơ sở để nâng scope tháng 6 hay không.
- Nếu chưa đạt KPI SEO outcome, phải chốt rõ là do:
  - chưa đủ rollout
  - chưa đủ thời gian index
  - chưa có lớp đo dữ liệu

Deliverables:
- tổng kết tháng 5
- đề xuất kế hoạch tháng 6
- bảng KPI thực tế vs mục tiêu

## 6. KPI tháng 5

### KPI bắt buộc

- Có bảng trạng thái cho `100%` site trong hệ.
- Tăng số site có `pipeline chạy thật` so với snapshot tháng 4.
- Có ít nhất `1 workflow evergreen MVP` chạy ra output thật.
- Có ít nhất `1 vòng verify sau fix` cho mỗi site ưu tiên audit.
- Có report tuần mẫu và log lỗi tập trung.

### KPI nên có

- Có số liệu publish thực tế theo site.
- Có số liệu review/capture fail theo site.
- Có số liệu batch taxonomy/audit đã xử lý xong.

### KPI không nên hứa quá mạnh trong tháng 5

- `14/14 site production stable`
- `Semrush traffic hiển thị rõ trên toàn hệ`
- `season/location production-ready`

Các mục này nên để dạng stretch goal hoặc mục tiêu tháng 6 nếu dữ liệu tháng 5 chứng minh đủ.

## 7. Công việc ngoài core plan nhưng vẫn có thể duy trì

Các nhánh sau có thể tiếp tục nhưng không được chiếm trọng tâm tháng 5:

- `deep-research-coin`
- `telegram-rss-art`
- `cmc-chart-capture`
- `x-automation`

Nguyên tắc:
- chỉ duy trì nếu hỗ trợ trực tiếp cho content, evidence, distribution hoặc research
- không để làm loãng mục tiêu `đóng vòng vận hành core system`

## 8. Đánh giá mức độ đúng hướng nếu làm theo kế hoạch này

Nếu bám đúng kế hoạch tháng 5 ở trên, hướng đi sẽ đúng hơn tháng 4 ở 3 điểm:

1. Bớt thiên về “đã có repo/tool” và tiến sang “đã chạy thật”.
2. Bớt mở rộng chiều ngang, tập trung vào closure và verification.
3. Tạo nền để tháng 6 có thể nói chuyện KPI thực hơn, thay vì chỉ nói kiến trúc.

## 9. Kết luận ngắn

Tháng 5 nên là tháng:
- đóng vòng
- chứng minh runtime
- chứng minh breadth vận hành thật
- chốt evergreen MVP
- giữ season/location ở mức kiểm soát

Nếu làm đúng, điểm tổng quan có thể tăng từ `7.2/10` lên khoảng `8.0/10` mà không cần hứa quá đà.
