# work-note



php artisan make:controller --super-domain=Admin --domain=AdminUser GetListAdminUserDetailController


php artisan make:action --super-domain=Admin --domain=AdminUser GetListAdminUserDetailAction


php artisan make:request --super-domain=Admin --domain=AdminUser GetListAdminUserDetailRequest


php artisan make:resource --super-domain=Admin --domain=AdminUser GetListAdminUserDetailResource


FILTER ---------
mail
username
status  -> disable, enable
two_fac_auth
status mail -> 




SORT -----
tang dan, giam dan


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