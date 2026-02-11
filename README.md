# Lottery - Chương Trình Quay Số May Mắn

Chương trình quay số may mắn với giao diện đẹp, hiệu ứng pháo hoa, nhạc nền, và hỗ trợ cấu hình đầy đủ. Phù hợp cho các sự kiện, lễ hội, giáo xứ, trường học, công ty,...

---

## Mục lục

1. [Giới thiệu](#giới-thiệu)
2. [Tải về và chạy chương trình](#tải-về-và-chạy-chương-trình)
3. [Cấu hình chương trình](#cấu-hình-chương-trình)
4. [Hướng dẫn sử dụng](#hướng-dẫn-sử-dụng)
5. [Trang kết quả](#trang-kết-quả)
6. [Thay đổi hình nền](#thay-đổi-hình-nền)
7. [Thêm nhạc nền và âm thanh](#thêm-nhạc-nền-và-âm-thanh)
8. [Cấu trúc thư mục](#cấu-trúc-thư-mục)
9. [Câu hỏi thường gặp](#câu-hỏi-thường-gặp)

---

## Giới thiệu

Đây là chương trình quay số may mắn chạy trên trình duyệt web (Chrome, Firefox, Edge,...). Không cần cài đặt thêm bất kỳ phần mềm nào.

**Tính năng chính:**
- Quay số ngẫu nhiên với hiệu ứng quay đẹp mắt
- Hiệu ứng pháo hoa trên nền hình ảnh
- Nhạc nền và âm thanh khi quay số
- Cấu hình tên tổ chức, tên chương trình
- Tự do thiết lập các giải thưởng (tên giải, phần thưởng, số lượng, số lượt quay/lần)
- Các cấp độ nổi bật cho giải thưởng (thường, nổi bật, đặc biệt)
- Xuất kết quả ra file CSV (mở được bằng Excel)
- Trang kết quả riêng để trình chiếu
- In kết quả trực tiếp từ trình duyệt
- Hỗ trợ nhiều hình nền, tự động nhận diện hình trong thư mục `background/`
- Lưu trữ dữ liệu trên máy (localStorage) - tắt trình duyệt vẫn giữ nguyên kết quả

---

## Tải về và chạy chương trình

### Bước 1: Tải về

- Nhấn nút **Code** (màu xanh) trên trang GitHub này
- Chọn **Download ZIP**
- Giải nén file ZIP vào một thư mục bất kỳ trên máy tính

### Bước 2: Chạy chương trình

- Mở thư mục đã giải nén
- Nhấn đúp chuột vào file **`index.html`**
- Chương trình sẽ tự động mở trong trình duyệt web của bạn

> **Lưu ý:** Không cần kết nối internet để sử dụng chương trình (trừ lần đầu cần tải font chữ). Sau lần đầu, trình duyệt sẽ lưu font chữ vào bộ nhớ đệm (cache).

---

## Cấu hình chương trình

Khi mở chương trình lần đầu, bạn sẽ thấy tên mặc định là "TÊN TỔ CHỨC" và "CHƯƠNG TRÌNH QUAY SỐ". Bạn cần cấu hình lại cho phù hợp.

### Mở cấu hình

1. Nhìn góc dưới bên phải màn hình, tìm nút **"Cấu hình"** (biểu tượng bánh răng)
2. Nhấn vào nút đó, bảng cấu hình sẽ hiện lên

### Các mục cấu hình

#### Tên tổ chức
- Nhập tên tổ chức của bạn (ví dụ: `GIÁO XỨ NAM LỖ`, `TRƯỜNG THPT ABC`, `CÔNG TY XYZ`)
- Tên này sẽ hiển thị ở dòng đầu tiên trên màn hình chính và trang kết quả

#### Tên chương trình
- Nhập tên chương trình (ví dụ: `CHƯƠNG TRÌNH QUAY SỐ 2026`, `ĐẠI HỘI TỔNG KẾT`)
- Tên này sẽ hiển thị ở dòng thứ hai trên màn hình chính

#### Số lớn nhất (MAX)
- Đây là số lớn nhất có thể quay được
- Ví dụ: Nếu bạn có 5000 phiếu, nhập `5001` (vì số bắt đầu từ 0)
- Mặc định là `5001` (quay từ 00000 đến 05000)

#### Số không tham gia
- Nhập các số mà bạn muốn loại trừ (không được quay trúng)
- Cách nhau bằng dấu phẩy, ví dụ: `1001, 2002, 3003`
- Để trống nếu không cần loại trừ số nào

#### Danh sách giải thưởng
Đây là bảng để bạn thiết lập các giải thưởng:

| Cột | Ý nghĩa | Ví dụ |
|-----|---------|-------|
| **Tên giải** | Tên của giải thưởng | `Giải khuyến khích`, `Giải nhất` |
| **Phần thưởng** | Mô tả phần thưởng | `10 Ấm siêu tốc`, `1 Xe đạp` |
| **SL** | Số lượng giải (bao nhiêu người trúng) | `10`, `1` |
| **Quay/lượt** | Mỗi lần bấm quay sẽ ra bao nhiêu số | `5` (quay 5 số một lúc), `1` (quay từng số) |
| **Nổi bật** | Mức độ nổi bật khi hiển thị | `---` (thường), Sao (nổi bật), 2 Sao (đặc biệt) |

- Nhấn **"+ Thêm giải"** để thêm giải mới
- Dùng nút Lên/Xuống để sắp xếp thứ tự các giải
- Nhấn dấu X để xóa giải

> **Quan trọng:** Thứ tự các giải là thứ tự quay. Giải đầu tiên sẽ được quay trước, giải cuối cùng sẽ được quay sau cùng.

### Lưu cấu hình

- Nhấn nút **"Lưu & Đóng"** để lưu thay đổi
- **Lưu ý:** Khi lưu cấu hình, kết quả quay số trước đó sẽ bị xóa để bắt đầu lại từ đầu

### Đặt lại mặc định

- Nhấn nút **"Đặt lại mặc định"** để khôi phục về cấu hình ban đầu
- Sẽ có thông báo xác nhận trước khi đặt lại

---

## Hướng dẫn sử dụng

### Quay số

1. Màn hình chính hiển thị tên giải đang quay và phần thưởng
2. Nhấn nút **"QUAY"** (nút tròn lớn ở giữa) để bắt đầu quay số
3. Các ô số sẽ quay và dừng lại lần lượt, hiển thị số trúng thưởng
4. Số đã quay sẽ hiển thị ở hai bên trái và phải màn hình

### Chuyển giải

- Nhấn **"Giải trước"** để quay lại giải trước đó
- Nhấn **"Giải tiếp"** để chuyển sang giải tiếp theo
- Chương trình sẽ tự động biết giải nào đã quay đủ số lượng

### Thanh điều khiển (góc dưới bên phải)

| Nút | Chức năng |
|-----|-----------|
| **Pháo hoa** | Bật/tắt hiệu ứng pháo hoa |
| **Cấu hình** | Mở bảng cấu hình chương trình |
| **Nhạc nền** | Bật/tắt nhạc nền |
| **Kết quả** | Mở trang kết quả trong tab mới |
| **Xuất CSV** | Tải file kết quả về máy (định dạng CSV, mở bằng Excel) |
| **BG 1/2/3...** | Chọn hình nền |

---

## Trang kết quả

Khi nhấn nút **"Kết quả"**, một trang mới sẽ mở ra hiển thị toàn bộ kết quả quay số:

- Các giải được sắp xếp từ giải lớn nhất (Giải đặc biệt) đến giải nhỏ nhất
- Giải đặc biệt (2 sao) được hiển thị nổi bật nhất với số lớn
- Giải nổi bật (1 sao) được hiển thị ở mức trung bình
- Các giải thường được hiển thị ở mức bình thường
- Giải chưa quay sẽ hiển thị "Chưa quay"

### Các nút trên trang kết quả

| Nút | Chức năng |
|-----|-----------|
| **Quay lại** | Quay về trang quay số chính |
| **Xuất CSV** | Tải kết quả về máy |
| **In kết quả** | Mở hộp thoại in của trình duyệt (in giấy trắng, chữ đen) |

---

## Thay đổi hình nền

### Sử dụng hình nền có sẵn
- Ở góc dưới bên phải, tìm ô chọn **"BG 1"**, **"BG 2"**, **"BG 3"**,...
- Nhấn chọn hình nền bạn thích, hình sẽ thay đổi ngay lập tức

### Thêm hình nền mới
1. Mở thư mục `background/` trong thư mục chương trình
2. Đặt hình ảnh vào thư mục này với tên theo quy tắc:
   - `background1.jpg` (hoặc `.png`, `.webp`)
   - `background2.jpg`
   - `background3.webp`
   - `background4.png`
   - ...
3. Số thứ tự phải liên tiếp (1, 2, 3, 4,...)
4. Tải lại trang web, hình nền mới sẽ tự động xuất hiện trong danh sách chọn

> **Định dạng hỗ trợ:** `.jpg`, `.jpeg`, `.png`, `.webp`

---

## Thêm nhạc nền và âm thanh

Chương trình sử dụng 2 file âm thanh:

| File | Chức năng | Vị trí |
|------|-----------|--------|
| `music.mp3` | Nhạc nền phát liên tục | Cùng thư mục với file HTML chính |
| `spinwheel.mp3` | Âm thanh khi quay số | Cùng thư mục với file HTML chính |

Để thay đổi nhạc nền hoặc âm thanh quay:
1. Chuẩn bị file nhạc mới (định dạng `.mp3`)
2. Đổi tên file thành `music.mp3` (cho nhạc nền) hoặc `spinwheel.mp3` (cho âm thanh quay)
3. Thay thế file cũ trong thư mục chương trình

---

## Cấu trúc thư mục

```
lottery/
  |-- index.html    (Trang chính - quay số)
  |-- KET QUA.html            (Trang kết quả)
  |-- music.mp3               (Nhạc nền)
  |-- spinwheel.mp3           (Âm thanh quay số)
  |-- background/             (Thư mục chứa hình nền)
  |   |-- background1.jpg
  |   |-- background2.jpg
  |   |-- background3.webp
  |   |-- ...
  |-- Firework/               (Thư viện hiệu ứng pháo hoa phụ)
  |-- README.md               (File hướng dẫn này)
```

---

## Câu hỏi thường gặp

### Tôi tắt trình duyệt rồi, dữ liệu có mất không?
**Không.** Dữ liệu được lưu trên trình duyệt (localStorage). Chỉ cần bạn mở lại cùng trình duyệt và cùng file, dữ liệu vẫn còn nguyên.

### Làm sao để xóa hết kết quả và bắt đầu lại?
Mở **Cấu hình** > nhấn **"Lưu & Đóng"** (không cần thay đổi gì). Kết quả quay số sẽ được xóa và bắt đầu lại từ đầu.

### Tôi có thể chạy trên điện thoại không?
**Có.** Chương trình hỗ trợ giao diện responsive, có thể chạy trên điện thoại và máy tính bảng. Tuy nhiên, nên sử dụng trên màn hình lớn (máy tính, laptop, TV) để có trải nghiệm tốt nhất.

### File CSV mở bị lỗi font tiếng Việt?
Khi mở file CSV bằng Excel, nếu bị lỗi font:
1. Mở Excel
2. Chọn **File > Open** (không nhấn đúp chuột vào file)
3. Chọn file CSV
4. Ở mục **File Origin / Encoding**, chọn **UTF-8**
5. Nhấn **OK**

### Tôi muốn dùng trên máy khác, làm sao chuyển dữ liệu?
Dữ liệu lưu trong trình duyệt nên không tự động chuyển được. Bạn có thể:
- **Xuất CSV** trên máy cũ để lưu kết quả
- Trên máy mới, cấu hình lại chương trình

### Làm sao để trình chiếu kết quả lên màn hình lớn (TV/máy chiếu)?
1. Kết nối máy tính với TV/máy chiếu qua HDMI
2. Mở trang **KET QUA.html** trên trình duyệt
3. Nhấn **F11** để xem toàn màn hình
4. Trang kết quả sẽ tự động cập nhật khi bạn quay số trên trang chính (cần mở cả 2 trang trên cùng trình duyệt)

---

## Tác giả

Chương trình được phát triển bởi **vinctuyen2601**.

Nếu bạn gặp lỗi hoặc cần hỗ trợ, vui lòng tạo issue trên trang GitHub này.
