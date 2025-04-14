Области хранения данных:

- база данных на JSON-server
- BFF
- редакс стор

Сущности приложения:

- пользователь: БД (список пользователей), BFF (сессия текущего пользователя), стор (отображение в браузере)
- роль пользователя: БД (список ролей), BFF (сессия пользоваеля с ролью), стор (использование на клиенте)
- статья: БД (список статей), стор (отображение в браузере)
- комментарии: БД (список комментариев), стор (отображение в браузере)

Таблицы БД:

- пользователи - users: id / login / password / registed_at / role_id
- роли - roles: id / name
- статьи - posts: id / title / image_url / content / published_at
- комментарии - comments: id / author_id / post_id / content

Схема состояния на BFF:

- сессия текущего пользователя: login / password / role

Схема для редакс стор (на клиенте):

- user: id / login / roleId
- posts: массив post: id / title / imageURL / publishedAt / commentsCount
- post: id / title / imageURL / content /publishedAt / comments: массив comment: id / author / content / publishedAt
- users: массив user: id / login / registeredAr / role
