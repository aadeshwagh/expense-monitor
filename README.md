# Expense Monitor

> Turn your bank-statement PDFs into categorized spending — automatically.

Expense Monitor reads a monthly bank statement in PDF form, extracts every transaction, and sorts it into clear categories — then reports where your money actually went. No manual data entry, no spreadsheets.

> **Note:** currently supports the **Axis Bank** statement format.

## What it does

- **Parses** a monthly bank-statement PDF.
- **Extracts** individual transactions from the statement.
- **Categorizes** each transaction into one of three groups:
  - **Merchant payments**
  - **Person payments**
  - **Cash withdrawals**
- **Summarizes** the month with general results:
  - **Total expense**
  - **Total savings** — calculated as *money received from a registered payer − total expenses*

## Roadmap

- **v1.0** — Parse Axis Bank PDF statements, categorize transactions into the three main categories, and show general results.
- **v2.0** — Add sub-categories:
  - *Merchant payments* → Food, Lunch, Dinner, Big purchases (custom limit), Other
  - *Person payments* → Rent, total debited per person, total credited per person
- **v3.0** — Pull statements straight from email and auto-generate a monthly bill summary in Notion.

## Tech stack

- **Java 17**
- **Maven**
- **OkHttp** · **Lombok**

## Getting started

### Prerequisites
- Java 17+
- Maven

### Build

```bash
git clone https://github.com/aadeshwagh/expense-monitor.git
cd expense-monitor
mvn clean package
```

### Run

Open the project in your IDE (IntelliJ IDEA recommended) and run the parser's main class, pointing it at an Axis Bank statement PDF.

## Branches

- **`master`** — stable branch.
- **`features/dev`** — active development.

## Contributing

Issues and pull requests are welcome. Branch off `features/dev` for new work.
