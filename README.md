# Bahçeli Köyü — Web Sitesi

Ürgüp / Nevşehir, Kapadokya'daki Bahçeli Köyü için tek sayfalık, iki dilli (TR/EN) tanıtım sitesi.
Derleme (build) gerektirmez; doğrudan GitHub Pages'te yayınlanır.

## Dosya yapısı

```
bahceli-koyu/
├── index.html      ← Sitenin tamamı (HTML + CSS + JS gömülü)
├── images/         ← Fotoğraflarınız buraya
│   ├── hero.jpg
│   ├── galeri-01.jpg
│   └── ...
└── README.md
```

## 1. Görselleri ekleme

1. `images/` adında bir klasör oluşturun ve fotoğraflarınızı içine kopyalayın.
2. **Kapak (hero) görseli:** `index.html` içinde `.hero` bölümündeki `background:` satırını
   şununla değiştirin:
   ```css
   background:
     linear-gradient(180deg,rgba(26,19,14,0.18) 0%,rgba(26,19,14,0.55) 70%,rgba(26,19,14,0.78) 100%),
     url('images/hero.jpg');
   ```
3. **Galeri:** Galeri bölümündeki her `<figure>` kutusunun içini şununla değiştirin:
   ```html
   <figure><img src="images/galeri-01.jpg" alt="Açıklama"><figcaption>Açıklama</figcaption></figure>
   ```
   İstediğiniz kadar `<figure>` ekleyip çıkarabilirsiniz.

> İpucu: Fotoğrafları yüklemeden önce genişliğini ~1600 px'e küçültün; site hızlı açılır.

## 2. Metinleri düzenleme

Her metin iki dilde yazılı: `data-tr="..."` Türkçe, `data-en="..."` İngilizce.
İkisini de güncelleyin. Görünen metni de aynı yapın. Örnek:
```html
<h2 data-tr="Yeni başlık" data-en="New title">Yeni başlık</h2>
```
`XX`, `(eklenecek)` ve `ornek@eposta.com` gibi yer tutucuları kendi bilgilerinizle değiştirin
(mesafeler, telefon, e-posta, muhtarlık vb.).

## 3. GitHub Pages'te yayınlama

1. GitHub'da yeni bir **public** repo açın (ör. `bahceli-koyu`).
2. `index.html`, `README.md` ve `images/` klasörünü repoya yükleyin (sürükle-bırak ya da `git push`).
3. Repo → **Settings → Pages**.
4. **Source:** `Deploy from a branch` → **Branch:** `main` → **/(root)** → **Save**.
5. Birkaç dakika sonra site şu adreste yayında olur:
   `https://KULLANICIADINIZ.github.io/bahceli-koyu/`

### Kendi alan adınızı bağlamak (opsiyonel)
Settings → Pages → **Custom domain** alanına alan adınızı yazın ve alan adı sağlayıcınızda
bir `CNAME` kaydı oluşturun.

---
Sorular ve eklemeler için site üzerinde birlikte çalışmaya devam edebiliriz.

## Yapı görselleri — dosya adları

Her yapı kartı için bir kapak fotoğrafı bekleniyor. Fotoğrafları aşağıdaki adlarla `images/` klasörüne koyun; kartlardaki yer tutucu kutu zaten bu adı gösteriyor:

| # | Yapı | Dosya adı |
|---|------|-----------|
| 01 | İki Damönü Kilisesi | `images/01-dam-onu-kilisesi.jpg` |
| 02 | Ali Bağı Kilisesi | `images/02-ali-bagi-kilisesi.jpg` |
| 03 | Gülistan Kilisesi | `images/03-gulistan-kilisesi.jpg` |
| 04 | İçeridere Kilisesi | `images/04-iceridere-kilisesi.jpg` |
| 05 | Bukalemun Kayası | `images/05-bukalemun-kayasi.jpg` |
| 06 | Gavur Deresi | `images/06-gavur-deresi.jpg` |
| 07 | Kırk Guğle | `images/07-kirk-gugle.jpg` |
| 08 | Su Tünelleri | `images/08-su-tunelleri.jpg` |
| 09 | Eski Bahçeli Köyü | `images/09-eski-bahceli-koyu.jpg` |
| 10 | Mamasun Vadisi | `images/10-mamasun-vadisi.jpg` |
| 11 | Mamasun Vadisi Çiçekleri | `images/11-mamasun-cicekleri.jpg` |
| 12 | Anıt Mezar | `images/12-anit-mezar.jpg` |
| 13 | Acı Su | `images/13-aci-su.jpg` |
| 14 | Ala Kilise | `images/14-ala-kilise.jpg` |
| 15 | Osman Efendi Camii | `images/15-osman-efendi-camii.jpg` |
| 16 | Büyük Oluk Kilisesi | `images/16-buyuk-oluk-kilisesi.jpg` |

Hazır olduğunda fotoğrafları bana iletin; kartlardaki yer tutucuları gerçek `<img>` etiketleriyle değiştireyim.

> Durum: Tüm görseller yerleştirildi (16 yapı + kapak). Bir fotoğrafı değiştirmek için
> `images/` klasöründeki ilgili dosyanın üzerine aynı adla yenisini koymanız yeterli.
