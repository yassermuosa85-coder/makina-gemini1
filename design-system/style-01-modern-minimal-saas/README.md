# Style 01 — Modern Minimal SaaS

مستوحى من: Linear · Vercel · Raycast

نظام تصميم كامل لكاروسيلات Instagram (1080×1350، نسبة 4:5) لحساب ينشر عن الذكاء الاصطناعي، أدوات AI، السوشيال ميديا، الدروبشوبينغ، والتجارة الإلكترونية.

## الملفات

| الملف | المحتوى |
|---|---|
| `slides.html` | الشرائح السبع كاملة (Cover, Content, Quote, Stats, Tips, Comparison, CTA) بمثال محتوى واحد متكامل |
| `components.html` | عرض لكل المكوّنات القابلة لإعادة الاستخدام منفصلة عن أي شريحة |
| `README.md` | هذا الملف — توثيق الـ Design Tokens |

افتح الملفين مباشرة بأي متصفح (لا يحتاجان خادماً — يحمّلان الخطوط من Google Fonts مباشرة).

## Typography

**الخط العربي (عناوين ونصوص):** IBM Plex Sans Arabic — خط هندسي حديث بنفس روح Linear/Vercel، يدعم العربي بجودة كاملة بعكس Inter/Geist/Manrope/Satoshi المطلوبة أصلاً (لاتينية فقط).
**الخط اللاتيني (أرقام، وسوم إنكليزية، UI صغيرة):** Inter — كما طُلب، يُستخدم فقط في السياقات اللاتينية (AI، أرقام الإحصائيات، Badges إنكليزية).
**خط البيانات/الأكواد:** JetBrains Mono — للأرقام الكبيرة بالإحصائيات والعدادات (٠١/٠٧ إلخ).

| الاسم | الخط | الوزن | الحجم | Line-height | الاستخدام |
|---|---|---|---|---|---|
| Heading XL | IBM Plex Sans Arabic | 800 | 64px | 1.15 | عنوان شريحة الغلاف |
| Heading L | IBM Plex Sans Arabic | 700 | 44px | 1.25 | عناوين شرائح المحتوى |
| Heading M | IBM Plex Sans Arabic | 600 | 28px | 1.35 | عناوين البطاقات الفرعية |
| Body | IBM Plex Sans Arabic | 500 | 20px | 1.75 | نص فقرات |
| Caption | Inter | 700 | 13px, uppercase, tracking .08em | 1.4 | Eyebrow/تسميات صغيرة |
| Data | JetBrains Mono | 700 | 56px | 1 | أرقام الإحصائيات الكبيرة |

## Color Palette

| Token | القيمة | الاستخدام |
|---|---|---|
| `--bg` | `#0A0A0B` | خلفية الشريحة الأساسية |
| `--surface` | `#131316` | خلفية البطاقات |
| `--surface-2` | `#1C1C20` | بطاقات متداخلة / hover |
| `--border` | `#26262B` | حدود رفيعة (hairline) |
| `--text-primary` | `#F5F5F7` | نص أساسي (أبيض مكسور) |
| `--text-secondary` | `#9A9AA2` | نص ثانوي |
| `--text-tertiary` | `#5F5F68` | نص باهت جداً (تسميات صامتة) |
| `--accent` | `#4C8DFF` | اللون الأساسي (أزرق) |
| `--accent-soft` | `rgba(76,141,255,.12)` | خلفيات الشارات والتوهج |
| `--success` | `#34D399` | حالة إيجابية (مقارنات، ✓) |
| `--warning` | `#FBBF24` | تنبيه |
| `--danger` | `#F87171` | حالة سلبية (✗) |

## Spacing System — شبكة 8px

`4 · 8 · 16 · 24 · 32 · 48 · 64 · 96 · 120`

هوامش الشريحة الآمنة: 96px يمين/يسار، 120px أعلى، 140px أسفل (فوق شريط البراند).

## Radius

| Token | القيمة | الاستخدام |
|---|---|---|
| `--r-sm` | 8px | شارات/وسوم صغيرة |
| `--r-md` | 16px | بطاقات عادية |
| `--r-lg` | 24px | بطاقات كبيرة/مميزة |
| `--r-pill` | 999px | أزرار وشارات دائرية |

## Shadows / Glow

- بطاقة عادية: `0 8px 24px rgba(0,0,0,.35)`
- توهج اللون الأساسي (Soft Glow): `0 0 60px rgba(76,141,255,.18)`
- حدّ داخلي علوي خفيف (لمسة عمق): `inset 0 1px 0 rgba(255,255,255,.04)`

## Stroke Width

- حدود البطاقات: 1px
- أيقونات الخط: 1.5px

## Components الموثّقة في `components.html`

Badge · Tag/Category · Breaking News Label · AI Label · Social Label · Dropshipping Label · Button (Primary/Ghost) · Number Card · Info Card · Quote Card · Feature Card · Comparison Row · Timeline · Progress Bar · Highlight Box · CTA Box

## اقتراحات حركة (Animation) — للتنفيذ المستقبلي عند التصدير كفيديو/ريلز

- دخول العناوين: fade + translateY(8px) خفيف، 300ms ease-out
- الشارات: scale من 0.9 إلى 1 مع fade، 200ms
- بطاقات الإحصائيات: تتابع دخول (stagger) 80ms بين كل بطاقة
- التوهج الخلفي: نبض بطيء جداً (breathing) اختياري، 4s ease-in-out infinite — يُستخدم بحذر شديد فقط إذا صار تصدير فيديو، وليس PNG ثابت
