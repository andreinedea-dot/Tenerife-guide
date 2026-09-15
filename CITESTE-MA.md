# Ghid Tenerife — cum îl pui online

Folderul ăsta e aplicația completă. Ca să devină aplicație pe telefon,
trebuie pusă pe o adresă `https`. Durează vreo zece minute, o singură dată.

---

## Pasul 1 — pune folderul online

### Varianta cea mai simplă: Netlify Drop

1. Dezarhivează folderul pe calculator
2. Intră pe **app.netlify.com/drop**
3. Trage folderul întreg în pagină (nu fișierele separat — folderul)
4. Primești un link de forma `https://ceva-aleatoriu.netlify.app`

Nu e nevoie de cont ca să încerci. Dacă îți faci cont gratuit, poți
schimba numele linkului în ceva memorabil și poți actualiza mai târziu.

### Alternativă: GitHub Pages

1. Creezi un repository nou, public
2. Încarci toate fișierele din folder în rădăcină
3. Settings → Pages → Source: `main`, folder `/ (root)`
4. După un minut primești `https://numele-tau.github.io/numele-repo/`

---

## Pasul 2 — instalează pe telefon

### iPhone
1. Deschide linkul **în Safari** (nu Chrome — pe iOS doar Safari poate instala)
2. Butonul Share, jos în mijloc
3. **Add to Home Screen**
4. Gata — apare ca aplicație, cu iconiță

### Android
1. Deschide linkul în Chrome
2. Apare singur un banner „Instalează aplicația", sau
3. Meniul cu trei puncte → **Adaugă la ecranul de pornire**

---

## Pasul 3 — verifică că merge offline

1. Deschide aplicația o dată, cu internet
2. Lasă-o deschisă vreo zece secunde
3. Pune telefonul pe modul avion
4. Deschide din nou aplicația — trebuie să funcționeze normal

Dacă merge, ești acoperit. Cache-ul rămâne pe telefon.

---

## Cum actualizezi la o versiune nouă

1. Înlocuiești fișierele în Netlify sau GitHub (Netlify: tragi noul folder peste)
2. Deschizi aplicația pe telefon
3. Prima deschidere arată încă versiunea veche — **închide-o complet și redeschide-o**
4. Acum e versiunea nouă

**Datele tale nu se pierd** — planul pe zile, bifele, activitățile proprii și
pozele stau separat de cod. Dar fă oricum o copie înainte, din pagina
„Datele mele": e gratuit și durează două secunde.

---

## Ce e în folder

| Fișier | Rol |
|---|---|
| `index.html` | Aplicația întreagă — ghid, cod, date |
| `manifest.webmanifest` | Numele, iconița, culorile pentru instalare |
| `sw.js` | Service worker-ul — face aplicația să meargă offline |
| `icon-*.png` | Iconițele |
| `apple-touch-icon.png` | Iconița pentru iPhone |

Toate trebuie să stea în **același folder**, altfel nu se instalează.

---

## Dacă ceva nu merge

**Nu apare „Add to Home Screen" pe iPhone** — ești în Chrome sau Firefox.
Doar Safari poate instala aplicații web pe iOS.

**Nu merge offline** — deschide aplicația din linkul https, nu din fișier local.
Service worker-ul nu pornește de pe `file://`.

**Versiunea veche rămâne după actualizare** — închide aplicația complet
(scoate-o din lista de aplicații recente) și redeschide-o.

**Am pierdut datele** — încarcă fișierul de copie din pagina „Datele mele".
De asta merită făcut export din când în când.
