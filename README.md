
# Rubber Receipt (GitHub Pages)

หน้าใบจ่ายเงินค่าน้ำยาง (HTML) สำหรับเปิดจาก Glide/Google Sheets พร้อมพิมพ์เป็น PDF

## โครงสร้าง
- `receipt.html` — เทมเพลตหลัก (พร้อมชื่อสหกรณ์เริ่มต้น: สหกรณ์กองทุนสวนยางบ้านหนองหว้า จำกัด)
- `README.md` — คู่มือนี้
- `.nojekyll` — ให้ GitHub Pages เสิร์ฟไฟล์ตรง ๆ

## วิธีเผยแพร่ด้วย GitHub Pages
1) สร้าง Repository ใหม่ใน GitHub (Public)
2) อัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้
3) ไปที่ **Settings → Pages** เลือก **Source = Deploy from a branch**, Branch = `main` และ Folder = `/root`
4) ระบบจะให้ URL รูปแบบ: `https://<username>.github.io/<repo>/receipt.html`

## วิธีเรียกใช้งานจาก Glide/Sheets
ให้สร้าง Template URL แล้วส่งพารามิเตอร์ เช่น:

```
https://<username>.github.io/<repo>/receipt.html
?pay_date=27/10/2025
&sale_date=27/10/2025
&slip_no=000123
&member_name=นาย%20เพียร%20ยงค์หนู
&member_id=191
&wet_weight=34.7
&drc=35
&price_perkg=50
&employer=100
&employee=0
&deduct=0
&payer_name=นาง%20สมใจ
```

## หมายเหตุการพิมพ์
- เลือกขนาด A4, Margin = Default/Normal, Scale = 100%
- หากต้องการแก้ layout ให้แก้ `padding` ภายใน `.sheet`
