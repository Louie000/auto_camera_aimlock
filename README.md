# auto_camera_aimlock

🔫 เปลี่ยนกล้องอัตโนมัติเป็น First Person ขณะเล็ง และกลับ Third Person เมื่อไม่ได้เล็ง พร้อมปิดการยิงในมุมกล้องที่ไม่ใช่ First Person เพื่อเพิ่มความสมจริงและป้องกันการยิงแบบสเปรย์

## Features
- เปลี่ยนกล้องอัตโนมัติ: First Person ตอนเล็ง, Third Person ตอนไม่ได้เล็ง
- ปิดการยิงเมื่ออยู่ใน Third Person และไม่ได้เล็ง
- ประหยัด CPU โดยตรวจสอบทุก 800ms เมื่อไม่ถืออาวุธ

## วิธีติดตั้ง
1. วางโฟลเดอร์ `auto_camera_aimlock` ลงใน `resources/`
2. เพิ่มบรรทัดนี้ใน `server.cfg` หรือ `resources.cfg`:
