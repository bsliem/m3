GitHub **Release không dùng `git push` / `git pull` như repo bình thường**.
 Release là **một lớp khác của GitHub** (assets attached to a tag). Vì vậy có **2 cách làm**:

------

# 1️⃣ Cách bạn đang làm (Web GitHub) – KHÔNG cần lệnh

Bạn:

```
Create release
Upload mp3
```

→ xong.

Không cần git.

------

# 2️⃣ Cách dùng command line (chuẩn dân dev)

Dùng **GitHub CLI (`gh`)**

## Cài GitHub CLI

Mac:

```
brew install gh
```

Windows:

```
winget install GitHub.cli
```

------

## Login GitHub

```
gh auth login
```

------

# 3️⃣ Tạo release bằng lệnh

Ví dụ bạn đang ở repo

```
/Users/mac/Documents/m3
```

Tạo release:

```
gh release create audio-dia-tang-v1 *.mp3 \
--title "Audio Dia Tang v1" \
--notes "Bản audio Kinh Địa Tạng"
```

GitHub sẽ:

```
upload mp3
tạo release
attach files
```

------

# 4️⃣ Upload thêm file vào release

Ví dụ thêm mp3:

```
gh release upload audio-dia-tang-v1 18.mp3
```

------

# 5️⃣ Download release

Download toàn bộ:

```
gh release download audio-dia-tang-v1
```

------

# 6️⃣ Xóa release

```
gh release delete audio-dia-tang-v1
```

------

# 7️⃣ Liệt kê releases

```
gh release list
```

------

# So sánh

| thao tác    | repo git   | release               |
| ----------- | ---------- | --------------------- |
| upload file | `git push` | `gh release upload`   |
| download    | `git pull` | `gh release download` |
| version     | commit     | tag                   |

------

# Workflow chuẩn cho repo audio của bạn

1️⃣ code / quarto

```
git add .
git commit -m "update quarto"
git push
```

2️⃣ audio

```
gh release upload audio-dia-tang-v1 *.mp3
```

------

# Một mẹo rất hay cho repo `m3`

Bạn có thể upload cả folder:

```
gh release create audio-dia-tang-v2 di_zang_du/*.mp3
```

GitHub tự attach tất cả mp3.

------

💡 Nếu bạn muốn, tôi có thể chỉ bạn **1 workflow rất mạnh cho repo audio**:

```
drop mp3 vào folder
chạy 1 lệnh
→ GitHub tự tạo release
```

(automation kiểu **1 lệnh build + upload mp3**) 🚀
 Dùng rất tiện cho repo kinh Phật của bạn.

Tóm tắt phiên làm việc vừa rồi cho tôi để tôi làm md

Dưới đây là **bản tóm tắt phiên làm việc** để bạn có thể **copy vào file `.md`** trong repo (ví dụ `session_2026_03_14.md`).

```
# Phiên làm việc GitHub – quản lý audio MP3 bằng Releases
Ngày: 2026-03-14

## 1. Mục tiêu
Thiết lập hệ thống lưu trữ và phân phối file **audio MP3 tụng kinh** trên GitHub mà:
- repo vẫn nhẹ
- dễ tải
- dễ quản lý phiên bản

---

# 2. Nguyên tắc quan trọng

Không commit file mp3 lớn trực tiếp vào repo.

Lý do:

- GitHub cảnh báo từ 50 MB
- GitHub giới hạn cứng 100 MB / file
- repo > 1–5 GB sẽ rất chậm

Giải pháp tốt hơn:
```

repo → code + markdown + quarto
 release → mp3

```
---

# 3. Thiết lập Release

Đã tạo release:
```

audio-dia-tang-v1

```
tag:
```

di_zang

```
Nội dung:

- mp3 Kinh Địa Tạng
- chia theo phẩm

Ví dụ:
```

01-地藏菩薩本願經開頭.mp3
 02-01 香讚.mp3
 03-02 淨口業真言.mp3
 ...
 17-12 見聞利益品.mp3

```
Release trở thành nơi lưu trữ **audio chính**.

---

# 4. Cấu trúc repo
```

m3
 │
 ├── README.md
 ├── m3.qmd
 ├── _quarto.yml
 ├── di_zang_du
 ├── leng_yan_jing_yuan_dao_chen_yuan
 │
 └── GitHub Releases
 └── audio-dia-tang-v1
 ├── mp3 files

```
---

# 5. Link tải trực tiếp mp3

Dạng link:
```

https://github.com/henrydoth/m3/releases/download/di_zang/<filename>.mp3

```
Ví dụ:
```

https://github.com/henrydoth/m3/releases/download/di_zang/01-地藏菩薩本願經開頭.mp3

```
Có thể dùng link này để:

- nhúng audio player
- làm website
- chia sẻ mp3

---

# 6. Lệnh Git dùng cho repo

Quy trình chuẩn:
```

git add .
 git commit -m "update"
 git push

```
Dùng cho:

- quarto
- markdown
- scripts

---

# 7. Release không dùng git push

Release có hai cách:

### Cách đơn giản

Trên GitHub web:
```

Create release
 upload mp3
 publish

```
### Cách CLI

Dùng GitHub CLI:
```

gh release create audio-dia-tang-v1 *.mp3

```
---

# 8. Bài học quan trọng

### 1. Tách repo và data
```

repo → text/code
 release → audio

```
### 2. Repo luôn nhẹ

git clone nhanh.

### 3. Release phù hợp cho

- mp3
- video
- dataset
- model AI

---

# 9. Việc cần làm tiếp

- thêm README đẹp cho repo
- tạo audio player
- tạo release cho:
  - Lăng Nghiêm
  - Chú Đại Bi
  - các kinh khác

---

# 10. Kết luận

GitHub Releases là giải pháp tốt để:

- lưu trữ audio lớn
- phân phối file
- giữ repo sạch và nhẹ

Repo `m3` hiện đã thiết lập đúng workflow.
```

------

Nếu bạn muốn, tôi có thể viết thêm cho bạn **một file `README.md` chuẩn cho repo `m3`**, có:

- bảng các kinh
- audio player nghe trực tiếp
- link download

Repo sẽ **giống một thư viện kinh online**.