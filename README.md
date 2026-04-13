# MA-Elektro Web

Statyczna strona firmowa oparta o Astro i przygotowana pod GitHub Pages.

## Wymagania
- Node.js 22+ (zalecane przez nvm)
- npm

## Start lokalny
```bash
npm ci
npm run dev
```

## Build i podglad produkcyjny
```bash
npm run build
npm run preview
```

## Struktura projektu
- `src/pages/index.astro` - glowna strona (homepage-first)
- `src/layouts/MainLayout.astro` - bazowy layout i metadane
- `src/assets/images/` - zrodlowe obrazy do optymalizacji
- `.github/workflows/deploy.yml` - pipeline wdrozenia GitHub Pages

## Obrazy i optymalizacja
- Uzywaj komponentow `Image` lub `Picture` z `astro:assets`.
- Trzymaj obrazy zrodlowe w `src/assets/images/`.
- Domyslnie stosuj:
	- formaty: AVIF i WebP (z fallbackiem)
	- responsywne szerokosci (`widths`)
	- poprawne `alt`
- Nie dodawaj duzych obrazow do `public/`, bo omija to optymalizacje Astro.

## Deploy na GitHub Pages
1. W repozytorium GitHub ustaw Pages source na **GitHub Actions**.
2. Upewnij sie, ze branch produkcyjny to `main`.
3. Workflow z `.github/workflows/deploy.yml` zbuduje i wdrozy `dist/`.
4. Dla domeny `ma-elektro.pl` utrzymuj wpis w `public/CNAME`.

## Uwaga o tresci
W pierwszym etapie projekt obejmuje tylko strone glowna. Kolejne podstrony mozna migrowac stopniowo.
