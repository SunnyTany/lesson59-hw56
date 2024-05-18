# RESTful Api & NODE.JS & EXPRESS.JS

Для початку роботи потребуэться встановити бібліотеку Express 

npm i express

Для тестування запитів в режимі розробки допоможе nodemon

npm i -D nodemon

- cервер (app) виконаний за допомогою Node.js та Express.js, 
- реагує на url та метод у запиті за допомогою use
- прослуховується методом listen, де первим параметром є порт, а другим callback

Кожен окремий маршрут оброблються згідно методу запиту та певним колбеком, в якому описані дії на сервері в цьому випадку (логування певної інформації):

Головний маршрут: /:
  метод:
    - GET: клієнту повертає "Get root route".


Маршрут для користувачів: /users: 
  методи:
    - GET: клієнту повертає "Get users route".
    - POST: клієнту повертає "Post users route".

Маршрут для окремого користувача: /users/:userId: 
  методи:
    - для отримання GET: клієнту повертає "Get user by Id route: {userId}".
    - для оновлення PUT: клієнту повертає "Put user by Id route: {userId}".
    - для видалення DELETE: клієнту повертає "Delete user by Id route: {userId}".

Маршрут для статей: /articles: 
  методи:
    - для отримання - GET: клієнту повертає "Get articles route".
    - для відправлення - POST: клієнту повертає "Post articles route".

Маршрут для конкретної статті: /articles/:articleId: 
  методи:
    - для отримання - GET: клієнту повертає "Get article by Id route: {articleId}".
    - для оновлення - PUT: клієнту повертає "Put article by Id route: {articleId}".
    - для видалення - DELETE: клієнту повертає "Delete article by Id route: {articleId}".

Код розподілений на логіку виконання (controllers) та опис маршрутів (routes). 
