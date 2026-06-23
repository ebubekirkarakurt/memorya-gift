# Memorya Gift

> Kişiye özel hediye tasarım ve sipariş platformu.

Anlık canlı tasarım editörü, güvenli ödeme altyapısı ve otomatik baskı varlığı (print asset) üretimi sunan, uçtan uca geliştirilmiş bir e-ticaret platformu.

🌐 **Canlı:** [memoryagift.com](https://memoryagift.com)

---

## 🚀 Özellikler

- **Canlı Tasarım Editörü** — Kullanıcı fotoğraf yükler, metin girer; sonucu anlık önizler. `html-to-image` ile baskıya hazır yüksek çözünürlüklü PNG çıktısı üretilir ve siparişe eklenir.

- **3D Kupa Önizlemesi** — Three.js ile gerçek zamanlı 3D kupa render. Kullanıcı tasarımını kupaya texture olarak görebiliyor; kamerayı döndürebiliyor.

- **Fabric.js Editörü** — Kupa ürünleri için canvas tabanlı tasarım editörü. Katman yönetimi, metin, emoji ve görsel ekleme destekleniyor.

- **Güvenli Ödeme Akışı** — iyzico entegrasyonu ile 3D Secure destekli ödeme. Sipariş oluşturma → ödeme başlatma → callback doğrulama zinciri backend üzerinden yönetiliyor. Duplicate callback ve başarısız ödemeler otomatik temizleniyor.

- **Fotoğraf Yönetimi** — Müşterinin yüklediği görseller private Supabase Storage'a kaydediliyor. Signed URL sistemi ile güvenli erişim. Admin, sipariş detayından tüm fotoğraflara doğrudan ulaşıp indirebiliyor.

- **Admin Paneli** — Sipariş takibi, aşama yönetimi, kargo girişi ve otomatik kargo bildirimi. Finans dashboard'u ile aylık gelir/gider analizi ve ürün bazlı kar marjı hesaplama.

- **Otomatik E-posta Bildirimleri** — Resend API ile sipariş onayı, ödeme doğrulama ve kargo bildirimi mailleri otomatik gönderiliyor.

- **SEO** — Her ürün sayfasına özel meta tag, Open Graph, Twitter Card ve JSON-LD structured data. Google Analytics ve Search Console entegrasyonu.

---

## 🛠 Tech Stack

### Frontend
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)


### Backend & Altyapı
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-1C1C1C?style=for-the-badge&logo=supabase&logoColor=3ECF8E)

**Üçüncü Parti:** iyzico (Ödeme), Resend (E-posta), Render.com (Hosting)

---

## 📐 Sistem Mimarisi

```
[ İstemci (React + Vite) ]
          │  HTTPS / REST
          ▼
[ Express.js API (Render.com) ]
          │
          ├──► [ PostgreSQL & Storage (Supabase) ]
          │         └── Siparişler, ürünler, müşteri fotoğrafları
          │
          ├──► [ iyzico Payment Gateway ]
          │         └── 3D Secure, callback doğrulama
          │
          └──► [ Resend API ]
                    └── Sipariş, ödeme, kargo mailleri
```

---

---

## 📸 Ekran Görüntüleri

> Siteyi ziyaret edebilirsiniz -> [memoryagift.com](https://memoryagift.com)

---

## Durum

✅ Aktif olarak yayında — gerçek kullanıcı siparişleri alınıyor
