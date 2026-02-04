# Pokédex App

A clean, mobile-first Pokédex interface built with React, TypeScript, and Vite.

## Features

- **Pokédex List**: Browse Pokémon in a responsive grid layout
- **Pokémon Details**: View detailed information including stats, types, moves, and descriptions
- **Filters**: Search by name and filter by type
- **Load More**: Pagination with "Load More" button
- **Responsive Design**: Mobile-first design that works on all screen sizes
- **Loading States**: Skeleton loaders and loading indicators
- **Type Colors**: Color-coded type pills for all 18 Pokémon types

## Tech Stack

- React 18
- TypeScript
- React Router DOM
- Vite
- PokéAPI (https://pokeapi.co)

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

1. Install dependencies:
```bash
npm install
```

2. Start the development server:
```bash
npm run dev
```

3. Open your browser and navigate to `http://localhost:5173`

### Build for Production

```bash
npm run build
```

The built files will be in the `dist` folder.

### Preview Production Build

```bash
npm run preview
```

## Data Source

This app uses the [PokéAPI](https://pokeapi.co) to fetch Pokémon data:
- List endpoint: `/pokemon?limit=60&offset=0`
- Details endpoint: `/pokemon/{id}`
- Species endpoint: `/pokemon-species/{id}`

All data is fetched on-demand from the API (no local JSON files).

## Project Structure

```
src/
├── components/          # Reusable components
│   ├── Header.tsx
│   ├── PokemonCard.tsx
│   ├── PokemonGrid.tsx
│   ├── TypePill.tsx
│   ├── FilterModal.tsx
│   └── LoadingSkeleton.tsx
├── pages/              # Route pages
│   ├── PokedexList.tsx
│   └── PokemonDetails.tsx
├── api.ts              # API functions
├── types.ts            # TypeScript types
├── App.tsx             # Main app component
└── main.tsx            # Entry point
```

## Routes

- `/` - Pokédex list page
- `/pokemon/:id` - Pokémon details page

## Accessibility

- All buttons are keyboard-focusable
- Images have alt text
- Semantic HTML structure
- ARIA labels where appropriate

## Browser Support

Works on all modern browsers (Chrome, Firefox, Safari, Edge).
