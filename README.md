<p align="center">
  <img src="https://img.shields.io/badge/HieuTool-v2.0.0-blueviolet?style=for-the-badge&logo=discord&logoColor=white" alt="Version"/>
  <img src="https://img.shields.io/badge/Node.js-%3E%3D18-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node"/>
  <img src="https://img.shields.io/badge/TypeScript-5.3+-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
  <img src="https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge" alt="License"/>
</p>

<h1 align="center">🔮 HieuTool — Discord Quest [Updated]</h1>

<p align="center">
  <b>Công cụ tự động hoàn thành và nhận thưởng Quest trên Discord</b><br/>
  <i>Auto-complete & auto-claim Discord Quests — fast, silent, and effortless.</i>
</p>

---

## ✨ Giới thiệu

**HieuTool** là một công cụ dòng lệnh (CLI) được viết bằng TypeScript, giúp bạn **tự động hoàn thành** các Discord Quest và **nhận thưởng (claim)** mà không cần thao tác thủ công.

### 🎯 Tính năng chính

| Tính năng | Mô tả |
|-----------|-------|
| 🎬 **Auto Watch Video** | Tự động xem video quest với tiến trình giả lập chính xác |
| 🎮 **Auto Play on Desktop** | Giả lập heartbeat cho quest dạng chơi game trên desktop |
| 📡 **Auto Stream** | Hỗ trợ quest dạng stream trên desktop |
| 🕹️ **Auto Play Activity** | Hỗ trợ quest dạng chơi Activity |
| ⭐ **Auto Claim Rewards** | Tự động nhận thưởng ngay khi hoàn thành quest |
| 🔮 **Orbs Tracking** | Theo dõi số Orbs trước và sau khi hoàn thành |
| 📊 **Live Dashboard** | Giao diện CLI real-time hiển thị tiến trình từng quest |

---

## 📋 Yêu cầu hệ thống

- **Node.js** >= 18
- **npm** (đi kèm với Node.js)
- **Discord User Token** (token tài khoản người dùng)

---

## 🚀 Hướng dẫn cài đặt & sử dụng

### Bước 1: Clone hoặc tải source code

```bash
git clone https://github.com/Nguoibianhz/Discord-Auto-Quests.git
cd Discord-Auto-Quests
```

### Bước 2: Cài đặt dependencies

```bash
npm install
```

### Bước 3: Cấu hình Token

Tạo file `.env` trong thư mục gốc của project với nội dung:

```env
TOKEN=your_discord_user_token_here
```

> ⚠️ **Lưu ý bảo mật**: Không bao giờ chia sẻ token của bạn cho bất kỳ ai. Token cho phép truy cập toàn bộ tài khoản Discord của bạn.

### Bước 4: Chạy tool

```bash
npm run go
```

Hoặc chạy trực tiếp:

```bash
npx tsx --env-file=.env farm.ts
```

---

## 🖥️ Giao diện Dashboard

Khi chạy, tool sẽ hiển thị một bảng dashboard real-time trong terminal:

```
   __  __   ____   ______   __  __   ______   ____    ____    __
  / / / /  /  _/  / ____/  / / / / /_  __/  / __ \  / __ \  / /
 / /_/ /  / /   / __/   / / / /   / /   / / / / / / / / /
/ __  /  / /   / /___  / /_/ /   / /   / /_/ / / /_/ / / /___
/_/ /_/  \___/  \____/   \____/   /_/    \____/ \____/  /_____/

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  ⦿ Account: username | ID: 123456 | Orbs: 🔮 500 | 12:00:00
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
┌────┬──────────────────────┬────────┬──────────┬──────────┬──────────┐
│ #  │ QUEST                │ TYPE   │ REWARD   │REMAINING │ STATUS   │
├────┼──────────────────────┼────────┼──────────┼──────────┼──────────┤
│ 1  │ Watch Trailer        │  🎬    │ 50 Orbs  │ 2m 30s   │ ⟳ RUN   │
│ 2  │ Play Game X          │  🎮    │ 100 Orbs │ ● DONE   │ ★ CLAIM  │
└────┴──────────────────────┴────────┴──────────┴──────────┴──────────┘

  Progress ████░░ 1/2 (1 active)

  Press Ctrl+C to stop
```

---

## 📁 Cấu trúc dự án

```
farmdiscord/
├── farm.ts           # Entry point — UI dashboard & orchestration
├── src/
│   └── engine.ts     # Core engine — Discord API, Quest logic
├── .env              # Cấu hình token (không commit lên git!)
├── package.json      # Dependencies & scripts
├── tsconfig.json     # TypeScript config
├── LICENSE           # Giấy phép sử dụng
└── README.md         # Tài liệu bạn đang đọc
```

---

## ❓ Câu hỏi thường gặp (FAQ)

<details>
<summary><b>Cách lấy Discord User Token?</b></summary>

1. Mở Discord trên trình duyệt hoặc ứng dụng Desktop
2. Nhấn `Ctrl + Shift + I` để mở Developer Tools
3. Chuyển sang tab **Network**
4. Thực hiện bất kỳ hành động nào trên Discord
5. Tìm request đến `discord.com/api` và copy giá trị `Authorization` trong Headers

</details>

<details>
<summary><b>Tool có an toàn không?</b></summary>

Tool hoạt động bằng cách giả lập các request API giống như Discord Client chính thức. Tuy nhiên, việc sử dụng user token tự động có thể vi phạm Terms of Service của Discord. **Sử dụng có rủi ro bị ban tài khoản.**

</details>

<details>
<summary><b>Tại sao một số quest bị SKIP?</b></summary>

Một số quest có thể chưa được hỗ trợ hoặc đã hết hạn. Tool chỉ xử lý các quest đang hoạt động và chưa hoàn thành.

</details>

---

## 📊 Thống kê dự án

<p align="center">
  <a href="https://github.com/Nguoibianhz/Discord-Auto-Quests/stargazers">
    <img src="https://img.shields.io/github/stars/Nguoibianhz/Discord-Auto-Quests?style=for-the-badge&logo=github&color=f0e68c" alt="Stars"/>
  </a>
  <a href="https://github.com/Nguoibianhz/Discord-Auto-Quests/network/members">
    <img src="https://img.shields.io/github/forks/Nguoibianhz/Discord-Auto-Quests?style=for-the-badge&logo=github&color=87ceeb" alt="Forks"/>
  </a>
  <a href="https://github.com/Nguoibianhz/Discord-Auto-Quests/issues">
    <img src="https://img.shields.io/github/issues/Nguoibianhz/Discord-Auto-Quests?style=for-the-badge&logo=github&color=ffa07a" alt="Issues"/>
  </a>
  <a href="https://github.com/Nguoibianhz/Discord-Auto-Quests/commits">
    <img src="https://img.shields.io/github/commit-activity/m/Nguoibianhz/Discord-Auto-Quests?style=for-the-badge&logo=github&color=98fb98" alt="Commits"/>
  </a>
  <img src="https://img.shields.io/github/last-commit/Nguoibianhz/Discord-Auto-Quests?style=for-the-badge&logo=github&color=dda0dd" alt="Last Commit"/>
  <img src="https://img.shields.io/github/watchers/Nguoibianhz/Discord-Auto-Quests?style=for-the-badge&logo=github&color=c9b1ff" alt="Watchers"/>
</p>

## 📈 Star History

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=Nguoibianhz/Discord-Auto-Quests&type=Date&theme=dark&t=20260311" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=Nguoibianhz/Discord-Auto-Quests&type=Date&t=20260311" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=Nguoibianhz/Discord-Auto-Quests&type=Date&t=20260311" />
  </picture>
</p>

---

## 👨‍💻 Tác giả

<p align="center">
  <a href="https://nguyenmanhhieu.info.vn/">
    <img src="https://img.shields.io/badge/Website-nguyenmanhhieu.info.vn-blue?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Website"/>
  </a>
</p>

| | Thông tin |
|---|---|
| 👤 **Tên** | **Nguyễn Mạnh Hiếu** |
| 🌐 **Website** | [nguyenmanhhieu.info.vn](https://nguyenmanhhieu.info.vn/) |
| 🛠️ **Dự án** | HieuTool — Discord Quest Auto Claim |

> 💬 Nếu bạn muốn sử dụng source code này cho mục đích cá nhân hoặc thương mại, vui lòng **liên hệ tác giả** để xin phép tại [nguyenmanhhieu.info.vn](https://nguyenmanhhieu.info.vn/).

---

## 📜 Bản quyền

Copyright © 2024-2026 **Nguyễn Mạnh Hiếu**. All rights reserved.

Xem chi tiết tại file [LICENSE](./LICENSE).

---

<p align="center">
  <sub>Made with ❤️ by <a href="https://nguyenmanhhieu.info.vn/">Nguyễn Mạnh Hiếu</a></sub>
</p>
