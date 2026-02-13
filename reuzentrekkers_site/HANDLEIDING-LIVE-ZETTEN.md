# Reuzentrekkers.nl live zetten (GRATIS)

## Wat je nodig hebt

- TransIP-account (heb je al — daar staat je domein reuzentrekkers.nl)
- Een gratis Netlify-account
- De map `reuzentrekkers_site` met alle bestanden

## Stap 1 — Netlify account aanmaken (gratis)

1. Ga naar https://www.netlify.com en klik **Sign up**
2. Maak een account aan (kan met e-mail of GitHub)

## Stap 2 — Site uploaden

1. Na inloggen, ga naar https://app.netlify.com
2. Je ziet een scherm met "Drag and drop your site output folder here"
3. Sleep de hele `reuzentrekkers_site`-map naar dat vlak
4. Klaar! Je site is nu live op een tijdelijke URL (bijv. `random-naam-123.netlify.app`)
5. Test of alles werkt

## Stap 3 — Je eigen domein koppelen (reuzentrekkers.nl)

### In Netlify:
1. Ga naar **Domain management** → **Add a custom domain**
2. Typ `reuzentrekkers.nl` en klik **Verify** → **Add domain**
3. Netlify geeft je nameservers, bijv:
   - `dns1.p01.nsone.net`
   - `dns2.p01.nsone.net`

### In TransIP:
1. Log in op https://www.transip.nl/cp/
2. Ga naar **Domeinen** → **reuzentrekkers.nl** → **DNS**
3. Kies **Nameservers wijzigen**
4. Vervang de TransIP-nameservers door die van Netlify
5. Sla op. Dit kan 1-24 uur duren om actief te worden.

### SSL (https://):
Netlify regelt automatisch een gratis SSL-certificaat. Na het koppelen van het domein klik je op **Verify DNS** en dan **Provision certificate**.

## Stap 4 — Testen

1. Open https://reuzentrekkers.nl in je browser
2. Check of de site er goed uitziet op desktop en mobiel
3. Test de taalschakelaar (Mestreechs / Nederlands)
4. Test de "Mail ons" knop

## Site bijwerken

Als je iets wilt aanpassen (tekst, foto's):

1. Pas het bestand aan op je computer (in een teksteditor)
2. Ga naar Netlify → **Deploys**
3. Sleep de hele map opnieuw naar het upload-vlak
4. Klaar — de site is direct bijgewerkt

## Tekst aanpassen

1. Open `index.html` in een teksteditor (VS Code, Notepad++, of zelfs Kladblok)
2. Zoek de tekst die je wilt aanpassen (Ctrl+F / Cmd+F)
3. **Belangrijk:** Pas BEIDE taalversies aan:
   - `data-lang="ms"` = Maastrichts
   - `data-lang="nl"` = Nederlands
4. Sla op en upload de map opnieuw naar Netlify

### Voorbeeld: datum volgende optocht aanpassen

Zoek naar `15 februari 2026` en vervang door de nieuwe datum. Dit staat op twee plekken: de Maastrichtse en Nederlandse versie.

### Voorbeeld: foto toevoegen

1. Zet de foto in de `afbeeldingen/`-map
2. Voeg in `index.html` een `<figure>` toe in de galerij-sectie:
```html
<figure class="gal-item" onclick="openLB(this)">
    <img src="afbeeldingen/jouw-foto.jpg" alt="Beschrijving">
    <figcaption>Bijschrift</figcaption>
</figure>
```
3. Upload de hele map opnieuw naar Netlify

## E-mail instellen: info@reuzentrekkers.nl (gratis)

Via ImprovMX (gratis) kun je alle mail naar @reuzentrekkers.nl doorsturen naar je eigen e-mailadres.

1. Ga naar https://improvmx.com
2. Vul in: domein `reuzentrekkers.nl`, forward naar je eigen e-mailadres
3. ImprovMX geeft je DNS-records (2x MX + 1x TXT)
4. Ga naar TransIP → Domeinen → reuzentrekkers.nl → DNS
5. Verwijder bestaande MX-records
6. Voeg de ImprovMX-records toe
7. Wacht 5-30 minuten → klaar!

Alle mail naar info@reuzentrekkers.nl (of elk ander @reuzentrekkers.nl adres) komt dan in je eigen inbox.

## Nog te doen

- **Vrouwelijke govie foto**: Sla de foto op als `afbeeldingen/historisch/govie-vrouwelijk-1992.jpg`

## Kosten

- **Netlify**: Gratis (voor statische sites)
- **ImprovMX**: Gratis (e-mail forwarding)
- **TransIP domein**: ~€10/jaar (heb je al)
- **Totaal: ~€10/jaar**
