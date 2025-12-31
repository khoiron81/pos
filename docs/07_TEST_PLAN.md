# Test Plan (Manual)

1) Auth
- GET /login -> form tampil
- POST /login -> sukses redirect admin/select-outlet

2) Outlet Select
- SUPER_ADMIN: tampil semua outlet
- Non superadmin: tampil outlet assigned saja
- POST select-outlet -> session outlet_id terset

3) Admin CRUD
- /admin/brands list/create/edit/delete
- /admin/outlets list/create/edit/delete

4) QR
- /qr/{token} tampil skeleton
- POST /api/orders create order + create tickets