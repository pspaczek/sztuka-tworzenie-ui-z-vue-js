# Sztuka tworzenia UI z Vue.js

Prezentacja meetupowa przygotowana w [Slidev](https://sli.dev/).

## Wymagania

- Node.js 24 (wersję wskazuje plik `.nvmrc`)
- npm

## Praca lokalna

```sh
npm ci
npm run dev
```

Slidev uruchomi prezentację w trybie deweloperskim. Slajdy edytuj w pliku `slides.md`.

Aby sprawdzić produkcyjny build lokalnie:

```sh
npm run build
```

Wynik znajdzie się w katalogu `dist/`.

## Publikacja na GitHub Pages

1. Utwórz puste repozytorium na GitHubie (bez dodatkowego README, licencji ani `.gitignore`).
2. W katalogu projektu podłącz repozytorium i wypchnij pliki na gałąź `main`:

   ```sh
   git init -b main
   git add .
   git commit -m "Initial Slidev setup"
   git remote add origin https://github.com/USER/REPOSITORY.git
   git push -u origin main
   ```

   W adresie `origin` zastąp `USER` nazwą konta lub organizacji, a `REPOSITORY` nazwą repozytorium.
3. W repozytorium przejdź do **Settings → Pages** i jako źródło wdrażania wybierz **GitHub Actions**.
4. Po każdym pushu na `main` lub `master` workflow z `.github/workflows/deploy.yml` zbuduje prezentację i opublikuje ją na Pages. Możesz też uruchomić go ręcznie na karcie **Actions**.

Workflow sam ustawia ścieżkę bazową: `/` dla repozytorium `użytkownik.github.io` albo `/nazwa-repozytorium/` dla pozostałych repozytoriów. Adres opublikowanej prezentacji znajdziesz w ustawieniach Pages lub w podsumowaniu wdrożenia workflow.