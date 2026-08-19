# โครงข่ายลูกเต๋า (Cube Net Visualizer)

เครื่องมือ interactive สอนเรื่อง cube net (โครงข่ายลูกบาศก์) ใน 3 ขั้นตอน — เขียนด้วย vanilla HTML/CSS/JS ไฟล์เดียว ไม่ใช้ library ภายนอกเลย

**Demo:** https://mynameisnampetch51-del.github.io/cube/

## 3 ขั้นตอน

1. **วางแปลน (Layout)** — ลากวาง 6 หน้าเป็นโครงข่ายบนกริด เลือกได้ว่าจะวางแบบไหนถึงจะพับเป็นลูกบาศก์ได้จริง
2. **วาด (Draw)** — วาด/ลบลงบนแต่ละหน้าด้วยพาเลท 5 สี ก่อนพับ
3. **พับ (Fold)** — ดูโครงข่ายพับเป็นลูกบาศก์ 3 มิติ พร้อมลวดลายที่วาดไว้ ใช้ CSS 3D transform ล้วน ไม่ใช้ WebGL/Three.js

## เทคนิคที่ใช้

- **Canvas 2D** สำหรับวาดลวดลายลงแต่ละหน้า (pen/eraser tool)
- **CSS 3D transform** (`rotateX`, `rotateY`, `translateZ`) พับกล่องแบนให้เป็นทรงลูกบาศก์จริง ไม่พึ่ง library กราฟิก
- Design token system (`--accent`, `--surface`, ...) รองรับ light/dark mode อัตโนมัติผ่าน `prefers-color-scheme` และสลับมือได้ผ่าน `data-theme`
- ปรับ layout ให้ responsive และรองรับข้อความไทยที่ไม่มีช่องว่าง (`overflow-wrap: anywhere`)

## รันเอง

เปิด `index.html` ในเบราว์เซอร์ได้เลย ไม่ต้องติดตั้งอะไรเพิ่ม
