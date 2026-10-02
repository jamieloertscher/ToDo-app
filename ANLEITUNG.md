# Mein Heft – Einrichtung

Mein Heft ist deine eigene App für Kalender, Aufgaben, Noten und Dokumente. Sie besteht aus zwei GitHub-Repos:

- **mein-heft** (öffentlich): Hier liegt nur der Programmcode. GitHub Pages macht daraus deine App-Adresse.
- **mein-heft-daten** (privat): Hier speichert die App deine Termine, Aufgaben, Noten und Dokumente. Nur du hast Zugriff.

Die Einrichtung dauert etwa 15 Minuten und muss nur einmal gemacht werden.

## 1. App-Repo erstellen und hochladen

1. Auf github.com oben rechts auf **＋ → New repository**.
2. Name: `mein-heft`, Sichtbarkeit: **Public**. „Add a README file“ ankreuzen, dann **Create repository**.
3. Im neuen Repo auf **Add file → Upload files** klicken und alle Dateien aus diesem Ordner hineinziehen:
   `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`.
4. Unten auf **Commit changes** klicken.
5. **Settings → Pages**: Bei „Source“ **Deploy from a branch** wählen, Branch **main**, Ordner **/ (root)**, dann **Save**.
6. Nach 1–2 Minuten steht oben deine Adresse, z.B. `https://DEINNAME.github.io/mein-heft/`.

## 2. Privates Daten-Repo erstellen

1. Wieder **＋ → New repository**.
2. Name: `mein-heft-daten`, Sichtbarkeit: **Private** (wichtig!). „Add a README file“ ankreuzen, **Create repository**.

## 3. Zugriffstoken erstellen

Das Token ist wie ein Schlüssel, mit dem die App in dein Daten-Repo schreiben darf – und zwar nur dort.

1. Oben rechts auf dein Profilbild → **Settings**.
2. Ganz unten links **Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
3. Token name: `Mein Heft`. Expiration: so lang wie möglich (danach einfach ein neues erstellen).
4. **Repository access → Only select repositories** → `mein-heft-daten` auswählen.
5. **Permissions → Repository permissions → Contents → Read and write**.
6. **Generate token** und das Token (`github_pat_…`) kopieren. Es wird nur einmal angezeigt – bewahre es sicher auf, z.B. in deinem Passwort-Manager.

## 4. App öffnen und verbinden

1. Öffne deine Adresse aus Schritt 1.
2. Gib deinen GitHub-Benutzernamen, `mein-heft-daten` und das Token ein → **Verbinden**.
3. Fertig! Das machst du auf jedem Gerät einmal (Laptop, Handy).

## 5. Als App installieren

- **Laptop (Chrome/Edge):** In der Adresszeile rechts auf das Installieren-Symbol klicken → **Installieren**. Danach hat Mein Heft ein eigenes Fenster und ein Symbol in der Taskleiste.
- **iPhone (Safari):** Teilen-Symbol → **Zum Home-Bildschirm**.
- **Android (Chrome):** Menü ⋮ → **App installieren** bzw. **Zum Startbildschirm hinzufügen**.

## 6. Daten aus der Claude-Version übernehmen

1. In der Claude-Version: ⚙︎ → **Daten exportieren** → Datei `mein-heft-export.json` speichern.
2. In deiner neuen App: ⚙︎ → **Daten importieren** → diese Datei auswählen.
3. Dokumente lädst du in der neuen App einfach nochmals hoch.

## Gut zu wissen

- Oben rechts siehst du den Speicherstatus. Ein Klick darauf synchronisiert sofort.
- Ohne Internet funktioniert die App weiter; Änderungen werden gespeichert, sobald du wieder online bist.
- Bearbeitest du auf zwei Geräten, werden die Änderungen zusammengeführt.
- Jede Änderung ist im Daten-Repo als Commit sichtbar – du kannst notfalls alte Stände wiederherstellen.
- Dateien bis 25 MB pro Stück. Das Daten-Repo sollte insgesamt unter 1 GB bleiben.
- Steht oben „Token ungültig oder abgelaufen“: neues Token erstellen (Schritt 3), dann ⚙︎ → **Abmelden** und neu verbinden.
- **Updates:** Bekommst du eine neue Version, ersetzt du einfach die Dateien im Repo `mein-heft`. Deine Daten bleiben unberührt.
