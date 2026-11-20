# Network Security Dashboard

A responsive, accessible React + TypeScript dashboard for monitoring network security: KPI overview, traffic and threat charts, a searchable/filterable alerts table, and a device status view.

## Features
- Loading and error states (with a Try again button) on every data view; add `?fail` to the URL to preview the error state
- Overview with KPI cards, traffic line chart and threats-by-type bar chart (Recharts)
- Alerts table with search, severity filter and sortable severity column, pagination and an empty state (Redux Toolkit state)
- Device grid with a detail panel (uptime, last seen); status shown as text plus a colour marker
- Notification settings form with validation and accessible error messages
- Light/dark mode
- Accessibility: semantic HTML, labelled controls, table captions, `aria-sort`, `aria-current`, visible focus styles
- Responsive layout (mobile to desktop) with Tailwind CSS
- Unit tests with Jest and React Testing Library

## Tech stack
React 18, TypeScript, Vite, Tailwind CSS, Redux Toolkit, Recharts, Jest, React Testing Library

## Getting started
```bash
npm install
npm run dev      # start the dev server
npm test         # run unit tests
npm run build    # type-check and build for production
```

## Project structure
```
src/
  components/  Overview, Alerts, Devices, Settings, Async
  useAsync.ts  data-loading hook (loading / error / retry)
  data.ts      mock alerts, devices and chart data
  store.ts     Redux Toolkit store (search, severity filter, theme)
  App.tsx      layout and navigation
  Alerts.test.tsx
```
