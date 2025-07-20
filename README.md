# t4-back

NestJS API приложение для управления пользователями с JWT аутентификацией.

## Функциональность

- 🔐 JWT аутентификация с cookie
- 👥 CRUD операции с пользователями
- 📚 Swagger документация
- 🛡️ Валидация данных
- 🍪 Session management

## Технологии

- NestJS
- TypeScript
- JWT
- Swagger/OpenAPI
- Class Validator
- Express Session

## Локальная разработка

### Установка зависимостей

```bash
npm install
```

### Запуск в режиме разработки

```bash
npm run start:dev
```

### Сборка проекта

```bash
npm run build
```

### Запуск production версии

```bash
npm run start:prod
```

## API Endpoints

### Аутентификация

- `POST /api/v1/auth/login` - Вход в систему
- `POST /api/v1/auth/logout` - Выход из системы
- `GET /api/v1/auth/me` - Получить текущего пользователя

### Пользователи

- `GET /api/v1/users` - Получить всех пользователей
- `POST /api/v1/users` - Создать пользователя
- `GET /api/v1/users/:id` - Получить пользователя по ID
- `PATCH /api/v1/users/:id` - Обновить пользователя
- `DELETE /api/v1/users/:id` - Удалить пользователя

## Swagger документация

Доступна по адресу: `/api`

## Переменные окружения

- `NODE_ENV` - Режим работы (production/development)
- `JWT_SECRET` - Секретный ключ для JWT токенов
- `FRONTEND_URL` - URL фронтенд приложения для CORS
- `PORT` - Порт приложения (по умолчанию 4000)

## Деплой на Vercel

### 1. Подготовка проекта

Проект уже настроен для деплоя на Vercel с:

- `vercel.json` - конфигурация Vercel
- `api/index.ts` - точка входа для serverless функций

### 2. Установка Vercel CLI

```bash
npm i -g vercel
```

### 3. Деплой

```bash
vercel
```

### 4. Настройка переменных окружения в Vercel

В панели Vercel добавьте:

- `JWT_SECRET=your-super-secret-jwt-key`
- `FRONTEND_URL=https://your-frontend-domain.com`

## Тестовые данные

По умолчанию создается администратор:

- Email: `admin@inno.tech`
- Password: `admin`

## Команды для тестирования

### Запуск тестов

```bash
npm run test
```

### Запуск e2e тестов

```bash
npm run test:e2e
```

### Проверка покрытия

```bash
npm run test:cov
```
