# 🎥 YouTube Auto Live Stream (OBS ছাড়া)

GitHub Actions দিয়ে 24/7 YouTube Live Streaming — সম্পূর্ণ ফ্রি!

---

## ✅ Setup করার ধাপ

### Step 1: Video Google Drive এ Upload করো
- যেকোনো MP4 video Google Drive এ upload করো
- File এ Right Click → **Share** → **Anyone with the link** → Copy link
- Link টা এরকম দেখাবে:
  ```
  https://drive.google.com/file/d/XXXXXXXXXXXXXXXXX/view
  ```
- শুধু মাঝের ID টা নাও: `XXXXXXXXXXXXXXXXX`

### Step 2: GitHub Repo বানাও
- github.com এ যাও → **New Repository**
- **Public** রাখো (Unlimited minutes এর জন্য)
- এই folder এর সব files upload করো

### Step 3: Secrets Add করো
GitHub Repo → **Settings** → **Secrets and variables** → **Actions** → **New repository secret**

দুইটা secret বানাও:

| Secret Name | Value |
|------------|-------|
| `STREAM_KEY` | YouTube Stream Key |
| `VIDEO_URL` | Google Drive File ID (শুধু ID, পুরো link না) |

### Step 4: YouTube Stream Key নাও
- youtube.com/livestreaming যাও
- **Stream** tab → Stream Key copy করো

### Step 5: Live Start করো
- GitHub Repo → **Actions** tab
- **YouTube Auto Live Stream** → **Run workflow** → **Run**
- 2-3 মিনিট পর YouTube Studio তে দেখো live শুরু হয়েছে!

---

## ⏱️ কীভাবে চলবে

```
Manual Start → 5 ঘণ্টা 50 মিনিট চলে → বন্ধ
↓
10 মিনিট পর Auto Restart → আবার 5 ঘণ্টা 50 মিনিট
↓
এভাবে 24/7 চলতে থাকবে ♾️
```

> ⚠️ প্রতি 6 ঘণ্টায় ~10 মিনিটের gap আসবে — এটা স্বাভাবিক

---

## 🔒 Stream Key কি Safe?

হ্যাঁ! Repo public হলেও **GitHub Secrets** কেউ দেখতে পারে না।
