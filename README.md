# ⚡ StrujaMeter — HEP Kalkulator

PWA aplikacija za praćenje i izračun troškova električne energije prema aktualnim HEP tarifama.

🔗 **[Otvori aplikaciju](https://borisorbis.github.io/strujameter/)**

---

## Značajke

- 📊 Podrška za sve HEP tarifne modele — **jednotarifni (JT)**, **dvotarifni (VT/NT)** i **dirigirano brojilo (DIR)**
- 🧮 Točan izračun prema HEP cjeniku (distribucija, prijenos, opskrba, OIE, PDV)
- 📅 Povijest očitanja s grafikonima potrošnje po kWh i €
- ⚠️ Upozorenje pri prekoračenju praga od 3000 kWh (uvećanje +35%)
- 💾 Podaci se čuvaju lokalno u pregledniku (localStorage)
- 📤 Export u PDF i Excel
- 🌙 Tamni / svijetli način prikaza
- 📱 Instalabilno kao PWA — radi offline

---

## Tarifni modeli

| Model | Opis |
|-------|------|
| **Jednotarifni (JT)** | Jedna tarifa cijeli dan |
| **Dvotarifni (VT/NT)** | Viša tarifa danju, niža noću |
| **Dirigirano brojilo (DIR)** | Kontrolirano upravljanje — R1 i R2 registar |

---

## Instalacija kao PWA

1. Otvori u Chrome/Safari
2. Na mobitelu: izbornik → **"Dodaj na početni zaslon"**
3. Na desktopu: ikona instalacije u adresnoj traci
4. Aplikacija radi **offline** nakon prve posjete

---

## Tehnologije

- Vanilla HTML / CSS / JavaScript (bez frameworka)
- [Chart.js](https://www.chartjs.org/) — grafikoni
- [jsPDF](https://github.com/parallax/jsPDF) — PDF export
- [SheetJS](https://sheetjs.com/) — Excel export
- Service Worker — offline podrška i PWA

---

## Ažuriranje cjenika

Cijene se mogu ručno urediti u postavkama (hamburger izbornik → Cijene) ili učitati iz JSON datoteke `hep_tarife.json`.

Format JSON datoteke:
```json
{
  "distJT": 0.023933,
  "prijenosJT": 0.008175,
  "opskrbaJT": 0.037686,
  "ommJT": 1.043000,
  "nakOpskrbaJT": 0.053000,
  "distVT": 0.044446,
  "prijenosVT": 0.021256,
  "opskrbaVT": 0.097189,
  "distNT": 0.020514,
  "prijenosNT": 0.008175,
  "opskrbaNT": 0.047688,
  "ommDvot": 1.983000,
  "nakOpskrbaDvot": 0.982000,
  "distDIR": 0.037608,
  "prijenosDIR": 0.014716,
  "opskrbaDIR": 0.091324,
  "ommDIR": 1.983000,
  "nakOpskrbaDIR": 0.982000,
  "OIE": 0.013239,
  "solidarna": 0.003982,
  "PDV": 13,
  "prag": 3000,
  "uvecanje": 35
}
```

---

## Autor

**Boris Orbis** — [github.com/BorisOrbis](https://github.com/BorisOrbis)

---

*Napomena: Izračuni su informativni i temelje se na javno dostupnom HEP cjeniku. Za službeni obračun uvijek se osloni na HEP-ov račun.*
