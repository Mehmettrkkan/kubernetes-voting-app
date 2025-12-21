# Kubernetes Voting App (Microservices) 🗳️

Bu proje, Kubernetes üzerinde çalışan çok katmanlı (Microservices) bir oylama uygulamasıdır.

## Mimari
* **Frontend:** Python (Kullanıcı oylama ekranı)
* **Backend:** Redis (Geçici hafıza - Queue)
* **Worker:** .NET (Veri işleyici)
* **DB:** PostgreSQL (Kalıcı veritabanı - Persistent Volume)
* **Result:** Node.js (Sonuç ekranı)

## Kurulum
Dosyalar `k8s-manifests` klasörü altındadır.
