post�ύ����ʱ����ʾ���£�

The page has expired due to inactivity. 

Please refresh and try again
1
2
3
����������laravel������д�Ҫ���κ�ָ�� web �� POST, PUT �� DELETE ·�ɵ� HTML ������Ӧ�ð���һ�� CSRF ���ƣ�����������󽫻ᱻ�ܾ���

<form method="POST" action="/profile">
{{ csrf_field() }}
    ...
</form>
=====================
https://51.ruyo.net/3127.html#1

------------------------------
��ʼ������
���ߣ�mrcn
���ӣ�https://www.zhihu.com/question/35537084/answer/181734431
��Դ��֪��
����Ȩ���������С���ҵת������ϵ���߻����Ȩ������ҵת����ע��������
composer install --no-dev
#��װ�����޸�.env������
APP_ENV=production
APP_DEBUG=false
�Լ�������һЩ���ã�ȷ��MySQL����������
php artisan migrate
php artisan key:generate
php artisan down#ͣ����վ
git pull
php artisan migrate#���´��뼰���ݿ�
php artisan clear-compiled
php artisan cache:clear
php artisan config:cache
php artisan optimize
composer dump-autoload --optimize
#������ջ�����ؽ�����
php artisan up#�ر�ά��״̬���������


=============================================
Laravel.

===========
PHP Parse error:  syntax error, unexpected '?' in D:\GITHUB\gitee\vipVideo\vendo
r\laravel\framework\src\Illuminate\Foundation\helpers.php on line 233
--php�汾Ҫ>7.0
�������°��XAMPP
==================

�������ͼƬ���س���403����
��<head></head>�����һ��
<meta name="referrer" content="no-referrer"/>

=======================================================
[2018-04-10 08:53:08] local.ERROR: Call to undefined function App\Http\Controllers\randStr() {"exception":"[object] (Symfony\\Component\\Debug\\Exception\\FatalThrowableError(code: 0): Call to undefined function App\\Http\\Controllers\
andStr() at C:\\github\\vipVideo\\app\\Http\\Controllers\\UserController.php:43)
    "autoload": {
        "classmap": [
            "database/seeds",
            "database/factories"
        ],
	"files": [
            "vendor/function.php",
	    "vendor/sho/simple_html_dom.php"
        ],
        "psr-4": {
            "App\\": "app/"
        }
    },
composer dump-autoload
========================================================
�����Դ
MySql֧�ֵ�utf8��������ַ�����Ϊ3�ֽڣ��������4�ֽڵĿ��ַ��ͻ���ֲ����쳣�������ֽ�UTF-8����ܱ����Unicode�ַ���0xffff����Unicode�еĻ���������ƽ�棨BMP�����������Emoji���飨Emoji��һ�������Unicode���룩���ڵķǻ���������ƽ���Unicode�ַ����޷�ʹ��MySql��utf8�ַ����洢��

��ҲӦ�þ���Laravel 5.4����4�ֽڳ��ȵ�utf8mb4�ַ������ԭ��֮һ������Ҫע����ǣ�ֻ��MySql 5.5.3�汾�Ժ�ſ�ʼ֧��utf8mb4�ַ����루�鿴�汾��selection version();�������MySql�汾���ͣ���Ҫ���а汾���¡�

ע������Ǵ�Laravel 5.3������Laravel 5.4������Ҫ���ַ��������л���

�������
����MySql�汾��5.5.3���ϡ�

�ֶ�����Ǩ������migrate���ɵ�Ĭ���ַ������ȣ���AppServiceProvider�е���Schema::defaultStringLength������ʵ�����ã�

    use Illuminate\Support\Facades\Schema;

    /**
* Bootstrap any application services.
*
* @return void
*/
public function boot()
{
   Schema::defaultStringLength(191);
}

//����model
https://github.com/Xethron/migrations-generator