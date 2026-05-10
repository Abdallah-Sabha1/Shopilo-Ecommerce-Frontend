# Shopilo

A modern e-commerce storefront built with React 18 and React Router v6. The app consumes the DummyJSON API to serve real product data and runs entirely in the browser — no backend or server setup required.

---

## Features

- **Multi-page navigation** — Client-side routing with React Router v6 (`useNavigate`, `useParams`, nested routes)
- **Persistent shopping cart** — Global cart state managed via Context API and `useReducer`, saved to `localStorage` between sessions
- **Wishlist** — Mirrors the cart architecture; items survive page refreshes
- **Live product search** — Debounced input hook prevents unnecessary API calls while the user types
- **Category filtering** — Filters are reflected in the URL via Search Params, making results shareable and bookmarkable
- **Sorting & pagination** — Client-side derived state with `useMemo` for performance-conscious rendering
- **Loading skeletons** — Shimmer placeholders shown during data fetches to avoid layout shifts
- **Toast notifications** — Lightweight custom context with auto-dismiss timers; no third-party library
- **Coupon code support** — Discount logic handled in local state at checkout
- **Fully responsive** — CSS Grid and media queries, tested on mobile, tablet, and desktop

---

## Tech Stack

| Layer | Choice |
|---|---|
| UI Library | React 18 |
| Bundler | Vite |
| Routing | React Router v6 |
| Styling | CSS Modules + Tailwind CSS |
| Fonts | Cormorant Garamond, Syne (Google Fonts) |
| Data | DummyJSON REST API |
| State | Context API + useReducer |

No external UI component libraries are used — every component was written from scratch.

---

## Project Structure

```
src/
├── components/     # Shared UI components (Navbar, ProductCard, Skeleton, Toast, …)
├── pages/          # Route-level views (Home, Shop, ProductDetail, Cart, Wishlist)
├── context/        # Global state providers (CartContext, WishlistContext, ToastContext)
├── hooks/          # Custom hooks (useProducts, useDebounce)
└── utils/          # Pure utility functions (formatPrice, couponValidator, …)
```

---

## Getting Started

**Prerequisites:** Node.js 18+ and npm.

```bash
# Install dependencies
npm install

# Start the development server
npm run dev

# Build for production
npm run build

# Preview the production build locally
npm run preview
```

The dev server runs at `http://localhost:5173` by default.

---

## API Reference

All data comes from [DummyJSON](https://dummyjson.com/docs/products) — free to use, no API key or account required.

| Endpoint | Used for |
|---|---|
| `GET /products` | Product listing page |
| `GET /products/:id` | Product detail & reviews |
| `GET /products/search?q=` | Search results |
| `GET /products/categories` | Category navigation |
| `GET /products/category/:name` | Category filter pages |

---

## License

MIT
