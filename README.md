# Market Yönetim Sistemi

Bu proje, temel ve basit bir market yönetimi işlevlerini yerine getiren bir **Market Yönetim Sistemi** uygulamasıdır. Sistem, bir konsol tabanlı uygulama olarak tasarlanmış ve Türkçe dil desteği sunmaktadır. Kullanıcı dostu bir arayüzle, market yönetimi için gerekli olan temel işlemleri hızlı ve güvenli bir şekilde gerçekleştirmenizi sağlar.

---

## 📋 İçindekiler

- [Yönetici Girişi](#yönetici-girişi)

---

## 🚀 Özellikler

### **Admin Yönetimi**
- Admin giriş sistemi (kullanıcı adı/şifre kontrolü)
- Admin paneline özel erişim kontrolü
- Admin oturum yönetimi (giriş/çıkış)

### **Ürün Yönetimi**
- Ürün ekleme: Ad, kategori, fiyat, stok bilgileriyle ürün eklenebilir.
- Ürün listeleme: Tüm ürünler detaylı bir şekilde görüntülenebilir.
- Ürün silme: Ürünler ID bazlı olarak silinebilir.
- Ürün güncelleme: Fiyat ve stok bilgileri değiştirilebilir. (Yönetici Girişi ile aktif olur.)

### **Veri Saklama**
- Ürün bilgileri `product.txt` dosyasında saklanır.
- Veriler **CSV formatında** tutulur (virgülle ayrılmış değerler).
- Dosya işlemleri için hata yönetimi mevcuttur.

### **Veri Doğrulama**
- Fiyat ve stok değerlerinin sayısal olup olmadığının kontrolü.
- Boş alan kontrolü.
- Negatif değer kontrolü.
- Geçerli ürün ID doğrulaması.

### **Kullanıcı Arayüzü**
- Ana menü ve yönetici paneli menü sistemleri.
- Kullanıcı dostu konsol arayüzü.
- İşlem seçenekleri için numaralandırılmış menüler.

### **Güvenlik Özellikleri**
- Admin yetkisi gerektiren işlemler için kontrol mekanizması.
- Dosya işlemleri için `try-except` bloklarıyla hata yakalama.
- Veri girişi doğrulaması.

---

## ⚙️ Kurulum

1. **Proje Dosyasını İndirin:**
   ```
   git clone https://github.com/mreaktas/BasitMarketProje.git
   ```
2. **Gerekli Bağımlılıkları Yükleyin:**
   Proje için herhangi bir üçüncü taraf kütüphane gerekmemektedir. Python 3.x yeterlidir.

3. **Çalıştırma:**
   ```
   python marketproje.py
   ```

---

## 🛠️ Kullanım

1. Uygulama çalıştırıldığında bir **ana menü** görüntülenir.
2. Admin giriş yaparak özel işlemlere erişebilir.
3. Admin giriş yaptıktan sonra:
   - Yeni ürünler ekleyebilir.
   - Mevcut ürünleri listeleyebilir, güncelleyebilir veya silebilir.
4. Tüm işlemler kullanıcı dostu bir konsol arayüzü üzerinden yapılır.

---

## 🗂️ Dosya Yapısı ve Veri Saklama

- **`product.txt`**: 
  - Tüm ürün bilgileri burada CSV formatında saklanır.
  - Örnek format:
    ```
    1,Elma,Meyve,10.5,100
    2,Ekmek,Gıda,5.0,50
    ```
- **Hata Yönetimi**:
  - Dosya işlemlerinde hata oluşursa sistem, ilgili kullanıcıya bilgi verir ve işlem güvenliği sağlanır.

---

## 🔒 Güvenlik ve Doğrulama

1. **Admin Girişi**: 
   - Kullanıcı adı ve şifre kontrolü.
2. **Veri Doğrulama**:
   - Fiyat ve stok değerleri negatif olamaz.
   - Boş girişler kabul edilmez.
   - Geçersiz ürün ID’si kontrol edilir.

---

## 📖 Örnekler

### **Ürün Ekleme**
Kullanıcı aşağıdaki bilgileri girer:
```
Ürün Adı: Muz
Kategori: Meyve
Fiyat: 15.0
Stok: 50
```
**Sonuç**: `product.txt` dosyasına yeni ürün eklenir.

### **Ürün Güncelleme**
Kullanıcı ürün ID’sini girer ve güncellenmesi istenen bilgiyi sağlar:
```
Ürün ID: 1
Yeni Fiyat: 12.0
Yeni Stok: 80
```
**Sonuç**: Ürün bilgileri güncellenir.

### **Yönetici Girişi**
Yönetici kontrolüne bağlı olan işlemleri gerçekleştirebilmek için yönetici girişi yapmanız gerekmektedir.:
```
Kullanıcı Adı: Admin
Şifre: Admin
```
**Not**: Şifreleme için ek bir güvenlik veya şifreleme protokolü uygulanmamıştır.
