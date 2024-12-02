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

```
art db:seed --class=User2AddRoleSeeder
```

## Git
```
git branch | grep -v "$(git branch --show-current)" | xargs git branch -D
```

```
git pull --rebase
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


    {
      "id": 1,
      "email": "admin-sustech@yopmail.com",
      "user_name": "Sustech Admin 1",
      "admin_permission": "管理",
      "is_valid": true,
      "is_two_factor": true,
      "status": "確認済み",
      "updated_by_name": "Sustech Admin 1",
      "updated_at": "2024-11-26T10:33:49.000000Z"
    }


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
    power_plant (tram phat dien)         -> xem chart power_plant, list plan ... -> user, chỉ được phép access vào site user

=> power_plant < contractor_refer < contractor 

    internal 
    ai   


**LOGIN ELIC POWER**
"transmission_provider_code": Nếu power_contract_permission là true, bắt buộc phải có giá trị.
"occto_password": Tương tự với logic phụ thuộc vào power_contract_permission.

./cursor-0.42.5-build-24111460bf2loz1-x86_64.AppImage



## SQL
TO_CHAR(updated_content_at, 'YYYY-MM-DD HH24:MI'): Chuyển đổi kiểu dữ liệu timestamp của cột thành chuỗi định dạng cụ thể.

DISTINCT ON: Lấy các bản ghi duy nhất dựa trên giá trị định dạng của 
orderBy: Sắp xếp các bản ghi theo
$column + INTERVAL '9 hour': Cộng thêm 9 giờ vào giá trị của cột $column để điều chỉnh múi giờ (giả định hệ thống lưu UTC nhưng cần lọc theo múi giờ khác).
ILIKE: So sánh không phân biệt chữ hoa/thường với chuỗi con %$value%. `%\\`

in_array($column, User::COLUMN_NOT_STRING) -> return true / false


$this->model = $this->model->from($subQuery)->withTrashed()
    ->orderByRaw($column . ' ASC NULLS FIRST, company_name COLLATE "ja_JP.utf8" ASC, user_name COLLATE "ja_JP.utf8" ASC, email COLLATE "ja_JP.utf8" ASC');

    $this->model->from($subQuery):
        Thay thế query gốc bằng subQuery. subQuery được xác định trước đó (tùy thuộc vào $column là updated_content_at hay không).
        from() cho phép sử dụng một query con (subQuery) làm nguồn dữ liệu.


    withTrashed(): Bao gồm cả các bản ghi đã bị "soft deleted" 
    orderByRaw(): Thực hiện sắp xếp bằng câu SQL thô, cho phép kiểm soát chi tiết thứ tự và ưu tiên.
    $column . ' ASC NULLS FIRST':

    Sắp xếp cột $column theo thứ tự tăng dần (ASC).
    `NULLS FIRST`: Các giá trị NULL được ưu tiên trước các giá trị khác (thường dùng trong PostgreSQL).


isset(mixed $var): bool
    Trả về true nếu biến được khởi tạo và không phải là null.
    Trả về false nếu biến chưa được khởi tạo hoặc có giá trị null.


unset($dataUser['occto_password']):
    Xóa khóa 'occto_password' và giá trị tương ứng khỏi mảng $dataUser.
    Sau khi xóa, mảng $dataUser sẽ không chứa khóa 'occto_password'.

$user->roles()->detach(): xoa role cua $user