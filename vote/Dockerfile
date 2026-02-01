# Stage 1: Build Stage (Derleme)
FROM python:3.11-slim AS build-env
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt -t /app/lib

# Stage 2: Runtime Stage (Distroless - Güvenli)
FROM gcr.io/distroless/python3-debian11
COPY --from=build-env /app/lib /site-packages
COPY . /app
WORKDIR /app
# Python kütüphanelerini tanıtıyoruz
ENV PYTHONPATH=/site-packages
CMD ["app.py"]
