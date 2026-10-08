# Hostkap landing

[hostkap.dev](https://hostkap.dev/) için tek dosyalık statik açılış sayfası. Derleme adımı yoktur.

## Dosyalar
- `public/index.html`: Sayfanın tamamı (fontlar ve scriptler içine gömülü), SEO / Open Graph etiketleri dahil.
- `public/favicon.svg`, `public/apple-touch-icon.png`, `public/og-image.png`: İkonlar ve sosyal paylaşım görseli.
- `public/robots.txt`, `public/sitemap.xml`: Arama motorları için.
- `public/_headers`: Cloudflare güvenlik ve önbellek başlıkları.

## Cloudflare (Workers static assets)
- `wrangler.jsonc` yalnızca `public/` klasörünü yayınlar. Site dosyalarını bu klasöre koyun.
- Cloudflare'de Git bağlantılı Worker: deploy komutu `npx wrangler deploy`, build komutu boş.
- `main` dalına her push otomatik yayınlanır.
- Alan adı: Worker → **Settings → Domains & Routes → Add → Custom domain** → `hostkap.dev`.

## Yerel önizleme
```bash
python3 -m http.server 8000 -d public
```
