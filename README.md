# Noctua · Schlaftagebuch

Persönliches Schlaftracking mit Fokus auf Histamin-Analyse und Apple-Watch-Integration.

---

## 🚀 Deployment auf Vercel — Schritt für Schritt

### Schritt 1: Projekt auf GitHub hochladen

**Variante A: Über die GitHub-Weboberfläche (einfach, kein Terminal nötig)**

1. Gehe auf [github.com](https://github.com) → **"New repository"** (grüner Button oder Plus oben rechts)
2. Name: `noctua-schlaftracker` (oder wie du magst)
3. **Private** auswählen (damit deine Gesundheitsdaten nicht öffentlich werden)
4. **NICHT** "Add a README" ankreuzen
5. Klick **"Create repository"**
6. Auf der nächsten Seite: **"uploading an existing file"** anklicken
7. Alle Dateien aus diesem Ordner reinziehen (per Drag & Drop):
   - `package.json`
   - `vite.config.js`
   - `index.html`
   - `.gitignore`
   - Ordner `src/` (komplett)
   - Ordner `public/` (komplett)
   - Diese `README.md`
8. Unten **"Commit changes"** klicken

**Variante B: Mit Git-Terminal (für Technik-Affine)**

```bash
cd noctua-schlaftracker
git init
git add .
git commit -m "Initial commit - Noctua v1.2"
git branch -M main
git remote add origin https://github.com/DEIN-USERNAME/noctua-schlaftracker.git
git push -u origin main
```

### Schritt 2: Auf Vercel deployen

1. Gehe auf [vercel.com](https://vercel.com) und melde dich an (mit GitHub)
2. Klicke **"Add New..." → "Project"**
3. Suche dein Repository `noctua-schlaftracker` in der Liste
4. Klicke **"Import"**
5. Vercel erkennt automatisch, dass es ein Vite-Projekt ist — einfach **"Deploy"** klicken
6. Warte ~1 Minute — fertig!
7. Du bekommst eine URL wie `noctua-schlaftracker-xyz.vercel.app`

### Schritt 3: Auf dem Handy als App hinzufügen (optional, empfohlen)

Damit es sich wie eine echte App anfühlt:

**iPhone (Safari):**
1. Öffne deine Vercel-URL in Safari
2. Teilen-Button (Quadrat mit Pfeil) → **"Zum Home-Bildschirm"**
3. Name bestätigen → **"Hinzufügen"**
4. Jetzt hast du Noctua als App-Icon auf deinem Homescreen

**Android (Chrome):**
1. Öffne die URL in Chrome
2. Menü (drei Punkte) → **"App installieren"** oder **"Zum Startbildschirm"**

---

## 🔄 Updates einspielen

Wenn du später eine neue Version möchtest (z.B. `App.jsx` mit neuen Features):

**Weboberfläche:**
1. In deinem GitHub-Repo → `src/App.jsx` öffnen → Stift-Symbol zum Editieren
2. Kompletten Inhalt ersetzen → **"Commit changes"**
3. Vercel baut automatisch neu (~1 Min)

**Lokal (falls du lokal entwickelst):**
1. Änderungen machen
2. `git add . && git commit -m "Update" && git push`

---

## 💾 Wo liegen meine Daten?

Deine Schlaftracking-Daten liegen **im localStorage deines Browsers** auf dem jeweiligen Gerät. Das bedeutet:

- ✅ Keine Cloud, keine Datenbank, keine Kosten
- ✅ Daten bleiben lokal — niemand anders hat Zugriff
- ⚠️ Pro Gerät getrennt: Handy und Laptop haben unterschiedliche Daten
- ⚠️ Bei Browser-Datenlöschung sind die Daten weg

**Deshalb wichtig:** Regelmäßig Backup erstellen (Daten-Tab → Export als JSON).

---

## 🛠 Lokale Entwicklung (optional)

Falls du auf deinem Computer testen willst, bevor du deployst:

```bash
npm install
npm run dev
```

Dann öffnet sich die App unter `http://localhost:5173`.

---

## 📋 Version

v1.2 — Erste Vercel-Version (statt Claude-Artifact)

Made by Chang · Physiques Unlimited
