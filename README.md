# BNI Ventimiglia – Corsaro Nero

Sito statico con la lista aggiornata dei membri del capitolo BNI Ventimiglia, generato tramite scraping del portale BNI ufficiale.

🔗 **Sito live:** [paolo410.github.io/bni-sanremo](https://paolo410.github.io/bni-sanremo/)

## File

- `bni_scraper.py` — scarica i dati dei membri da BNI e genera `index.html`
- `index.html` — sito generato (non modificare manualmente)
- `img/bni_logo.png` — logo BNI usato nell'header e come favicon
- `requirements.txt` — dipendenze Python (`requests`, `beautifulsoup4`)
- `sitemap.xml` — mappa del sito per i motori di ricerca
- `robots.txt` — regole di indicizzazione per i crawler

## Uso

```bash
pip install -r requirements.txt
python bni_scraper.py
```

## Aggiornamento automatico

GitHub Actions aggiorna `index.html` ogni giorno alle 07:00 (ora italiana).

## SEO e Google Search Console

Il sito include i seguenti elementi per l'indicizzazione:

- **Meta tag** — description, keywords, canonical URL
- **Open Graph / Twitter Card** — anteprima corretta su social e chat
- **Structured Data (JSON-LD)** — schema `Organization` per Google
- **Verifica GSC** — meta tag `google-site-verification` nel `<head>`
- **Sitemap** — `sitemap.xml` da inviare in Search Console → Sitemap

> **Nota:** i meta tag SEO e il tag di verifica Google sono inclusi nel template HTML di `bni_scraper.py`, quindi vengono preservati ad ogni rigenerazione automatica.