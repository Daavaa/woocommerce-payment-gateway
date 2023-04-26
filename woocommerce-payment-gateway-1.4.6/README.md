# WooCommerce plugin for Payme

## Установка

#### Требования

- PHP >= 5.4
- [WordPress 4.x](https://wordpress.org/)
- [WooCommerce 3.x](https://woocommerce.com/)
- Регистрация в кабинете поставщика [Paycom](http://paycom.uz/)

#### GitHub

Скачайте плагин как [ZIP архив](https://github.com/PaycomUZ/woocommerce-payment-gateway/releases/latest)

Загрузите плагин в WordPress

![Upload plugin](images/upload-plugin.png)

...и установите его

![Install plugin from ZIP](images/install-from-zip.png)

Активируйте плагин после установки

![Activate plugin](images/activate-plugin.png)

#### Что бы Apache не игнорировал заголовок `Authorization` надо загрузить файл `.htaccess` со следующем содержанием:

```
RewriteEngine On
RewriteCond %{HTTP:Authorization} ^(.*)
RewriteRule .* - [e=HTTP_AUTHORIZATION:%1]
```

в корневую директорию сайта

Откройте страницу настроек WooCommerce

![WooCommerce Settings page](images/woocommerce-settings.png)

Откройте вкладку `Checkout`

![Checkout Tab](images/checkout-tab.png)

Откройте вкладку `Payme` и внесите необходимые данные.

![Payme Settings](images/payme-settings.png)

Скопируйте ваш `Endpoint URL` и внесите его в кабинете поставщика Paycom.

![Set Endpoint URL](images/endpoint-url.png)


## Фискализация

Для того что-бы самому отправлять фискальные данные, ван нужно будет включить эту функцию в настройках плагина.

![Fiscal Settings](images/fiscal_image.png)

В настройках товара в разделе `Данные товара`, во вкладке `Основные`, вы увидите 3 поля, которые нужно будет заполнить.

![Fiscal Settings](images/product_fiscal_image.png)