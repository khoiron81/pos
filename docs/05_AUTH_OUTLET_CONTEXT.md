# Auth + Outlet Context

## Tujuan
- Setelah login, user wajib memilih outlet aktif (kecuali SUPER_ADMIN bisa melihat semua outlet).
- Outlet aktif disimpan di session: `outlet_id`.
- Middleware `ResolveOutlet` memastikan request admin memiliki outlet_id.

## Rules
- Jika user bukan SUPER_ADMIN:
  - hanya boleh pilih outlet yang ter-assign di pivot `user_outlets`.
- Jika outlet belum dipilih:
  - redirect ke `admin.select-outlet`.

## Contract
- User model harus punya helper:
  - isSuperAdmin(): bool
  - role(): belongsTo(Role)
- Outlet relation:
  - User::outlets() belongsToMany via user_outlets