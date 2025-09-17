<img width="1851" height="2347" alt="pm2panel" src="https://github.com/user-attachments/assets/4e967004-76d0-41cf-a64d-3b877fb36a70" /># Pm2 Manager - Tüm işlemler tek dosyada!
PM2 Manager ile çalıştırdığınız pm2'ye bağlı sistemlerinizi detaylı olarak görüntüleyip, pm2 ile yapabileceğiniz tüm işlemleri uzaktan yapabilirsiniz. Ayrıca editör sayesinde kod dosyalarınızı online olarak yönetebilirsiniz.
<img width="1851" height="2347" alt="pm2panel" src="https://github.com/user-attachments/assets/8bf3b354-f60c-4a5f-8a51-8e96ef3d94b4" />


# 💣 Özellikler

### Ana Panel
- ✅ **Modern UI**: Koyu tema ile profesyonel görünüm
- ✅ **Real-time monitoring**: Socket.IO ile canlı takip
- ✅ **Process yönetimi**: Başlat, durdur, yeniden başlat, sil
- ✅ **Detaylı görünüm**: Her process için kapsamlı bilgiler
- ✅ **Responsive tasarım**: Mobil ve desktop uyumlu

### PM2 Entegrasyonu
- ✅ **Multi-app yönetimi**: Birden fazla uygulamayı tek yerden
- ✅ **Otomatik restart**: Crash durumunda otomatik yeniden başlatma
- ✅ **Log yönetimi**: Merkezi log takibi (helpers/logs altında)
- ✅ **Resource monitoring**: CPU, RAM kullanımı takibi

## 🌐 Erişim

- **Ana Panel**: http://localhost:3000
- **Dashboard**: http://localhost:3000/dashboard
- **Login**: http://localhost:3000/auth/login
- **Ornek1**: http://localhost:3001
- **Ornek2**: http://localhost:3002

## 🔐 Giriş Bilgileri

- **Kullanıcı adı**: `admin`
- **Şifre**: `1234`

## 📊 Monitoring

### Dashboard
- Process listesi ve durumları
- CPU ve RAM kullanımı
- Uptime ve restart sayıları
- Canlı log takibi

### Process Detayları
- Detaylı process bilgileri
- Sistem metrikleri
- Environment variables
- Raw PM2 data

## 🚨 Hata Ayıklama

### Log Dosyaları
- `src/_main_panel/helpers/logs/_main_panel.log`: Ana panel logları
- `src/_main_panel/helpers/logs/ornek1.log`: Ornek1 uygulama logları
- `src/_main_panel/helpers/logs/ornek2.log`: Ornek2 uygulama logları

## 🚀 Kurulum

```bash
# Bağımlılıkları yükle
npm install

# PM2 ile tüm uygulamaları başlat
npm run pm2:start

# Sadece ana paneli başlat
npm start

# Geliştirme modunda çalıştır
npm run dev
```

## 🏗️ Proje Yapısı

```
pm2-controller/
├── src/                    # 🎯 Tüm uygulamalar burada
│   ├── _main_panel/       # Ana PM2 Control Panel
│   │   ├── server.js      # Express server
│   │   ├── src/           # Routes ve Views
│   │   ├── helpers/       # Middleware ve utilities
│   │   │   └── logs/      # PM2 log dosyaları
│   │   └── public/        # CSS, JS ve statik dosyalar
│   ├── ornek1/            # Birinci test uygulaması
│   │   └── app.js         # Test uygulaması (Port 3001)
│   └── ornek2/            # İkinci test uygulaması
│       └── app.js         # Test uygulaması (Port 3002)
├── ecosystem.config.js     # ⚙️ PM2 konfigürasyonu
└── package.json            # 📦 Proje bağımlılıkları
```

## 🔄 Geliştirme

### Yeni Uygulama Ekleme
1. `src/` altında yeni klasör oluştur (örn: `ornek3/`)
2. `app.js` dosyası ekle
3. `ecosystem.config.js`'e ekle
4. PM2 ile başlat

### Örnek Yapı
```javascript
// src/ornek3/app.js
const http = require('http');
const server = http.createServer((req, res) => {
  // Uygulama kodları
});
server.listen(process.env.PORT || 3003);
```

## 📝 Lisans

MIT License - Detaylar için `LICENSE` dosyasına bakın.








