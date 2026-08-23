# Crave.js — Sushi Storefront Template

> [!WARNING]
> **Legacy visual reference only.** This repository pins the retired Storefront
> SDK 1.x browser-key contract. Do not use it as a production starter, expose a
> Crave API key in browser code, or use its one-click deployment flow. Build new
> integrations from the current [Storefront SDK guide](https://docs.craveup.com/getting-started/storefront-sdk)
> and treat this repository only as design and interaction reference material.

Tomodachi Sushi is a Next.js 15, React 19, and Tailwind CSS example for
studying menu, product-detail, cart, and restaurant marketing UI.

## Key Features

- **CraveUp Ordering** – Integrates the CraveUp storefront SDK for menu data, cart mutations, and checkout handoffs.
- **Responsive Menu UX** – Sticky category tabs, scroll-linked sections, and product dialogs optimized for both desktop and mobile.
- **Cart & Recommendations** – Full cart sidebar with quantity controls, suggestions carousel, and checkout CTA.
- **Dark & Light Themes** – Brandable palettes defined in CSS custom properties with instant theme toggling.
- **Accessible Components** – Built on shadcn/ui + Radix primitives with Drawer/Dialog parity and keyboard support.
- **Local Reference** – Includes `pnpm` scripts for local design and interaction study.

## Demo

| Hero (Light)                                            | Hero (Dark)                                           |
| ------------------------------------------------------- | ----------------------------------------------------- |
| ![Hero Light](public/screenshots/hero+navbar-light.png) | ![Hero Dark](public/screenshots/hero+navbar-dark.png) |

| Menu Grid                                        | Product Drawer                                                      |
| ------------------------------------------------ | ------------------------------------------------------------------- |
| ![Menu Page](public/screenshots/menu%20page.png) | ![Product Drawer](public/screenshots/product%20detail%20drawer.png) |

| Cart & Recommendations                                 | Menu Scroll GIF |
| ------------------------------------------------------ | --------------- |
| ![Cart Sidebar](public/screenshots/cart%20sidebar.png) | ![Menu Scroll GIF](public/screenshots/menu%20scrolling-gif.gif) |

## Tech Stack

- [Next.js 15 (App Router)](https://nextjs.org/)
- [React 19](https://react.dev/)
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/) with custom tokens
- [shadcn/ui](https://ui.shadcn.com/) + Radix UI primitives
- [CraveUp Storefront SDK](https://docs.craveup.com/)

## Getting Started

1. **Clone the repo**
   ```bash
   git clone --depth 1 https://github.com/your-org/tomodachi-sushi-template
   cd tomodachi-sushi-template
   ```
2. **Install dependencies**
   ```bash
   pnpm install
   ```
3. **Configure environment variables** (see next section).
4. **Run the dev server**
   ```bash
   pnpm dev
   ```
   Visit `http://localhost:3000` to explore the template.

## Environment Variables

Create a `.env.local` file only if you need a public location label while
studying the UI. Do not add a Crave API key: this legacy application is not a
supported live integration.

```bash
NEXT_PUBLIC_LOCATION_ID=loc_xxx
```

## Scripts

| Command      | Description                          |
| ------------ | ------------------------------------ |
| `pnpm dev`   | Run the local development server     |
| `pnpm build` | Create an optimized production build |
| `pnpm start` | Serve the production build locally   |
| `pnpm lint`  | Run ESLint                           |

## Customization Guide

1. **Branding & Assets** – Replace imagery in `public/images/` with your restaurant photography.
2. **Colors & Typography** – Update CSS variables in `src/app/globals.css` to match your brand system.
3. **Menu Content** – Study the legacy data flow locally; use the current Storefront SDK guide for a new live integration.
4. **Components** – Extend UI patterns inside `src/components/crave-ui` and `src/app/components`.
5. **Production work** – Rebuild against the current Storefront API and SDK contract rather than deploying this legacy integration.

## Project Structure

```
.
├── src
│   ├── app
│   │   ├── page.tsx, about/, menu/, reservation/  # App Router pages
│   │   ├── components/                            # Navbar, cards, layout primitives
│   │   └── globals.css                            # Tailwind + theme tokens
│   ├── components
│   │   ├── crave-ui/cart-component/               # Cart sidebar, counter button, etc.
│   │   └── ui/                                    # shadcn/ui wrappers
│   ├── hooks/                                     # Cart + ordering session hooks
│   ├── lib/                                       # API clients, utilities
│   └── store/                                     # Zustand cart store
├── public
│   ├── images/                                    # Brand imagery
│   └── screenshots/                               # README visuals
└── README.md
```

## Deployment status

Do not deploy this legacy integration as a live ordering storefront. Reuse its
visual ideas in a new application built against the current Storefront API and
SDK contract instead.

## Support & Reference

- [CraveUp Docs](https://docs.craveup.com/)
- [Next.js Documentation](https://nextjs.org/docs)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)
- [shadcn/ui Documentation](https://ui.shadcn.com/)

## License

Distributed under the [MIT License](LICENSE) © Crave Up Inc.

Happy building, and enjoy launching your sushi storefront! 🍣
