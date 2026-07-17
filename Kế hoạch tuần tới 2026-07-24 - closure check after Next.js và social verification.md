# Kế hoạch tuần tới 2026-07-24 - closure check after Next.js và social verification

## 1. Tóm tắt điều hành

- Thời gian áp dụng: `Monday, July 20, 2026` đến `Friday, July 24, 2026`
- Mục tiêu chính:
  - chốt `Check after Next.js` từ `10/11` lên `11/11`
  - dọn các `local-only pending changes`
  - hoàn tất `visual verification` cho social layer đã merge từ MKT

Kết luận ngắn:

- Tuần tới nên tập trung vào **closure**, không mở thêm nhánh lớn mới.
- Mục tiêu là kết thúc tuần với:
  - evidence kỹ thuật đủ `11/11`
  - repo sạch hơn
  - social UI được verify thực tế trên toàn batch

## 2. Trọng tâm chính

### 2.1 Chốt `Check after Next.js` đủ 11 site

Việc cần làm:

- xác định chính xác site còn thiếu evidence trong batch tuần này
- re-check đầy đủ:
  - `sitemap`
  - `robots.txt`
  - `canonical`
  - `URL indexation`
  - author/trust route nếu liên quan
- tạo checkpoint note local giống các site còn lại

Kết quả mong đợi:

- có đủ evidence cho `11/11 site`
- không còn phải report theo trạng thái `10/11`

### 2.2 Dọn các local pending changes

Việc cần làm:

- review toàn bộ repo còn dirty
- ưu tiên đóng trước:
  - `Kanalcoin`
  - `TrustCrypto`
  - `ttn-legacy-preview`
  - `news-pipeline`
- tách rõ:
  - code đáng push
  - file checkpoint nên giữ
  - artifact/noise không nên commit

Kết quả mong đợi:

- giảm số repo đang còn local-only changes
- mỗi repo còn mở phải có lý do rõ ràng

### 2.3 Verify social layer sau merge

Việc cần làm:

- chạy một vòng visual verification riêng cho `11 site`
- check:
  - social icons/links có hiện đúng không
  - có vỡ layout mobile hay không
  - có cross-brand / cross-domain nhầm link hay không
  - có issue trust/UI nào phát sinh sau merge không

Kết quả mong đợi:

- có checklist trạng thái cho `11 site`
- phân loại:
  - `pass`
  - `minor UI fix`
  - `wrong link / wrong data`
  - `needs code fix`

## 3. Kế hoạch theo ngày

### Monday, July 20, 2026

- xác định site thứ 11 còn thiếu evidence
- audit nhanh tất cả repo đang dirty
- khóa scope tuần, không mở nhánh mới ngoài closure

### Tuesday, July 21, 2026

- hoàn tất re-check site thứ 11
- viết checkpoint note local
- cập nhật summary trạng thái thành `11/11`

### Wednesday, July 22, 2026

- xử lý `Kanalcoin` trước
- push hoặc loại bỏ các local pending changes quan trọng
- chốt repo nào còn dirty và vì sao

### Thursday, July 23, 2026

- chạy visual verification cho social merge trên toàn bộ 11 site
- ghi lỗi theo mức độ

### Friday, July 24, 2026

- fix nhanh các lỗi social/UI nhỏ nếu có
- chốt weekly report cuối tuần

## 4. KPI tuần tới

- `11/11` site có evidence re-check đầy đủ
- `100%` repo ưu tiên có trạng thái sạch hoặc được giải thích rõ
- `11/11` site có kết quả visual verification cho social layer
- `0` lỗi social cross-brand nghiêm trọng còn mở
- `1` weekly report cuối tuần với trạng thái done/pending rõ ràng

## 5. Rủi ro cần tránh

- tiếp tục cộng dồn local pending changes mà không quyết định push hay bỏ
- claim `social done` nhưng chưa có visual QA
- mở thêm feature mới trước khi đóng xong verification và cleanup
- trộn lỗi frontend public với lỗi upstream WordPress trong cùng một nhóm xử lý

## 6. Hỗ trợ / quyết định cần từ quản lý

- xác nhận có cần một vòng `visual QA checklist` chính thức cho social layer hay chỉ cần verify kỹ thuật mức nhóm làm
- xác nhận site nào nên được ưu tiên nếu site thứ 11 còn thiếu evidence cần external check hoặc live review thêm

## 7. Câu tóm tắt ngắn

Tuần tới tập trung vào closure thay vì mở rộng: chốt đủ `11/11` site cho vòng `Check after Next.js`, dọn các local pending changes còn tồn, và hoàn tất một vòng `visual verification` riêng cho social layer đã merge từ MKT. Mục tiêu là kết thúc tuần với technical verification complete hơn, repo sạch hơn, và social UI được xác nhận thực tế trên toàn network.
