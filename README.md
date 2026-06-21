# Shopilo

A full e-commerce store built with React. You can browse products, search, filter by category, add items to a cart or wishlist, apply coupon codes, and go through checkout. There's no backend — all the product data comes from a free public API ([DummyJSON](https://dummyjson.com/docs/products)), and everything else (cart, wishlist, etc.) is handled in the browser and saved with localStorage.

**Live demo:** https://shopilooo.netlify.app

## Why I built it

I wanted a project that goes beyond "fetch some data and show it on a page." So instead of just listing products, I built out the stuff a real store needs: a cart that doesn't reset when you refresh the page, search that doesn't spam the API on every keystroke, filters you can share as a link, loading skeletons instead of blank screens, and a checkout flow with coupons and shipping rules.

## Features

- Browse products, filter by category, sort, and search
- Product pages with images, ratings, and reviews (from the API)
- Cart and wishlist that stay saved even after closing the tab
- Coupon codes with real discount calculation
- Free shipping over $50, with a message telling you how much more to add
- Undo button after clearing your cart
- "Recently viewed" products
- Toast notifications, loading skeletons, and a back-to-top button
- Works on mobile and desktop

## Built with

- React + Vite
- React Router
- Context API + useReducer (for cart/wishlist state)
- Tailwind CSS
- DummyJSON for product data

No UI library — everything you see (cards, toasts, the carousel, etc.) is built from scratch.

## Running it locally

```bash
git clone https://github.com/Abdallah-Sabha1/shopilo.git
cd shopilo
npm install
npm run dev
```

No API keys or setup needed, the API is free and public.

## Project structure

```
src/
├── components/   # Navbar, Footer, ProductCard, Toast, etc.
├── pages/        # Home, Shop, ProductDetail, Cart, Wishlist
├── context/      # Cart, Wishlist, RecentlyViewed (global state)
├── hooks/        # useProducts, useDebounce
└── utils/        # small helper functions
```

## Notes

This is a front-end only project on purpose — the goal was to focus on React state, performance, and UI details, not build a full backend. If I extended it, the next steps would be real authentication, an actual backend for orders, and payments through something like Stripe.

---

Built by [Abdallah Sabha](https://github.com/Abdallah-Sabha1)
