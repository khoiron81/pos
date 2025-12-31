# POS Dapoer Bengawan — Work Plan (Source of Truth)

Repo: https://github.com/khoiron81/pos
Branch: main

## Prinsip Kerja
1. Dokumen di folder `docs/` adalah acuan utama (single source of truth).
2. Jangan ubah struktur database tanpa update `docs/01_DATABASE_SCHEMA_V1.md` dan catat di `docs/09_CHANGELOG_RULES.md`.
3. Setiap task wajib menyebut:
   - target file/fitur
   - expected output
   - constraint (mis: tidak boleh ubah schema)
4. Jika ada error runtime, perbaiki minimal (surgical change), tidak refactor besar.

## Milestone
### M0 — Bootstrap (DONE/IN PROGRESS)
- Laravel 12 running on CWP Pro
- Core migrations RMS v1
- Seed roles + superadmin

### M1 — Auth + Outlet Context (ACTIVE)
- Login UI route
- Select Outlet page + store selected outlet in session
- Middleware ResolveOutlet + global outlet context

### M2 — Admin Master Data
- CRUD Brands
- CRUD Outlets
- CRUD Tables (meja + QR token)
- Outlet Settings (local_base_url)

### M3 — Ordering (QR + Cashier)
- QR landing (choose menu, cart)
- Create order API (service-driven)
- Split kitchen tickets + workflow status

### M4 — POS Payment + Receipt
- Pay order
- Print view / receipt

### M5 — Audit + Anti-miss
- order_events append-only
- minimal reporting