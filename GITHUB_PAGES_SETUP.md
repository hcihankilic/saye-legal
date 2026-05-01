# GitHub Pages Kurulum Talimatı

`saye-legal` adında public bir repo aç ve bu klasörü içine push'la. ~2 dakika içinde live olur.

## Adımlar

### 1. GitHub'da yeni public repo oluştur
Browser: <https://github.com/new>
- Repository name: **saye-legal**
- Visibility: **Public**
- Initialize: hiçbirini işaretleme (boş repo)
- "Create repository"

### 2. legal/ klasörünü ayrı bir git deposu olarak push'la

```bash
cd /Users/cihan.kilic/Desktop/Uygulama/Saye/Saye/legal
git init
git add .
git commit -m "initial: privacy policy + terms of use"
git branch -M main
git remote add origin https://github.com/hcihankilic/saye-legal.git
git push -u origin main
```

### 3. GitHub Pages'i aktif et
Browser: <https://github.com/hcihankilic/saye-legal/settings/pages>
- Source: **Deploy from a branch**
- Branch: **main** · Folder: **/ (root)**
- Save

### 4. URL'leri doğrula
~2 dakika sonra şu URL'ler aktif olur:

- <https://hcihankilic.github.io/saye-legal/>
- <https://hcihankilic.github.io/saye-legal/privacy-policy.html>
- <https://hcihankilic.github.io/saye-legal/terms-of-use.html>

App Store Connect'te Privacy Policy URL alanına `privacy-policy.html` adresini gir.

## Güncelleme Akışı

İçeriği güncellemek için:

```bash
cd /Users/cihan.kilic/Desktop/Uygulama/Saye/Saye/legal
# dosyaları düzenle
git add .
git commit -m "update: <ne değişti>"
git push
```

GitHub Pages 1-2 dakika içinde yeni içeriği yayına alır.

## Custom Domain (Opsiyonel)

Kendi domain'in varsa (örn. `saye.app`):
1. DNS'te `legal.saye.app` için CNAME → `hcihankilic.github.io`
2. Repo Settings → Pages → Custom domain → `legal.saye.app` → Save
3. "Enforce HTTPS" işaretle
