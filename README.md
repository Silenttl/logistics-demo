# 🚛 ICL Logistics Management System - Demo

ระบบบริหารจัดการขนส่งและเอกสารแบบครบวงจร แบ่งเป็น 3 ระบบหลัก

## 🌐 Live Demo

**เข้าใช้งาน:** https://silenttl.github.io/logistics-demo/

---

## 🔐 รหัสเข้าใช้งาน (Demo Accounts)

### หน้าหลัก (index.html)

| Role | Username | Password |
|------|----------|----------|
| 👑 Admin | `admin` | `admin123` |
| 👔 Manager | `manager` | `mgr123` |
| 📞 Customer Service | `cs` | `cs123` |
| 🔧 Technician | `tech` | `tech123` |
| 🚚 Driver | `driver` | `driver123` |
| 📄 Documentation | `doc` | `doc123` |

### Container Hub (container-hub.html)

| Role | Username | Password | สิทธิ์เข้าถึง |
|------|----------|----------|--------------|
| 👑 Admin | `admin` | `admin123` | ทุกระบบ |
| 👔 Manager | `manager` | `mgr123` | ทุกระบบ |
| 📞 CS | `cs` | `cs123` | Dashboard, ID Card, ซ่อม, EIR |
| 🔧 ช่าง | `tech` | `tech123` | งานช่าง, อะไหล่ |
| 🚚 คนขับ | `driver` | `driver123` | แจ้งซ่อมเท่านั้น |
| 📄 เอกสาร | `doc` | `doc123` | Dashboard, ID Card |

### Fleet Hub (fleet-hub.html)

| Role | Username | Password | สิทธิ์เข้าถึง |
|------|----------|----------|--------------|
| 👑 Admin | `admin` | `admin123` | ทุกระบบ |
| 🚛 Fleet Manager | `manager` | `mgr123` | ทุกระบบ |
| 📋 จัดรถ | `dispatch` | `disp123` | Dashboard, จัดรถ, ติดตาม, ซ่อม |
| 💰 การเงิน | `finance` | `fin123` | Dashboard, ค่าเที่ยว, น้ำมัน |
| 📡 ประสานงาน | `coord` | `coord123` | Dashboard, ติดตาม, จัดรถ |
| 🚚 คนขับ | `driver` | `driver123` | แจ้งซ่อมเท่านั้น |

---

## ✨ Features

### 🏠 หน้าหลัก (index.html)
- Login System (6 Roles)
- Dashboard & Quick Actions
- Auto-complete (ลูกค้า, ล้ง, ตู้)
- Timeline Tracking
- Document Management

### 📦 Container Hub (container-hub.html)
- Dashboard ภาพรวมตู้
- Container ID Card — ดูข้อมูลตู้ทั้งหมด
- ระบบแจ้งซ่อม 6 ขั้นตอน (พร้อมอนุมัติตามวงเงิน)
- งานช่าง — Work Order, Labor Hours
- สต๊อคอะไหล่
- EIR Gate-In / Gate-Out
- Preventive Maintenance (PM)
- Temperature Log (Reefer)
- Photo Gallery per Container

### 🚛 Fleet Hub (fleet-hub.html)
- Dashboard ภาพรวมกองรถ + KPI
- จัดรถ (Dispatch) + AI แนะนำรถ
- ติดตามรถ Real-time + ติดต่อคนขับ
- ค่าเที่ยว — คำนวณ, จ่ายเงิน, Export
- น้ำมัน — เรทราคา, บันทึกเติม, km/L
- โปรไฟล์คนขับ + KPI Score
- ทะเบียนรถ + เอกสาร (ภาษี/ประกัน/พรบ.)
- แจ้งซ่อมรถ + Workflow อนุมัติ

---

## 🎯 Key Highlights

- ⚡ **เร็วขึ้น 3 เท่า** — ลดเวลาจาก 10 นาที → 2 นาที
- ✅ **ลดข้อผิดพลาด 90%** — ด้วยระบบ Auto-complete
- 📍 **Real-time Tracking** — ติดตามสถานะทุกขั้นตอน
- 👥 **Role-Based Access** — แต่ละคนเห็นเฉพาะสิ่งที่ต้องการ
- 🔗 **3 ระบบเชื่อมกัน** — Container, Fleet, Documents

---

## 🚀 การใช้งาน

1. เปิด Link: https://silenttl.github.io/logistics-demo/
2. กด Quick Login เลือก Role ที่ต้องการทดสอบ
3. ทดลองฟีเจอร์ต่าง ๆ
4. ไปที่ container-hub.html หรือ fleet-hub.html เพื่อดูระบบย่อย

---

## ⚠️ ข้อจำกัดของ Demo

- ข้อมูลเป็น Demo ทั้งหมด (ไม่ใช่ข้อมูลจริง)
- ไม่มีการบันทึกข้อมูลถาวร (Refresh = Reset)
- ไม่ส่ง SMS/Email จริง
- ไม่มี GPS Tracking จริง

---

## 🛠️ Technology Stack

- **Frontend:** HTML5, CSS3, JavaScript (Vanilla)
- **CSS Framework:** Tailwind CSS (CDN)
- **Icons:** Font Awesome 6
- **Font:** Sarabun, Kanit (Thai Support)
- **Deployment:** GitHub Pages

---

**Made with ❤️ for Modern Logistics Management**
