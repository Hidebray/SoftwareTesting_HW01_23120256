# Test Cases – Quạt công nghiệp Kim Cương

## Product Information

- **Product:** Quạt Công Nghiệp B5 5 Cánh – Quạt Cây Đứng Kim Cương
- **Model:** B5 (5 cánh)
- **Source:** https://giadungkimcuong.vn/quat-cong-nghiep-kim-cuong/
- **Power:** 65 W
- **Rotation Speed:** 1200 vòng/phút
- **Height:** 130 cm
- **Weight:** 6 kg
- **Blade Count:** 5 cánh
- **Motor:** Quấn bằng dây đồng
- **Body Material:** Nhựa PP (Polypropylene)
- **Guard Material:** Thép không gỉ
- **Speed Levels:** 3 mức tốc độ (Mức 1, Mức 2, Mức 3) + Vị trí Tắt
- **Control:** Núm xoay gắn trên thân quạt (manual rotary knob)
- **Remote Control:** Không có
- **Timer:** Không có / N/A
- **Oscillation (đảo gió):** Không đề cập / N/A
- **Warranty:** Bảo hành chính hãng 12 tháng
- **Voltage/Frequency:** Không nêu cụ thể trên trang (N/A)

---

## Test Case Summary

| ID | Test Case Title | Priority | Test Type |
|---|---|---|---|
| TC-001 | Bật quạt từ trạng thái tắt sang Mức 1 | High | Functional |
| TC-002 | Chuyển tốc độ từ Mức 1 lên Mức 2 | High | Functional |
| TC-003 | Chuyển tốc độ từ Mức 2 lên Mức 3 | High | Functional |
| TC-004 | Tắt quạt đang hoạt động ở Mức 3 | High | Functional |
| TC-005 | Chuyển trực tiếp từ Mức 1 sang Mức 3 (bỏ qua Mức 2) | Medium | Functional |
| TC-006 | Kiểm tra độ ổn định của quạt trên bề mặt phẳng | Medium | Safety |
| TC-007 | Kiểm tra lồng quạt che chắn cánh quạt khi vận hành | High | Safety |
| TC-008 | Tháo và lắp lại lồng quạt để vệ sinh | Medium | Functional |
| TC-009 | Rút phích cắm điện khi quạt đang chạy ở Mức 2 | High | Safety |
| TC-010 | Bật quạt ngay sau khi cắm điện (không xoay núm) | Medium | Boundary |
| TC-011 | Xoay núm điều khiển ngược chiều từ Mức 1 về vị trí Tắt | Medium | Functional |
| TC-012 | Kiểm tra quạt hoạt động ở Mức 3 liên tục trong thời gian dài | Low | Robustness |
| TC-013 | Kiểm tra độ ổn định khi đặt quạt trên bề mặt không bằng phẳng | Medium | Safety |
| TC-014 | Kiểm tra trạng thái quạt sau khi cắm điện trở lại do mất điện đột ngột | Medium | Boundary |
| TC-015 | Kiểm tra núm điều khiển không phản hồi khi xoay vượt giới hạn tối đa | Low | Negative |

---

## Detailed Test Cases

### TC-001 – Bật quạt từ trạng thái tắt sang Mức 1

**Objective:** Xác minh rằng quạt có thể khởi động thành công ở mức tốc độ thấp nhất (Mức 1) khi xoay núm điều khiển từ vị trí Tắt sang Mức 1.

**Preconditions:**
- Quạt đang ở trạng thái tắt (núm điều khiển ở vị trí Off/Tắt).
- Phích cắm điện đã được cắm vào ổ điện.
- Quạt được đặt trên bề mặt phẳng, ổn định.

**Test Data:**
- Thao tác: Xoay núm điều khiển từ vị trí Tắt sang vị trí Mức 1.

**Test Steps:**
1. Đặt quạt trên bề mặt phẳng, ổn định.
2. Cắm phích cắm điện vào ổ điện.
3. Xác nhận núm điều khiển đang ở vị trí Tắt (Off).
4. Xoay núm điều khiển sang vị trí Mức 1.
5. Quan sát phản hồi của quạt.

**Expected Result:**
- Cánh quạt bắt đầu quay trong vòng ≤ 3 giây sau khi xoay núm.
- Quạt phát ra âm thanh vận hành ở mức tốc độ thấp nhất.
- Không có âm thanh bất thường (kẹt, cọ xát).

**Priority:** High

**Test Type:** Functional

---

### TC-002 – Chuyển tốc độ từ Mức 1 lên Mức 2

**Objective:** Xác minh rằng quạt tăng tốc độ rõ rệt và chính xác khi chuyển từ Mức 1 sang Mức 2.

**Preconditions:**
- Quạt đang hoạt động ổn định ở Mức 1 (ít nhất 10 giây).
- Phích cắm điện đã được cắm vào ổ điện.

**Test Data:**
- Thao tác: Xoay núm điều khiển từ vị trí Mức 1 sang vị trí Mức 2.

**Test Steps:**
1. Đảm bảo quạt đang chạy ổn định ở Mức 1.
2. Xoay núm điều khiển sang vị trí Mức 2.
3. Quan sát sự thay đổi tốc độ quay của cánh quạt.
4. Cảm nhận/đo mức độ gió thổi ra so với Mức 1.

**Expected Result:**
- Cánh quạt tăng tốc độ quay rõ ràng so với Mức 1.
- Luồng gió mạnh hơn và nghe thấy tiếng vận hành lớn hơn so với Mức 1.
- Không có âm thanh bất thường hoặc rung lắc đột ngột.

**Priority:** High

**Test Type:** Functional

---

### TC-003 – Chuyển tốc độ từ Mức 2 lên Mức 3

**Objective:** Xác minh rằng quạt đạt tốc độ tối đa (Mức 3) và hoạt động ổn định khi chuyển từ Mức 2 sang Mức 3.

**Preconditions:**
- Quạt đang hoạt động ổn định ở Mức 2 (ít nhất 10 giây).
- Phích cắm điện đã được cắm vào ổ điện.

**Test Data:**
- Thao tác: Xoay núm điều khiển từ vị trí Mức 2 sang vị trí Mức 3.

**Test Steps:**
1. Đảm bảo quạt đang chạy ổn định ở Mức 2.
2. Xoay núm điều khiển sang vị trí Mức 3.
3. Quan sát sự thay đổi tốc độ quay của cánh quạt.
4. Cảm nhận/đo mức độ gió thổi ra so với Mức 2.

**Expected Result:**
- Cánh quạt tăng tốc độ quay rõ ràng so với Mức 2.
- Luồng gió mạnh nhất (tương ứng công suất 65W, 1200 vòng/phút).
- Quạt vận hành ổn định, không rung lắc bất thường.

**Priority:** High

**Test Type:** Functional

---

### TC-004 – Tắt quạt đang hoạt động ở Mức 3

**Objective:** Xác minh rằng quạt dừng hoàn toàn khi xoay núm điều khiển về vị trí Tắt từ Mức 3.

**Preconditions:**
- Quạt đang hoạt động ổn định ở Mức 3.
- Phích cắm điện đã được cắm vào ổ điện.

**Test Data:**
- Thao tác: Xoay núm điều khiển từ vị trí Mức 3 về vị trí Tắt (Off).

**Test Steps:**
1. Đảm bảo quạt đang chạy ổn định ở Mức 3.
2. Xoay núm điều khiển về vị trí Tắt (Off).
3. Quan sát quá trình cánh quạt dừng lại.
4. Lắng nghe xem âm thanh vận hành đã ngừng hoàn toàn chưa.

**Expected Result:**
- Cánh quạt bắt đầu giảm tốc và dừng hẳn trong vòng ≤ 10 giây.
- Không còn âm thanh vận hành sau khi cánh quạt dừng.
- Quạt không tự khởi động lại.

**Priority:** High

**Test Type:** Functional

---

### TC-005 – Chuyển trực tiếp từ Mức 1 sang Mức 3 (bỏ qua Mức 2)

**Objective:** Xác minh rằng quạt phản hồi đúng khi người dùng xoay núm nhanh qua Mức 2 và dừng ở Mức 3.

**Preconditions:**
- Quạt đang hoạt động ổn định ở Mức 1.
- Phích cắm điện đã được cắm vào ổ điện.

**Test Data:**
- Thao tác: Xoay núm điều khiển từ vị trí Mức 1 thẳng sang vị trí Mức 3 (bỏ qua Mức 2).

**Test Steps:**
1. Đảm bảo quạt đang chạy ổn định ở Mức 1.
2. Xoay nhanh núm điều khiển từ Mức 1 thẳng đến vị trí Mức 3, bỏ qua Mức 2.
3. Dừng núm tại vị trí Mức 3.
4. Quan sát tốc độ quay và luồng gió.

**Expected Result:**
- Quạt chuyển sang hoạt động ở Mức 3 với tốc độ cao nhất.
- Không xảy ra hiện tượng kẹt núm, rung lắc bất thường hoặc dừng đột ngột.

**Priority:** Medium

**Test Type:** Functional

---

### TC-006 – Kiểm tra độ ổn định của quạt trên bề mặt phẳng

**Objective:** Xác minh rằng đế quạt hình vòm tròn đủ ổn định, không bị lật đổ khi quạt hoạt động ở Mức 3 trên bề mặt phẳng.

**Preconditions:**
- Quạt được đặt trên bề mặt phẳng, ngang.
- Phích cắm điện đã được cắm vào ổ điện.
- Khu vực xung quanh quạt không có vật cản.

**Test Data:**
- Bề mặt: Sàn phẳng (sàn gạch hoặc sàn gỗ).
- Tốc độ: Mức 3 (tốc độ tối đa).

**Test Steps:**
1. Đặt quạt trên bề mặt sàn phẳng.
2. Cắm điện và bật quạt lên Mức 3.
3. Để quạt hoạt động liên tục trong 5 phút.
4. Quan sát xem quạt có bị rung lắc, dịch chuyển hoặc có dấu hiệu lật đổ không.

**Expected Result:**
- Quạt không bị lật đổ, dịch chuyển đáng kể hoặc rung lắc bất thường khi hoạt động ở Mức 3.
- Đế quạt tiếp xúc ổn định với bề mặt sàn trong suốt quá trình hoạt động.

**Priority:** Medium

**Test Type:** Safety

---

### TC-007 – Kiểm tra lồng quạt che chắn cánh quạt khi vận hành

**Objective:** Xác minh rằng lồng quạt thép không gỉ được lắp chắc chắn, không bị lỏng hoặc bung ra trong khi cánh quạt đang quay, đảm bảo an toàn người dùng.

**Preconditions:**
- Lồng quạt đã được lắp đúng cách và đầy đủ trước khi cắm điện.
- Quạt được đặt trên bề mặt phẳng.

**Test Data:**
- Tốc độ kiểm tra: Mức 3 (tốc độ tối đa).
- Thời gian quan sát: 2 phút.

**Test Steps:**
1. Lắp lồng quạt theo đúng hướng dẫn và đảm bảo chốt/vít cố định đã được xiết chặt.
2. Cắm điện và bật quạt lên Mức 3.
3. Quan sát lồng quạt từ khoảng cách an toàn (≥ 1 mét) trong 2 phút.
4. Kiểm tra xem có bộ phận nào của lồng bị rung hoặc có dấu hiệu bung ra không.

**Expected Result:**
- Lồng quạt không bị rung tách khỏi thân, không phát ra tiếng lạch cạch do lỏng lẻo.
- Cánh quạt không tiếp xúc với lồng trong quá trình quay.

**Priority:** High

**Test Type:** Safety

---

### TC-008 – Tháo và lắp lại lồng quạt để vệ sinh

**Objective:** Xác minh rằng người dùng có thể tháo rời và lắp lại lồng quạt dễ dàng để vệ sinh theo đúng thiết kế của sản phẩm.

**Preconditions:**
- Quạt đang tắt (núm điều khiển ở vị trí Off).
- Phích cắm đã được rút khỏi ổ điện (để đảm bảo an toàn).

**Test Data:**
- Thao tác: Tháo lồng quạt bằng tay, lau chùi, sau đó lắp lại.

**Test Steps:**
1. Tắt quạt và rút phích cắm điện khỏi ổ điện.
2. Tháo lồng quạt theo hướng dẫn sử dụng (mở chốt/xoay khung lồng).
3. Lau chùi lồng quạt và cánh quạt bằng khăn khô.
4. Lắp lại lồng quạt vào đúng vị trí và cố định chốt.
5. Kiểm tra xem lồng quạt đã được lắp chắc chắn chưa.
6. Cắm điện và bật quạt lên Mức 1 để kiểm tra hoạt động sau khi lắp lại.

**Expected Result:**
- Lồng quạt có thể tháo ra bằng tay mà không cần dụng cụ.
- Sau khi lắp lại, quạt hoạt động ở Mức 1 với âm thanh bình thường, không có tiếng kêu lạ do lồng không khớp vị trí.

**Priority:** Medium

**Test Type:** Functional

---

### TC-009 – Rút phích cắm điện khi quạt đang chạy ở Mức 2

**Objective:** Xác minh rằng quạt dừng hoạt động ngay lập tức và an toàn khi nguồn điện bị ngắt đột ngột.

**Preconditions:**
- Quạt đang hoạt động ổn định ở Mức 2.
- Phích cắm điện đang cắm trong ổ điện.

**Test Data:**
- Thao tác: Rút phích cắm điện trực tiếp khỏi ổ điện trong khi quạt đang chạy ở Mức 2.

**Test Steps:**
1. Bật quạt lên Mức 2 và để chạy ổn định trong ít nhất 10 giây.
2. Rút phích cắm điện ra khỏi ổ điện.
3. Quan sát quá trình cánh quạt dừng lại.
4. Kiểm tra trạng thái núm điều khiển (vẫn ở Mức 2).

**Expected Result:**
- Cánh quạt dừng quay trong vài giây sau khi rút điện (do quán tính).
- Không có tia lửa điện, mùi khét, hoặc hiện tượng bất thường tại đầu phích cắm.
- Núm điều khiển vẫn giữ nguyên ở vị trí Mức 2.

**Priority:** High

**Test Type:** Safety

---

### TC-010 – Bật quạt ngay sau khi cắm điện (không xoay núm)

**Objective:** Xác minh rằng quạt không tự động khởi động khi cắm điện mà không có tác động vào núm điều khiển (núm đang ở vị trí Off).

**Preconditions:**
- Quạt đang tắt, núm điều khiển ở vị trí Off.
- Phích cắm chưa được cắm vào ổ điện.

**Test Data:**
- Thao tác: Cắm phích điện vào ổ điện, sau đó đứng quan sát trong 10 giây mà không thao tác núm.

**Test Steps:**
1. Đảm bảo núm điều khiển đang ở vị trí Tắt (Off).
2. Cắm phích cắm điện vào ổ điện.
3. Quan sát trạng thái của quạt trong 10 giây mà không chạm vào núm.

**Expected Result:**
- Cánh quạt không tự quay khi núm điều khiển ở vị trí Tắt.
- Quạt ở trạng thái chờ, im lặng, không phát ra âm thanh vận hành.

**Priority:** Medium

**Test Type:** Boundary

---

### TC-011 – Xoay núm điều khiển ngược chiều từ Mức 1 về vị trí Tắt

**Objective:** Xác minh rằng quạt dừng hoạt động khi người dùng xoay núm ngược chiều về vị trí Tắt từ Mức 1.

**Preconditions:**
- Quạt đang hoạt động ổn định ở Mức 1.
- Phích cắm điện đã được cắm vào ổ điện.

**Test Data:**
- Thao tác: Xoay núm điều khiển ngược chiều từ vị trí Mức 1 về vị trí Tắt (Off).

**Test Steps:**
1. Đảm bảo quạt đang chạy ổn định ở Mức 1.
2. Xoay núm điều khiển ngược chiều về vị trí Tắt.
3. Quan sát phản hồi của cánh quạt.

**Expected Result:**
- Cánh quạt bắt đầu dừng lại ngay khi núm chuyển qua vị trí Tắt.
- Quạt dừng hoàn toàn trong vòng ≤ 10 giây, không có tiếng động bất thường.

**Priority:** Medium

**Test Type:** Functional

---

### TC-012 – Kiểm tra quạt hoạt động ở Mức 3 liên tục trong thời gian dài

**Objective:** Xác minh rằng quạt có thể duy trì hoạt động ổn định ở Mức 3 trong 60 phút liên tục mà không quá nhiệt hoặc xuất hiện sự cố.

**Preconditions:**
- Quạt đang tắt, đặt trên bề mặt phẳng, thoáng khí.
- Phích cắm điện đã được cắm vào ổ điện.
- Phòng có điều kiện thông gió bình thường.

**Test Data:**
- Tốc độ: Mức 3 (tối đa).
- Thời gian: 60 phút liên tục.

**Test Steps:**
1. Bật quạt lên Mức 3.
2. Để quạt chạy liên tục trong 60 phút.
3. Mỗi 15 phút, kiểm tra thân máy bằng cách chạm nhẹ để cảm nhận nhiệt độ.
4. Quan sát xem có mùi khét, tiếng bất thường hoặc rung lắc xuất hiện không.
5. Sau 60 phút, tắt quạt và ghi nhận trạng thái.

**Expected Result:**
- Quạt duy trì hoạt động liên tục 60 phút mà không tự dừng.
- Thân máy ấm nhẹ do nhiệt sinh ra từ motor, nhưng không quá nóng (không bỏng tay khi chạm).
- Không xuất hiện mùi khét, khói hoặc âm thanh bất thường trong suốt quá trình chạy.

**Priority:** Low

**Test Type:** Robustness

---

### TC-013 – Kiểm tra độ ổn định khi đặt quạt trên bề mặt không bằng phẳng

**Objective:** Xác minh phản hồi của quạt khi đặt trên bề mặt có độ nghiêng nhẹ, kiểm tra nguy cơ lật đổ.

**Preconditions:**
- Quạt đang tắt và chưa cắm điện.
- Có sẵn bề mặt không bằng phẳng để thử nghiệm (ví dụ: tấm ván có độ nghiêng nhẹ ~5°).

**Test Data:**
- Bề mặt: Tấm ván hoặc sàn có độ nghiêng khoảng 5 độ.
- Tốc độ kiểm tra: Mức 1, Mức 3.

**Test Steps:**
1. Đặt quạt trên bề mặt có độ nghiêng ~5°.
2. Cắm điện và bật quạt lên Mức 1.
3. Quan sát sự ổn định của quạt trong 1 phút.
4. Chuyển sang Mức 3 và quan sát thêm 1 phút.
5. Ghi nhận xem quạt có bị lật hoặc trượt không.

**Expected Result:**
- Ở Mức 1: Quạt đứng ổn định, không bị trượt hoặc lật trên bề mặt nghiêng 5°.
- Ở Mức 3: Quạt có thể xuất hiện rung nhẹ nhưng không bị lật đổ trên bề mặt nghiêng 5°.

**Priority:** Medium

**Test Type:** Safety

---

### TC-014 – Kiểm tra trạng thái quạt sau khi cắm điện trở lại do mất điện đột ngột

**Objective:** Xác minh hành vi của quạt sau khi nguồn điện bị ngắt và phục hồi, ghi nhận trạng thái hoạt động để đánh giá tính an toàn.

**Preconditions:**
- Quạt đang hoạt động ở Mức 2.
- Núm điều khiển ở vị trí Mức 2.

**Test Data:**
- Thao tác: Rút phích cắm điện (giả lập mất điện) rồi cắm lại vào ổ điện sau 5 giây mà không thay đổi vị trí núm.

**Test Steps:**
1. Bật quạt lên Mức 2, để chạy ổn định ít nhất 10 giây.
2. Rút phích cắm điện đột ngột (giả lập mất điện).
3. Chờ 5 giây.
4. Cắm lại phích cắm điện vào ổ điện mà không thay đổi vị trí núm điều khiển.
5. Quan sát hành vi của quạt ngay sau khi điện phục hồi.

**Expected Result:**
- Hành vi quạt sau khi cắm lại được ghi nhận: quạt có thể tự khởi động lại ở Mức 2 (do núm cơ học vẫn ở Mức 2) hoặc không tự khởi động.
- Không có hiện tượng phát sáng, mùi khét, hoặc tiếng nổ.

**Assumption:** Quạt sử dụng núm điều khiển cơ học; hành vi sau mất điện phụ thuộc vào thiết kế mạch điện. Thông tin này không được nêu rõ trên trang sản phẩm. Kết quả thực tế cần được ghi nhận để so sánh với tài liệu kỹ thuật.

**Priority:** Medium

**Test Type:** Boundary

---

### TC-015 – Kiểm tra núm điều khiển không phản hồi khi xoay vượt giới hạn tối đa

**Objective:** Xác minh rằng núm điều khiển có cơ chế giới hạn vật lý, không thể xoay vượt quá vị trí Mức 3 hoặc vượt quá vị trí Tắt theo chiều ngược, tránh hư hỏng.

**Preconditions:**
- Quạt đang tắt, phích cắm đã cắm điện.
- Núm điều khiển ở vị trí Tắt.

**Test Data:**
- Thao tác 1: Xoay núm thêm sau khi đã đến vị trí Mức 3 (cố xoay tiếp theo chiều tăng tốc).
- Thao tác 2: Xoay núm ngược chiều khi đã ở vị trí Tắt (cố xoay tiếp theo chiều giảm tốc).

**Test Steps:**
1. Xoay núm từ Tắt lên Mức 3 (tốc độ tối đa).
2. Tiếp tục cố xoay núm theo chiều tăng tốc vượt qua vị trí Mức 3.
3. Ghi nhận phản hồi cơ học của núm.
4. Xoay núm về vị trí Tắt.
5. Tiếp tục cố xoay núm theo chiều giảm tốc vượt qua vị trí Tắt.
6. Ghi nhận phản hồi cơ học của núm.

**Expected Result:**
- Ở bước 2: Núm điều khiển có điểm chặn vật lý, không thể xoay thêm quá vị trí Mức 3; cánh quạt vẫn quay ổn định ở Mức 3.
- Ở bước 5: Núm có điểm chặn vật lý, không thể xoay vượt quá vị trí Tắt; quạt không phát ra âm thanh hoặc phản hồi bất thường.

**Priority:** Low

**Test Type:** Negative

---

*Tổng số test case: 15 (TC-001 → TC-015)*  
*Ngày tạo: 27/09/2026*  
*Tester: QA Engineer*  
*Nguồn thông tin sản phẩm: https://giadungkimcuong.vn/quat-cong-nghiep-kim-cuong/*
