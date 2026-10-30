# เผยแพร่ Portfolio ให้คนนอกเปิดได้

โปรเจ็กต์นี้เป็นเว็บ static: เปิดจาก `index.html` ได้เลย และไม่ต้องติดตั้ง Node.js หรือสั่ง build ก่อนเผยแพร่

## วิธีแนะนำ: GitHub + Vercel

วิธีนี้เหมาะถ้าต้องการแก้เว็บในอนาคต เพราะทุกครั้งที่อัปโหลดการแก้ไขขึ้น GitHub, Vercel จะเผยแพร่เวอร์ชันใหม่ให้อัตโนมัติ

1. แตกไฟล์ ZIP นี้ลงในโฟลเดอร์หนึ่งบนเครื่องก่อน อย่าอัปโหลดไฟล์ ZIP เข้า Vercel โดยตรง
2. เข้า [GitHub](https://github.com) และลงชื่อเข้าใช้ แล้วกด **New repository**
3. ตั้งชื่อ เช่น `thanakrit-qa-portfolio` เลือก **Public** แล้วกด **Create repository**
4. กด **Add file** → **Upload files** แล้วลากไฟล์และโฟลเดอร์ทั้งหมดที่อยู่ในโปรเจ็กต์นี้เข้าไป: `index.html`, `img`, `reports` และ `DEPLOY.md` จากนั้นกด **Commit changes**
5. เข้า [Vercel](https://vercel.com) แล้วลงชื่อเข้าใช้ด้วย GitHub
6. กด **Add New…** → **Project** แล้วกด **Import** ที่ repository `thanakrit-qa-portfolio`
7. ในหน้าตั้งค่า ให้ปล่อย Build Command และ Output Directory ว่างไว้ (เว็บนี้ไม่มีขั้นตอน build) แล้วกด **Deploy**
8. รอจนขึ้นสถานะสำเร็จ แล้วกด **Visit** หรือคัดลอกลิงก์ `https://...vercel.app` ส่งให้คนอื่นเปิดได้ทันที

เมื่อต้องการอัปเดตเว็บในครั้งต่อไป ให้แก้ไฟล์ แล้วอัปโหลด/commit ไฟล์ที่เปลี่ยนขึ้น GitHub; Vercel จะสร้างลิงก์เวอร์ชันใหม่ให้อัตโนมัติและอัปเดตลิงก์หลัก

คู่มืออ้างอิง: [Vercel: Deploying Git repositories](https://vercel.com/docs/git) และ [Vercel: Builds for static websites](https://vercel.com/docs/builds)

## ทางเลือก: GitHub Pages (ไม่ต้องมี Vercel)

1. ทำขั้นตอน 1–4 ของวิธี GitHub + Vercel ด้านบนก่อน
2. ใน repository บน GitHub กด **Settings** → **Pages**
3. ที่ **Build and deployment** เลือก **Source: Deploy from a branch**
4. เลือก branch `main` และ folder `/(root)` แล้วกด **Save**
5. หลัง GitHub สร้างเว็บเสร็จ ให้เปิดลิงก์ที่แสดงในหน้า Pages ซึ่งมักเป็น `https://ชื่อผู้ใช้.github.io/thanakrit-qa-portfolio/`

คู่มืออ้างอิง: [GitHub Pages: configuring a publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

## ตรวจสอบก่อนแชร์

- เปิด `index.html` ในเบราว์เซอร์ แล้วตรวจปุ่ม **English / ภาษาไทย** ในหัวข้อรายงาน ShopLab
- กดเปิด PDF ภาษาไทยทั้ง 4 รายการ และกดดูใบรับรองทั้ง 2 ใบ
- เว็บไซต์นี้มีอีเมล เบอร์โทร และภาพใบรับรองแบบเต็มอยู่แล้ว ตรวจให้แน่ใจก่อนตั้ง repository เป็น Public หรือส่งลิงก์ให้คนภายนอก

