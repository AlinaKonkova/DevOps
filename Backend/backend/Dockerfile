# Используем официальный Python-образ
FROM python:3.12-slim

# Устанавливаем рабочую директорию внутри контейнера
WORKDIR /app

# Копируем файл requirements.txt (если у тебя его нет, можно пропустить этот шаг)
COPY requirements.txt .

# Устанавливаем зависимости через pip
RUN pip install --no-cache-dir -r requirements.txt

# Копируем весь код приложения в контейнер
COPY . .

# Открываем порт для взаимодействия (если нужно)
EXPOSE 8000

# Команда для запуска сервера FastAPI
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]
