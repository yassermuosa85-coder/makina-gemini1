# Style 02 — Glassmorphism SaaS

بطاقات زجاجية شفافة عائمة فوق خلفية Gradient Mesh ملوّنة — عمق حقيقي (Depth) بدل التسطيح.

## الملفات

| الملف | المحتوى |
|---|---|
| `slides.html` | الشرائح السبع كاملة بنفس مثال المحتوى المستخدم بـ Style 01 (للمقارنة المباشرة بين الأنظمة) |
| `components.html` | مكتبة المكوّنات الزجاجية |
| `README.md` | هذا الملف |

## Typography

نفس نظام الخطوط بـ Style 01 (ثابت عبر كل الأنظمة الأربعة للحفاظ على هوية بصرية موحّدة):
**عربي:** IBM Plex Sans Arabic · **لاتيني/أرقام:** Inter · **بيانات:** JetBrains Mono

| الاسم | الوزن | الحجم | الاستخدام |
|---|---|---|---|
| Heading XL | 800 | 68px | غلاف |
| Heading L | 700 | 46px | عناوين محتوى |
| Heading M | 600 | 28px | عناوين بطاقات |
| Body | 500 | 21px | فقرات |
| Caption | 700 (Inter) | 13px uppercase | Eyebrow |

## Color Palette

| Token | القيمة | الاستخدام |
|---|---|---|
| `--bg-base` | `#0D0B1A` | القاعدة الغامقة خلف التدرّجات |
| `--mesh-purple` | `#8B5CF6` | فقاعة تدرّج علوية |
| `--mesh-magenta` | `#EC4899` | فقاعة تدرّج وسطية (دفء) |
| `--mesh-cyan` | `#22D3EE` | فقاعة تدرّج + اللون الأساسي التفاعلي |
| `--glass-bg` | `rgba(255,255,255,.06)` | تعبئة البطاقة الزجاجية |
| `--glass-border` | `rgba(255,255,255,.16)` | حدّ البطاقة (highlight) |
| `--text-primary` | `#F5F3FF` | نص أساسي (أبيض بميلان بنفسجي خفيف) |
| `--text-secondary` | `rgba(245,243,255,.64)` | نص ثانوي |
| `--accent` | `#22D3EE` | سيان — العنصر التفاعلي الأساسي |
| `--accent-2` | `#A78BFA` | بنفسجي — لمسات ثانوية/زخرفية |
| `--success` | `#34D399` | إيجابي |
| `--danger` | `#FB7185` | سلبي |

## Glass Effect (الخاصية المحورية للنظام)

```css
background: var(--glass-bg);
backdrop-filter: blur(20px) saturate(150%);
-webkit-backdrop-filter: blur(20px) saturate(150%);
border: 1px solid var(--glass-border);
box-shadow: 0 8px 32px rgba(0,0,0,.35), inset 0 1px 0 rgba(255,255,255,.12);
```

## Spacing — شبكة 8px

`4 · 8 · 16 · 24 · 32 · 48 · 64 · 96 · 120` — نفس شبكة Style 01.

## Radius

| Token | القيمة |
|---|---|
| `--r-md` | 20px (بطاقات) |
| `--r-lg` | 32px (لوحات كبيرة) |
| `--r-pill` | 999px (شارات/أزرار) |

الاستدارة الكبيرة هنا مقصودة ومتماشية مع طبيعة الزجاجية نفسها (أشكال عائمة ناعمة) — وليست استدارة موحّدة عشوائية؛ فقاعات الخلفية بأشكال blob غير منتظمة تكسر الرتابة.

## Components الموثّقة في `components.html`

Glass Badge · Glass Tag · Glass Button (Primary/Ghost) · Floating Number Card · Glass Info Card · Glass Quote Card · Glass Comparison Row · Glass Timeline · Glass Progress Bar · Highlight/CTA Box زجاجي

## اقتراحات حركة

- دخول البطاقات الزجاجية: fade + scale من .96 إلى 1، 350ms — يعزز إحساس "العوم"
- فقاعات الخلفية: حركة بطيئة جداً (drift) لو تحوّل لفيديو، 12s ease-in-out — تُترك ثابتة بالتصدير الساكن PNG
