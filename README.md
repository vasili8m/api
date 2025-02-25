# HeadHunter API

**По-русски** | [In english](docs_eng/README.md)

HeadHunter API — это инструментарий для интеграции
[HeadHunter](http://hh.ru/) в ваш продукт.

Для начала ознакомьтесь с [общей информацией](docs/general.md) по работе API,
[часто задаваемыми вопросами](docs/FAQ.md) и
с требованиями к [использованию логотипов](https://dev.hh.ru/articles/logos) и
[названию приложений](https://dev.hh.ru/articles/apps).

Для использования методов, требующих авторизацию пользователя или приложения, вам необходимо
зарегистрировать приложение по адресу [https://dev.hh.ru](https://dev.hh.ru)
и настроить процесс [авторизации](docs/authorization.md).

Зарегистрированное приложение может запрашивать у пользователей hh.ru
разрешение доступа к их персональным данным, без получения и хранения их
логина и пароля.


> ‼️ Обратите внимание на [описание](docs/payable/resume.md) новой модели работы с базой резюме. 

> Доступ к ряду методов для работодателя [платный](docs/payable/employer_methods.md). 

> Для уточнения стоимости API необходимо обратиться к Вашему персональному менеджеру или позвонить по телефону: 
> +7 495 974-64-27 (для Москвы и Подмосковья),  
> +7 812 458-45-45 (для Санкт-Петербурга),  
> 8 800 100-64-27 (для регионов России).

## OpenAPI

Доступная в OpenAPI документация будет со временем дополняться.
Методы, описанные в данной документации и доступные в OpenAPI, имеют соответствующую ссылку.

Визуализации [ReDoc](https://api.hh.ru/openapi/redoc) и [Swagger](https://api.hh.ru/openapi/swagger).

Спецификация HeadHunter API: [openapi.yml](https://api.hh.ru/openapi/specification/public).

<a name="content"></a>
## Содержание

Пометки в документации:

* <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> –
  актуально для анонимных запросов, не требует авторизации.
* <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> – актуально для запросов от имени приложения, требует [авторизацию приложения](docs/authorization_for_application.md)
* <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> –
  актуально для запросов от имени соискателя, требует [авторизацию пользователя](docs/authorization_for_user.md).
* <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" /> –
  актуально для бесплатных методов работодателя, требует  [авторизацию пользователя](docs/authorization_for_user.md).
* <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" /> –
  актуально для [платных](docs/payable/employer_methods.md) методов работодателя, требует  [авторизацию пользователя](docs/authorization_for_user.md).


<a name="general"></a>
### Общая информация

* [Общая информация](docs/general.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Условия использования сервиса API](https://dev.hh.ru/admin/developer_agreement) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Требования к использованию логотипов](https://dev.hh.ru/articles/logos) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Требования к названию приложений](https://dev.hh.ru/articles/apps) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Авторизация](docs/authorization.md) <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Кэширование](docs/cache.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Ошибки и коды ответов](docs/errors.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Платный доступ для работодателей к некоторым методом API](docs/payable/employer_methods.md) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
* [Новая модель работы с базой резюме (поддержка в API)](docs/payable/resume.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />

<a name="resources"></a>
<a name="context"></a>
### Контекст

* [Информация об авторизованном пользователе или приложении](docs/me.md) <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Получение информации об авторизованном пользователе](docs/me.md#user-info) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Редактирование информации авторизованного пользователя](docs/me.md#user-edit) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Получение информации об авторизованном приложении](docs/me.md#application-info) <img src="http://hhru.github.io/api/badges/client.png" alt="client" />
* Информация о менеджере
  * [Рабочие аккаунты менеджера](docs/manager_accounts.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Предпочтения менеджера](docs/manager_settings.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Информация по активным услугам API для платных методов](docs/payable/employer_services.md#payable-api-actions) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Локализация](docs/locales.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Выбор сайта](docs/hosts.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />


<a name="resume"></a>
### Резюме

* [Поиск резюме](docs/resumes_search.md) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
* [Сохраненные поиски резюме](docs/resumes_saved_searches.md) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Список сохраненных поисков резюме](docs/resumes_saved_searches.md#resumes-saved-search-list) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Получение единичного сохраненного поиска резюме](docs/resumes_saved_searches.md#resumes-saved-search-item) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Создание нового сохраненного поиска резюме](docs/resumes_saved_searches.md#resumes-saved-search-create) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Обновление сохраненного поиска резюме](docs/resumes_saved_searches.md#resumes-saved-search-update) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Удаление сохраненного поиска резюме](docs/resumes_saved_searches.md#resumes-saved-search-delete) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Передача сохраненного поиска резюме другому менеджеру](docs/resumes_saved_searches.md#resumes-saved-search-move-to-other-manager) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
* [Просмотр резюме](docs/resumes.md#item) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
* [Работа с резюме для соискателя](docs/resumes.md) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Список резюме авторизованного пользователя](docs/resumes.md#mine) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Создание и редактирование резюме](docs/resumes.md#create_edit) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Публикация и продление резюме](docs/resumes.md#publish) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Удаление резюме](docs/resumes.md#delete) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [История просмотра резюме](docs/resumes.md#views) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Информация о статусе резюме и готовности резюме к публикации](docs/resumes.md#status-and-publication) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Списки видимости резюме](docs/resume_visibility.md) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
* [Артефакты (фото, портфолио)](docs/artifacts.md) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
* [Поиск по вакансиям, похожим на резюме](docs/resumes.md#similar) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
* [История откликов/приглашений по резюме](docs/resume_negotiations_history.md) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />

<a name="vacancies"></a>
### Вакансии

* [Получение вакансий](docs/vacancies.md) <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Поиск по вакансиям](docs/vacancies.md#search) <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
    * [Кластеры](docs/clusters.md) <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
    * [Описание использованных параметров](docs/vacancies_search_arguments.md) <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Получение информации о вакансии](docs/vacancies.md#item) <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Поиск по вакансиям, похожим на вакансию](docs/vacancies.md#similar) <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Отобранные вакансии](docs/vacancies.md#favorited) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
* [Скрытые вакансии](docs/blacklisted.md) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
* [Сохраненные поиски вакансий](docs/saved_search.md#vacancies-saved-search-list) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
* [Работа с вакансиями](docs/employer_vacancies.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Возможные варианты публикации вакансий](docs/employer_vacancies.md#available_types) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Публикация вакансий](docs/employer_vacancies.md#creation) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Редактирование вакансий](docs/employer_vacancies.md#edit) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Продление вакансий](docs/employer_vacancies.md#prolongate) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Список опубликованных вакансий](docs/employer_vacancies.md#active) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Архивация вакансий](docs/employer_vacancies.md#archive) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Список архивных вакансий](docs/employer_vacancies.md#archived) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Удаление вакансий](docs/employer_vacancies.md#hide) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Список удаленных вакансий](docs/employer_vacancies.md#hidden) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Список улучшений для вакансии](docs/employer_vacancy_upgrades.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Статистика по вакансии](docs/employer_vacancies.md#stats) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Черновики вакансий](docs/vacancy_drafts.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Получение списка черновиков](docs/vacancy_drafts.md#draft_list) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Удаление черновика](docs/vacancy_drafts.md#draft_delete) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Отмена автопубликации](docs/vacancy_autopublication.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />

<a name="applicants"></a>
### Соискатели

* [Комментарии к соискателю](docs/applicant_comments.md) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />


<a name="employers"></a>
### Работодатели/компании

* [Поиск компаний](docs/employers.md#search) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Получение информации о компании](docs/employers.md#item) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />

<a name="employer_managers"></a>
### Менеджеры работодателя

* [Менеджеры](docs/employer_managers.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Добавление менеджера](docs/employer_managers.md#add) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Редактирование менеджера](docs/employer_managers.md#edit) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Удаление менеджера](docs/employer_managers.md#delete) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Справочник менеджеров работодателя](docs/employer_managers.md#list) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Получение информации о менеджере](docs/employer_managers.md#item) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Дневной лимит просмотра резюме для текущего менеджера](docs/employer_manager_resume_limit.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />

<a name="negotiations"></a>
### Переписка (отклики/приглашения)

* [Переписка для соискателя](docs/negotiations.md) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Получение списка откликов](docs/negotiations.md#get_negotiations) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Получение списка активных откликов](docs/negotiations.md#get_negotiations_active) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Откликнуться на вакансию](docs/negotiations.md#post_negotiation) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Просмотр отклика/приглашения](docs/negotiations.md#get_negotiation) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Скрыть отклик](docs/negotiations.md#hide_message) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Просмотр списка сообщений в отклике](docs/negotiations.md#get_messages) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Отправка сообщений в отклике](docs/negotiations.md#send_message) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Редактирование сообщения в отклике](docs/negotiations.md#edit_message) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
* Резюме для отклика на указанную вакансию <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Список резюме, которыми можно откликнуться на указанную вакансию](docs/suitable_resumes.md) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
  * [Резюме, сгруппированные по возможности отклика на данную вакансию](docs/resumes_by_status.md) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" />
* [Переписка для работодателя](docs/employer_negotiations.md) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Модель работы, термины и процедуры](docs/employer_negotiations.md#model) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Общее описание процесса работы с откликами/приглашениями](docs/employer_negotiations.md#flow) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Коллекции и работодательские состояния откликов/приглашений](docs/employer_negotiations.md#collections) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Список откликов/приглашений](docs/employer_negotiations.md#negotiations-list) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Просмотр отклика/приглашения](docs/employer_negotiations.md#get-negotiation) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Работа с сообщениями по отклику/приглашению для работодателя](docs/employer_negotiations.md#get-messages) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Приглашение соискателя на вакансию](docs/employer_negotiations.md#add-invite) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Действия по отклику/приглашению (смена состояния)](docs/employer_negotiations.md#actions) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
  * [Статистика по работе с откликами](docs/employer_negotiations_statistics.md) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
* [Тексты сообщений](docs/negotiation_message_templates.md) <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />
* [Инструменты оценки](docs/assessment.md) <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp_paid.png" alt="employer with paid access" />


<a name="dictionaries"></a>
### Справочники

* [Регионы](docs/areas.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Специализации](docs/specializations.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Метро](docs/metro.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Языки](docs/languages.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Отрасли компаний](docs/industries.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Учебные заведения](docs/educational_institutions.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Основная информация об учебных заведениях](docs/university.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Факультеты учебных заведений](docs/faculties.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Справочники работодателя](docs/employer_dictionaries.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Адреса](docs/employer_addresses.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Типы и права менеджера](docs/employer_managers.md#dict) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Менеджеры работодателя](docs/employer_managers.md#list) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Департаменты](docs/employer_departments.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Тесты](docs/employer_tests.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Регионы вакансий](docs/employer_vacancy_areas_active.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Брендированные шаблоны вакансий](docs/employer_vacancy_branded_templates.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Ключевые навыки](docs/key_skills.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Прочие справочники](docs/dictionaries.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />


<a name="suggests"></a>
### Подсказки (autosuggest, autocomplete)

* [Подсказки](docs/suggests.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [по названиям университетов](docs/suggests.md#educational_institutions) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [по организациям](docs/suggests.md#companies) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [по специализациям](docs/suggests.md#specializations) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [по ключевым навыкам](docs/suggests.md#key-skills) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [по должностям](docs/suggests.md#positions) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [по регионам](docs/suggests.md#areas) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [по ключевым словам поиска вакансий](docs/suggests.md#vacancy-search-keyword) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />


<a name="salary"></a>
### Банк данных заработных плат

* [Отчёты Банка данных заработных плат](docs/salary_reports.md) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Оценка заработной платы без прогнозов](docs/salary_reports.md#salary-evaluation) <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
* [Справочники Банка данных заработных плат](docs/salary_dictionaries.md) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Отрасли](docs/salary_dictionaries.md#salary-industries) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Уровни специалистов](docs/salary_dictionaries.md#employee-levels) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Профобласти и специализации](docs/salary_dictionaries.md#professional-areas) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />
  * [Регионы и города](docs/salary_dictionaries.md#salary-areas) <img src="http://hhru.github.io/api/badges/anon.png" alt="anonymous" /> <img src="http://hhru.github.io/api/badges/client.png" alt="client" /> <img src="http://hhru.github.io/api/badges/app.png" alt="applicant" /> <img src="http://hhru.github.io/api/badges/emp.png" alt="employer" />


<a name="feedback"></a>
## Поддержка, обратная связь, новости

Общайтесь с нами через twitter [@apihhru](https://twitter.com/apihhru) или
через почту api@hh.ru.

Если вы нашли баг в работе HeadHunter API или
[виджетах](https://dev.hh.ru/admin/widgets), загляните в
[issues](https://github.com/hhru/api/issues), возможно, про него мы уже знаем и
чиним. Если нет, лучше всего сообщить о нём там. Там же вы можете оставлять свои
пожелания и предложения.

Если вы нашли проблему на одном из сайтов HeadHunter,
[напишите в поддержку по сайту](https://hh.ru/feedback) или в
[сообщество поддержки](https://feedback.hh.ru/).

За новостями вы можете следить по
[коммитам](https://github.com/hhru/api/commits/master) в этом репозитории.
[RSS](https://github.com/hhru/api/commits/master.atom).

Часто задаваемые вопросы собраны в [FAQ](docs/FAQ.md).
