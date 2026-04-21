# heyzack-docs

Documentation for my project

## Getting Started

```bash
# Install dependencies
npm install

# Start development server
npm run dev
```

Your docs will be available at [http://localhost:3000](http://localhost:3000)

## Switching between Partner and CRM docs

The header includes a **Partner | CRM** control that links to a sibling documentation app (for example `heyzackcrm-docs` running on another port).

1. Copy `.env.example` to `.env.local`.
2. Set `NEXT_PUBLIC_DOCS_SITE=partner` in this repo (Partner Portal docs).
3. Set `NEXT_PUBLIC_CRM_DOCS_URL` to your CRM docs URL (e.g. `http://localhost:3001/docs` when the CRM docs app uses port 3001).

In the **CRM docs** repository, set `NEXT_PUBLIC_DOCS_SITE=crm` and `NEXT_PUBLIC_PARTNER_DOCS_URL` to this app’s docs URL. Mirror the same `docs-switcher` component and `lib/docs-switcher.ts` there so both headers stay in sync.

## Project Structure

```
├── app/                  # Next.js app directory
├── content/
│   └── docs/            # Your documentation (MDX files)
├── lib/
│   └── theme-config.ts  # Site configuration
└── public/              # Static assets
```

## Writing Documentation

Add MDX files to `content/docs/` to create new pages. The sidebar navigation is automatically generated based on your file structure.

## Built with Unmint

This documentation site was created with [Unmint](https://github.com/gregce/unmint), a free and open-source documentation system.
