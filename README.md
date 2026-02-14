# De Reuzentrekkers 🎭

Website van de Reuzentrekkers — de groep die sinds 2013 de Mestreechse Govies door de straten trekt tijdens carnaval.

🌐 **Live:** [reuzentrekkers.nl](https://reuzentrekkers.nl)

## Structuur

```
public/
├── index.html          # Hoofdpagina
├── afbeeldingen/       # Foto's
│   └── historisch/     # Historische foto's tijdlijn
```

## Deployen

Site wordt gehost op Netlify. Push naar `main` triggert automatisch een deploy.

- **Publish directory:** `public`
- **Build command:** _(geen, static HTML)_

## Lokaal bekijken

```bash
cd public
python3 -m http.server 8000
# of
npx serve public
```

Open [localhost:8000](http://localhost:8000)
