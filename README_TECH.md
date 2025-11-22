# BIOSZAMBA - Technical Documentation

## Struktura Projektu

```
Bioszamba/
├── index.html              # Główna strona
├── css/
│   └── style.css          # Wszystkie style (responsive)
├── js/
│   └── main.js            # JavaScript (Swiper, AOS, GLightbox)
├── images/
│   ├── logo/
│   │   └── wizytowka.png
│   ├── produkty/
│   │   ├── image1.jpeg
│   │   ├── image2.png
│   │   └── image3.jpeg
│   └── montaz/
│       ├── 0.jpeg
│       ├── 1.jpeg
│       ├── 2.jpeg
│       ├── 3.jpeg
│       ├── 4.png
│       ├── 5.png
│       └── 6.png
├── CLAUDE.md              # Plan projektu
├── Wprowadzenie.md        # Treść źródłowa
└── README_TECH.md         # Ten plik
```

## Technologie

### Frontend
- **HTML5** - Semantyczny markup
- **CSS3** - Custom Properties (CSS Variables), Flexbox, Grid
- **JavaScript (Vanilla)** - Bez frameworków

### Biblioteki (CDN)
- **Swiper.js 11** - Karuzele (Hero + Montaż)
- **Font Awesome 6.5.1** - Ikony
- **AOS 2.3.1** - Animacje scroll
- **GLightbox** - Lightbox dla galerii

## Funkcjonalności

### Header
- Sticky header z przyciskami CTA
- Responsywna nawigacja
- Linki: tel: i mailto:

### Hero Section
- Karuzela 3 zdjęć z autoplay
- Fade effect między slajdami
- Overlay z gradientem granatowym
- CTA po lewej, tekst po prawej

### Sekcje
1. **O nas** - 3 karty z ikonami + opis
2. **Produkty** - 2 kolumny (Zbiorniki + Ziemianki)
3. **Montaż** - Etapy procesu + karuzela ze zdjęć
4. **Zalety** - 4 karty
5. **Kontakt** - Info + Google Maps

### Animacje
- AOS fade-in przy scrollowaniu
- Hover effects na kartach
- Smooth scroll do sekcji

## Responsywność

### Breakpoints
- Desktop: > 992px
- Tablet: 768px - 992px
- Mobile: < 768px
- Small Mobile: < 480px

### Mobile-first approach
- Flexbox/Grid dostosowują się automatycznie
- Karuzele: 1 slajd na mobile, 1.5-2 na tablet/desktop
- Menu: pełna szerokość na mobile

## Optymalizacja

### Performance
- Lazy loading obrazów
- CDN dla bibliotek
- Minified CSS (można dodać)
- Deferred JS loading

### SEO
- Meta tags (title, description, keywords)
- Semantic HTML5
- Alt tags dla obrazów
- Open Graph (można dodać)

## Deployment - GitHub Pages

### Setup
1. Push do repozytorium GitHub
2. Settings → Pages → Source: main branch / root
3. Cloudflare DNS: CNAME wskazujący na `username.github.io`
4. GitHub: Settings → Pages → Custom domain

### CNAME File
Utworzyć plik `CNAME` w root z domeną:
```
bioszamba.pl
```

### Automatyczne deploy
- Każdy `git push` do main = automatyczny deploy
- GitHub Actions można dodać dla optymalizacji

## Rozwój

### Lokalne testowanie
```bash
# Opcja 1: Python
python3 -m http.server 8000

# Opcja 2: Node.js
npx serve

# Potem otwórz: http://localhost:8000
```

### Git workflow
```bash
git add .
git commit -m "opis zmian"
git push origin main
```

## Przyszłe ulepszenia (opcjonalne)

- [ ] Kompresja obrazów (WebP)
- [ ] Service Worker (PWA)
- [ ] Dark mode
- [ ] Formularz kontaktowy (backend)
- [ ] Blog/aktualności
- [ ] Multilanguage (EN)
- [ ] Analytics (Google Analytics)
- [ ] Cookie consent
- [ ] Testimonials/opinie

## Browser Support

- Chrome/Edge: ✅ Pełne wsparcie
- Firefox: ✅ Pełne wsparcie
- Safari: ✅ Pełne wsparcie
- Opera: ✅ Pełne wsparcie
- IE11: ⚠️ Częściowe (brak CSS Grid)

## Kontakt techniczny

Dla zmian i poprawek - edytuj pliki i push do repo.
Strona automatycznie zaktualizuje się na GitHub Pages.
