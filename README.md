# Fitness Exercise Catalog

"Get Body in Shape" — a multi-page website for browsing a fitness exercise catalog by body part, muscle, or equipment, with search, favorites, and user ratings.

## Features

- Browse exercise categories by muscles, body parts, or equipment, with pagination
- Filter and search exercises by keyword within a category
- Exercise details modal with description and rating form
- Rate exercises and submit feedback via the rating modal
- Save and view favorite exercises on a dedicated page
- Daily motivational quote widget
- Responsive layout with a mobile menu and scroll-to-top control
- Email subscription form

## Technology

- Vanilla JavaScript (ES modules) with HTML partial injection
- Vite build tooling with multi-page (HTML) entry points
- Axios for HTTP requests to the exercises REST API
- SimpleLightbox, iziToast, body-scroll-lock, Font Awesome
- TypeScript type-checking (`tsc --noEmit`) without a TypeScript build step
- Prettier for formatting
- GitHub Actions workflow deploying the production build to GitHub Pages

## Project structure

```
src/
  partials/   HTML fragments injected into pages (header, hero, filters, modals, footer)
  css/        Stylesheets per component/section
  js/         Feature modules (fetching, pagination, modals, favorites, ratings)
  images/     Responsive image assets (avif/webp/jpg)
  fonts/      Custom fonts and icon font
  index.html       Home page (exercise catalog)
  favorites.html   Favorites page
```

## Commands

```
npm install        # install dependencies
npm run dev        # start the Vite dev server
npm run build      # build for production (GitHub Pages base path)
npm run preview    # preview the production build
npm run type-check # type-check with TypeScript (no emit)
npm run format     # format files with Prettier
```

## Deployment

Pushes to `main` trigger a GitHub Actions workflow that builds the project and deploys the `dist` output to the `gh-pages` branch for GitHub Pages.
