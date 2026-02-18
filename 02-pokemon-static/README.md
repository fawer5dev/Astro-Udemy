# Pokemon Static

A statically generated Pokemon website built with **Astro** and **Tailwind CSS v4**. It fetches data from the [PokeAPI](https://pokeapi.co/) at build time and generates static pages for the first 151 Pokemon, including paginated lists, individual detail pages with official artwork, and audio cries.

## About the Project

This project was built as part of an Astro course and demonstrates:

- **Static Site Generation (SSG)** — All pages are pre-rendered at build time using `getStaticPaths`, resulting in fast load times and zero client-side API calls.
- **PokeAPI Integration** — Fetches Pokemon data (names, sprites, cries) from the public PokeAPI.
- **Pagination** — The Pokemon list is paginated (20 per page) with previous/next navigation.
- **Dynamic Routes** — Individual Pokemon pages are generated using `[name].astro` and `[page].astro` dynamic routes.
- **SEO & Open Graph Metadata** — Each page includes `title`, `description`, and `og:image` meta tags.
- **Tailwind CSS v4** — Styled with utility-first CSS using the latest Tailwind CSS integrated via its Vite plugin.
- **View Transitions** — Smooth page transitions powered by Astro's built-in `ViewTransitions`.

## Project Structure

```text
/
├── public/                          # Static assets
├── src/
│   ├── components/
│   │   ├── Welcome.astro            # Welcome component
│   │   └── pokemons/
│   │       └── PokemonCard.astro    # Reusable Pokemon card component
│   ├── consts/
│   │   └── site-info.ts             # Global site metadata constants
│   ├── interfaces/
│   │   └── pokemon-list.response.ts # TypeScript interface for PokeAPI response
│   ├── layouts/
│   │   ├── Layout.astro             # Base layout
│   │   └── MainLayout.astro         # Main layout with SEO meta tags
│   ├── pages/
│   │   ├── index.astro              # Home page (first 20 Pokemon)
│   │   ├── pokemon/
│   │   │   └── [id].astro           # Pokemon detail page by ID
│   │   └── pokemons/
│   │       ├── [name].astro         # Pokemon detail page by name
│   │       └── [page].astro         # Paginated Pokemon list
│   └── styles/
│       └── global.css               # Global styles
├── astro.config.mjs                 # Astro configuration
├── package.json
└── tsconfig.json
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher)
- [pnpm](https://pnpm.io/) package manager

### Installation

1. Clone the repository:

   ```sh
   git clone <repository-url>
   cd 02-pokemon-static
   ```

2. Install dependencies:

   ```sh
   pnpm install
   ```

3. Start the development server:

   ```sh
   pnpm dev
   ```

4. Open your browser at [http://localhost:4321](http://localhost:4321)

## Commands

All commands are run from the root of the project:

| Command             | Action                                       |
| :------------------ | :------------------------------------------- |
| `pnpm install`      | Install dependencies                         |
| `pnpm dev`          | Start dev server at `localhost:4321`          |
| `pnpm build`        | Build the production site to `./dist/`        |
| `pnpm preview`      | Preview the production build locally          |
| `pnpm astro ...`    | Run Astro CLI commands (e.g. `astro check`)   |

## Tech Stack

- [Astro](https://astro.build/) v5 — Static site framework
- [Tailwind CSS](https://tailwindcss.com/) v4 — Utility-first CSS
- [PokeAPI](https://pokeapi.co/) — Pokemon data source
- [TypeScript](https://www.typescriptlang.org/) — Type safety

## Summary

**Pokemon Static** is a fully static website that showcases the original 151 Pokemon. Every page is generated at build time, making the site extremely fast with no runtime API dependencies. Users can browse Pokemon through a paginated list, view detailed information for each Pokemon (including official artwork and audio cries), and navigate seamlessly with smooth view transitions.
