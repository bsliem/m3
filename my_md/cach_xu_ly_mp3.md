------

# 1️⃣ Việc bạn đã làm sáng nay (workflow hoàn chỉnh)

### 1. Chuẩn bị file audio

Bạn mở file tụng **地藏菩薩本願經** trong **Audacity**.

Sau đó xử lý cơ bản:

- kiểm tra waveform
- nhận ra có **noise nền nhẹ**
- chạy **Noise Reduction**

quy trình:

```
Effect
→ Noise Removal and Repair
→ Noise Reduction
```

------

### 2. Xử lý lỗi âm thanh

Bạn sửa các lỗi nhỏ:

- click noise
- đoạn âm thanh đột ngột
- peak quá lớn

các công cụ dùng:

```
Repair
Clip Fix
Amplify
```

------

### 3. Chuẩn hóa âm lượng

Bạn đã normalize toàn bộ file:

```
Ctrl + A
Effect
→ Normalize
→ -1 dB
```

Kết quả:

- âm lượng đồng đều
- không bị clipping

------

### 4. Tạo hệ thống bookmark (label)

Bạn tạo **17 label** tương ứng các phần kinh:

```
0:00   地藏菩薩本願經開頭
0:16   香讚
1:03   淨口業真言
2:03   覺林菩薩偈
4:22   讚
5:58   開經偈
6:29   忉利天宮神通品第一
22:48  分身集會品第二
34:43  閻浮眾生業感品第四
49:30  地獄名號品第五
56:02  如來讚歎品第六
1:10:37 利益存亡品第七
1:18:37 閻羅王眾讚歎品第八
1:31:50 稱佛名號品第九
1:38:07 校量布施功德緣品第十
1:46:07 地神護法品第十一
1:50:33 見聞利益品第十二
2:08:25 囑累人天品第十三
```

và xác nhận:

```
2:21:51 = cuối file
```

→ **không thừa đoạn nào**.

------

### 5. Sửa file label

Bạn đã:

- chỉnh tab
- import lại label
- kiểm tra bookmark khớp với điện thoại.

------

### 6. Export thành nhiều MP3

Bạn cấu hình:

```
Export Audio
→ Multiple Files
→ Split based on Labels
→ Using Label Name
```

Bitrate:

```
170–210 kbps
```

------

# 2️⃣ Bài học quan trọng hôm nay

## 1. Label phải khớp timeline audio

Bookmark điện thoại **không phải lúc nào cũng khớp 100%** với file gốc.

Luôn kiểm tra:

```
Label Editor
```

------

## 2. Phần đầu kinh thường có đoạn “giới thiệu”

Trong file hôm nay:

```
0:00 – 0:16
```

là đoạn đọc tên kinh.

→ cần tạo label riêng:

```
地藏菩薩本願經開頭
```

------

## 3. Phẩm cuối phải kéo đến hết file

Bạn đã phát hiện lỗi quan trọng:

```
囑累人天品第十三
```

không kết thúc ở bookmark mà phải kéo tới:

```
2:21:51
```

------

## 4. Normalize trước khi export

Nếu không normalize:

- mỗi đoạn MP3 âm lượng khác nhau
- nghe rất khó chịu.

------

## 5. Export Multiple giúp tiết kiệm rất nhiều thời gian

Nếu cắt thủ công:

```
17 đoạn × 3 phút = ~50 phút
```

Export Multiple:

```
10 giây
```

------

# 3️⃣ Kinh nghiệm rút ra

### 1. Workflow chuẩn khi làm audio kinh

```
1 import audio
2 noise reduction
3 repair lỗi
4 normalize
5 tạo label
6 kiểm tra label
7 export multiple mp3
```

------

### 2. Label nên đặt số trước

Ví dụ:

```
01 香讚
02 淨口業真言
03 覺林菩薩偈
```

để điện thoại **không sắp xếp sai**.

------

### 3. Luôn giữ file label

File:

```
ksitigarbha_labels.txt
```

rất quan trọng.

Sau này nếu audio lỗi bạn chỉ cần:

```
import label
```

→ 17 bookmark tự xuất hiện.

------

### 4. Audacity xử lý file dài vẫn ổn

File của bạn:

```
2h21m
```

Noise reduction vẫn chạy được, chỉ cần chờ.

------

# 4️⃣ Kết quả cuối cùng của buổi sáng

Bạn đã có:

- audio sạch hơn
- bookmark chuẩn
- label file chuẩn
- khả năng export thành **17 mp3 riêng**

tương ứng:

```
香讚
淨口業真言
覺林菩薩偈
開經偈
...
囑累人天品第十三
```

------

💡