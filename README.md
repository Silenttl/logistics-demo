# 🚛 Logistics Management System - Demo

ระบบบริหารจัดการขนส่งและเอกสารแบบครบวงจร แบ่งเป็น 3 ทีมหลัก

## 🌐 Live Demo

**เข้าใช้งาน:** https://silenttl.github.io/logistics-demo/

## 🔐 Demo Accounts

# 🚛 Logistics Demo - ระบบจัดการขนส่งและเอกสาร v2.0

ระบบสาธิตการบริหารจัดการงาน Logistics แบบครบวงจร ตั้งแต่การสร้างงานด่วน การติดตามตู้คอนเทนเนอร์ ไปจนถึงการจัดการเอกสารส่งออก

## 🚀 ฟีเจอร์หลัก (Key Features)
* **Quick Login:** ระบบล็อกอินด่วนสำหรับทดสอบตามสิทธิ์ผู้ใช้งาน (Admin, CS, Driver, Document)
* **Quick Actions:** สร้างงานใหม่ จัดรถ และอัปเดตสถานะได้ในคลิกเดียวจากหน้า Dashboard
* **Container Tracking:** ระบบติดตามหมายเลขตู้คอนเทนเนอร์ เบอร์ซีล (Seal) และสถานะการคืนตู้ (Empty Return)
* **Auto-Complete System:** ระบบช่วยเติมข้อมูลลูกค้าและหมายเลขตู้คอนเทนเนอร์อัตโนมัติ
* **Job Timeline:** แสดงประวัติการทำงานย้อนหลังแบบละเอียดในแต่ละงานขนส่ง

## 🔑 ข้อมูลสำหรับการทดสอบ (Test Accounts)
สามารถใช้งานปุ่ม "Quick Login" ในหน้าแรก หรือกรอกข้อมูลดังนี้:
- **Admin:** User: `admin` / Pass: `admin123` (จัดการได้ทุกส่วน)
- **CS Team:** User: `cs` / Pass: `cs123` (สร้างและจัดการงาน)
- **Driver:** User: `driver` / Pass: `driver123` (อัปเดตสถานะขนส่ง)

## 🛠️ วิธีการติดตั้งและรันโปรเจค (Mac/Windows)
1.  **Clone โปรเจค:**
    ```bash
    git clone [https://github.com/Silenttl/logistics-demo.git](https://github.com/Silenttl/logistics-demo.git)
    ```
2.  **เปิดด้วย VS Code:**
    - ลากโฟลเดอร์โปรเจคเข้าโปรแกรม VS Code
    - ติดตั้ง Extension **"Live Server"**
3.  **รันระบบ:**
    - คลิกขวาที่ไฟล์ `index.html` แล้วเลือก **"Open with Live Server"**

## 📂 โครงสร้างไฟล์
- `index.html`: ไฟล์หลักที่รวม HTML, CSS (UI Design), และ JavaScript (Logic ระบบ)
- `README.md`: คู่มือการใช้งานและข้อมูลโปรเจค

---
*พัฒนาเพื่อเป็นตัวอย่างระบบจัดการขนส่งสินค้า (TMS) สำหรับธุรกิจส่งออก*

## ✨ Features

### Team 1: Fleet Management 🚚
- ระบบจ่ายงานให้คนขับ
- ส่งคำสั่งงานผ่าน SMS/Line
- ระบบแจ้งซ่อมรถ
- ติดตามสถานะรถ

### Team 2: Document Management 📄
- เอกสารครบทั้ง 4 ประเภท
- สถานะ 7 ขั้นตอน
- Checklist ต่อตู้ (เช่น ครบ 2/4)
- ระบบขออนุมัติจากหน่วยงานรัฐ
- การขอแก้ไขเอกสาร

### Team 3: Container Management 📦
- ติดตามตำแหน่งตู้
- กราฟอุณหภูมิ (Reefer) ทุก 6 ชม.
- รายงานความเสียหาย
- สถิติการใช้งาน

## 🎯 Key Highlights

- ⚡ **เร็วขึ้น 3 เท่า** - ลดเวลาจาก 10 นาที → 2 นาที
- ✅ **ลดข้อผิดพลาด 90%** - ด้วยระบบ Auto-complete
- 📍 **Real-time Tracking** - ติดตามสถานะทุกขั้นตอน
- 👥 **แบ่งทีมชัดเจน** - ไม่สับสน แต่ละคนรู้หน้าที่
- 🔗 **Integration** - 3 ทีมทำงานร่วมกันได้ลื่นไหล

## 📱 QR Code

สแกนเพื่อเข้าใช้งาน Demo:

```
[สร้าง QR Code ที่ https://www.qr-code-generator.com]
```

## 🚀 การใช้งาน

1. เปิด Link: https://silenttl.github.io/logistics-demo/
2. เลือก Quick Login → Admin / Fleet / Document / Container
3. ทดลองใช้งานฟีเจอร์ต่าง ๆ
4. อ่านคู่มือในเมนู "📖 คู่มือการใช้งาน"

## 📊 สิ่งที่ Demo แสดง

- ✅ Dashboard แสดงภาพรวม
- ✅ Quick Actions (สร้างงาน, จัดรถ, อัพเดทสถานะ)
- ✅ Auto-complete (ลูกค้า, ล้ง, ตู้)
- ✅ Timeline Tracking
- ✅ Document Status Flow
- ✅ Container Monitoring
- ✅ Integration Between Teams

## ⚠️ ข้อจำกัดของ Demo

- ข้อมูลเป็น Demo ทั้งหมด
- ไม่มีการบันทึกข้อมูลจริง (Read-Only)
- ไม่ส่ง SMS/Email จริง
- ไม่มี GPS Tracking จริง

## 📄 เอกสารเพิ่มเติม

- [คู่มือ Deploy](./DEPLOY-GUIDE.md)
- [การออกแบบระบบ 3 ทีม](./3-TEAMS-SYSTEM-DESIGN.md)
- [สรุปโปรเจค](./PROJECT_SUMMARY.md)

## 🛠️ Technology Stack

- **Frontend:** HTML5, CSS3, JavaScript (Vanilla)
- **Font:** Sarabun, Kanit (Thai Support)
- **Design:** Single Page Application (SPA)
- **Deployment:** GitHub Pages

## 📞 Contact

สนใจพัฒนาต่อ หรือมีคำถาม:
- อ่านเอกสารประกอบใน Repository
- ดู Issues สำหรับปัญหาที่พบ

## 📝 License

Demo Version - For Presentation Only

---

**Made with ❤️ for Modern Logistics Management**
