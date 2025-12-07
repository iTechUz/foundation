## HTML va JavaScript orqali sahifa rangini o'zgartirish

### Masala Berilishi (Problem Statement)
**Masala**: 
- Siz veb-sahifa yaratishingiz kerak, unda bitta tugma bo'lsin.
- Tugmani bosganingizda, sahifaning fon rangi tasodifiy ravishda o'zgarsin. Masalan, qizil, yashil, ko'k yoki boshqa ranglarga aylansin.
- Bu loyiha orqali siz HTML (sahifani tuzish uchun) va JavaScript (harakat qo'shish uchun) tillarini birlashtirib, interaktiv (o'zaro ta'sirli) sahifa yaratishni o'rganasiz.

### Nazariy Bilimlar (Theoretical Knowledge)
**HTML nima?**
- HTML (HyperText Markup Language) - bu veb-sahifalarni yaratish uchun ishlatiladigan til. U sahifaning tuzilishini belgilaydi, masalan, matn, rasmlar yoki tugmalar. HTML teglar (masalan, `<button>`) orqali ishlaydi. Bu "uy qurish"ga o'xshaydi: HTML devorlarni quradi.

**JavaScript nima?**
- JavaScript - bu sahifaga "hayot" beradigan til. U hodisalarga (events) javob beradi, masalan, tugma bosilishiga. JavaScript orqali siz hisob-kitob qilishingiz, tasodifiy sonlar yaratishingiz va sahifani o'zgartirishingiz mumkin. Bu "uyga elektr" qo'shishga o'xshaydi: sahifa harakatlanadi va o'zgaradi.

**Funktsiya (Function) nima?**
- Funktsiya - bu kodning bir bo'lagi, uni alohida chaqirib ishlatish mumkin. Masalan, "changeColor()" funktsiyasi tugma bosilganda ishga tushadi. Funktsiyalar kodni tartibli saqlaydi va qayta ishlatishga yordam beradi.

**Massiv (Array) nima?**
- Massiv - bu ro'yxat, unda bir nechta qiymat saqlanadi. Masalan, colors = ["red", "green", "blue"] - bu ranglar ro'yxati. Siz massivdan tasodifiy element tanlashingiz mumkin.

**Tasodifiy son (Random) nima?**
- Kompyuter tasodifiy son yaratishi mumkin, masalan, Math.random() orqali. Bu o'yinlar yoki tasodifiy o'zgarishlar uchun ishlatiladi. Math.floor() sonni butun songa aylantiradi.

**DOM (Document Object Model) nima?**
- DOM - bu sahifani JavaScript orqali boshqarish usuli. Masalan, document.body.style.backgroundColor orqali sahifaning fon rangini o'zgartirishingiz mumkin. Bu sahifani "jonlantirish"ga yordam beradi.

**Hodisa (Event) nima?**
- Hodisa - bu foydalanuvchi harakati, masalan, tugma bosilishi (onclick). JavaScript hodisaga javob berib, funktsiyani ishga tushiradi.

### Qanday Qilib Qilamiz? Qadam-ba-Qadam Tushuntirish (Step-by-Step Guide)
**Fayl yaratish:**
- Yangi HTML fayl yarating (masalan, index.html). Bu fayl sahifani ochadi.
HTML qismini yozish:
`<button>` tegini qo'shing: `<button onclick="changeColor()">Rangni o'zgartir</button>`
- **Tushuntirish:** : Bu tugma yaratadi. onclick - tugma bosilganda changeColor() funktsiyasini chaqiradi. "Rangni o'zgartir" - tugmadagi matn.

**JavaScript qismini yozish:**
- `<script>` tegini qo'shing: Sahifaning pastida yozing.
- **Tushuntirish:**: JavaScript kodini `<script>` ichida yozamiz, chunki u sahifani yuklaganda ishlaydi.

**Funktsiyani yaratish:**
- `function changeColor() { ... }`
- **Tushuntirish:**
Bu funktsiya tugma bosilganda ishlaydi. Ichida rangni o'zgartiramiz.

**Ranglar massivini yaratish:**
- `const colors = ["red", "green", "blue", "yellow", "purple", "orange"];`
Tushuntirish: Bu ranglar ro'yxati. const - qiymatni o'zgarmas qiladi. Rang nomlari inglizcha, chunki brauzer ularni tushunadi.

**Tasodifiy rang tanlash:**
- `const random = colors[Math.floor(Math.random() * colors.length)];`
- **Tushuntirish:** `Math.random()` - 0 dan 1 gacha tasodifiy son beradi (masalan, 0.7).
- `Math.random() * colors.length` - ro'yxat uzunligi (6) bilan ko'paytiradi (masalan, 4.2).
- `Math.floor()` - butun songa aylantiradi (masalan, 4).
- `colors[4]` - ro'yxatdan 4-indeksdagi rangni oladi (masalan, "purple").


**Fon rangini o'zgartirish:**
- document.body.style.backgroundColor = random;
- **Tushuntirish:** document.body - butun sahifani bildiradi. style.`backgroundColor` - fon rangini o'zgartiradi. random - tanlangan rang.

**Sinov qilish:**
- Faylni brauzerda oching. Tugmani bosing - fon o'zgarishi kerak. Agar ishlamasa, xatolarni tekshiring (masalan, qavslar yopilmaganmi?).

To'liq Kod: - [Bu yerda](./index.html)


### Qo'shimcha Maslahatlar
**Kodni o'zgartiring:** Yangi ranglar qo'shing yoki matnni o'zgartiring.
Xatolar bo'lsa: Brauzer konsolini oching (F12) va xatolarni ko'ring.

Kengaytma: Tugmani bosganda matn ham o'zgarsin.