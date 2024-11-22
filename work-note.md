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
    'two_factor_auth',//
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


- man hinh da doc:
 -  Quan ly admin user
    + QA:
    + API:
    + 

 -  Quan ly position
 -  Quan ly kiem soat pin luu tru (chart)
    + Lua chon: are name,BG name (require), pin name
 -  Quan ly BG
 -  Quan ly plan
 -  Quan ly quyen
 -  Quan ly setting tram phat dien

 - (Setting) Quan ly pin luu tru
   + FEATURE: 
      +  CURD kiem soat pin
      +  admin only view

  + API:
      +  get list kiem soat pin
      +  




task est / start date

self review
 - full-lint
 - happy case
 - telescop
   + duaration, memory: 30 MB 
   + query: time
   + vai tram ms


research
queues, worker 
horizon 

ELIC POWER: LAP KE HOACH SAC, XA PIN

SRS
1. tab list item dang ky CSV
    0 tron minh phai validate
2. tab giam sat thanh tich ke hoat phat dien
   cot xanh: plant di nop
   cot vang: thuc te 
        lay third-party-> CSV, lay theo thoi gian Job
        baplace
        1030   30kkw
        11h00  35kw
   duong xanh green: du doan
        ke hoach lap ra tu truoc, gia tri minh co 
        traning 72h next



      ------
      ke hach phat dien: phat cho khong or.

      ke hoach ban dien: phat ra va thu tien


signal


3. tab~ IMBALACE: giam sat thanh tich plan ke hoach
    chart cot len, cot xuong, mau ne
    do: ke hoac - du doan
    vang: ke hoach - thuc te
    duong dut gay: du doan gia dien
    duong xanh lien: gia tien dien thuc te

4. tab tao position
    self consuin
    relative trading: dung 1 phan, ban 1 phan
    spot market: chi ban
    surplus imbalance: dung con du moi ban


    .- tom tat 
    - position graph (duong lon xon, doc lai cho dung mau)
        duong xanh: du bao luong phat dien moi nhat
        duong do: du bao gia
        duong  : du bao

        tong 4 chong === tong luong dien sinh ra (real power)

    chart sac, xa dien
        duong xanh: SOC
        duong nhiet do
        cot sac
        cot xa
    

    chart doanh thu (line 820)
        cot total
        . choongf len tung khoi theo dk chon



5. tab kiem soat pin luu tru
    duong vang: luong phat dien, pin noi voi tram solar
    cot hong: 
    cot xanh

    third-party return (ELIC link,...)
    luong xa, sac dien ~ co the nhap tay vao

    sac dien nhap gia tri am. 
    xa dien nhap gia tri duong

6. tab Quan ly postion
   
   set job de di qua third-party di lay du lieu



7. tab quan ly kiem soat pin luu tru (battery control management )
   
    setting time de qua third-party di get data

8. tab quan ly plan

9. tab giao dich JEPX
    nhu la san giao dich, de mua ban dien

    - do ra gia dau thau

10. tb quan ly quyen
    chuyen lai thanh company with