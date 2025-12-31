# Route Map

## Auth
GET  /login        -> Auth\LoginController@show
POST /login        -> Auth\LoginController@login
POST /logout       -> Auth\LoginController@logout

## Admin
GET  /admin/home           -> admin.home
GET  /admin/select-outlet  -> admin.select-outlet (web, auth)
POST /admin/select-outlet  -> admin.select-outlet.save (web, auth)

CRUD:
- /admin/brands   -> BrandController (resource)
- /admin/outlets  -> OutletController (resource)

## QR Public
GET  /qr/{token}          -> QR landing skeleton
POST /api/orders (public) -> create order