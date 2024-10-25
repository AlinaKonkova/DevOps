# Используем официальный образ Node.js
FROM node:18-alpine

# Устанавливаем рабочую директорию внутри контейнера
WORKDIR /app

# Копируем package.json и package-lock.json для установки зависимостей
COPY package*.json ./

# Устанавливаем зависимости
RUN npm install

# Копируем исходный код приложения Vue.js в контейнер
COPY . .

# Сборка приложения для production (если нужно)
RUN npm run build

# Открываем порт для взаимодействия (если нужно)
EXPOSE 8080

# Команда для запуска сервера разработки Vue
CMD ["npm", "run", "serve"]
