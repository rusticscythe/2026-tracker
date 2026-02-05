# 🎯 Performance Tracking Dashboard 2026

ระบบติดตามผลการดำเนินงานตามกลยุทธ์ 2569 แบบ Interactive Web Dashboard

![Dashboard Preview](https://img.shields.io/badge/Status-Active-success)
![Version](https://img.shields.io/badge/Version-1.0-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## ✨ Features

- 📊 **Real-time Dashboard** - Summary cards แสดงความคืบหน้าทันที
- 🎯 **3 Strategic Themes** - Theme 1 (Core Business), Theme 2 (Digital), Theme 3 (Future)
- 📈 **Quarterly Tracking** - ติดตาม Q1-Q4 แยกแต่ละ KPI
- 🏢 **Department Filter** - กรองตามฝ่ายงาน
- ✅ **Action Items** - Checklist management
- 💾 **Auto-save** - บันทึกอัตโนมัติทุก 30 วินาที
- 📥 **Export JSON** - ส่งออกข้อมูล backup

## 🚀 Deploy บน GitHub Pages

### วิธีที่ 1: Fork และ Deploy (แนะนำ)

1. คลิก **Fork** repository นี้
2. ไปที่ **Settings** → **Pages**
3. ใน Source เลือก:
   - Branch: `main`
   - Folder: `/` (root)
4. คลิก **Save**
5. รอ 1-2 นาที
6. เข้าใช้งานที่: `https://[username].github.io/[repo-name]/`

### วิธีที่ 2: Create New Repository

```bash
# 1. สร้าง repository ใหม่บน GitHub (เช่น performance-dashboard)

# 2. Clone และเพิ่มไฟล์
git clone https://github.com/[username]/performance-dashboard.git
cd performance-dashboard

# 3. คัดลอกไฟล์ index.html และ README.md เข้าไป

# 4. Push ไป GitHub
git add .
git commit -m "Initial commit - Performance Dashboard"
git push origin main

# 5. Enable GitHub Pages ตามวิธีที่ 1 ข้อ 2-6
```

## 💻 ใช้งาน Local

```bash
# เปิดไฟล์ index.html ด้วย browser โดยตรง
# หรือใช้ local server:

# Python
python -m http.server 8000

# Node.js
npx http-server

# เข้าใช้งานที่ http://localhost:8000
```

## 📋 วิธีใช้งาน

### 1️⃣ เลือก Tab
- **Overview**: เป้าหมายรายได้รวมและกำไร
- **Theme 1-3**: KPIs แยกตาม Theme
- **ช่องทาง**: รายได้แยกตาม Sales Channel

### 2️⃣ กรองตามฝ่าย
คลิกปุ่มกรองเพื่อดู KPIs ที่เกี่ยวข้อง:
- ขาย-โครงการ
- ขาย-ค้าส่ง
- ขาย-ปลีก
- Merchandising
- โลจิสติกส์
- IT/Digital

### 3️⃣ กรอกข้อมูล
- ใส่ **Target** และ **Actual** แต่ละไตรมาส
- Progress % คำนวณอัตโนมัติ
- สถานะ:
  - 🟢 On Track (≥90%)
  - 🟡 At Risk (70-89%)
  - 🔴 Behind (<70%)
  - 🔵 Completed (100%)
  - ⚪ Not Started (0%)

### 4️⃣ จัดการ Action Items
- ติ๊ก ✓ เมื่อทำเสร็จ
- **+ เพิ่ม Action** สำหรับรายการใหม่

### 5️⃣ บันทึกและ Export
- **💾 Save**: บันทึกข้อมูล
- **📥 Export**: ดาวน์โหลด JSON file

## 🎯 KPIs ที่ติดตาม

### Theme 1: Core Business Strength
| KPI | เป้าหมาย | ฝ่ายรับผิดชอบ |
|-----|---------|--------------|
| Drop Ship | ครอบคลุม 50% อีสาน, ≥5MB | ขาย-ค้าส่ง, โลจิสติกส์ |
| งบภาครัฐ | สนับสนุน ≥50% | ขาย-โครงการ |
| สินค้ากึ่งสำเร็จรูป | 3 ชิ้น (GP≥15%) | Merchandising |
| Hero Product Online | 100K/เดือน | ขาย-ปลีก |
| ปรับโชว์รูม | 50% ในปี 2569 | Merchandising |

### Theme 2: Digital & Data Foundation
| KPI | เป้าหมาย | ฝ่ายรับผิดชอบ |
|-----|---------|--------------|
| ฐานข้อมูลลูกค้า | ระบบพร้อมใช้งาน | IT/Digital |
| AI Readiness | วัดสถานะได้ | IT/Digital |
| ลดเอกสาร Offline | ลด 30% | ทุกฝ่าย |
| PoC Systems | 2 ระบบ | IT/Digital |

### Theme 3: Future Blueprint
| KPI | เป้าหมาย | ฝ่ายรับผิดชอบ |
|-----|---------|--------------|
| M&A/OEM | 6 candidates, 2 pilots | ผู้บริหาร |
| Process Improvement | แผนกละ 1 case | ทุกฝ่าย |
| Environmental Impact | Template พร้อม | Merchandising |

### รายได้แยกช่องทาง
- **Wholesale**: 487 MB (Baseline 2568)
- **Project**: 491 MB (Baseline 2568, -25% YoY)
- **Retail**: 109 MB (Baseline 2568, -20% YoY)
- **SCG Home**: 107 MB (Baseline 2568, -14% YoY)

## 🔧 Customization

### เพิ่ม KPI ใหม่

แก้ไขใน `index.html`:

```html
<div class="kpi-item" data-department="sales-project">
    <div class="kpi-header">
        <div class="kpi-title">ชื่อ KPI</div>
        <div class="status-badge status-not-started">Not Started</div>
    </div>
    <p style="color: #666; margin-bottom: 15px;">
        <strong>เป้า:</strong> เป้าหมายของคุณ<br>
        <strong>ฝ่าย:</strong> ฝ่ายรับผิดชอบ
    </p>
    <div class="quarter-grid">
        <div class="quarter-card">
            <h4>Q1</h4>
            <input type="number" class="quarter-input" placeholder="Value">
        </div>
        <!-- Q2-Q4... -->
    </div>
    <textarea class="notes-textarea" placeholder="หมายเหตุ..."></textarea>
</div>
```

### เปลี่ยนสี Theme

```css
/* Primary gradient */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Status colors */
.status-on-track { background: #d4edda; color: #155724; }
.status-at-risk { background: #fff3cd; color: #856404; }
.status-behind { background: #f8d7da; color: #721c24; }
```

## 💡 Tech Stack

- HTML5
- CSS3 (Flexbox, Grid, Animations)
- Vanilla JavaScript
- LocalStorage API
- Responsive Design

## 📱 Mobile Responsive

✅ ทำงานได้บน mobile และ tablet  
✅ Touch-friendly interface  
✅ Adaptive layout

## 🔒 Privacy & Security

- ข้อมูลเก็บใน **browser localStorage** (client-side)
- **ไม่มีการส่งข้อมูลไปยัง server**
- แต่ละคนเห็นเฉพาะข้อมูลของตัวเอง
- Export เป็น JSON สำหรับ backup

## 📝 To-Do / Roadmap

- [ ] เพิ่ม Charts/Graphs visualization
- [ ] Multi-user collaboration (Firebase/Supabase)
- [ ] PDF Export
- [ ] Email notifications
- [ ] Dark mode
- [ ] Import from Excel

## 🤝 Contributing

พัฒนาต่อยอดได้เลย:

1. Fork repository
2. Create feature branch: `git checkout -b feature/NewFeature`
3. Commit: `git commit -m 'Add NewFeature'`
4. Push: `git push origin feature/NewFeature`
5. Open Pull Request

## 📄 License

MIT License - ใช้งานได้เลยครับ

## 📞 Support

ติดปัญหา?
- เปิด Issue บน GitHub
- หรือติดต่อทีม IT

---

**Created by**: Bo's Strategic Planning Team  
**Last Updated**: February 2026  
**Version**: 1.0  

⭐ ถ้าชอบให้ Star repo นะครับ!