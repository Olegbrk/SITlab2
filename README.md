# Концептуальная модель

![](/концептуальная_модель.png)

На основе анализа предметной области "Блог", были выделены следующие информационные объекты, которые необходимо хранить в базе данных:

1. Автор (user):
    - user_id (bigint, PK) - идентификатор пользователя
    - user_name (varchar(30)) - имя пользователя
    - user_password (varchar(30)) - пароль пользователя
2. Статья (article):
    - article_id (bigint, PK) - идентификатор статьи
    - article_name (varchar(255)) - название статьи
    - article_text (varchar(5000)) - текст статьи
    - article_date(timestamp) - дата публикации статьи
    - category_id(bigint, FK) - внешний ключ для связи с таблицей "category"
    - author_id (bigint, FK) - внешний ключ для связи с таблицей "user" 
3. Комментарий (comment):
    - comment_id (bigint, PK) - идентификатор комментария
    - comment_text (varchar(255)) - текст комментария
    - comment_date (timestamp) - дата публикации комментария
    - user_id (bigint, FK) - внешний ключ для связи с таблицей "user"
    - article_id (bigint, FK) - внешний ключ для связи с таблицей "article"
4. Категория статьи (category):
    - category_id (bigint, PK) - идентификатор категории
    - category_name (varchar(100)) - название категории
    - category_description(varchar(255)) - описание категории

# Логическая модель

На основе концептуальной модели, была построена логическая модель базы данных

![](/логическая_модель.png)
