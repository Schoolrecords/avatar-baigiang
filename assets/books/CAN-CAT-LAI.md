# Kho hình minh hoạ — sổ theo dõi ảnh cần cắt lại

Soát ngày 27/08/2026 bằng `node scripts/bang-anh.mjs`, xem 259 ảnh trong 11 tấm
bằng mắt. Sổ này chỉ ghi ảnh **thật sự hỏng**, không ghi ảnh chỉ có dải nền màu
chạm mép (thứ đó không phải lỗi).

## Vì sao hỏng

Ảnh của **Global Maths 3** cắt trước ngày 27/08 làm theo lối cũ: khoanh MỘT KHUNG
CHỮ NHẬT trên trang sách đã render rồi cắt. Lối đó dính hai tật cùng lúc — khung
ôm luôn chữ, số trang, dải màu của trang sách; mà mép khung lại cắt ngang thân vật.

Ảnh của **Global Maths 1** và các bài **Review** cắt sau đó theo lối mới
(`anh-don.mjs` cắt từng vật rồi `ghep-anh.mjs` ghép lại) thì sạch — 24/24 ảnh tấm 1
và gần hết tấm 4 không có lỗi nào. Lối mới là lối đúng.

## Hạng A — ĐÃ CẮT LẠI XONG ngày 27/08/2026 ✓

20 ảnh dưới đây đã cắt lại theo lối mới và đã lắp vào bài.

| Ảnh | Trước đây hỏng thế nào | Nay |
|---|---|---|
| `s7-u1-nguyen-tu.png` | KHÔNG phải hình nguyên tử — chỉ là một mảng màu xanh/vàng nhoè. Lại là ảnh DUY NHẤT của bài Khoa học 7. | Xoá, thay bằng **hai** ảnh mới: `s7-u1-mo-hinh-nguyen-tu.png` (mô hình nguyên tử lithium có đủ 5 ô ghi nhãn) và `s7-u1-democritus.png` (tượng Democritus ở phần Getting Ready). |
| `u13-butchi.png` | Tên là "bút chì" nhưng trong ảnh không có bút chì nào, chỉ có cây thước cụt ở vạch 8. | Cắt lại đúng ô số 2 trang 32: có cả bút chì lẫn thước. Cắt lại luôn `u13-ca`, `u13-qua`, `u13-oto` cùng bài. |
| `u11-butchi.png` | Có vệt đen chạy ngang. **Vệt đen nằm trong chính bản PDF**, thử đủ ba chế độ render đều còn — không phải lỗi cắt. | Cắt phần trên của ba ô, dừng ngay trên vệt đen. Phần bị mất là ô điền đáp án, mà app tự vẽ ô đó rồi. |
| `u11-vit.png` | Vệt đen ở đáy — cùng nguyên nhân. | Cắt gọn lấy riêng sơ đồ đoạn thẳng Uncle/Jenny. Cắt lại luôn `u11-bupbe`, `u11-bang`. |
| `u30-bupbe.png` | Bảng số liệu cụt mất cột: "Hoa" cụt thành "Hoc", số 10 mất một nửa. | Cắt lại trọn bảng 4 cột. |
| `u30-oto.png` | Cùng lỗi, cụt ở "Jac…" và số 12. | Cắt lại trọn bảng 4 cột. |
| `u21-robot.png` | Gần như trống, chỉ còn số trang 51 và vài vệt màu. | Cắt lại trọn con robot, đủ từ đầu tới bàn chân. |
| `u26-ca.png` | Đồng hồ bị cắt, lại dính nguyên chữ tiêu đề "Learn" của trang sách. | Cắt lại riêng mặt đồng hồ. |
| `u26-cb.png` | Đồng hồ cụt mất đỉnh, dính hình mờ HEID. | Cắt lại riêng đồng hồ báo thức, đủ cả chuông lẫn chân. |
| `u26-cc.png` | Đồng hồ cụt cả đỉnh lẫn cạnh trái. | Cắt lại riêng mặt đồng hồ. |
| `u20-vuong.png` | Dính dòng chữ cụt hai đầu "…en, circle and wr…". | Cắt lại riêng hình vuông trên lưới ô 1 cm. Cắt lại luôn `u20-cn`, `u20-ab`. |
| `u21-abcd.png` | Dính chữ của bài khác: "Maths in Life / My head is c…". | Cắt lại riêng hình chữ nhật ABCD. Cắt lại luôn `u21-efgh`. |

## Hạng B — dính chữ thừa, số trang, hoặc cụt nhẹ

Nhìn vẫn hiểu được nhưng lên máy chiếu thì luộm thuộm. **33 ảnh, chưa sửa:**

`u10-cam` · `u12-bong` · `u12-sticker` · `u13-be` · `u13-but` · `u13-kien` ·
`u13-learn` · `u13-sach` · `u15-binh` · `u15-coc` · `u15-learn` · `u16-aoam` ·
`u16-dam` · `u16-lanh` · `u19-p3` · `u20-hinh` · `u21-bang` · `u21-luoi` ·
`u22-oo` · `u24-khoi` · `u24-learn` · `u25-c1` · `u25-c2` · `u25-xedap` ·
`u26-guong` · `u27-lich` · `u27-thang3` · `u28-the` · `u29-trai` · `u30-bang` ·
`u30-butchi` · `u31-xucxac` · `r2-sapmau` · `r4-dongho` · `r4-the`

Tật hay gặp nhất, theo thứ tự: dính số trang và dải màu chân trang; dính chữ
tiêu đề mục ("Learn", "Practise", "Maths in Life"); dính hình mờ HEID; cụt mất
một mẩu chữ của bài bên cạnh.

## Một chuyện KHÔNG phải lỗi ảnh, nhưng phát hiện cùng lúc

Trang 49 (Unit 20) có bài tập **2. Listen, circle and write — Track 39**, bốn hình
tam giác để nghe rồi viết chu vi. App bỏ hẳn bài này. Không phải quên: **đáp án
nằm trong file nghe Track 39 mà trung tâm chưa có**, không thể suy ra từ hình.

Đây là một giới hạn có thật của cả quy trình, không riêng bài này: **bài tập nào
đáp án chỉ có trong băng thì chưa số hoá được cho tới khi xin được bộ mp3 của
NXB.** Thà bỏ trống còn hơn tự nghĩ ra số.

## Cắt lại thế nào

```bash
# 1. Vẽ trang sách ra ảnh lớn
node scripts/pdf-render.mjs "<pdf>" <trang> <trang> nguon-sach/tam 3

# 2. Cắt TỪNG VẬT một, khung rộng rãi, để script tự xén sát viền
node scripts/anh-don.mjs nguon-sach/tam/trang-NN.png <x> <y> <w> <h> \
     public/assets/books/<ten>.png --le=16 --nen=trong

# 3. Cần ghép nhiều vật thành một dãy thì
node scripts/ghep-anh.mjs public/assets/books/<ten>.png <a.png> <b.png> --cao=320 --so

# 4. Soi lại
node scripts/bang-anh.mjs --loc=<ten>
```

**Không bao giờ cắt theo cụm.** Một khung ôm nhiều vật là nguồn gốc của toàn bộ
danh sách trên.
