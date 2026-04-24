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

###text
Username: admin
Password: admin123

Staff
Username: pharmacy
Password: pharmacy123

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

---

##Step 2 : เลือกใช้งานฐานข้อมูล
USE PharmacyTempControl;
GO

---

Step 3 : CREATE TABLE
Medicine
CREATE TABLE Medicine (
    MDC_ID VARCHAR(5) PRIMARY KEY,
    MDC_Name VARCHAR(50) NOT NULL UNIQUE,
    TEMP_REQ DECIMAL(4,2) NOT NULL,
    MDC_Date DATE NOT NULL,
    MDC_Exd DATE NOT NULL,
    MDC_Total INT NOT NULL
);
Cabinet_temp
CREATE TABLE Cabinet_temp (
    C_ID INT PRIMARY KEY,
    TEMP_cap DECIMAL(4,2) NOT NULL,
    MDC_ID VARCHAR(5) NOT NULL UNIQUE,
    FOREIGN KEY (MDC_ID) REFERENCES Medicine(MDC_ID)
);
Company
CREATE TABLE Company (
    CPN_ID VARCHAR(10) PRIMARY KEY,
    CPN_Name VARCHAR(100) NOT NULL UNIQUE,
    CPN_No VARCHAR(100) NOT NULL UNIQUE,
    CPN_Address VARCHAR(200) NOT NULL,
    MDC_ID VARCHAR(5) NOT NULL UNIQUE,
    MDC_Date DATE NOT NULL,
    MDC_Total INT NOT NULL,
    FOREIGN KEY (MDC_ID) REFERENCES Medicine(MDC_ID)
);
Pharmacy
CREATE TABLE Pharmacy (
    PMC_ID VARCHAR(10) PRIMARY KEY,
    PMC_Name VARCHAR(50) NOT NULL,
    PMC_NO VARCHAR(15) NOT NULL UNIQUE
);
Medicine_order
CREATE TABLE Medicine_order (
    Order_ID VARCHAR(10) NOT NULL UNIQUE,
    MDC_ID VARCHAR(5) NOT NULL UNIQUE,
    M_qty INT NOT NULL,
    FOREIGN KEY (MDC_ID) REFERENCES Medicine(MDC_ID)
);
Customer
CREATE TABLE Customer (
    Cus_Name VARCHAR(50) NOT NULL,
    Cus_NO VARCHAR(15) NOT NULL UNIQUE
);

---

Step 4 : SQL VIEW
View แสดงยาในคลัง
CREATE VIEW Medicine_Inventory AS
SELECT
    MDC_ID,
    MDC_Name,
    MDC_Total,
    TEMP_REQ,
    MDC_Date,
    MDC_Exd
FROM Medicine;
View แสดงข้อมูลตู้ควบคุมอุณหภูมิ
CREATE VIEW Cabinet_Status AS
SELECT
    C.C_ID,
    C.TEMP_cap,
    M.MDC_Name,
    M.TEMP_REQ
FROM Cabinet_temp C
INNER JOIN Medicine M
ON C.MDC_ID = M.MDC_ID;
View แสดงบริษัทผู้จัดส่งยา
CREATE VIEW Company_Details AS
SELECT
    CPN_ID,
    CPN_Name,
    CPN_No,
    CPN_Address,
    MDC_ID
FROM Company;
View แสดงรายการสั่งซื้อยา
CREATE VIEW Medicine_Order_Details AS
SELECT
    O.Order_ID,
    M.MDC_Name,
    O.M_qty
FROM Medicine_order O
INNER JOIN Medicine M
ON O.MDC_ID = M.MDC_ID;

---

Step 5 : INSERT SAMPLE DATA
Medicine
INSERT INTO Medicine
VALUES
('M001','Paracetamol',25.00,'2026-01-10','2027-01-10',100),
('M002','Amoxicillin',18.00,'2026-01-12','2027-02-15',80),
('M003','Insulin',4.00,'2026-01-15','2026-12-30',50);
Cabinet_temp
INSERT INTO Cabinet_temp
VALUES
(1,25.00,'M001'),
(2,18.00,'M002'),
(3,4.00,'M003');
Company
INSERT INTO Company
VALUES
('CP001','Bangkok Pharma','0812345678','Bangkok','M001','2026-01-10',100),
('CP002','Medical Supply Co.','0898765432','Chiang Mai','M002','2026-01-12',80);
Pharmacy
INSERT INTO Pharmacy
VALUES
('P001','Somchai','0891111111'),
('P002','Suda','0892222222');
Medicine_order
INSERT INTO Medicine_order
VALUES
('ORD001','M001',20),
('ORD002','M002',15);
Customer
INSERT INTO Customer
VALUES
('Anan','0811111111'),
('Nida','0822222222');

---

Step 6 : ตรวจสอบผลลัพธ์
SELECT * FROM Medicine_Inventory;
SELECT * FROM Cabinet_Status;
SELECT * FROM Company_Details;
SELECT * FROM Medicine_Order_Details;

---

หมายเหตุเพิ่มเติม
รองรับการขยายระบบเป็น Smart Medicine Cabinet
สามารถต่อยอดเชื่อมต่อ IoT และ Sensor ได้
รองรับการพัฒนาเป็นระบบควบคุมอุณหภูมิแบบ Real-time

---
