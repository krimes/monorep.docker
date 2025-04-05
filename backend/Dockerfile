# Dockerfile
FROM oven/bun

EXPOSE 3000

WORKDIR /backend

COPY package*.json ./
RUN bun i

COPY . /backend

# запускаем скрипт генерации
CMD ["bun", "start"]