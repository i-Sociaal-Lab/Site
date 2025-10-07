## 🧭 Handleiding – Opbouw van deze GitHub Pages-website

url: i-sociaal-lab.github.io

Deze site is opgebouwd met GitHub Pages en Jekyll.
De inhoud staat in de map /docs, die GitHub gebruikt als basis voor publicatie.

### 📁 Mappenstructuur

- **docs/**
  - `index.md` – hoofdpagina (start)
  - `_config.yml` – site-instellingen
  - `xxx.md` – diverse pagina's
  - **dashboards/**
    - `wachttijden.md`
    - `datakwaliteit.md`
  - **datasets/**
    - `cpb-leeftijdskosten.md`
  - **assets/css/**
    - `custom.scss` – opmaak
    - `favicon.png` – pictogram in browser
    - `logo.png` – logo i-Sociaal Lab
- `README.md` – uitleg voor beheerders
⸻

### 🧩 Werking in het kort
**1.	Markdown-pagina’s** 

Elke webpagina is een .md-bestand.
Bovenin elke pagina staat een YAML-blok (de “front matter”) met instellingen zoals titel, navigatie en volgorde. 

Voorbeeld:
•	title: Wachttijden
•	parent: Data-producten
•	nav_order: 3
•	permalink: /dashboards/wachttijden/        ← exacte pad naar markdown pagina

Dit bepaalt hoe de pagina in het menu verschijnt en naar welke “ouderpagina” (zoals Data-producten) hij hoort.

**2.	Hoofdpagina (index.md)**
Dit is de startpagina van de site.
Alles wat hier staat, wordt als eerste getoond wanneer iemand naar de website-URL gaat.
	
**3.	Stijl (SCSS / CSS)**
In docs/assets/css/custom.scss staat de eigen opmaak (bijv. knoppen en kleuren).
Deze SCSS-file wordt automatisch omgezet naar CSS bij het bouwen van de site.
	
**4.	Configuratie (_config.yml)**
Deze YAML-file bepaalt:
	•	welk thema wordt gebruikt (bijv. just-the-docs)
	•	titel van de site
	•	navigatie-instellingen
	•	links naar GitHub of zoekfunctie

Voorbeeld:

**5.	Thema (Just-the-Docs)**
Het thema verzorgt de layout, zijbalk, zoekbalk en structuur.
De navigatie-hiërarchie wordt automatisch opgebouwd op basis van de parent- en nav_order-velden in de front matter.

⸻

### 🚀 Publicatie
	•	GitHub Pages bouwt de site automatisch bij elke commit naar de main-branch.
	•	De site wordt gepubliceerd op
https://<organisatie>.github.io/<repositorynaam>/
(of op een eigen domein als dat is ingesteld).

⸻

### 💡 Tips voor beheerders
	•	Nieuwe pagina maken? Voeg een nieuwe .md toe in de juiste map en geef hem een title en parent in de YAML-kop.
	•	Tekstopmaak kan gewoon in Markdown (kopjes, lijsten, tabellen, links).
	•	Stijl aanpassen? Bewerk assets/css/custom.scss.
	•	Configuratie wijzigen (titel, thema, navigatie-opties)? Pas _config.yml aan.
