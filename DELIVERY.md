# OpenAPI Tasarımı Ödevi Teslim Raporu

## 👤 Öğrenci Bilgileri
- **Ad Soyad**: Saniye Ece Kaya
- **Öğrenci Numarası**: 170422051

---

## 📂 OpenAPI YAML Dosyası

- **openapi.yaml** dosyasını projenizin GitHub reposuna yükledim.
- Swagger Editor ile test edildi ve doğrulandı.

### 🔗 GitHub Repo Linki
[[https://github.com/username/library-api](https://github.com/username/library-api)](https://github.com/ecekaya1/OpenAPI-ile-REST-API-Tasar-m-/tree/main)

## 📝 API Açıklaması

Bu API, üniversitenin çevrim içi kütüphane sistemi için tasarlanmıştır. Üç ana varlık yer almaktadır:

- **books**: Kitaplar için CRUD işlemleri
- **students**: Öğrenciler için CRUD işlemleri
- **loans**: Ödünç alma ve kitap iade etme işlemleri

**CRUD işlemleri ve endpoint’ler:**
- **books**:
  - `GET /books` (sayfalama destekli)
  - `GET /books/{id}`
  - `POST /books`
  - `PUT /books/{id}`
  - `DELETE /books/{id}`
- **students**:
  - `GET /students`
  - `GET /students/{id}`
  - `POST /students`
  - `PUT /students/{id}`
  - `DELETE /students/{id}`
- **loans**:
  - `GET /loans`
  - `GET /loans/{id}`
  - `POST /loans`
  - `PATCH /loans/{id}/return`

**components/schemas** kısmında tüm veri modelleri tanımlandı. `parameters` bölümünde path ve query parametreleri, `responses` kısmında ise 200, 201, 400, 404 ve 500 yanıtları örneklerle yer aldı. Ayrıca:

- **Sayfalama**: `GET /books` endpoint’inde `page` ve `size` query parametreleri tanımlandı.
- **Hata yönetimi**: `400`, `404` ve `500` durumları için örnek yanıtlar hazırlandı.
- **Example**: `POST /books` ve `POST /students` gibi endpoint’lerde örnek istek gövdeleri (`example`) kullanıldı.
- Açıklayıcı `description` ve `tags` eklendi.

---

## 🧪 Test Notları (Opsiyonel)

Swagger Editor üzerinden test edildi:
- `GET /books` çağrısı, sayfalama parametreleriyle birlikte kitap listesini JSON formatında döndürüyor.
- `POST /students` için örnek istek:
```json
{
  "name": "Ali Veli",
  "studentNumber": "20231234",
  "email": "ali.veli@example.com",
  "isActive": true
}
