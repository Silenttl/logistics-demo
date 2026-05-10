# 📦 CONTAINER ID CARD SYSTEM
## ระบบบัตรประจำตัวตู้คอนเทนเนอร์ + การรายงานความเสียหาย

---

## 🎯 CONCEPT: "บัตรประจำตัวตู้"

เหมือนบัตรประชาชน มี **Container Number** เป็นเลขประจำตัวที่ไม่เปลี่ยน

```
┌─────────────────────────────────────────────────────┐
│  📦 CONTAINER ID CARD                               │
│  ระบบบัตรประจำตัวตู้คอนเทนเนอร์                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│  🔍 ค้นหาด้วย:                                      │
│     • Container Number (TBCU2122923)               │
│     • RFID Tag                                     │
│     • QR Code                                      │
│     • Barcode                                      │
│                                                     │
│  📊 แสดงข้อมูล:                                     │
│     • ข้อมูลพื้นฐาน                                 │
│     • ประวัติการใช้งาน                              │
│     • ประวัติการซ่อม                                │
│     • ประสิทธิภาพ                                   │
│     • สถานะปัจจุบัน                                 │
│                                                     │
│  🔒 Access Control:                                │
│     • หัวหน้าทีม                                    │
│     • ผู้จัดการ                                     │
│     • เจ้าหน้าที่ที่เกี่ยวข้อง                       │
│                                                     │
└─────────────────────────────────────────────────────┘
```

---

## 🔍 1. CONTAINER IDENTIFICATION (ตัวระบุตู้)

### **1.1 Primary Key - Container Number**

```
รูปแบบ: 4 ตัวอักษร + 7 ตัวเลข
ตัวอย่าง: TBCU2122923

โครงสร้าง:
├─ TBC     : Owner Code (3-4 ตัว)
├─ U       : Category (U=Freight Container)
├─ 212292  : Serial Number
└─ 3       : Check Digit

คุณสมบัติ:
✅ ไม่ซ้ำกัน (Unique)
✅ ไม่เปลี่ยนแปลง (ตลอดอายุการใช้งาน)
✅ มาตรฐานสากล (ISO 6346)
```

### **1.2 Secondary Identifiers (ตัวระบุเสริม)**

```
1. QR Code
   ┌─────────────┐
   │  █▀▀▀▀▀▀▀█ │
   │  █ ▄▄▄ █  │
   │  █ ███ █  │   → สแกนได้ Container Number
   │  █▄▄▄▄▄▄▄█ │      + Link ไปหน้า ID Card
   └─────────────┘
   
2. RFID Tag
   • ติดที่ตู้
   • อ่านได้ระยะไกล 1-10 เมตร
   • เก็บข้อมูล: Container Number, Owner, Type
   
3. Barcode (1D)
   ||||||||||||||||||||
   TBCU2122923
   
4. GPS Tracker (Optional)
   • ติดตามตำแหน่งแบบ Real-time
   • ประวัติเส้นทาง
```

---

## 📋 2. CONTAINER ID CARD LAYOUT

### **2.1 หน้าจอ Container ID Card**

```
┌──────────────────────────────────────────────────────────────┐
│  🔍 ค้นหาตู้                                    [🔒 Admin]   │
├──────────────────────────────────────────────────────────────┤
│  Container Number: [TBCU2122923          ] [🔍 ค้นหา]       │
│  หรือสแกน: [📱 QR Code] [📡 RFID] [📊 Barcode]              │
└──────────────────────────────────────────────────────────────┘

╔══════════════════════════════════════════════════════════════╗
║  📦 CONTAINER ID CARD                                        ║
║  TBCU2122923                                  [พิมพ์ ID Card]║
╠══════════════════════════════════════════════════════════════╣
║                                                              ║
║  ┌────────────────────┐  ┌──────────────────────────────┐   ║
║  │                    │  │ 🏷️ ข้อมูลพื้นฐาน             │   ║
║  │   [รูปตู้]          │  │                              │   ║
║  │                    │  │ Container No: TBCU2122923    │   ║
║  │   [QR Code]        │  │ Size: 40HC (40ft High Cube)  │   ║
║  │                    │  │ Type: Reefer (ตู้เย็น)       │   ║
║  └────────────────────┘  │ Owner: MAMMOTH               │   ║
║                          │ Mfg Year: 2018               │   ║
║  📊 สถานะ: 🟢 พร้อมใช้   │ Tare Weight: 4,200 kg       │   ║
║  📍 ตำแหน่ง: ลานจอด A3  │ Max Payload: 26,580 kg      │   ║
║                          │ CSC Valid: 2026-12-31       │   ║
║                          └──────────────────────────────┘   ║
║                                                              ║
║  ┌──────────────────────────────────────────────────────┐   ║
║  │ 📈 ประสิทธิภาพ (Performance Score: 92/100)          │   ║
║  ├──────────────────────────────────────────────────────┤   ║
║  │ Uptime:        ████████████████░░ 85%               │   ║
║  │ Condition:     ██████████████████ 95%               │   ║
║  │ Utilization:   ████████████████░░ 88%               │   ║
║  │ Reliability:   ███████████████████ 98%              │   ║
║  └──────────────────────────────────────────────────────┘   ║
║                                                              ║
║  ┌──────────────────────────────────────────────────────┐   ║
║  │ 📊 สถิติการใช้งาน                                   │   ║
║  ├──────────────────────────────────────────────────────┤   ║
║  │ 🚛 Total Trips:        127 เที่ยว                   │   ║
║  │ 📏 Total Distance:     65,400 km                     │   ║
║  │ ⏱️ Total Hours:        3,250 ชม.                    │   ║
║  │ 📅 Days in Service:    420 วัน                       │   ║
║  │ 💰 Revenue Generated:  ฿1,850,000                    │   ║
║  │ 🔧 Maintenance Cost:   ฿125,400                      │   ║
║  │ 💵 Cost per Trip:      ฿987                          │   ║
║  └──────────────────────────────────────────────────────┘   ║
║                                                              ║
╠══════════════════════════════════════════════════════════════╣
║  [📜 ประวัติการใช้งาน] [🔧 ประวัติซ่อม] [⚠️ รายงานเสีย]   ║
╚══════════════════════════════════════════════════════════════╝
```

### **2.2 Tab: ประวัติการใช้งาน (Usage History)**

```
┌──────────────────────────────────────────────────────────────┐
│  📜 ประวัติการใช้งาน - TBCU2122923                          │
├──────────────────────────────────────────────────────────────┤
│  [ล่าสุด ▼] [30 วันย้อนหลัง ▼] [🔍 ค้นหา: RN/วันที่]      │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  ┌────────────────────────────────────────────────────────┐ │
│  │ 🚚 Trip #127                    [ดูรายละเอียด]        │ │
│  ├────────────────────────────────────────────────────────┤ │
│  │ RN Number: RN20260510-042                             │ │
│  │ วันที่: 2026-05-08 → 2026-05-10 (3 วัน)              │ │
│  │ เส้นทาง: ตลาดไท → หนองคาย (485 km)                   │ │
│  │ สินค้า: ทุเรียน (960 Bxs / 21,235 kg)                │ │
│  │ อุณหภูมิ: Set 14°C | เฉลี่ย 13.8°C ✅                │ │
│  │ สถานะ: ✅ ส่งมอบสำเร็จ                                │ │
│  │ Rating: ⭐⭐⭐⭐⭐ (5.0)                              │ │
│  └────────────────────────────────────────────────────────┘ │
│                                                              │
│  ┌────────────────────────────────────────────────────────┐ │
│  │ 🚚 Trip #126                    [ดูรายละเอียด]        │ │
│  ├────────────────────────────────────────────────────────┤ │
│  │ RN Number: RN20260504-025                             │ │
│  │ วันที่: 2026-05-03 → 2026-05-05 (3 วัน)              │ │
│  │ เส้นทาง: จันทบุรี → เชียงของ (625 km)                │ │
│  │ สินค้า: มังคุด (1,200 Bxs / 18,500 kg)               │ │
│  │ อุณหภูมิ: Set 12°C | เฉลี่ย 12.2°C ✅                │ │
│  │ สถานะ: ✅ ส่งมอบสำเร็จ                                │ │
│  │ Rating: ⭐⭐⭐⭐ (4.5)                                 │ │
│  └────────────────────────────────────────────────────────┘ │
│                                                              │
│  [โหลดเพิ่ม...] (125 รายการก่อนหน้า)                       │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

### **2.3 Tab: ประวัติการซ่อม (Maintenance History)**

```
┌──────────────────────────────────────────────────────────────┐
│  🔧 ประวัติการซ่อม - TBCU2122923                            │
├──────────────────────────────────────────────────────────────┤
│  [ทั้งหมด ▼] [สำเร็จแล้ว ✅] [กำลังซ่อม 🔄] [รออนุมัติ ⏳]│
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  📊 สรุป:                                                    │
│  • ซ่อมทั้งหมด: 8 ครั้ง                                     │
│  • ค่าใช้จ่ายรวม: ฿125,400                                   │
│  • เฉลี่ยต่อครั้ง: ฿15,675                                   │
│  • Downtime รวม: 45 วัน                                      │
│                                                              │
├──────────────────────────────────────────────────────────────┤
│  ┌────────────────────────────────────────────────────────┐ │
│  │ ⚠️ Repair #8 - PENDING APPROVAL                        │ │
│  ├────────────────────────────────────────────────────────┤ │
│  │ รายงานเมื่อ: 2026-05-09 16:45                         │ │
│  │ รายงานโดย: นายประสิทธ์พร (คนขับ)                      │ │
│  │                                                        │ │
│  │ 🔴 ความรุนแรง: High (สูง)                             │ │
│  │ 📝 ปัญหา: ระบบทำความเย็นทำงานผิดปกติ                  │ │
│  │          อุณหภูมิไม่คงที่ ขึ้นลง 10-18°C              │ │
│  │                                                        │ │
│  │ 📷 รูปภาพ: [🖼️ IMG_001.jpg] [🖼️ IMG_002.jpg]          │ │
│  │                                                        │ │
│  │ 💰 ประมาณการ:                                         │ │
│  │    • ค่าชิ้นส่วน: ฿35,000 (Compressor)                │ │
│  │    • ค่าแรง: ฿8,000                                   │ │
│  │    • รวม: ฿43,000                                     │ │
│  │    • ระยะเวลา: 3-5 วัน                                │ │
│  │                                                        │ │
│  │ 🏢 อู่แนะนำ: บริษัท ช่างตู้เย็น จำกัด                 │ │
│  │ 📞 โทร: 02-123-4567                                   │ │
│  │                                                        │ │
│  │ 📋 สถานะ: ⏳ รออนุมัติจากผู้จัดการ                    │ │
│  │                                                        │ │
│  │ [✅ อนุมัติ] [❌ ปฏิเสธ] [✏️ ขอข้อมูลเพิ่ม]          │ │
│  └────────────────────────────────────────────────────────┘ │
│                                                              │
│  ┌────────────────────────────────────────────────────────┐ │
│  │ ✅ Repair #7 - COMPLETED                               │ │
│  ├────────────────────────────────────────────────────────┤ │
│  │ รายงาน: 2026-04-15 | เสร็จ: 2026-04-18 (3 วัน)       │ │
│  │ ปัญหา: ประตูชำรุด ปิดไม่สนิท                          │ │
│  │ ความรุนแรง: 🟡 Medium                                 │ │
│  │ ซ่อมโดย: ร้านประตูตู้ XYZ                             │ │
│  │ ค่าใช้จ่าย: ฿12,500                                    │ │
│  │ ผู้อนุมัติ: ผู้จัดการสมชาย                            │ │
│  │ [ดูรายละเอียด]                                        │ │
│  └────────────────────────────────────────────────────────┘ │
│                                                              │
│  [ดูทั้งหมด 8 รายการ]                                       │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

---

## 🚨 3. DAMAGE REPORTING WORKFLOW

### **3.1 ขั้นตอนการรายงานความเสียหาย**

```
┌─────────────────────────────────────────────────────────────┐
│  STEP 1: รายงานโดยผู้พบเห็น (Reporter)                      │
│  👤 คนขับ / เจ้าหน้าที่ / พนักงานล้ง                        │
└─────────────────────────────────────────────────────────────┘
          │
          ↓
┌─────────────────────────────────────────────────────────────┐
│  กรอกแบบฟอร์มรายงาน:                                        │
│  ├─ Container Number (Auto-fill ถ้าใช้ QR/RFID)            │
│  ├─ วันที่/เวลาพบ                                          │
│  ├─ สถานที่พบ                                              │
│  ├─ ระดับความรุนแรง (Minor/Medium/Severe)                  │
│  ├─ ประเภทความเสียหาย                                      │
│  │  • โครงสร้าง (บุบ, ฉีก, รั่ว)                          │
│  │  • ประตู (ชำรุด, บานพับหลุด)                           │
│  │  • พื้น (ทะลุ, เป็นรู)                                  │
│  │  • ระบบไฟฟ้า (ไฟไม่ติด, สายขาด)                        │
│  │  • ระบบทำความเย็น (Reefer เสีย, อุณหภูมิผิดปกติ)        │
│  │  • อื่นๆ                                                │
│  ├─ รายละเอียด (Text)                                      │
│  ├─ รูปภาพ (1-10 รูป)                                      │
│  ├─ วิดีโอ (Optional)                                      │
│  └─ ผลกระทบต่อการใช้งาน                                   │
│     • ใช้งานได้ปกติ                                        │
│     • ใช้งานได้ แต่ต้องระวัง                               │
│     • ไม่ควรใช้งาน                                         │
│     • ห้ามใช้งาน (อันตราย)                                 │
└─────────────────────────────────────────────────────────────┘
          │
          ↓
┌─────────────────────────────────────────────────────────────┐
│  STEP 2: ส่งให้ Container Manager ตรวจสอบ                   │
│  📧 Notification ทันที                                      │
└─────────────────────────────────────────────────────────────┘
          │
          ↓
┌─────────────────────────────────────────────────────────────┐
│  Container Manager ตรวจสอบ:                                 │
│  ├─ ยืนยันข้อมูล                                           │
│  ├─ ประเมินความรุนแรงอีกครั้ง                              │
│  ├─ ตรวจสอบประวัติตู้                                       │
│  └─ ตัดสินใจ:                                              │
│     • Minor → ซ่อมเอง / บันทึกไว้                          │
│     • Medium/Severe → ส่งต่อขออนุมัติ                      │
└─────────────────────────────────────────────────────────────┘
          │
          ↓ (Medium/Severe)
┌─────────────────────────────────────────────────────────────┐
│  STEP 3: ขออนุมัติซ่อม                                     │
│  Container Manager สร้าง Repair Request:                    │
│  ├─ ข้อมูลความเสียหาย (จาก Report)                         │
│  ├─ ประมาณการค่าใช้จ่าย                                    │
│  │  • ค่าชิ้นส่วน                                          │
│  │  • ค่าแรง                                               │
│  │  • ค่าขนส่ง (ถ้าต้องลาก)                               │
│  │  • รวมทั้งหมด                                           │
│  ├─ ระยะเวลาซ่อม (ประมาณการ)                               │
│  ├─ อู่ที่แนะนำ (2-3 ราย พร้อมราคา)                        │
│  ├─ ผลกระทบต่อธุรกิจ                                       │
│  │  • ตู้หยุดใช้งาน X วัน                                  │
│  │  • รายได้ที่เสียไป X บาท                                │
│  │  • ต้องหาตู้ทดแทน (ใช่/ไม่)                             │
│  └─ ความเร่งด่วน (ด่วนมาก/ด่วน/ปกติ)                      │
└─────────────────────────────────────────────────────────────┘
          │
          ↓
┌─────────────────────────────────────────────────────────────┐
│  STEP 4: ผู้มีอำนาจพิจารณา                                 │
│                                                             │
│  ระดับอำนาจตามวงเงิน:                                       │
│  ├─ < ฿10,000    → หัวหน้าทีม                             │
│  ├─ ฿10,001-50,000 → ผู้จัดการแผนก                        │
│  ├─ ฿50,001-200,000 → ผู้จัดการทั่วไป                     │
│  └─ > ฿200,000   → ผู้บริหาร                              │
│                                                             │
│  ตัวเลือก:                                                  │
│  ✅ อนุมัติ → ดำเนินการซ่อม                                │
│  ❌ ปฏิเสธ → ระบุเหตุผล                                    │
│  ⏸️ รอพิจารณา → ขอข้อมูลเพิ่ม                             │
│  ✏️ แก้ไข → ปรับราคา/อู่/วิธีการ                          │
└─────────────────────────────────────────────────────────────┘
          │
          ↓ (อนุมัติ)
┌─────────────────────────────────────────────────────────────┐
│  STEP 5: ดำเนินการซ่อม                                     │
│  ├─ สร้าง Work Order                                       │
│  ├─ ส่งตู้เข้าอู่                                           │
│  ├─ ติดตามความคืบหน้า                                      │
│  │  • วันที่เข้าอู่                                         │
│  │  • กำลังซ่อม (% Complete)                               │
│  │  • ปัญหาเพิ่มเติม (ถ้าพบ)                               │
│  │  • ETA เสร็จ                                            │
│  ├─ รับตู้กลับ                                             │
│  ├─ ตรวจสอบการซ่อม                                         │
│  └─ ทดสอบการใช้งาน                                         │
└─────────────────────────────────────────────────────────────┘
          │
          ↓
┌─────────────────────────────────────────────────────────────┐
│  STEP 6: ปิดงาน (Close Repair)                             │
│  ├─ ค่าใช้จ่ายจริง                                         │
│  ├─ ระยะเวลาจริง                                           │
│  ├─ ผลการทดสอบ (Pass/Fail)                                │
│  ├─ Warranty (ระยะเวลารับประกัน)                           │
│  ├─ รูปภาพหลังซ่อม                                         │
│  ├─ เปลี่ยนสถานะตู้: กลับมาพร้อมใช้งาน                     │
│  └─ บันทึกลง Container ID Card                            │
└─────────────────────────────────────────────────────────────┘
```

---

## 🔒 4. ACCESS CONTROL (การควบคุมสิทธิ์)

### **4.1 ระดับการเข้าถึง**

```
┌──────────────────────────────────────────────────────────┐
│  ROLE-BASED ACCESS CONTROL                              │
├──────────────────────────────────────────────────────────┤
│                                                          │
│  👑 Level 1: CEO / ผู้บริหาร                            │
│  ├─ ✅ ดูได้ทุกตู้                                       │
│  ├─ ✅ ดูข้อมูลทั้งหมด (รวมต้นทุน)                      │
│  ├─ ✅ อนุมัติการซ่อมทุกระดับ                            │
│  └─ ✅ Export ข้อมูล                                    │
│                                                          │
│  👔 Level 2: ผู้จัดการทั่วไป (General Manager)          │
│  ├─ ✅ ดูได้ทุกตู้                                       │
│  ├─ ✅ ดูข้อมูลทั้งหมด                                   │
│  ├─ ✅ อนุมัติ < ฿200,000                               │
│  └─ ✅ ดูรายงานสรุป                                     │
│                                                          │
│  👨‍💼 Level 3: ผู้จัดการแผนก (Department Manager)        │
│  ├─ ✅ ดูตู้ในความรับผิดชอบ                             │
│  ├─ ✅ ดูข้อมูลเกือบทั้งหมด                              │
│  ├─ ✅ อนุมัติ ฿10,001-50,000                           │
│  └─ ✅ สร้างรายงาน                                      │
│                                                          │
│  👷 Level 4: หัวหน้าทีม (Team Leader)                   │
│  ├─ ✅ ดูตู้ในทีม                                        │
│  ├─ ✅ ดูข้อมูลพื้นฐาน + ประวัติ                         │
│  ├─ ✅ อนุมัติ < ฿10,000                                │
│  ├─ ✅ รายงานความเสียหาย                                │
│  └─ ✅ สร้าง Repair Request                            │
│                                                          │
│  👤 Level 5: เจ้าหน้าที่ (Staff)                         │
│  ├─ ✅ ดูตู้ที่กำลังใช้งาน                               │
│  ├─ ✅ ดูข้อมูลพื้นฐาน                                   │
│  ├─ ✅ รายงานความเสียหาย                                │
│  └─ ❌ ไม่สามารถอนุมัติ                                 │
│                                                          │
│  🚚 Level 6: คนขับ (Driver)                             │
│  ├─ ✅ ดูตู้ที่ตัวเองรับผิดชอบ                           │
│  ├─ ✅ ดูข้อมูลสถานะ                                     │
│  ├─ ✅ รายงานความเสียหาย                                │
│  └─ ❌ ไม่เห็นข้อมูลต้นทุน                              │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

### **4.2 Data Visibility Matrix**

| ข้อมูล | Driver | Staff | Team Leader | Dept Mgr | GM | CEO |
|--------|--------|-------|-------------|----------|----|----|
| **Container Number** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| **ข้อมูลพื้นฐาน** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| **สถานะปัจจุบัน** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| **ประวัติการใช้งาน** | 📊 บางส่วน | ✅ | ✅ | ✅ | ✅ | ✅ |
| **ประวัติการซ่อม** | ❌ | 📊 บางส่วน | ✅ | ✅ | ✅ | ✅ |
| **ค่าใช้จ่ายซ่อม** | ❌ | ❌ | 📊 รวม | ✅ | ✅ | ✅ |
| **รายได้จากตู้** | ❌ | ❌ | ❌ | 📊 รวม | ✅ | ✅ |
| **Profit/Loss** | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ |
| **Depreciation** | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ |
| **Owner Info** | ❌ | 📊 บางส่วน | ✅ | ✅ | ✅ | ✅ |

**Legend:**
- ✅ = เห็นทั้งหมด
- 📊 = เห็นบางส่วน / สรุป
- ❌ = ไม่เห็น

---

## 📊 5. PERFORMANCE METRICS (ตัววัดประสิทธิภาพ)

### **5.1 คะแนนประสิทธิภาพ (Performance Score)**

```
┌──────────────────────────────────────────────────────────┐
│  📊 PERFORMANCE SCORE CALCULATION                        │
├──────────────────────────────────────────────────────────┤
│                                                          │
│  🎯 Overall Score: 92/100   [██████████████████░░]      │
│                             Excellent ⭐⭐⭐⭐⭐        │
│                                                          │
│  ประกอบด้วย 4 ตัวชี้วัด:                                 │
│                                                          │
│  1️⃣ Uptime (85%)                                        │
│     • ระยะเวลาที่พร้อมใช้งาน / เวลาทั้งหมด              │
│     • 360 วันพร้อมใช้ / 420 วันทั้งหมด                  │
│     • Downtime: 45 วัน + 15 วันซ่อม = 60 วัน           │
│     • Score: 85/100                                     │
│                                                          │
│  2️⃣ Condition (95%)                                     │
│     • สภาพตู้โดยรวม                                      │
│     • ความถี่การซ่อม (น้อย = ดี)                         │
│     • ความรุนแรงของความเสียหาย                          │
│     • 8 ครั้ง / 420 วัน = 0.019 ครั้ง/วัน              │
│     • Score: 95/100                                     │
│                                                          │
│  3️⃣ Utilization (88%)                                   │
│     • อัตราการใช้งาน                                     │
│     • 127 เที่ยว / 180 วันทำงาน = 0.7 เที่ยว/วัน       │
│     • Revenue per Day: ฿4,400                           │
│     • Score: 88/100                                     │
│                                                          │
│  4️⃣ Reliability (98%)                                   │
│     • ความน่าเชื่อถือ                                    │
│     • งานที่สำเร็จ / งานทั้งหมด                          │
│     • 125 สำเร็จ / 127 งาน = 98.4%                      │
│     • ล่าช้า: 2 ครั้ง                                   │
│     • Score: 98/100                                     │
│                                                          │
│  📈 Weighted Average:                                    │
│  (85×0.25) + (95×0.30) + (88×0.25) + (98×0.20) = 92    │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

### **5.2 Dashboard ประสิทธิภาพ**

```
┌──────────────────────────────────────────────────────────┐
│  📈 Container Performance Dashboard                      │
├──────────────────────────────────────────────────────────┤
│                                                          │
│  🏆 Top 10 Best Performers                              │
│  ┌────┬──────────────┬───────┬──────────┬─────────┐    │
│  │ #  │ Container    │ Score │ Trips    │ Revenue │    │
│  ├────┼──────────────┼───────┼──────────┼─────────┤    │
│  │ 1  │ TBCU2122923  │ 92    │ 127      │ 1.85M   │    │
│  │ 2  │ TBCU2055023  │ 91    │ 125      │ 1.78M   │    │
│  │ 3  │ CJCU2002715  │ 89    │ 118      │ 1.65M   │    │
│  │ 4  │ CICU4709644  │ 87    │ 115      │ 1.58M   │    │
│  │ 5  │ SZLU9095442  │ 85    │ 110      │ 1.45M   │    │
│  └────┴──────────────┴───────┴──────────┴─────────┘    │
│                                                          │
│  ⚠️ Needs Attention                                     │
│  ┌────┬──────────────┬───────┬──────────────────┐      │
│  │ #  │ Container    │ Score │ Issue            │      │
│  ├────┼──────────────┼───────┼──────────────────┤      │
│  │ 1  │ ABCD1234567  │ 52    │ ซ่อมบ่อย (15x)   │      │
│  │ 2  │ EFGH9876543  │ 58    │ Downtime สูง     │      │
│  │ 3  │ IJKL5555555  │ 62    │ ค่าซ่อมสูง       │      │
│  └────┴──────────────┴───────┴──────────────────┘      │
│                                                          │
│  📊 Fleet Health Overview                               │
│  • Excellent (90-100):  45 ตู้ (18%)                    │
│  • Good (75-89):       125 ตู้ (50%)                    │
│  • Fair (60-74):        65 ตู้ (26%)                    │
│  • Poor (<60):          15 ตู้ (6%)  ⚠️                │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

---

## 💾 6. DATABASE SCHEMA

### **6.1 Containers Table**

```sql
CREATE TABLE containers (
    -- Primary Key
    container_id INT AUTO_INCREMENT PRIMARY KEY,
    container_number VARCHAR(11) UNIQUE NOT NULL, -- TBCU2122923
    
    -- Basic Info
    size VARCHAR(10) NOT NULL,              -- 20FT, 40FT, 40HC, 45HR
    type VARCHAR(20) NOT NULL,              -- dry, reefer, open_top
    owner_code VARCHAR(4) NOT NULL,         -- TBC, MAM, etc.
    owner_name VARCHAR(100),                -- MAMMOTH, etc.
    manufacture_year INT,                   -- 2018
    tare_weight INT,                        -- 4200 kg
    max_payload INT,                        -- 26580 kg
    
    -- Status
    status VARCHAR(20) DEFAULT 'available', -- available, in_use, maintenance, damaged
    current_location VARCHAR(255),          -- ลานจอด A3
    last_inspection_date DATE,
    next_inspection_date DATE,
    csc_valid_until DATE,                   -- Container Safety Convention
    
    -- Performance Metrics
    total_trips INT DEFAULT 0,
    total_distance DECIMAL(10,2) DEFAULT 0, -- km
    total_hours INT DEFAULT 0,
    days_in_service INT DEFAULT 0,
    total_revenue DECIMAL(12,2) DEFAULT 0,
    total_maintenance_cost DECIMAL(12,2) DEFAULT 0,
    performance_score DECIMAL(5,2),         -- 0-100
    
    -- Additional Identifiers
    qr_code TEXT,                           -- QR Code data
    rfid_tag VARCHAR(50),                   -- RFID Tag ID
    barcode VARCHAR(50),                    -- Barcode
    gps_tracker_id VARCHAR(50),             -- GPS Device ID
    
    -- Timestamps
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    
    -- Indexes
    INDEX idx_container_number (container_number),
    INDEX idx_status (status),
    INDEX idx_owner (owner_code),
    INDEX idx_performance (performance_score DESC)
);
```

### **6.2 Damage Reports Table**

```sql
CREATE TABLE damage_reports (
    -- Primary Key
    report_id INT AUTO_INCREMENT PRIMARY KEY,
    
    -- Container Reference
    container_id INT NOT NULL,
    container_number VARCHAR(11) NOT NULL,
    
    -- Report Info
    reported_by_user_id INT NOT NULL,
    reported_by_name VARCHAR(100),
    reported_at TIMESTAMP NOT NULL,
    location VARCHAR(255),                  -- สถานที่พบ
    
    -- Damage Details
    severity VARCHAR(20) NOT NULL,          -- minor, medium, severe
    damage_type VARCHAR(50) NOT NULL,       -- structure, door, floor, electrical, cooling, other
    description TEXT NOT NULL,
    impact_on_usage VARCHAR(20),            -- usable, caution, not_recommended, forbidden
    
    -- Evidence
    photos JSON,                            -- Array of photo URLs
    videos JSON,                            -- Array of video URLs
    
    -- Status
    status VARCHAR(20) DEFAULT 'pending',   -- pending, reviewing, approved, rejected, repairing, completed
    reviewed_by_user_id INT,
    reviewed_at TIMESTAMP,
    
    -- Timestamps
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    
    -- Foreign Keys
    FOREIGN KEY (container_id) REFERENCES containers(container_id),
    
    -- Indexes
    INDEX idx_container (container_id),
    INDEX idx_status (status),
    INDEX idx_severity (severity),
    INDEX idx_reported_date (reported_at DESC)
);
```

### **6.3 Repair Requests Table**

```sql
CREATE TABLE repair_requests (
    -- Primary Key
    request_id INT AUTO_INCREMENT PRIMARY KEY,
    
    -- References
    damage_report_id INT NOT NULL,
    container_id INT NOT NULL,
    container_number VARCHAR(11) NOT NULL,
    
    -- Request Details
    requested_by_user_id INT NOT NULL,
    requested_at TIMESTAMP NOT NULL,
    urgency VARCHAR(20) NOT NULL,           -- urgent, high, medium, low
    
    -- Cost Estimation
    estimated_parts_cost DECIMAL(10,2),
    estimated_labor_cost DECIMAL(10,2),
    estimated_transport_cost DECIMAL(10,2),
    estimated_total_cost DECIMAL(10,2),
    estimated_days INT,
    
    -- Workshop
    recommended_workshop_id INT,
    recommended_workshop_name VARCHAR(100),
    workshop_contact VARCHAR(100),
    alternative_workshops JSON,             -- Array of {name, cost, days}
    
    -- Business Impact
    downtime_days INT,
    revenue_loss DECIMAL(10,2),
    replacement_needed BOOLEAN DEFAULT FALSE,
    
    -- Approval
    approval_status VARCHAR(20) DEFAULT 'pending', -- pending, approved, rejected, on_hold
    approver_user_id INT,
    approver_name VARCHAR(100),
    approved_at TIMESTAMP,
    approval_notes TEXT,
    approved_amount DECIMAL(10,2),
    
    -- Timestamps
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    
    -- Foreign Keys
    FOREIGN KEY (damage_report_id) REFERENCES damage_reports(report_id),
    FOREIGN KEY (container_id) REFERENCES containers(container_id),
    
    -- Indexes
    INDEX idx_container (container_id),
    INDEX idx_status (approval_status),
    INDEX idx_urgency (urgency),
    INDEX idx_cost (estimated_total_cost)
);
```

### **6.4 Maintenance Records Table**

```sql
CREATE TABLE maintenance_records (
    -- Primary Key
    maintenance_id INT AUTO_INCREMENT PRIMARY KEY,
    
    -- References
    repair_request_id INT,
    container_id INT NOT NULL,
    container_number VARCHAR(11) NOT NULL,
    
    -- Workshop Info
    workshop_id INT,
    workshop_name VARCHAR(100),
    technician_name VARCHAR(100),
    
    -- Dates
    start_date DATE NOT NULL,
    estimated_completion_date DATE,
    actual_completion_date DATE,
    
    -- Work Details
    work_description TEXT,
    parts_replaced JSON,                    -- [{part_name, quantity, cost}]
    work_performed TEXT,
    
    -- Costs
    parts_cost DECIMAL(10,2),
    labor_cost DECIMAL(10,2),
    other_costs DECIMAL(10,2),
    total_cost DECIMAL(10,2),
    
    -- Status
    status VARCHAR(20) DEFAULT 'scheduled', -- scheduled, in_progress, completed, cancelled
    completion_percentage INT DEFAULT 0,
    
    -- Quality Check
    quality_check_passed BOOLEAN,
    quality_notes TEXT,
    warranty_months INT,
    warranty_until DATE,
    
    -- Evidence
    before_photos JSON,
    after_photos JSON,
    invoice_url VARCHAR(255),
    
    -- Timestamps
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    
    -- Foreign Keys
    FOREIGN KEY (repair_request_id) REFERENCES repair_requests(request_id),
    FOREIGN KEY (container_id) REFERENCES containers(container_id),
    
    -- Indexes
    INDEX idx_container (container_id),
    INDEX idx_status (status),
    INDEX idx_dates (start_date, actual_completion_date)
);
```

---

## 🎨 7. UI MOCKUP

### **7.1 หน้าค้นหาตู้**

```
┌──────────────────────────────────────────────────────────────┐
│  🔍 ค้นหาตู้คอนเทนเนอร์                       [🔒 Manager]  │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  ┌────────────────────────────────────────────────────────┐ │
│  │  Container Number:                                     │ │
│  │  ┌──────────────────────────┐                         │ │
│  │  │ TBCU2122923              │ [🔍 ค้นหา]              │ │
│  │  └──────────────────────────┘                         │ │
│  │                                                        │ │
│  │  หรือใช้:                                              │ │
│  │  [📱 สแกน QR Code] [📡 อ่าน RFID] [📊 สแกน Barcode]  │ │
│  └────────────────────────────────────────────────────────┘ │
│                                                              │
│  📊 Quick Stats:                                            │
│  • Total Fleet: 250 ตู้                                     │
│  • Available: 186 ตู้ (74%)                                 │
│  • In Use: 42 ตู้ (17%)                                     │
│  • Maintenance: 8 ตู้ (3%)                                  │
│  • Damaged: 14 ตู้ (6%)                                     │
│                                                              │
│  🔥 Recent Searches:                                        │
│  • TBCU2122923 - 2 นาทีที่แล้ว                             │
│  • CJCU2002715 - 15 นาทีที่แล้ว                            │
│  • SZLU9095442 - 1 ชั่วโมงที่แล้ว                          │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

### **7.2 หน้ารายงานความเสียหาย (Mobile-Friendly)**

```
┌──────────────────────────────────────┐
│  ⚠️ รายงานความเสียหาย                │
├──────────────────────────────────────┤
│                                      │
│  📱 สแกน QR Code บนตู้               │
│  ┌────────────────────────────────┐ │
│  │                                │ │
│  │     [กล้อง เปิดสแกน]           │ │
│  │                                │ │
│  └────────────────────────────────┘ │
│                                      │
│  หรือพิมพ์เลขตู้:                   │
│  ┌────────────────────────────────┐ │
│  │ TBCU2122923                    │ │
│  └────────────────────────────────┘ │
│                                      │
│  📍 สถานที่พบ:                      │
│  ┌────────────────────────────────┐ │
│  │ ลานจอด A3                      │ │
│  └────────────────────────────────┘ │
│                                      │
│  ⚠️ ระดับความรุนแรง:                │
│  [ ] 🟢 Minor (เล็กน้อย)            │
│  [✓] 🟡 Medium (ปานกลาง)            │
│  [ ] 🔴 Severe (รุนแรง)             │
│                                      │
│  🔧 ประเภทความเสียหาย:              │
│  [ ] โครงสร้าง                      │
│  [✓] ประตู                          │
│  [ ] พื้น                           │
│  [ ] ระบบไฟฟ้า                      │
│  [ ] ระบบทำความเย็น                 │
│  [ ] อื่นๆ                          │
│                                      │
│  📝 รายละเอียด:                     │
│  ┌────────────────────────────────┐ │
│  │ ประตูปิดไม่สนิท                 │ │
│  │ บานพับด้านขวาหลวม              │ │
│  │                                │ │
│  └────────────────────────────────┘ │
│                                      │
│  📷 รูปภาพ: (0/10)                  │
│  [📸 ถ่ายรูป] [🖼️ เลือกจากอัลบั้ม]│
│                                      │
│  ผลกระทบ:                           │
│  [ ] ใช้งานได้ปกติ                  │
│  [✓] ใช้ได้ แต่ต้องระวัง            │
│  [ ] ไม่ควรใช้                      │
│  [ ] ห้ามใช้ (อันตราย)              │
│                                      │
│  [ส่งรายงาน]                        │
│                                      │
└──────────────────────────────────────┘
```

---

จบเอกสาร ✅

**หน้าถัดไป: การพัฒนาระบบจริง (Implementation)**
