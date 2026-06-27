# 🚀 Personal Training Mission — Complete Setup Guide

ผมช่วยเชียร์ให้คุณมีกำลังใจหลวะครับ! 💪⚡ คุณกำลังสร้างแอปที่จะช่วยคุณให้พร้อมสำหรับแข่ง 10K นี้

---

## 📱 ขั้นที่ 1 — Deploy บน GitHub Pages (ใช้เวลา ~5 นาที)

### ปรับปรุง: ตอนนี้ path ทั้งหมดชี้ไปที่ `/ptm-10k/` ถูกต้องแล้ว ✅

ได้ไฟล์พร้อมใช้ 7 ตัว:
- `index.html` (manifest + icons path fixed)
- `app.js` (pre-compiled, no Babel)
- `sw.js` (cache v4, paths fixed)
- `manifest.json` (start_url: `/ptm-10k/`)
- `icon-192.png` & `icon-512.png` (สีส้ม ⚡)
- `drive-backend.gs` (Google Sheets backend)

### ขั้นตอน:

**บน Computer:**
1. เปิด GitHub Desktop
2. โฟลเดอร์ `ptm-10k` → **ลบไฟล์เก่าทั้งหมด**
3. ใส่ไฟล์ 6 ตัวใหม่เข้าไป (ยกเว้น drive-backend.gs อยากใช้หลัง)
4. **Commit**: `Fix: complete path corrections for /ptm-10k/`
5. **Push origin**

**บน GitHub:**
- ให้ GitHub Pages deploy เอง (จะใช้เวลา 2-3 นาที)
- URL: `https://kerati-coder.github.io/ptm-10k/`

---

## 📲 ขั้นที่ 2 — ติดตั้งแอปบนมือถือ

**ลบแอปเก่าก่อน:**
- Android: กดค้างไอคอน → Uninstall
- iPhone: กดค้าง → Remove App

**ติดตั้งใหม่:**

**Android:**
1. เปิด Chrome
2. พิมพ์ `https://kerati-coder.github.io/ptm-10k/`
3. ⋮ → **Install app**

**iPhone:**
1. เปิด Safari
2. พิมพ์ URL เดิม
3. Share 📤 → **Add to Home Screen**

---

## ☁️ ขั้นที่ 3 — Google Drive Sync (Backup/Restore)

### 3.1 สร้าง Google Apps Script:

1. ไปที่ **script.google.com**
2. **New project** → ตั้งชื่อ "PTM Backend"
3. ลบโค้ดเดิม → วาง **`drive-backend.gs`** ทั้งหมด
4. **Save** (Ctrl+S)

### 3.2 Deploy เป็น Web App:

1. กด **Deploy** → **New deployment**
2. Type: **Web app**
3. Execute as: **Me** (บัญชี Google ของคุณ)
4. Who has access: **Anyone** ← **สำคัญ!**
5. กด **Deploy** → ให้ authorize → **Copy URL**

ตัวอย่าง URL: `https://script.google.com/macros/s/xxxxxxxxxxxxx/useless`

### 3.3 ใส่ URL ในแอป:

1. **เปิดแอป PTM** บนมือถือ
2. กด **☁️** (มุมขวาบน)
3. **วาง URL** ที่ copy ไป
4. กด **💾 บันทึก URL**
5. กด **⬆️ Backup** เพื่อทดสอบ

ถ้าขึ้น **✅ Backup สำเร็จ** = พร้อมใช้ได้แล้ว!

---

## 📊 ข้อมูลเก็บที่ไหน?

| ที่เก็บ | อธิบาย | ข้อดี |
|-------|--------|------|
| 📱 **Browser** (localStorage) | เก็บในมือถือเอง | เร็ว, offline ได้, ไม่ต้องรอ |
| ☁️ **Google Sheet** (Backup) | เก็บใน Drive ผ่าน Apps Script | ย้ายเครื่องได้, safe |

**Flow:** Log session → เก็บใน localStorage ทันที → Auto-backup ขึ้น Sheet (ถ้าตั้ง URL)

---

## 🎯 ให้กำลังใจตัวเองครับ! 💪

จากที่เห็น คุณ:
- ✅ เตรียมแผนซ้อม 18 สัปดาห์
- ✅ สร้างแอป gamified tracking
- ✅ Setup backend sync
- ✅ Deployed ได้แล้ว

**นี่คือทักษะเดียวกับที่ใช้ในวิ่ง:** คิด, วางแผน, execute, track, optimize, repeat. 

คุณมี **122 วันถึงแข่ง** ✨ ใช้แอปนี้ให้เต็มที่
- Log ทุก session อย่างจริงจัง
- ดูทรั้นด์ pace ทุกสัปดาห์
- ปรับแผนถ้าต้อง
- **ไฟต้องติดตั้งแต่ตอนนี้** 🔥

---

## ❓ ถ้าติดตรงไหน

- **แอปยังขึ้น 404?** → ลบแอป, clear browser cache, ติดตั้งใหม่
- **Drive sync ไม่ได้?** → เช็คว่า Apps Script deploy ให้ "Anyone" access แล้ว
- **ข้อมูลหาย?** → localStorage เก็บไว้ — try Restore บน Drive

---

## 📝 Files Included

```
ptm-10k/
├── index.html         ← Entry point (manifest + React CDN)
├── app.js            ← Pre-compiled app (3900+ lines)
├── sw.js             ← Service Worker (offline support)
├── manifest.json     ← PWA manifest (start_url: /ptm-10k/)
├── icon-192.png      ← App icon (Orange ⚡)
├── icon-512.png      ← Splash icon
└── drive-backend.gs  ← Google Apps Script (Sheets backend)
```

---

**Ready?** 🚀 

ลงมือก่อนเสีย คนที่ชนะ ไม่ใช่ศูนย์ที่สตาร์ท แต่คนที่ก้าวต่อไป

ปั่นมันสิครับ! 💪⚡

