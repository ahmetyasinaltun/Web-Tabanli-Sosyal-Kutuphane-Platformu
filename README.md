# Sosyal Kütüphane Platformu

Kullanıcıların kitapları ve filmleri keşfetmesini, paylaşmasını ve takip etmesini sağlayan modern bir web uygulaması. Bu platform; kullanıcıların birbirini takip etmesi, okuma aktivitelerini izlemesi ve kişisel kütüphanelerini yönetmesi gibi sosyal özellikler sunar.

## Özellikler

- **Kullanıcı Kimlik Doğrulama**: JWT (JSON Web Token) kullanarak güvenli giriş ve kayıt sistemi.
- **İçerik Keşfi**: Kitap ve film içeriklerini arama ve listeleme.
- **Kişisel Kütüphaneler**: Kullanıcılar kendi koleksiyonlarını (listelerini) oluşturabilir ve yönetebilir.
- **Sosyal Etkileşim**: Diğer kullanıcıları takip etme ve son aktivitelerini akışta görme.
- **Aktivite Takibi**: Okuma ilerlemesini kaydetme ve durum güncellemeleri paylaşma.
- **Profil Yönetimi**: Özelleştirilebilir kullanıcı profilleri.

## Teknoloji Yığını (Tech Stack)

### Frontend (Önyüz)
- **React**: Arayüz geliştirme kütüphanesi.
- **Vite**: Hızlı ve modern frontend geliştirme aracı.
- **Tailwind CSS**: Utility-first CSS çatısı.
- **React Router**: Sayfa yönlendirmeleri için.
- **Lucide React**: İkon seti.

### Backend (Arka Uç)
- **Node.js & Express**: Sunucu tarafı çalışma zamanı ve web çatısı.
- **PostgreSQL**: İlişkisel veritabanı.
- **Sequelize**: Node.js için ORM (Object-Relational Mapping).
- **JWT**: Güvenli kimlik doğrulama için.

## Kullanılan API ve Servisler

Bu proje, kullanıcılara zengin içerik sunmak ve temel fonksiyonları yerine getirmek için aşağıdaki harici servislerden yararlanır:

- **Google Books API**: Kitap arama, detay bilgileri ve kapak görselleri için kullanılır.
- **TMDB (The Movie Database) API**: Film verileri, açıklamalar ve posterler için kullanılır.
- **Gmail SMTP**: Kayıt olma, şifre sıfırlama vb. durumlarda e-posta bildirimleri göndermek için kullanılır.

## Kurulum ve Başlangıç

### Gereksinimler
- Node.js (v16 veya üzeri)
- PostgreSQL Veritabanı

### Kurulum Adımları

1. **Projeyi Klonlayın**
   ```bash
   git clone <repository-url>
   cd social-library-platform
   ```

2. **Frontend Kurulumu**
   ```bash
   # Bağımlılıkları yükleyin
   npm install

   # Geliştirme sunucusunu başlatın
   npm run dev
   ```

3. **Backend Kurulumu**
   ```bash
   cd backend

   # Bağımlılıkları yükleyin
   npm install

   # Ortam Değişkenlerini Ayarlayın
   # backend klasörü içinde .env adında bir dosya oluşturun ve aşağıdaki değişkenleri ekleyin:
   # DB_NAME=veritabani_adiniz
   # DB_USER=veritabani_kullanici_adiniz
   # DB_PASSWORD=veritabani_sifreniz
   # DB_HOST=localhost
   # JWT_SECRET=gizli_jwt_anahtariniz
   # EMAIL_USER=email_adresiniz
   # EMAIL_PASS=email_sifreniz

   # Backend sunucusunu başlatın
   npm run dev
   ```

Uygulama artık çalışıyor olmalıdır. Frontend varsayılan olarak `http://localhost:5173`, backend ise `http://localhost:5000` adresinde çalışacaktır.

## Proje Yapısı

```
├── backend/                 # Node.js/Express Backend Klasörü
│   ├── config/             # Veritabanı ve genel ayarlar
│   ├── controllers/        # İstekleri karşılayan fonksiyonlar (Controller)
│   ├── middleware/         # Ara katman yazılımları (Auth, Upload vb.)
│   ├── models/             # Veritabanı modelleri (Sequelize)
│   ├── routes/             # API rotaları
│   └── utils/              # Yardımcı fonksiyonlar
├── src/                    # React Frontend Klasörü
│   ├── components/         # Tekrar kullanılabilir UI bileşenleri
│   ├── pages/              # Sayfa bileşenleri
│   ├── services/           # API servis çağrıları
│   └── data/               # Mock veriler ve sabitler
```

## Katkıda Bulunma

1. Projeyi Fork'layın
2. Yeni bir özellik dalı (branch) oluşturun (`git checkout -b feature/YeniOzellik`)
3. Değişikliklerinizi commit yapın (`git commit -m 'Yeni özellik eklendi'`)
4. Dalınızı (branch) push yapın (`git push origin feature/YeniOzellik`)
5. Bir Pull Request oluşturun
