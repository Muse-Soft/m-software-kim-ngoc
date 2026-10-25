# DESIGN.md — Landing page tiệm trang sức thủ công Kim Ngọc

> Tài liệu thiết kế chốt cho sprint TEC-369 (task Thiết kế TEC-371). Dev (task Dev của sprint) dựng đúng tài liệu này, không tự thêm màu, font hay khối ngoài danh sách. QA đối chiếu bản dựng với tài liệu này, kèm kiểm tra đa dạng theo OPERATIONS.md mục 16.5.

## 0. Khác biệt so với các project gần nhất (bắt buộc theo mục 16.5 — đã đọc thật ngày 2026-10-25)

Thứ tự project mới nhất lấy từ /api/office, DESIGN.md đọc trực tiếp (raw.githubusercontent.com cho repo public, API GitHub cho repo private) ngày 2026-10-25:

1. **TarotLight** (tarotlight-app, TEC-352) — app mobile Flutter, KHÔNG có archetype bố cục web: DESIGN.md của app này ghi rõ "BỎ QUA luật đa dạng archetype cho app này theo issue TEC-352 — app theo thương hiệu PO chỉ định, không so sánh với các project web"; cặp font: Cormorant Garamond + (nội dung); nhiệt màu: tối (nền tím đêm `#120E24`, nhấn vàng đồng `#C9A227`); điểm nhấn: "Celestial luxury — huyền bí sang trọng".
2. **Bánh Lăn** (m-software-banh-lan, TEC-347) — archetype: **A6 Thanh bên cố định**; cặp font: **Fraunces + Be Vietnam Pro**; nhiệt màu: **sáng-ấm** (nền `#ECEAE4`, nhấn đỏ gạch gỉ `#C2452D`); điểm nhấn: "vạch hàn + tem cỡ khung".
3. **Sớm Mai** (m-software-som-mai, TEC-340) — archetype: **A8 Tạp chí nhiều cột**; cặp font: **Lora + Be Vietnam Pro**; nhiệt màu: **sáng-ấm** (nền `#F3EDE3`, nhấn vàng đồng hạt rang `#9A6A2F`); điểm nhấn: "thang rang 5 nấc".

Lựa chọn cho Kim Ngọc (đối chiếu trực tiếp với 3 project trên):

- **Archetype: A2 Split (chia đôi)** — KHÁC A6 của Bánh Lăn và KHÁC A8 của Sớm Mai, thỏa luật "không dùng lại archetype của 2 project liền trước" (TarotLight không có archetype web nên không tính trùng). Cách A2 thể hiện ở: mỗi khối chia đôi màn hình — một bên ảnh lớn, một bên nội dung — xen kẽ trái/phải theo khối (xem mục "Bố cục"), không phải thanh bên cố định (A6), không phải lưới nhiều cột kiểu tạp chí (A8).
- **Cặp font: Noto Serif Display + Manrope** — LÝ DO ĐỔI (bắt buộc theo cảnh báo chống trùng của task TEC-371): công thức gợi ý trong yêu cầu (Fraunces + Be Vietnam Pro) TRÙNG NGUYÊN cặp font của project liền trước Bánh Lăn (MSR-46), nên BẮT BUỘC đổi. Cặp mới khác nguyên cặp của cả Bánh Lăn (Fraunces + Be Vietnam Pro) lẫn Sớm Mai (Lora + Be Vietnam Pro): tiêu đề đổi sang Noto Serif Display (serif hiển thị nét tương phản cao, sang trọng kiểu trang sức cao cấp, hỗ trợ tiếng Việt), nội dung đổi sang Manrope (sans hình học, gọn, dễ đọc, hỗ trợ tiếng Việt). Tinh thần giữ nguyên: bảng màu tối-ấm `#141210`/`#F2EAD9`/`#B76E79` và không khí tạp chí trang sức nền tối, ánh kim lấp lánh.
- **Nhiệt màu: tối-ấm** — chuỗi nhiệt gần nhất: Kim Ngọc (tối-ấm) → Bánh Lăn (sáng-ấm) → Sớm Mai (sáng-ấm): chỉ 2 project sáng-ấm liên tiếp trước đó, KHÔNG tạo thành 3 project liên tiếp cùng nhiệt màu vì Kim Ngọc đổi hẳn sang tối-ấm. Nền tối-ấm của Kim Ngọc thiên về đêm tiệm kim hoàn (nền đen nâu than, chữ kem, nhấn vàng hồng), khác hẳn nền sáng của Bánh Lăn và Sớm Mai, và khác tím đêm của TarotLight (TarotLight là app, không tính vào chuỗi nhiệt web).
- **Điểm nhấn riêng** (xem mục "Điểm nhấn đặc sắc"): "vạch cắt giác + sao 4 cánh" — không project nào gần đây có.

## Tổng quan

- Sản phẩm: landing page 1 trang, visual-first, cho tiệm trang sức thủ công Kim Ngọc — chế tác tay nhẫn, dây chuyền, bông tai, vòng tay.
- Archetype: **A2 Split** — mỗi khối chia đôi: ảnh lớn một bên, nội dung một bên, xen kẽ trái/phải.
- Phong cách tham chiếu: **tạp chí trang sức cao cấp nền tối kiểu cửa tiệm kim hoàn về đêm** — ảnh cận cảnh kim loại và đá dưới ánh đèn điểm, nền tối sâu, chữ kem lớn, điểm nhấn vàng hồng lấp lánh; không dùng ảnh studio trắng, không dùng tông lạnh neon.
- Ngôn ngữ: tiếng Việt, hỗ trợ dấu đầy đủ (cả Noto Serif Display và Manrope đều hỗ trợ tiếng Việt).

## Bảng màu (mã hex + vai trò)

| Mã hex | Vai trò |
|---|---|
| `#141210` | Nền chính toàn trang — đen nâu than, tối-ấm |
| `#1E1A17` | Nền khối phụ xen kẽ (khối bộ sưu tập, khối cảm nhận) và nền thẻ |
| `#F2EAD9` | Chữ chính + tiêu đề — kem sáng, tương phản cao trên nền tối |
| `#A89A86` | Chữ phụ (mô tả ngắn, chú thích ảnh, ghi chú giá mẫu) — be xám ấm |
| `#B76E79` | Nhấn chính — vàng hồng (rose gold): nút bấm, giá mẫu, vạch cắt giác, sao 4 cánh |
| `#D4AF7A` | Nhấn phụ — vàng kim nhạt: đường kẻ mảnh, viền ảnh, chi tiết trang trí nhỏ; không làm nền khối lớn |

Quy tắc dùng màu: nền luôn là tối (`#141210` hoặc `#1E1A17` xen kẽ theo khối); không dùng khối nền sáng toàn trang; màu nhấn `#B76E79` chỉ dùng cho nút, giá, điểm nhấn — không tô nền lớn bằng màu nhấn.

## Font chữ

- Font tiêu đề: **Noto Serif Display** (serif hiển thị, nét tương phản cao, hỗ trợ tiếng Việt) — hero 64px desktop / 40px mobile, tiêu đề khối 40px desktop / 28px mobile, tên mẫu trang sức 28px.
- Font nội dung: **Manrope** (sans hình học, hỗ trợ tiếng Việt) — nội dung 17px, dòng cao 1.7; chú thích 14px; nút bấm 16px đậm; nhãn khối 13px đậm, chữ hoa.
- Không dùng thêm font thứ ba.

## Điểm nhấn đặc sắc: "vạch cắt giác + sao 4 cánh"

Nhìn thấy được, lặp lại xuyên suốt trang, không project gần đây nào có:

- **Vạch cắt giác**: đường chia giữa các khối không phải đường thẳng trơn mà là đường mảnh 1px màu `#D4AF7A`, ở chính giữa có một hình thoi 8×8px màu `#B76E79` xoay 45° (mô phỏng một mặt cắt của viên đá), dài toàn bộ chiều rộng nội dung.
- **Sao 4 cánh**: mỗi tiêu đề khối đi kèm một dấu sao 4 cánh ✦ màu `#B76E79`, cỡ 20px, đặt ngay trước tiêu đề; mỗi thẻ mẫu trang sức cũng có một sao 4 cánh nhỏ 12px ở góc trên bên phải ảnh.

## Bố cục (archetype A2)

- Desktop (rộng ≥ 1024px): lề nội dung tối đa 1200px, căn giữa; mỗi khối chia 2 cột 50/50 (ảnh — nội dung), khoảng cách giữa hai cột 48px, khoảng cách giữa các khối 96px; thứ tự ảnh/nội dung xen kẽ: khối chẵn ảnh trái — chữ phải, khối lẻ ảnh phải — chữ trái.
- Tablet/mobile (rộng < 1024px): mọi khối về 1 cột (ảnh trên, chữ dưới); khoảng cách khối 64px (tablet) / 48px (mobile); hero 40px tiêu đề.
- Thứ tự khối: (1) Hero → (2) Bộ sưu tập → (3) Quy trình chế tác → (4) Câu chuyện tiệm + cảm nhận khách → (5) Liên hệ / đặt lịch.

## Các khối và quy tắc hình ảnh

Tông ảnh chung cho toàn trang (§16.3): ảnh mẫu đồng tông tiệm kim hoàn tối-ấm — cận cảnh tay thợ, kim loại vàng hồng, đá lấp lánh dưới ánh đèn điểm ấm; ảnh lấy từ Unsplash, ghi rõ là ảnh mẫu trong comment kết quả của Dev. Không dùng ảnh tông lạnh, ảnh studio trắng.

| Khối | Nội dung | Tỉ lệ khung ảnh |
|---|---|---|
| 1. Hero | Ảnh lớn toàn màn hình cận cảnh chế tác (tay thợ đang chạm khắc/gắn đá); tiêu đề "Kim Ngọc — Trang sức chế tác bằng tay"; nút "Xem bộ sưu tập" và "Đặt lịch tư vấn" | Ảnh 16:9, cao 100vh, phủ tối 40% để chữ kem đọc được |
| 2. Bộ sưu tập | 4 nhóm: nhẫn, dây chuyền, bông tai, vòng tay — mỗi nhóm một cặp split (ảnh lớn + tên, mô tả 1–2 câu, giá mẫu); mỗi ảnh có sao 4 cánh 12px góc phải | Ảnh mỗi nhóm 4:5, bố cục split xen kẽ trái/phải |
| 3. Quy trình chế tác | 4 bước đánh số 01–04: (01) Phác thảo — (02) Đúc — (03) Chạm khắc — (04) Đánh bóng; mỗi bước 1 câu mô tả + ảnh thợ đang làm bước đó | Ảnh mỗi bước 3:2, lưới 2 cột desktop / 1 cột mobile |
| 4. Câu chuyện tiệm + cảm nhận khách | Ảnh tiệm + ảnh thợ chính; đoạn văn ngắn về triết lý chế tác tay; 3 cảm nhận khách (tên khách để placeholder, không bịa tên thật) | Ảnh tiệm 16:9, ảnh thợ 4:5 |
| 5. Liên hệ / đặt lịch | Form: họ tên, số điện thoại, mẫu quan tâm (chọn 1 trong 4 nhóm), ngày muốn tư vấn, ghi chú | Không ảnh lớn; form 1 cột, rộng tối đa 640px, đặt ở nửa phải của split, nửa trái là thông tin tiệm |

## Quy tắc dữ liệu thật / mẫu (bắt buộc cho Dev)

- Giá trên trang **luôn là giá mẫu**: mỗi giá phải kèm chữ "Giá mẫu" ngay cạnh, footer ghi rõ "Tất cả giá trên trang là giá mẫu".
- Địa chỉ, điện thoại, giờ mở cửa, người phụ trách và tên người cảm nhận để placeholder **`[CẦN BỔ SUNG]`**, tuyệt đối không bịa số liệu thật.
- Form liên hệ/đặt lịch **CHỈ giao diện**: submit dùng preventDefault và hiện thông báo mẫu ("Đây là bản giao diện mẫu — yêu cầu chưa được gửi đi thật"); không có thuộc tính action, không fetch, không mailto:, không tel:.
- Toàn bộ ảnh là ảnh mẫu (Unsplash), footer ghi rõ điều này.
