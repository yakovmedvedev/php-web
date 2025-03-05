here will be a description

https://github.com/slimphp/Slim/blob/4.x/README.md

https://github.com/slimphp/PHP-View

Самостоятельная работа

1.Создайте php-проект (используя Composer) с кодом из описания фреймворка https://github.com/slimphp/Slim

Выполните инициализацию проекта.
Установите фреймворк как зависимость.
Создайте файл public/index.php, куда добавьте пример из README (абзац — "Hello World using AppFactory with PSR-7 auto-detection").
Установите пакеты (зависимости) по инструкции из README.
Запустите проект, выполнив команду php -S localhost:5555 -t public в корне проекта.
Откройте страницу http://localhost:5555/hello/mike, а затем http://localhost:5555/hello/john.

2.Подключите к вашему проекту, созданному в предыдущем уроке, пакет PHP-View в соответствии с документацией. В начале файла public/index.php определите псевдоним для работы с пакетом:

      <?php

      use Slim\Views\PhpRenderer;
Создайте директорию templates в корне проекта.

Добавьте обработчик в файл public/index.php:

      <?php

      $app->get('/about', function ($request, $response) {
          $phpView = new PhpRenderer('../templates');
          return $phpView->render($response, 'about.phtml');
      });
Создайте файл templates/about.phtml. Добавьте туда любой html-код.

Запустите проект по аналогии с предыдущим уроком, и откройте в браузере страницу http://localhost:5555/about.
