# Laravel-tinker-tutorial
Hướng dẫn sử dụng laravel tinker
1. Vào workspace (nếu chạy bằng laradock)

```php
docker compose-exec workspace bash
```

2. Vào tinker
```php
php artisan tinker
```
3. Chạy hàm test ví dụ
```php
app()->make(namespace\Tên class::class)->hàm cần test()

app()->make(App\Models\MT100MemberC::class)->first()

$user = App\Models\MT100MemberC::first();
$user->delete();
```

4. Lưu ý
    - Khi thay đổi code cần test lại phải thoát tinker rồi vào lại
    - Khi truy vấn kết quả trả về là các collection thì nên sử  dụng hàm toArray()
      ```php 
      app()->make(App\Models\MT100MemberC::class)->first()->toArray()
    
      ```

5. [Link tham khảo](https://viblo.asia/p/debug-de-dang-hon-voi-laravel-tinker-YWOZrwy7lQ0)
