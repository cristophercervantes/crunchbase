# Crunchbase Query Generator

![version](https://img.shields.io/badge/version-1.0.0-blue) ![license](https://img.shields.io/badge/license-MIT-green)

🌐 **Live Application**  
https://cristophercervantes.github.io/crunchbase/

---

## Overview

The **Crunchbase Query Generator** is a focused web utility that builds targeted Google search queries (Google dorks) to discover acquisition-related information hosted on Crunchbase. It's especially handy for bug bounty hunters, security researchers, competitive intelligence analysts, and anyone performing acquisition or organizational-structure research.

The tool automates year-by-year query generation so you can quickly scan acquisitions or acquired-by results across a timespan without manually composing each search.

---

## Features

- **Smart Query Generation**: Automatically creates clean, time-based search patterns.
- **Dual Search Modes**:
  - **"acquired by"** — find companies acquired by your target.
  - **"acquires"** — find acquisitions made by your target.
- **Year-Range Coverage**: Generates queries from a start year up to the current year.
- **One-Click Copy**: Copy individual queries or the entire set with a single click.
- **Responsive Design**: Works well on desktop and mobile.
- **Clean Interface**: Modern, minimal UI for fast use.

---

## Quick Start

1. **Enter Company Name** — e.g., `Google`, `Microsoft`.
2. **Set Start Year** — choose how far back to search (default: `1990`).
3. **Select Query Type** — "`acquired by`" or "`acquires`".
4. **Generate Queries** — click **Generate**.
5. **Copy & Search** — paste queries into Google and review results.

---

## How It Works — Examples

**Mode: `acquired by`**  
For target `Google`, start year `2010`:

```
site:crunchbase.com "acquired by Google"
site:crunchbase.com "acquired by Google" intitle:"2024"
site:crunchbase.com "acquired by Google" intitle:"2023"
...
site:crunchbase.com "acquired by Google" intitle:"2010"
```

**Mode: `acquires`**  
For target `Google`, start year `2010`:

```
site:crunchbase.com "Google acquires"
site:crunchbase.com "Google acquires" intitle:"2024"
site:crunchbase.com "Google acquires" intitle:"2023"
...
site:crunchbase.com "Google acquires" intitle:"2010"
```

> The tool only generates the queries — it does **not** execute searches. Perform searches in Google manually and obey Google's Terms of Service.

---

## Use Cases

- **Bug Bounty Research** — discover subsidiary entities or acquired teams that may expand attack surface.
- **Security Audits** — map organizational relationships and integration history.
- **Competitive Intelligence** — track acquisition activity and market expansion.
- **Due Diligence** — explore merger & acquisition history during evaluations.

---

## Usage Tips

- Use **`acquired by`** to find companies bought *by* your target.
- Use **`acquires`** to find companies your target has bought.
- Year-specific queries can reduce noise — combine both year-specific and no-year queries for coverage.
- Combine both query modes (and multiple start years) for the most complete picture.

---

## Technical Details

- **Built With**: HTML5, CSS3, Vanilla JavaScript  
- **Styling**: Custom CSS, modern design system  
- **Deployment**: GitHub Pages  
- **Browser Support**: Modern browsers (Chrome, Firefox, Edge, Safari)

**Project Structure**
```
crunchbase-query-generator/
├── index.html          # Main application
├── (embedded CSS)      # Complete styling
├── (embedded JS)       # Application logic
└── README.md           # Documentation
```

---

## Local Development

Clone or download the repo:

```bash
git clone https://github.com/cristophercervantes/crunchbase.git
cd crunchbase
```

Serve the application locally:

```bash
# With Python 3
python -m http.server 8000

# Or with http-server (Node.js)
npx http-server
```

Open `http://localhost:8000` in your browser or simply open `index.html`.

---

## Example Output

Input:
- Company: `Facebook`
- Start Year: `2010`
- Query Type: `acquired by`

Generated:
```
site:crunchbase.com "acquired by Facebook"
site:crunchbase.com "acquired by Facebook" intitle:"2024"
site:crunchbase.com "acquired by Facebook" intitle:"2023"
...
site:crunchbase.com "acquired by Facebook" intitle:"2010"
```

---

## Important Notes & Ethics

- **This tool generates search queries only — it does not run searches.**  
- Always perform searches manually via Google and **respect rate limits** and Google’s Terms of Service.  
- Use this tool for **authorized** security testing, academic research, competitive intelligence, or legal due diligence only.  
- Be mindful of `robots.txt` and site policies on Crunchbase and other sites you query.

---

## Contribution

Contributions are welcome. Ways to help:
- Report bugs and issues via GitHub Issues
- Suggest features or enhancements
- Submit pull requests (PRs) with fixes or new functionality
- Improve documentation or add translations

---

## License

This project is released under the **MIT License**. See `LICENSE` for details.

---

## Support

If you encounter issues:
- Consult the usage tips in the application
- Verify inputs are correctly formatted
- Use a modern browser
- Open an issue on the repository

---

**Acknowledgements**  
Built and maintained by the original author. Thanks to contributors and the open-source community.
