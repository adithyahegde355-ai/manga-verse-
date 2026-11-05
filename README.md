# MangaVerse

MangaVerse is a responsive manga/manhwa discovery and reading app powered by the public MangaDex API. It is a complete Vite + vanilla JavaScript + Capacitor project, designed to be easy to run locally and build into an Android APK with GitHub Actions.

## Features
- Search MangaDex catalogue and browse popular titles
- Genre filter and sorting
- Manga/manhwa detail pages with English chapter list
- Chapter reader using MangaDex@Home data-saver pages
- Local bookmarks and reading history (saved on the device)
- Responsive desktop and mobile layout
- Capacitor Android wrapper
- GitHub Actions workflow that builds an APK artifact and attaches it to tagged releases

## Run on your computer
1. Install Node.js 22 or newer.
2. Extract this ZIP.
3. Open a terminal in the `mangaverse` folder.
4. Run `npm install`.
5. Run `npm run dev` and open the local URL shown.

## Build an APK with GitHub Actions
1. Create a GitHub repository.
2. Upload the contents of this folder to the repository root (including `.github/workflows/build.yml`).
3. Open the **Actions** tab and enable workflows if asked.
4. Choose **Build MangaVerse Android APK** → **Run workflow**.
5. When it finishes, open the workflow run and download **MangaVerse-debug-apk** under Artifacts.

### Publish APK in GitHub Releases
Create and push a version tag, for example:

```bash
git tag v1.0.0
git push origin v1.0.0
```

The same workflow builds the APK and attaches it to the GitHub Release for that tag.

## Data and attribution
Catalogue metadata, chapters, and reader pages are served by MangaDex. MangaVerse is an independent client and is not affiliated with MangaDex. Respect MangaDex's terms and API rate limits, creator/scanlation-group credits, and removal requests. Availability and translations depend on the source.

## Notes
- Bookmarks and history use browser/device `localStorage`; they are not synced across devices.
- This project does not include a backend, account system, or hosted database.
- The debug APK is suitable for testing and sharing; a signed release build is needed for Play Store publication.
