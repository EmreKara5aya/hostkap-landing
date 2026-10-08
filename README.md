# Hostkap landing

[hostkap.dev](https://hostkap.dev/) için tek dosyalık statik açılış sayfası. Derleme adımı yoktur.

## Dosyalar
- `index.html`: Sayfanın tamamı (fontlar ve scriptler içine gömülü), SEO / Open Graph etiketleri dahil.
- `favicon.svg`, `apple-touch-icon.png`, `og-image.png`: İkonlar ve sosyal paylaşım görseli.
- `robots.txt`, `sitemap.xml`: Arama motorları için.
- `_headers`: Cloudflare Pages güvenlik ve önbellek başlıkları.

## Cloudflare Pages
1. Cloudflare panelinde **Workers & Pages → Create → Pages → Connect to Git** ile bu repoyu seçin.
2. Production branch: `main`. Framework preset: **None**. Build command: boş. Output directory: `/`.
3. **Custom domains** sekmesinden `hostkap.dev` ekleyin. `www` → kök alan yönlendirmesi için Cloudflare **Redirect Rules** kullanılabilir.

## Yerel önizleme
```bash
python3 -m http.server 8000
```
