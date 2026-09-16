# AUDIT-ARMIN — وضعیت مخزن

> Branch: `audit/zcode-20260828` · Date: 2026-08-28

مخزن `Armin` با توضیح «Painting lead generation» ساخته شده اما فقط دو فایل دارد (آخرین تغییر گیت‌هاب: 2026-06-30):

1. `heart-awareness-map-v3.html`
2. `سیستم-همیشه-روشن-پرامپت-و-دستورالعمل.md` — که خواندیم: **طرح پیدایش LANGAR** است (بات HRV تک‌کاربره، SQLite، kill-switch، systemd always-on). ربط مستقیمی به lead generation نقاشی ندارد.

**نکتهٔ حیاتی:** پای نقاشیِ واقعی و درحال‌اجرا روی برد 138 زندگی می‌کند (OFN tenant `lead`، port 8792، `lead.master-painting.com`، `painting.sqlite` با ۸ ردیف پایلوت، quote از طریق outbox) — یعنی در مخزن `ofn-node`، نه این‌جا. این جداافتادگی خودش یک «جعبهٔ سیاه naming» است.

**شکاف‌ها نسبت به توضیح مخزن:** صفر domain model، صفر pipeline لید، صفر تست، صفر adapter CRM/email/calendar.

**دو گزینهٔ مالک (تصمیم):**
- (الف) این مخزن رسماً به «specs/نقشه‌ها» تغییر کارکرد دهد؛ بیزنس زنده در ofn بماند — سازگار با وضعیت فعلی.
- (ب) طبق سند معماری خود مالک، اسکلت `domain/ pipeline/ learning/ adapters/ tests/` این‌جا ساخته شود و از OFN تفکیک شود.

جزئیات در `EVIDENCE/armin-evidence.json`. رودمپ کلی و تصمیم‌ها در شاخهٔ audit مخزن ofn-node (`ROADMAP.md` / `OWNER-DECISIONS-NEEDED.md`).
