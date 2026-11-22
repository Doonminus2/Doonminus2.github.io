# Website Project: Round Table Landing Page

> Agent: อ่านไฟล์นี้เพื่อเข้าใจว่าผู้เรียนกำลังทำอะไร แล้วอ่าน `CLAUDE.md` ด้วย
> กฎใน `CLAUDE.md` (ติวเตอร์, ห้ามเขียนโค้ดให้) ยังใช้เต็มที่ ไฟล์นี้บอกแค่เป้าหมายของโปรเจกต์

## เป้าหมาย

ทำ **landing page หน้าเดียว** ด้วย HTML + **Tailwind CSS v4** (โหลดผ่าน CDN ใน `src/index.html`)
เพื่อฝึก Tailwind โดยเลียนแบบ layout และสไตล์ของเว็บอ้างอิง แล้วเปลี่ยน content เป็นธีมอัศวินโต๊ะกลม (King Arthur)

- เว็บอ้างอิง (layout/สไตล์): https://chitsanuapts-superb-site.webflow.io/
- ที่มาของ content: `day1/story.html` (เรื่อง King Arthur และสมาชิกโต๊ะกลม)
- ไฟล์ที่ทำงาน: `src/index.html`

## แนวทาง "ผสมของเก่ากับของใหม่"

| ส่วน | เอามาจาก |
|---|---|
| โครง layout (navbar, hero, marquee, การ์ด, gallery, footer) | เว็บ Webflow |
| ฟอนต์หัวข้อ/เนื้อหา | Webflow: Anton, IBM Plex Sans |
| ฟอนต์ตกแต่ง | day1: UnifrakturMaguntia |
| สี (กระดาษเก่า/แดง/ทอง/น้ำเงิน) | day1: `--paper #F2E6C2`, `--red #8B1E1E`, `--gold #B8860B`, `--blue #1F3A5F`, `--ink #2B2118` |
| เนื้อหา | day1: King Arthur, Lancelot, Gawain, Galahad, Historicity |

## Assets (เตรียมไว้แล้วใน `src/assets/`)

- `icons/` — smile-face, shape-06/09/19 (.svg), arrow-black.svg, favicon.png
- `images/hero/` — hero-1..3.jpg
- `images/team/` — team-04..07.jpg (ใช้เป็นการ์ดอัศวิน)
- `images/project/` — project-1,4,5,6,7,8.jpg, featured.jpg (ใช้เป็น gallery)
- `images/arthur/` — cover.png, king.png, lancelot.png (จาก day1)

รูปใน hero/team/project เป็นรูป template ใช้เป็น placeholder ถ้าจะ deploy จริงต้องเปลี่ยน
`king.png` หนัก ~4.6 MB ควรย่อก่อนใช้งานจริง

## โครงหน้าเว็บ (ลำดับที่จะทำ)

1. **Navbar** — โลโก้ + ลิงก์ (Home / About / Contact)
2. **Hero** — หัวข้อใหญ่, ข้อความสั้น, ปุ่ม CTA, รูป King Arthur
3. **Marquee** — แถบข้อความวิ่ง (เช่น "Round Table")
4. **Members** — การ์ด 3 ใบ: Sir Lancelot, Sir Gawain, Sir Galahad
5. **Gallery / Featured** — grid รูป
6. **Historicity / About** — ข้อความจาก day1
7. **Footer + Contact form** — ชื่อ, อีเมล, ข้อความ, ปุ่มส่ง

## Theme (Tailwind v4)

กำหนดใน `<style type="text/tailwindcss">` ด้วย `@theme` เช่น `--color-paper`, `--color-red`, `--font-display`
ใช้เป็น class ได้ เช่น `bg-paper text-ink font-display`

## สถานะ

- [x] เตรียม assets
- [ ] ตั้งค่า theme + Google Fonts
- [ ] Navbar
- [ ] Hero
- [ ] Marquee
- [ ] Members
- [ ] Gallery
- [ ] About
- [ ] Footer + form
- [ ] Responsive (มือถือ → จอใหญ่)

## วิธีที่ agent ควรช่วย

- ผู้เรียนเขียนโค้ดเอง agent ให้คำใบ้ อธิบายแนวคิด และตัวอย่างเล็กที่ไม่ใช่คำตอบตรงๆ
- เมื่อผู้เรียนส่งโค้ดมา ให้รีวิวตามขั้นตอนใน `CLAUDE.md`
- ถ้าถามเรื่อง Tailwind ให้ชี้ utility class ที่เกี่ยวข้องและเหตุผล เช่น `flex`, `grid`, `gap-*`, `md:` (responsive)
- ห้ามแก้ไฟล์ใน `src/` เว้นแต่เป็นการเตรียม asset ตามที่ผู้เรียนขอ
