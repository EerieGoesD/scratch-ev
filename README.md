# Scratch Ticket & Lottery EV Calculator

Calculate the Expected Value of scratch tickets and lottery games. Compare pre/post-tax return for every game.

**[Live Demo →](https://scratch-ev.eeriegoesd.com)**

![Preview](og-image.png)

## Features

- 74 Portuguese scratch tickets + lottery games (EuroDreams, Lotaria Clássica, Lotaria Popular)
- Pre & post-tax EV with configurable tax rules
- Full comparison table with sorting, target prize filter, CSV export
- Custom game input, save/load, JSON import/export
- Bilingual PT/EN (auto-detected)
- Single HTML file, zero dependencies
- GDPR compliant (cookie consent + GA4 Consent Mode v2)

## Project Structure

```
├── index.html              # Entire app
├── games/
│   ├── index.json          # Game registry
│   ├── scratch-tickets/PT/ # 74 scratch ticket JSONs
│   └── lottery/PT/         # Lottery games
├── og-image.png
├── robots.txt
├── sitemap.xml
└── favicon-*.png
```

## Adding Games

Open `index.html` in a browser. No server needed.

New game JSON format (`games/scratch-tickets/<COUNTRY_CODE>/`):

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

Then add the path to `games/index.json`.

## Add Your Country

Send official prize tables and tax rules to [eeriegoesd@gmail.com](mailto:eeriegoesd@gmail.com).

## Data Sources

**Portugal** — [Jogos Santa Casa](https://www.jogossantacasa.pt) official prize tables. EuroMilhões/EuroDreams official regulations.

## License

MIT

## Author

**EERIE** — [eeriegoesd.com](https://eeriegoesd.com) · [Buy Me a Coffee](https://buymeacoffee.com/eeriegoesd)
