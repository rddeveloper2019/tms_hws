# tms_hws
```Создать HTTP-сервер на Node.js, который:
    - отдаёт статические файлы по запросу (например, .html, .css, .png)
    - логирует события (запросы, ошибки, успешную отдачу файлов)
    - использует EventEmitter для логирования
    
Используемые технологии:
    - Node.js (чистый, без фреймворков)
    - Модули: http, fs, path, events
    
Функционал сервера
Сервер должен:
    Обрабатывать HTTP-запросы на порт 3000
    Отдавать файлы из папки public/ (например: index.html, style.css)
    Если файл не найден — возвращать 404
    Работать с абсолютным путём (через path.join(__dirname, ...))
    Поддерживать хотя бы два формата файлов (любой из .html, .css, .js, .png, .jpg)
    
Логирование (через EventEmitter)
Реализовать модуль логгера на основе EventEmitter, который:
Подписывается на события:
   'request' — каждый HTTP-запрос
   'fileServed' — успешная отдача файла
   'notFound' — файл не найден
   'error' — ошибка сервера

Записывает логи в файл logs.log в едином формате, например
[2025-03-27T12:00:00.000Z] [fileServed] /index.html


project/
├── public/
│   ├── index.html (самый-самый простой)
├── logger.js  ← модуль с EventEmitter (который заимпортируется в server.js)
├── server.js  ← HTTP-сервер (http.createServer и т.д.)
└── server.log ← файл логов (создаётся автоматически)
```
