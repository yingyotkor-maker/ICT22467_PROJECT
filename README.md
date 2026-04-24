# ICT22467_PROJECT
This is my ICT22467_PROJECT.
# 💊 Pharmacy Temperature Control System

ระบบควบคุมอุณหภูมิสำหรับการจัดเก็บยาในร้านขายยา (Pharmacy)  
พัฒนาขึ้นเพื่อช่วยควบคุมอุณหภูมิในการเก็บรักษายาให้เหมาะสม  
รองรับการจัดการข้อมูลยา การควบคุมอุณหภูมิตู้ยา และการตรวจสอบจำนวนยาในคลัง

พัฒนาด้วย SQL Server + Database Management + Temperature Control System + Inventory Management

---

# 📌 ภาพรวมระบบ (System Overview)

โปรเจกต์นี้ถูกออกแบบมาเพื่อใช้สำหรับระบบควบคุมอุณหภูมิภายในร้านขายยา (Pharmacy)  
โดยเฉพาะในพื้นที่ห่างไกล เช่น ร้านขายยาขนาดเล็กในชนบท หรือพื้นที่บนดอย  
ซึ่งมีปัญหาเรื่องการขนส่งยาและการจัดส่งที่ไม่สะดวก

ระบบนี้ช่วยให้สามารถกำหนดอุณหภูมิที่เหมาะสมสำหรับการจัดเก็บยาแต่ละประเภท  
เพื่อรักษาคุณภาพและประสิทธิภาพของยาให้ดีที่สุด ลดความเสียหายจากการเก็บรักษาที่ไม่เหมาะสม  
รวมถึงช่วยลดจำนวนรอบในการจัดส่งยา และสามารถบริหารคลังยาได้อย่างมีประสิทธิภาพ

เหมาะสำหรับใช้เป็นโปรเจกต์ฐานข้อมูล (Database Project) หรือ Final Project ระดับมหาวิทยาลัย

---

# 🛠 เทคโนโลยีและเครื่องมือที่ใช้ (Tech Stack & Tools)

| ส่วนงาน | เทคโนโลยี |
|---|---|
| Database System | Microsoft SQL Server |
| Database Design | ER Diagram + Data Dictionary |
| SQL Development | CREATE TABLE + VIEW + Query |
| Interface Preview | SQL View / Inventory Display |
| Inventory Control | Medicine Stock Management |
| Temperature System | Cabinet Temperature Control |

---

# 🎨 แนวคิดของระบบ (System Concept)

- ควบคุมอุณหภูมิในการเก็บรักษายา
- ลดการเสื่อมสภาพของยา
- รองรับร้านขายยาในพื้นที่ห่างไกล
- ลดจำนวนรอบการจัดส่งยา
- จัดการข้อมูลยาและคลังสินค้าได้อย่างมีประสิทธิภาพ

---

# 👥 ขอบเขตการทำงานของระบบ (System Scope)

## 1. จัดการข้อมูลเกี่ยวกับยา (Medicine Management)

### ระบบสามารถ

- เก็บข้อมูลชื่อยา
- ประเภทยา
- จำนวนยา
- วันที่รับเข้า
- วันหมดอายุ
- อุณหภูมิที่เหมาะสมในการเก็บรักษา

เพื่อให้สามารถตรวจสอบได้ว่าคลังยามีอะไรบ้าง และเหลือจำนวนเท่าใด

---

## 2. จัดการการเก็บรักษายาในตู้ควบคุมอุณหภูมิ (Cabinet Temperature)

### ระบบสามารถ

- กำหนดอุณหภูมิของตู้เก็บยา
- ตรวจสอบอุณหภูมิที่เหมาะสมของยาแต่ละชนิด
- เชื่อมโยงข้อมูลยาเข้ากับตู้ควบคุมอุณหภูมิ

เพื่อให้สามารถเก็บรักษายาได้อย่างเหมาะสมและปลอดภัย

---

## 3. จัดการจำนวนยาในคลัง (Inventory Management)

### ระบบสามารถ

- เพิ่มจำนวนยาเมื่อรับสินค้าเข้า
- ลดจำนวนยาเมื่อมีการขาย
- ตรวจสอบจำนวนคงเหลือ
- แสดงรายการยาในคลังผ่านระบบ SQL View

เพื่อช่วยให้ร้านขายยาสามารถบริหารคลังสินค้าได้ง่ายขึ้น

---

# 🗂 ตารางหลักภายในระบบ (Database Tables)

ระบบนี้ประกอบด้วย 6 ตารางหลัก ได้แก่

## 1. Medicine

ใช้สำหรับเก็บข้อมูลยา

### Fields

- MDC_ID
- MDC_Name
- TEMP_REQ
- MDC_Date
- MDC_Exd
- MDC_Total

---

## 2. Cabinet_temp

ใช้สำหรับเก็บข้อมูลตู้ควบคุมอุณหภูมิ

### Fields

- C_ID
- TEMP_cap
- MDC_ID

---

## 3. Company

ใช้สำหรับเก็บข้อมูลบริษัทผู้จัดส่งยา

### Fields

- CPN_ID
- CPN_Name
- CPN_No
- CPN_Address
- MDC_ID

---

## 4. Pharmacy

ใช้สำหรับเก็บข้อมูลเภสัชกร

### Fields

- PMC_ID
- PMC_Name
- PMC_NO

---

## 5. Medicine_order

ใช้สำหรับเก็บข้อมูลการสั่งซื้อยา

### Fields

- Order_ID
- MDC_ID
- M_qty

---

## 6. Customer

ใช้สำหรับเก็บข้อมูลลูกค้า

### Fields

- Cus_Name
- Cus_NO

---

# 🔐 บัญชีสำหรับทดสอบระบบ (Test Credentials)

## Admin

```text
Username: admin
Password: admin123

Staff
Username: pharmacy
Password: pharmacy123'''

---

###⚙️ ขั้นตอนการติดตั้งระบบ (Installation Guide)

แนะนำให้ใช้งานผ่าน Microsoft SQL Server

โปรแกรมที่ต้องมี (Prerequisites)
- Microsoft SQL Server
- SQL Server Management Studio (SSMS)
- Visual Studio Code (สำหรับจัดการไฟล์ SQL)
- Database Script ของระบบ

---

## Step 1 : สร้างฐานข้อมูล
CREATE DATABASE PharmacyTempControl;
GO

----

