# SimpleMVCFramework
Simpe framework for understanding and realize test projects more comfortably
### Простой MVC фреймворк  предназначен для ознакомительных целей
##
Данный фреймворк исключительно для понимания MVC модели и для упрощения дальнейшей разработки проекта на его основе.

## Описание
Для взаимодействия MVC паттерна имеются 3 класса в папке *libraries*
* `Core.php` - создаёт пути и загружает главные контроллеры
* `Controller.php` - главный контроллер, загружает модели и представления
* `Database.php` - подключение к БД, подготовка и получение данных 

## Установка
Скачать репозиторий и разорхивировать готовую структуру в любую IDE

## Запуск / разработка
По стандарту папка *app* для разработки, папка *public* отображения информации.
* В файле  `config.php` необходимо установить свои значения для инициализации БД и URL проекта.
* В файле  `public/.httaccess` в *RewriteBase* указать название проекта *projectname*/mvc
* Модели разрабатываются в соответствующей папке `models`. Для работы с данными требуется экземпляр класса Database.
 * Контроллеры разрабатываются в соответствующей папке `controllers`. Для работы с представлениями и моделями требуется объявить их экземпляры с наследуемого главного контроллера `Controllers.php`
 
   1. объявление модели для получения доступа к данным.
``` php
public function __construct(

    )
    {
        $this->userModel = $this->model('Model');
    }
 ```
 
 2. объявление представления для отображения результатов на странице.
``` php
Class ClassName extends Controller
{
  // загрузить представление (view)
  $this->view('your/path', $data);
}
 ```
 ---



 

* Visit [http://localhost/](http://localhost/)
* 


