# Enver Kollari

I build and sell business software, and I spent thirteen years in banking before that.

That order matters. I came to software from the side of the desk where the numbers get checked:
thirteen years preparing and testing business financial statements, five of them managing a bank
branch. The systems I build are for the kind of business I used to lend to, so I already know the
work the software has to do.

Based in Rahovec, Kosovo. CET.

---

## Products

### XPOS - point of sale and stock, for cafés and restaurants

Sold and live.

Sales, expenses and stock movements, with weighted-average cost inventory valuation recomputed on
every stock intake, and a management profit summary the owner reads daily. Built to be used at
speed by people who are not looking at the screen.

React with TypeScript on Vite, Node and Express, PostgreSQL accessed through raw SQL rather than an
ORM, Socket.IO. On-premise and self-hosted, installed as a Windows service.

[Walkthrough with screenshots](https://github.com/enverkollari/XPOS)

### LogiTrack - logistics and fleet management

Sold and live.

Pickups, depots, cities, sales points, products, suppliers and expenses, with an admin and driver
split. Changes are broadcast over WebSockets, so every connected device reflects them without
anyone refreshing. Route building is manual and deliberate: you pick the stops per city and save
the route.

React, Vite, TypeScript, Node, Prisma, socket.io, PWA.

[Walkthrough with screenshots](https://github.com/enverkollari/LogiTrack)

### XCount - double-entry accounting, in development

In progress, and my main build right now.

Built for an accounting practice serving many clients rather than for one company. Chart of
accounts with normal balances, fiscal years and periods that open and close, journal entries by
book, payment allocations with open items, workpapers, a statutory rules engine, and an audit log.

The double-entry is enforced rather than described. An unbalanced entry is rejected. A line
carrying both a debit and a credit is refused. The trial balance knows whether it balances, and
reversals mirror debits to credits. Amounts use a dedicated money type rather than floating point,
and the integrity rules live in the database migrations as constraints and triggers, where
application code cannot step around them.

TypeScript, Node, Next.js, PostgreSQL with Prisma. Unit tests over the ledger, the money type and
the rules engine. Albanian interface.

[Walkthrough with screenshots](https://github.com/enverkollari/XCount)

---

## How I work

I use AI heavily, Claude daily, and I read what it writes. The judgement about what the system
should do, and whether a number is right, is the part I will not delegate - it is the part I was
trained in.

## Why the source is private

These are commercial products, so the code stays closed. The three repositories linked above are
walkthroughs of the working systems, not the source. Happy to talk through architecture, schema or
specific decisions in a conversation.

## Contact

- LinkedIn: [linkedin.com/in/enver-kollari](https://linkedin.com/in/enver-kollari)
- Email: enverkollari@hotmail.com

Available for remote work, employment or contract.
