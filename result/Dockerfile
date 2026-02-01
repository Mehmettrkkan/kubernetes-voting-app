# Stage 1: Build Stage (Derleme)
FROM node:18-slim AS build-env
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production

# Stage 2: Distroless Runtime (Güvenli, Shell yok)
FROM gcr.io/distroless/nodejs18-debian11
COPY --from=build-env /app/node_modules /app/node_modules
COPY . /app
WORKDIR /app
EXPOSE 80
CMD ["server.js"]
