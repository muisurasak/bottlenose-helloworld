# โปรโตคอลการส่ง Commit และมาตรฐานการสังเกตการณ์

## Git & Commit Protocols (กฎ 9-12)
| กฎ | รายละเอียด |
| --- | --- |
| 9 | ตรวจสอบโค้ดก่อน Commit โดยใช้ `pre-commit` hook |
| 10 | ทดสอบเฉพาะส่วนที่เปลี่ยนแปลงด้วย `npm test` |
| 11 | ใช้ Conventional Commits สำหรับข้อความ Commit เช่น `feat:` หรือ `fix:` |
| 12 | บันทึกผลลัพธ์หลัง Commit ใน `CHANGELOG.md` |

## Observability Standards (กฎ 13-16)
| กฎ | รายละเอียด |
| --- | --- |
| 13 | ใช้ JSDoc เพื่อเอกสารฟังก์ชันและพารามิเตอร์ |
| 14 | บันทึกข้อมูลตามระดับความสำคัญ (error, warn, info) |
| 15 | อัปเดตเอกสารเมื่อเปลี่ยนแปลงสถาปัตยกรรม |
| 16 | ใช้ `console.log` สำหรับการ debug ชั่วคราวเท่านั้น |

## Pre-flight Checklist
1. ตรวจสอบว่าไม่มี error ใน `npm run typecheck`
2. ทดสอบฟังก์ชันที่เปลี่ยนแปลงด้วย `npm test`
3. ใช้ `pre-push hook` เพื่อตรวจสอบอัตโนมัติก่อน push ไปยัง remote

> หมายเหตุ: `pre-push hook` จะรัน `npm test` และ `lint` อัตโนมัติ