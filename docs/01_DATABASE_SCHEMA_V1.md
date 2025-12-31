# RMS v1 — Database Schema (LOCKED)

## Catatan Penting
- Struktur inti mengikuti schema v1 yang sudah disepakati (brands/outlets/roles/users/user_outlets/tables_restaurant/menu/orders/payments/events).
- Jika ada kebutuhan tambahan: buat migration baru + update dokumen ini.

## Tables (ringkas)
Platform Core:
- brands
- outlets
- tables_restaurant
- roles
- users
- user_outlets
- outlet_settings

Menu:
- menu_categories
- menu_items

Ordering + Kitchen:
- orders
- order_items
- kitchen_tickets
- kitchen_ticket_items
- order_events

Payments:
- payments

## Field penting yang harus konsisten
- roles: (code, name)  — code ENUM-like (SUPER_ADMIN, OWNER_BRAND, dst)
- users: id UUID/char(36), role_id FK roles.id
- outlets: outlet_code (bukan `code`)
- tables_restaurant: table_no, qr_token