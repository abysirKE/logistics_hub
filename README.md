Logistics Hub

Logistics Hub is a web dashboard for viewing supply-chain operations in one
place. It brings together inventory, production, deliveries, suppliers,
analytics, and blockchain-related views.

The project includes a Next.js web app and a separate collection of smart
contract examples under `smart_contracts`. The dashboard is currently a
front-end prototype: its screens show sample dashboard data and are not
connected to a live logistics database or to the contracts.

What you can explore

**Dashboard:** an overview of supply-chain activity.
**Inventory:** inventory levels, trends, and alerts.
**Production:** production progress and quality metrics.
**Logistics:** shipment and delivery information.
**Suppliers:** supplier information and performance views.
**Analytics:** charts and operational metrics.
**Blockchain:** transaction and smart-contract views.

Technology

The web app uses Next.js, React, and TypeScript. Its interface is styled with
Tailwind CSS and uses charting and icon libraries. The `smart_contracts`
directory contains contract examples, including Soroban contracts for
production steps and supply-chain metrics.

Running the web app

You will need Node.js and npm installed. From the project folder:

```bash
npm install
npm run dev:all
```

Then open [http://localhost:3000](http://localhost:3000) in your browser. The
home page redirects to the dashboard.

> **Before using `npm run dev`:** that script also runs `npm run set-style`,
> which executes `src/app/globals_light.css` as Node.js code. That file contains
> obfuscated executable code, not just CSS. Do not run `npm run dev` or
> `npm run set-style` until the file and script have been reviewed and cleaned
> up. `npm run dev:all` starts the Next.js development server without invoking
> that extra script.

Other scripts defined in `package.json` include `npm run build`,
`npm run start`, and `npm run lint`.

Project layout

`src/app` contains the pages and global styles for the web app.
`src/components` contains the dashboard, charts, navigation, and reusable UI.
`src/lib` and `src/hooks` contain shared helpers and React hooks.
`public` contains images and other static assets.
`smart_contracts` contains the smart-contract workspace and examples.

Smart contracts

The contracts are maintained separately from the dashboard. For contract
development instructions, prerequisites, and tests, see the README files inside
`smart_contracts` and its contract folders. The web app does not currently
connect to a deployed contract.
