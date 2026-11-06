# UNO Party Arena — HTML Prototype

งานชุดนี้เป็น **static HTML prototype** ไม่ใช่เว็บไซต์ที่ deploy และไม่ต้องติดตั้ง dependency

## เปิดดู

- เปิด `index.html` เพื่อเลือกว่าจะดู Prototype หรือ Design System
- เปิด `design-system.html` เพื่อดู tokens, typography, controls, cards และ avatars
- เปิด `prototype.html` เพื่อทดลอง flow และเล่นกับ Bot
- ออกแบบแบบ mobile-first สำหรับหน้าจอแนวตั้ง 9:16 และยังเปิดบน desktop ได้

## สิ่งที่กดทดลองได้

Home → Avatar → Create Room → Lobby → Game → Result, Join Room demo, ปรับ capacity 2–10, เพิ่ม Bot, สลับ player/spectator, invitation modal, เล่นไพ่/จั่วไพ่, Skip, Reverse, +2, Wild, +4, UNO และ rematch

## ขอบเขต

State อยู่ใน browser memory ไม่มี backend, authentication หรือ multiplayer synchronization จริง QR เป็น visual demo และ LINE share เปิด URL ของ prototype เท่านั้น

## Deploy ด้วย GitHub Actions

โปรเจกต์มี workflow ที่ `.github/workflows/deploy-pages.yml` สำหรับ GitHub Pages แล้ว โดยจะ deploy อัตโนมัติเมื่อ push เข้า branch `main` หรือสั่งรันเองจากแท็บ Actions

1. สร้าง repository บน GitHub
2. เปิด Terminal ในโฟลเดอร์นี้แล้วรัน:

   ```bash
   git init
   git add .
   git commit -m "Add UNO Party Arena prototype"
   git branch -M main
   git remote add origin https://github.com/USERNAME/REPOSITORY.git
   git push -u origin main
   ```

3. เปิด repository บน GitHub แล้วไปที่ **Settings → Pages**
4. ที่ **Build and deployment → Source** เลือก **GitHub Actions**
5. เปิดแท็บ **Actions** เพื่อตรวจ workflow ชื่อ “Deploy static prototype to GitHub Pages”

เมื่อ deploy สำเร็จ URL จะมีรูปแบบ `https://USERNAME.github.io/REPOSITORY/`
