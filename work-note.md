# work-note

## Example

```
$ npm install --save @github/clipboard-copy-element
```

Inline `code` has `back-ticks around` it.

| Tables        |      Are      |  Cool |
| ------------- | :-----------: | ----: |
| col 3 is      | right-aligned | $1600 |
| col 2 is      |   centered    |   $12 |
| zebra stripes |   are neat    |    $1 |

## Table of Contents
- [Command](#command)
- [Usage](#usage)
- [Features](#features)


## Command
```
php artisan make:controller --super-domain=Admin --domain=AdminUser GetListAdminUserDetailController
```
```
php artisan make:action --super-domain=Admin --domain=AdminUser GetListAdminUserDetailAction
```
```
php artisan make:request --super-domain=Admin --domain=AdminUser GetListAdminUserDetailRequest 
```
```
php artisan make:resource --super-domain=Admin --domain=AdminUser GetListAdminUserDetailResource
```

## Git
```
git branch | grep -v "$(git branch --show-current)" | xargs git branch -D
```


ubuntu@dsoft-dev-link:/var/www/dev-docker docker compose exec postgres sh
# pg_dump -U default -d management_dev_4 -f dev4.sql
ubuntu@dsoft-dev-link:/var/www/dev-docker docker compose cp postgres:/dev4.sql ./

máy mình: scp dsoft-dev-elic-link:/var/www/dev-docker/dev4.sql ./
máy mình local docker: docker compose cp ~/Downloads/dev4.sql postgres:/
psql -U default client-dev-5 < client-dev-5.sql





-----



FILTER ---------
mail
username
status  -> disable, enable
two_fac_auth
status mail -> 

SORT -----
tang dan, giam dan


**SORT** -----
'tang dan, giam dan'


    'id',
    'email',
    'user_name',
    'admin_permission', //
    'is_valid', // trang thai dang ky
    'is_two_factor',//
    'address',
    'status', //  xac nhan email confirm, confirmed , confirming

    'updated_by', // change
    'updated_at',


MAN HINH CAN QUAN TAM
1. A (Cài đặt) Quản trị quản lý người dùng trang web
2. A Cài đặt (quản lý nhà máy điện)
3. A Cài đặt (Quản lý nhà máy điện mặt trời)
4. Một cài đặt (quản lý pin lưu trữ)
5. Danh sách mục đăng ký CSV




**PERMISSION**
site admin user:

    sustech-admin           => CRUD all view, trừ create plan, người mua 
    sustech-refer-admin     => only read

=> userAdmin < admin

site user:
    contractor          -> create plan, create người mua
    contractor_refer    -> only read
    power_plant         -> xem chart power_plant, list plan ... -> user, chỉ được phép access vào site user

=> power_plant < contractor_refer < contractor 

    internal 
    ai   




./cursor-0.42.5-build-24111460bf2loz1-x86_64.AppImage

