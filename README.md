# DapurERP — Small Food Stall ERP (Sunset Stall)

Simple ERP system for a small food stall, built for a final-year thesis project.
Fully in English. Live demo: https://oblay-thesis-demo.vercel.app/

## How to run

- **Easiest:** open `index.html` directly in a browser, or open the Vercel link above.
- **Deploy it yourself on Vercel:** import this repo in Vercel, framework "Other", no build command.
- No login, no install. A single self-contained HTML file (CSS + JS inside).

## Pages (11 separate pages)

Overview, Cashier, Menu & Ingredients, Recipes & Production, Purchasing, Supplier,
Customers, Employees, Cash & Expenses, Reports, Settings.

## Features

- **Start-from-zero mode:** all figures start at Rp 0, the owner inputs everything from scratch.
- **Cashier:** the "+ New transaction" button opens the form (customer/table name, menu, quantity, status).
  Save → the transaction is recorded and the Overview figures update.
- **Automatic stock:** a sale in Cashier deducts ingredient stock per the recipe
  (e.g. Iced Latte → coffee beans, milk, sugar go down). Purchases add stock.
  Stock below minimum shows up in "Ingredients to buy" + a Buy button.
  Not enough stock → the transaction is blocked + a warning names the missing ingredients.
- **Edit / Delete:** every menu, ingredient, and recipe row can be edited (form pre-filled)
  and deleted (with confirmation). Deleting a menu also deletes its recipe.
- **"Sales this week" chart:** calculated from entered transactions
  (Mon–Sun, week 2–8 Nov 2026), today’s bar is orange + labelled with the amount.
- **Reports:** the "Generate Monthly PDF Report" button exports every section into one PDF.
- **Month-End Closing:** on the Reports page. The PDF must be exported first before the button activates.
  After confirmation, that month’s transactions/purchases/cash notes are cleared
  (new month starts at Rp 0) and the month’s PDF is stored in "Report History".
  Menus, recipes, ingredients + current stock, suppliers, customers, and employees stay.

## Data notes

- This version (static preview) stores data in the browser session only —
  refreshing the page returns to start-from-zero mode.
- Live version later: plug in Supabase (free, 500 MB — enough for years
  at food-stall scale, ~5 MB/month). Tables: transactions, menus, ingredients, recipes,
  purchases, suppliers, customers, employees, cash.
- Starting demo data: Sunset Stall, Sunset Admin, Wednesday 4 November 2026.

## Repo structure

- `index.html` — the whole app (HTML + CSS + JS) in one file.
- `README.md` — this file.
