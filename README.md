# Sample Hotel 2022 | Data Analytics Portfolio

โปรเจกต์วิเคราะห์เชิงสำรวจจากรีวิว Amari Phuket จำนวน 1,000 รายการ ครอบคลุมการตรวจคุณภาพข้อมูล การทำความสะอาด การวิเคราะห์คะแนนและแนวโน้มตามวันที่เขียนรีวิว และการค้นประเด็นในรีวิวคะแนนต่ำ

**ชุดข้อมูลต้นฉบับและ CSV ที่ทำความสะอาดแล้วไม่เผยแพร่ด้วยเหตุผลด้านความเป็นส่วนตัวของผู้รีวิว** ฉบับนี้เผยแพร่ Notebook เอกสาร และกราฟที่สรุปผลในระดับกลุ่ม

## ดูผลงาน

- [Project Summary](docs/project_summary.md) สรุปโจทย์ วิธีทำ และผลสำคัญ
- [Insights](docs/insights.md) อธิบายหลักฐาน ข้อเสนอแนะ และข้อจำกัด
- [กราฟ EDA ทั้ง 7 รูป](outputs/eda/) ดูได้ทันที
- [Data Dictionary](docs/data_dictionary.md) อธิบายคอลัมน์ต้นทางและตัวแปรที่สร้างเพิ่ม

## รันด้วยข้อมูลที่ได้รับอนุญาต

1. เตรียม CSV ที่ได้รับอนุญาตให้ใช้และมีคอลัมน์ต้นทางครบ 13 คอลัมน์ตาม [Data Dictionary](docs/data_dictionary.md) สร้างโฟลเดอร์ `data/raw/` ในสำเนา Portfolio แล้ววางไฟล์ชื่อ `samplehotel - Sheet1.csv` ลงในโฟลเดอร์นั้น
2. ใช้ Python 3.10 ขึ้นไป เปิดเทอร์มินัลที่โฟลเดอร์ Portfolio และรันคำสั่งด้านล่าง

```powershell
python -m pip install pandas matplotlib notebook
python -m notebook
```

3. เปิด Notebook ทีละเล่มตามลำดับ แล้วเลือก **Restart Kernel and Run All Cells**

| ลำดับ | Notebook | สิ่งที่ทำ |
|---|---|---|
| 01 | [Data Understanding](notebooks/01_data_understanding.ipynb) | ตรวจโครงสร้าง ค่าว่าง แถวซ้ำ วันที่ และคุณภาพข้อความ |
| 02 | [Data Cleaning](notebooks/02_data_cleaning.ipynb) | ตรวจคะแนนและวันที่ แล้วเขียนผล Cleaning ใน `data/processed/` |
| 03 | [EDA](notebooks/03_eda.ipynb) | สร้างตารางและกราฟใน `outputs/eda/` |

หากใช้ข้อมูลคนละชุดกับงานเดิม ให้ทดลองในสำเนาแยก เพราะตัวเลขอาจต่างจากที่รายงาน และ Notebook 03 จะเขียนกราฟทับในสำเนาที่ใช้รัน เก็บโฟลเดอร์ `data/` ไว้เฉพาะในเครื่อง และล้าง Notebook outputs ก่อนแชร์สำเนาที่ผ่านการรันด้วยข้อมูลของคุณ
