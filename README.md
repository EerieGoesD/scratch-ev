# Scratch Ticket & Lottery EV Calculator

Free browser-based Expected Value (EV) calculator for scratch tickets and lottery games worldwide. Compare return before and after taxes, find the best odds per euro spent, and make informed decisions.

**[Live Demo →](https://scratch-ev.eeriegoesd.com)**

![Preview](og-image.png)

## Features

- **Multi-country support** — currently 74 Portuguese scratch tickets, with more countries coming soon
- **Lottery support** — EuroDreams, Lotaria Clássica, Lotaria Popular
- **Pre & post-tax EV** — configurable tax rate and threshold for any country
- **Full comparison table** — sortable columns, target prize filter, CSV export
- **Custom games** — input any scratch ticket or lottery from anywhere in the world
- **Save & load** — persist custom games in localStorage
- **Import/Export** — share games as JSON files
- **Bilingual** — Portuguese and English (auto-detected)
- **Zero dependencies** — single HTML file, no build tools, no frameworks
- **GDPR compliant** — cookie consent banner, Google Analytics 4 with Consent Mode v2
- **SEO optimized** — Open Graph, Twitter Cards, JSON-LD structured data (FAQ + WebApplication)

## How It Works

Each scratch ticket has a fixed number of tickets and a known prize table. The calculator computes:

- **Expected Value (EV)** — average return per ticket
- **Net EV** — EV minus ticket cost
- **Return %** — percentage of bet returned on average
- **Odds** — probability of winning any prize
- **Post-tax EV** — adjusted for your country's tax rules

For lottery games, EV is estimated using the official payout rate (50–52% of revenue).

## Project Structure

```
├── index.html          # Entire application (HTML + CSS + JS)
├── games/
│   ├── index.json      # Game registry
│   ├── scratch-tickets/
│   │   └── PT/         # 74 Portuguese scratch ticket JSONs
│   └── lottery/
│       └── PT/         # Portuguese lottery games
├── og-image.png        # Social media preview image
├── robots.txt          # Crawler directives
├── sitemap.xml         # Search engine sitemap
└── favicon-*.png       # Favicons at multiple sizes
```

## Usage

Just open `index.html` in a browser. No server required.

To add a new game, create a JSON file in `games/scratch-tickets/<COUNTRY_CODE>/` following this format:

```json
{
  "name": "Game Name",
  "mode": "scratch",
  "cost": 3,
  "totalTickets": 1000000,
  "tiers": [
    { "qty": 200000, "prize": 3 },
    { "qty": 50000, "prize": 10 },
    { "qty": 5, "prize": 100000 }
  ]
}
```

Then add the file path to `games/index.json`.

## Data Sources

- **Portugal** — Scratch ticket prize tables from [Jogos Santa Casa](https://www.jogossantacasa.pt) (planos de prémios oficiais). Lottery odds from official EuroMilhões and EuroDreams regulations.

## Add Your Country

We're expanding to include scratch tickets and lottery games from every country. If you'd like to contribute data from your country, open an issue or email [eeriegoesd@gmail.com](mailto:eeriegoesd@gmail.com).

## License

MIT

## Author

**EERIE** — [eeriegoesd.com](https://eeriegoesd.com) · [Buy Me a Coffee](https://buymeacoffee.com/eeriegoesd)
