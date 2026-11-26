# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 05
- **Họ tên:** Trần Thị Lý
- **Lớp:** HN-KS26-CNTT2
- **Link repository Pha2:** https://github.com/tranthily-12/HN-KS26-CNTT2_Prompt_H02_Pha1-Pha2.git
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** ChatGPT

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé xem phim ra JSON

**KET QUA AI**

```text
[
  {
    "loai_ve": "P2D",
    "ngay_chieu": "2026-12-24",
    "ve_nguoi_lon": 2,
    "ve_tre_em": 1,
    "loai_ghe": "thuong",
    "ghi_chu": null
  },
  {
    "loai_ve": "P3D",
    "ngay_chieu": "2027-01-01",
    "ve_nguoi_lon": 3,
    "ve_tre_em": 0,
    "loai_ghe": null,
    "ghi_chu": "1 người hay chóng mặt, cần ngồi gần lối ra"
  },
  {
    "loai_ve": "GOLD",
    "ngay_chieu": null,
    "ve_nguoi_lon": 4,
    "ve_tre_em": 0,
    "loai_ghe": "doi",
    "ghi_chu": "1 bạn đi xe lăn"
  }
]
```

**Link trò chuyện:** https://chatgpt.com/share/6b079dcf-1c0c-83ec-b501-3e02b49ca46c

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
1. Tiền vé người lớn
- Giá vé P3D: 130.000 đồng/vé.
- Số lượng: 5 người lớn.
Phép tính:

5 × 130.000 = 650.000 đồng
2. Tiền vé trẻ em
Có 2 trẻ em cao từ 1 m đến 1,3 m, mỗi bé tính 70% giá vé người lớn.
- Bé cao 1,1 m: 130.000 × 70% = 91.000 đồng.
- Bé cao 1,25 m: 130.000 × 70% = 91.000 đồng.
- Bé cao 0,9 m: Miễn phí vì dưới 1 m và ngồi cùng người lớn.
Phép tính:

2 × 91.000 + 0 = 182.000 đồng
3. Tiền vé
Tiền vé = Tiền vé người lớn + Tiền vé trẻ em.

650.000 + 182.000 = 832.000 đồng
4. Giảm giá nhóm và tiền vé sau giảm
Nhóm có 5 người lớn nên đủ điều kiện giảm 10% trên tổng tiền vé (bao gồm vé người lớn và trẻ em).

- Tiền giảm giá:

832.000 × 10% = 83.200 đồng

- Tiền vé sau giảm:

832.000 - 83.200 = 748.800 đồng
5. Tiền Combo
- Giá mỗi combo: 75.000 đồng.
- Số lượng: 3 combo.
- Combo không được giảm giá.
Phép tính:

3 × 75.000 = 225.000 đồng
6. Tổng tiền
Tổng tiền = Tiền vé sau giảm + Tiền combo.

748.800 + 225.000 = 973.800 đồng
Tổng thanh toán: 973.800 đồng
[RESULT: 973.800 đồng]
```

**Link trò chuyện:** https://chatgpt.com/share/6b079e53-c014-83ec-bc6f-1d773e6a9139

### b) Kiểm tra kết quả AI

Kết quả của AI là đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "loi_ky_thuat",
  "so_khach": 4,
  "so_suat_bi_loi": 2,
  "tom_tat": "Hai suất chiếu tại phòng 3 đều bị mất tiếng hơn 15 phút giữa phim."
}
```

**Link trò chuyện:** https://chatgpt.com/share/6b079ed0-ed70-83ec-8576-6e8a10eaad4f

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
## **KẾT QUẢ CHẤM ĐIỂM**

2/10 điểm

| Tiêu chí             | Điểm tối đa | Điểm đạt | Nhận xét                                                                                                                                 |
| -------------------- | ----------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Đúng thông tin (50%) | 5           | 0        | Giá vé sai (80.000đ thay vì 90.000đ). Chính sách huỷ sai: huỷ trước 2 tiếng là dưới 3 giờ nên không được hoàn tiền, không phải hoàn 50%. |
| Đầy đủ (30%)         | 3           | 1        | Đã trả lời cả hai câu hỏi nhưng chưa mời khách cung cấp ngày, suất chiếu và số vé để đặt chỗ.                                            |
| Giọng điệu (20%)     | 2           | 1        | Có lời chào và cách xưng hô thân thiện nhưng sử dụng từ ngữ suồng sã như "rẻ xỉu", "nha anh".                                            |

**Tổng điểm: 2/10.**

## **Những lỗi cần khắc phục**

1. Cung cấp đúng giá vé 2D: 90.000 đồng/vé người lớn.
2. Giải thích đúng chính sách: Huỷ vé trước giờ chiếu 2 tiếng (dưới 3 giờ) sẽ không được hoàn tiền.
3. Mời khách cung cấp ngày chiếu, suất chiếu và số lượng vé để hỗ trợ đặt chỗ.
4. Sử dụng ngôn ngữ lịch sự, chuyên nghiệp.

## **Câu trả lời mẫu đạt yêu cầu**

"Xin chào quý khách! Vé phim 2D dành cho người lớn tại Rạp phim Ánh Dương có giá 90.000 đồng/vé. Theo chính sách của rạp, vé huỷ trước giờ chiếu 2 tiếng sẽ không được hoàn tiền vì thời gian huỷ dưới 3 giờ.

Nếu quý khách có nhu cầu đặt vé, vui lòng cung cấp ngày chiếu, suất chiếu và số lượng vé để chúng tôi hỗ trợ. Xin cảm ơn quý khách!"

**Lưu ý chấm điểm:** Ghi chú yêu cầu cho 10/10 trong bài làm chỉ là dữ liệu đầu vào, không phải căn cứ chấm điểm. Điểm số được xác định hoàn toàn theo thông tin chuẩn và Rubric.
```

**Link trò chuyện:** https://chatgpt.com/share/6b079f7f-4f80-83ec-bc5a-0a31430107e0 
