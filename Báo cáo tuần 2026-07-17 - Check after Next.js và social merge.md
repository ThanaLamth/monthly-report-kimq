# Báo cáo tuần 2026-07-17 - Check after Next.js và social merge

## 1. Tóm tắt điều hành

- Tuần báo cáo: `Friday, July 17, 2026`
- Trọng tâm theo kế hoạch tuần trước:
  - `2.1 Check after Next.js (11 sites)`
  - `Re-check sitemap / robots.txt / canonical / URL indexation`
  - `Merge social đã order từ MKT lên UI web 11 sites`

Kết luận ngắn:

- Hướng đi tuần này là **đúng trọng tâm**.
- Phần `check after Next.js` đã có bằng chứng local rõ cho **10/11 site** trong batch này.
- Phần `merge social` đã **được thực hiện xong**, nhưng chưa có batch verify UI riêng cho đủ 11 site trong cùng note tuần này.

## 2. Kết quả nổi bật

- Hoàn tất một vòng re-check kỹ thuật sâu cho phần lớn network headless Next.js, tập trung vào:
  - `sitemap`
  - `robots.txt`
  - `canonical`
  - `indexation governance`
  - `author trust pages`
  - `WordPress -> Next.js parity`
- Nhiều site không chỉ dừng ở kiểm tra mà đã có fix live hoặc local verification rõ ràng:
  - `Coinwy`
  - `MarketBit`
  - `CCPress`
  - `Coinlineup`
  - `Trustscrypto`
  - `Aicryptocore`
  - `NFTENEX`
  - `CryptoDailyAlert`
  - `TokenTopNews`
  - `Kanalcoin`
- Social components từ MKT đã được merge vào UI web theo kế hoạch.

Giá trị tạo ra:

- Giảm rủi ro crawl/indexation lỗi sau cutover Next.js
- Tăng độ sạch của tín hiệu SEO kỹ thuật giữa frontend public và WordPress origin
- Tăng trust/EEAT qua author pages, `llms.txt`, metadata, sitemap, crawl control

## 3. Phần đã làm được theo kế hoạch

### 3.1 Check after Next.js

Đã có checkpoint hoặc evidence local rõ cho `10/11` site trong batch này:

- `Coinwy`
  - fix author slug resolution, `Person` schema, `.webm` routing, CMS origin separation, taxonomy/indexing cleanup
- `MarketBit`
  - fix `llms.txt`, author routes, `uncategorized` noindex, legacy/backend redirects, sitemap cleanup
- `CCPress`
  - tighten `llms.txt`, category indexation, author hubs, search overlay, robots cleanup
- `Coinlineup`
  - fix real redirect cho `/uncategorized`, hoàn tất `llms.txt`, crawl/index governance, WordPress SEO parity
- `Trustscrypto`
  - ổn định frontend fallback, feed/sitemap behavior, smoke test production pass, QC revalidation
- `Aicryptocore`
  - sửa SEO parity, author/avatar fallback, image proxy non-`www`, stale Railway `robots.txt`
- `NFTENEX`
  - route hardening, pseudo-author cleanup, category indexing, `llms.txt`, logout query cleanup
- `CryptoDailyAlert`
  - sitemap architecture, canonical redirects, search URL normalization, broken-link cleanup, OG/Twitter metadata, crypto calendar rollout
- `TokenTopNews`
  - harden author pages, fallback author profiles, author sitemap URLs, `Person` JSON-LD, trust signals
- `Kanalcoin`
  - article layout cleanup, image optimization, table/list rendering, mobile-readable article tables

### 3.2 Merge social từ MKT lên UI web

- Phần `merge social đã order từ MKT lên UI web` đã được thực hiện.
- Trong batch local evidence tuần này, phần technical checkpoints nghiêng về SEO/crawl/indexation nhiều hơn là visual QA của social layer, nên nên ghi nhận là:
  - `Merged`
  - `chưa làm một vòng UI verification riêng đủ 11 site trong cùng report`

## 4. Phần chưa làm được hoặc chưa có bằng chứng đủ chắc

- Chưa có checkpoint local mới rõ ràng cho `1/11 site` trong batch report này.
  - Từ evidence hiện tại, site còn thiếu note verify mới nhiều khả năng là `Coincu`.
- `Kanalcoin` vẫn còn local-only pending changes chưa push:
  - `src/app/globals.css`
  - `src/app/layout.tsx`
  - `src/components/ads/SevioAds.tsx`
  - `src/components/ads/SevioLoader.tsx`
  - một số handoff docs liên quan `Cloudflare / www / apex`
- `Trustscrypto`:
  - public Next.js frontend đã ổn
  - nhưng WordPress public system routes vẫn chưa ổn định hoàn toàn, nên chưa nên coi là “sạch hẳn” ở tầng upstream
- `Coinlineup`:
  - hero-image cleanup đã implement
  - nhưng checkpoint vẫn khuyến nghị visual confirmation thêm trên 1-2 bài live

## 5. Đánh giá hướng đi

Nhận định:

- **Đúng hướng nhưng cần chốt thêm evidence cho site cuối và đóng local pending changes.**

Lý do:

- Tuần này bám đúng trọng tâm `post-cutover technical verification`, thay vì mở thêm nhánh việc mới.
- Kết quả có chiều sâu thực tế: không chỉ kiểm tra, mà nhiều site đã có live/local verification rõ.
- Tuy nhiên, để claim trọn vẹn `11 sites` thì vẫn cần thêm một lớp evidence hoặc checkpoint cho site còn thiếu.

## 6. Công việc ngoài kế hoạch nhưng đáng ghi nhận

- `CryptoDailyAlert` đã đi xa hơn mức re-check thuần kỹ thuật khi rollout thêm:
  - crypto calendar SSR
  - section hubs
  - social metadata đầy đủ
- `TokenTopNews` tăng thêm lớp trust qua author-page hardening, WP author endpoint reference, và sitemap author URLs
- `Trustscrypto` có thêm nhánh QC revalidation riêng, giúp tách rõ phần đã fix và phần còn là vấn đề upstream

## 7. Trọng tâm tuần tiếp theo

- Chốt evidence còn thiếu để hoàn tất claim `11/11 site checked after Next.js`
- Dọn các local-only pending changes, ưu tiên `Kanalcoin`
- Nếu cần, làm một vòng visual verification riêng cho phần `social merge` thay vì chỉ ghi nhận đã merge

## 8. Hỗ trợ / quyết định cần từ quản lý

- Xác nhận có cần một vòng `UI verification checklist` riêng cho phần social sau khi merge hay không
- Xác nhận site thứ 11 trong batch re-check này cần ưu tiên verify lại ngay là site nào nếu muốn chốt con số `11/11`

## 9. Câu tóm tắt có thể dùng cho báo cáo quản lý

Trong tuần kết thúc ngày `Friday, July 17, 2026`, trọng tâm được giữ đúng theo kế hoạch là re-check network sau cutover Next.js và merge social layer từ MKT lên UI web. Phần kiểm tra kỹ thuật đã có bằng chứng local rõ cho `10/11` site, với các hạng mục chính gồm `sitemap`, `robots.txt`, `canonical`, `indexation governance`, `author trust pages`, và `WordPress-to-Next.js parity`. Phần social đã được merge xong. Điểm còn lại cần xử lý là bổ sung evidence cho site cuối cùng trong batch, đóng một số local pending changes ở `Kanalcoin`, và nếu cần thì chạy thêm một vòng visual verification riêng cho social layer.
