# beu_blog
# BEUBlog - MERN Stack Blog Platform

BEUBlog, modern web teknolojileri kullanılarak geliştirilmiş tam yığin (full-stack) bir blog platformudur. Kullanıcıların kayıt olup giriş yapabileceği, kendi blog yazılarını oluşturabileceği ve düzenleyebileceği, aynı zamanda diğer kullanıcıların yazılarını okuyabileceği zengin içerikli bir sistem sunar.

##  Özellikler

- **Kullanıcı Kimlik Doğrulaması:** JWT (JSON Web Tokens) tabanlı güvenli kayıt olma ve giriş yapma sistemi.
- **Kullanıcı Yetkilendirmesi:** Admin ve standart kullanıcı rolleri.
- **Dinamik Blog Yönetimi:** Yazı (post) oluşturma, düzenleme, silme ve okuma işlemleri (CRUD).
- **Zengin Metin Editörü:** React Quill entegrasyonu ile yazılarınızı zenginleştirilmiş metin (kalın, italik, liste, bağlantı vb.) formatında oluşturma imkanı.
- **Görsel Yükleme:** Blog yazıları için kapak fotoğrafı yükleme özelliği (Multer ve yerel dosya sistemi ile).
- **Kategori Sistemi:** Yazıları belirli kategoriler altında gruplandırma.
- **Karanlık/Aydınlık Mod (Dark/Light Theme):** Kullanıcı tercihine göre değişebilen modern arayüz tasarımı.
- **Duyarlı (Responsive) Tasarım:** Mobil, tablet ve masaüstü cihazlarla tam uyumlu kullanıcı deneyimi.
- **Kullanıcı Paneli (Dashboard):** Kullanıcıların kendi detaylarını ve paylaştıkları yazıları yönetebildiği özel kontrol paneli.

##  Kullanılan Teknolojiler

### Frontend (İstemci Tarafı)
- **[React.js](https://reactjs.org/):** Kullanıcı arayüzünü oluşturmak için kullanılan JavaScript kütüphanesi.
- **[Vite](https://vitejs.dev/):** Hızlı geliştirme ortamı ve modern derleme aracı.
- **[React Router DOM](https://reactrouter.com/):** Sayfa yönlendirmeleri (routing) için.
- **[Axios](https://axios-http.com/):** HTTP istekleri göndermek için.
- **[Lucide React](https://lucide.dev/):** Modern vektörel ikonlar için.
- **[React Quill](https://github.com/zenoamaro/react-quill):** Zengin metin editörü.

### Backend (Sunucu Tarafı)
- **[Node.js](https://nodejs.org/) & [Express.js](https://expressjs.com/):** Sunucu altyapısı ve RESTful API oluşturmak için.
- **[MongoDB](https://www.mongodb.com/) & [Mongoose](https://mongoosejs.com/):** Veritabanı yönetimi ve obje/model eşleme.
- **[JSON Web Tokens (JWT)](https://jwt.io/):** Güvenli oturum yönetimi ve kimlik doğrulama için.
- **[Bcrypt.js](https://www.npmjs.com/package/bcryptjs):** Kullanıcı parolalarını güvenli bir şekilde şifrelemek için.
- **[Multer](https://github.com/expressjs/multer):** Dosya ve görsel yükleme işlemleri için.

##  Proje Yapısı

\`\`\`bash
beublog/
├── backend/                  # Node.js / Express sunucu klasörü
│   ├── config/               # Veritabanı yapılandırması
│   ├── controllers/          # İstek - yanıt mantığını işleyen kontrolcüler
│   ├── middleware/           # Kimlik doğrulama ve hata kontrolü ara yazılımları
│   ├── models/               # MongoDB veri şablonları (User, Post, Category, vb.)
│   ├── routes/               # API yönlendirme tanımları
│   ├── uploads/              # Yüklenen kapak görselleri dizini
│   └── server.js             # Sunucu başlatma dosyası
│
└── frontend/                 # React (Vite) istemci klasörü
    ├── src/
    │   ├── assets/           # Statik dosyalar
    │   ├── components/       # Tekrar kullanılabilen React bileşenleri
    │   ├── context/          # React Context API dosyaları (AuthContext vb.)
    │   ├── pages/            # Ana sayfa görünümleri (Home, Login vb.)
    │   └── App.jsx           # Ana React bileşeni ve Router tanımları
    └── index.html            # Ana HTML şablonu
\`\`\`

## 🛠️ Kurulum ve Çalıştırma

Projeyi kendi bilgisayarınızda çalıştırmak için aşağıdaki adımları izleyin.

### Ön Koşullar
- Node.js (Sürüm 16 veya üzeri)
- MongoDB (Yerel kurulum veya Atlas bulut hesabı)

### 1. Depoyu Klonlayın
\`\`\`bash
git clone https://github.com/nazareylulsayinda/beu_blog.git
cd beu_blog
\`\`\`

### 2. Backend Ayarları
1. \`backend\` klasörüne gidin: \`cd backend\`
2. Paketleri yükleyin: \`npm install\`
3. Backend dizininde \[.env\](cci:7://file:///c:/Users/Acer/Documents/Web%20tabanl%C4%B1%20%C3%B6dev/beublog/backend/.env:0:0-0:0) adında dosya oluşturup aşağıdaki değişkenleri tanımlayın:
   \`\`\`env
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/blogdb
   JWT_SECRET=super_gizli_anahtariniz
   \`\`\`
4. Sunucuyu başlatın: \`npm run dev\`

### 3. Frontend Ayarları
1. \`frontend\` klasörüne gidin: \`cd frontend\`
2. Paketleri yükleyin: \`npm install\`
3. Arayüzü başlatın: \`npm run dev\`

Tarayıcınızdan \`http://localhost:5173\` adresine giderek siteyi görebilirsiniz.
