# Portal thegood
> หน้า redirect เดียว: `officethegood.github.io` → IT Portal ตัวจริงบน Google Sites ใช้โดยพนักงาน The Good ที่จำ URL หลักได้ง่ายกว่า

## ระบบคืออะไร / ทำอะไรได้
- มีไฟล์เดียวคือ `index.html` — redirect ทันที (meta refresh + `location.replace`) ไปที่
  `https://sites.google.com/view/thegoodambulance/`
- ไม่มี logic อื่น ไม่มี backend

## Stack & บริการภายนอก
- Static HTML บน **GitHub Pages** (user site root)
- Git remote: `https://github.com/officethegood/officethegood.github.io.git`
- ปลายทาง redirect: Google Sites `thegoodambulance` (IT Portal ตัวจริง แก้เนื้อหาที่ Google Sites ไม่ใช่ที่ repo นี้)

## โครงสร้างไฟล์สำคัญ
- `index.html` — ไฟล์เดียวทั้งโปรเจกต์ (redirect + ลิงก์สำรองถ้า redirect ไม่ทำงาน)

## การทำงานหลักของระบบ
1. ผู้ใช้เปิด `https://officethegood.github.io/`
2. `<meta http-equiv="refresh">` + JS `location.replace()` พาไป Google Sites
3. deploy = `git push` ไป `main` (Pages auto-deploy)

## สถานะ
- **Active** — commit ล่าสุด 2026-07-10 ("redirect: officethegood.github.io → IT Portal ตัวจริง (Google Sites)")

## Gotchas / ข้อควรระวัง
- อย่าเข้าใจผิดว่า Portal ตัวจริงอยู่ที่นี่ — เนื้อหา Portal อยู่บน Google Sites ทั้งหมด
- URL root ของ GitHub Pages นี้ยังเป็น base ของ project sites อื่นด้วย (เช่น `/thegood-stock/`, `/pt-medical-system/` เป็น repo แยก ไม่เกี่ยวกับโฟลเดอร์นี้)

## เอกสารอื่นในโปรเจกต์
- ไม่มี
