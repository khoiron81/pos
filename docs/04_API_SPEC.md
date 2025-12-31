# API Spec (Minimal)

## Create Order (Public)
POST /api/orders

Body:
{
  "qr_token": "....",
  "customer_name": "Budi",
  "items": [
    {"menu_item_id": "uuid", "qty": 2, "notes": "pedas"}
  ],
  "notes": "..."
}

Response 201:
{
  "order_id": "uuid",
  "order_no": "DBW-SRG-20251230-0001",
  "status": "BARU",
  "grand_total": 50000
}