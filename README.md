## Описание проекта

Проект разворачивает полноценную блог-платформу WordPress с использованием MySQL в качестве базы данных и Redis для кэширования. Все сервисы запускаются в Docker-контейнерах с использованием Docker Compose.

## Технологический стек

- **WordPress 6.5** — CMS для блога
- **MySQL 8.0** — реляционная база данных
- **Redis 7-alpine** — система кэширования
- **Docker Compose** — оркестрация контейнеров
## Требования

- Установленный Docker и Docker Compose
- Порт 8080 должен быть свободен

## Инструкция по запуску

### 1. Клонируйте репозиторий

```{bash}
git clone https://github.com/florenskaial118/docker-compose-assignment.git
cd docker-compose-assignment
```

2. Настройте переменные окружения

```{bash}
cp .env.example .env
# Отредактируйте .env при необходимости (пароли и настройки)
```

3. Запустите проект

```{bash}
docker compose up -d
```

4. Проверьте статус контейнеров

```{bash}
docker compose ps
```

5. Откройте WordPress в браузере

```{text}
http://localhost:8080
```
6. Остановка и очистка

```{bash}
# Остановка контейнеров
docker compose down

# Остановка с удалением томов (удаляет все данные)
docker compose down -v
```