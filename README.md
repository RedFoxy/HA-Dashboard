# HA-Dashboard

[Italiano](#italiano) | [English](#english)

---

## Italiano

Qui dentro ci sono le dashboard che uso davvero sul mio Home Assistant. Le ho messe online perché più di una persona mi ha chiesto "come hai fatto quella card?", quindi invece di mandare screenshot e pezzi di YAML in giro ho fatto prima a pubblicare tutto.

Non è un pacchetto da installare e far partire. Sono file YAML presi così come sono dalla mia installazione, con i miei nomi delle entità e le mie immagini. Prendeteli come spunto, copiate le parti che vi servono e adattatele al vostro impianto.

### Cosa c'è

| File | Cosa mostra |
|------|-------------|
| `3d-printer.yaml` | Stampante 3D Bambu Lab X1C con due AMS: stato della stampa, slot dei filamenti, umidità e temperatura degli AMS, errori HMS |
| `solar-panels.yaml` | Impianto fotovoltaico con inverter Growatt: produzione, batteria in carica e scarica, consumi e storico |
| `tesla.yaml` | La mia Tesla (si chiama KITT): batteria, ricarica, clima, porte e finestrini, pressione gomme, posizione sulla mappa |
| `ups-battery.yaml` | UPS APC SU2200INET: carico, carica e autonomia delle batterie, temperatura, con una soglia minima regolabile |
| `vacuum.yaml` | Robot aspirapolvere (Bartolomeo) con mappa e pulizia per singola stanza |
| `wallbox.yaml` | Wallbox per la ricarica dell'auto: avvio e stop, corrente di ricarica, stato e consumi |

### Card personalizzate usate

Quasi tutte le dashboard usano card che non sono incluse in Home Assistant. Le trovate su HACS:

- [Mushroom](https://github.com/piitaya/lovelace-mushroom) (tesla, solar-panels, wallbox, 3d-printer)
- [button-card](https://github.com/custom-cards/button-card) (wallbox, 3d-printer)
- [bar-card](https://github.com/custom-cards/bar-card) (solar-panels, ups-battery, wallbox)
- [config-template-card](https://github.com/iantrich/config-template-card) (3d-printer)
- [tabbed-card](https://github.com/kinghat/tabbed-card) (3d-printer)
- [ha-bambulab](https://github.com/greghesp/ha-bambulab) con la sua card di stampa (3d-printer)
- [auto-entities](https://github.com/thomasloven/lovelace-auto-entities) e [vertical-stack-in-card](https://github.com/ofekashery/vertical-stack-in-card) (ups-battery)
- [xiaomi-vacuum-map-card](https://github.com/PiotrMachowski/lovelace-xiaomi-vacuum-map-card) e [layout-card](https://github.com/thomasloven/lovelace-layout-card) per il layout masonry (vacuum)

Se una card vi appare come "Custom element doesn't exist", di solito manca una di queste.

### Come usarle

1. Installate le card che servono da HACS.
2. Create una nuova dashboard (o una nuova vista) e aprite l'editor YAML dalla modalità di modifica.
3. Incollate il contenuto del file che vi interessa.
4. Sostituite le entità con le vostre. Le mie hanno nomi in italiano perché il mio Home Assistant è in italiano, quindi il cerca e sostituisci sarà la parte più lunga.
5. Alcune card puntano a immagini in `/local/` (cioè la cartella `www` di Home Assistant). Quelle immagini non sono nel repository, quindi mettete le vostre oppure togliete i riferimenti.

### Note

Le dashboard cambiano man mano che modifico qualcosa a casa, quindi può capitare che un file venga aggiornato o che qualcosa si rompa con una nuova versione di Home Assistant o di una card. Se trovate un errore o avete un'idea, aprite pure una issue.

---

## English

These are the dashboards I actually use on my Home Assistant. I put them online because people kept asking me "how did you make that card?", and publishing everything was easier than sending screenshots and YAML snippets around.

This isn't a package you install and run. They're YAML files taken straight from my setup, with my entity names and my images. Use them as a starting point, copy the parts you need and adapt them to your own system.

### What's inside

| File | What it shows |
|------|---------------|
| `3d-printer.yaml` | Bambu Lab X1C 3D printer with two AMS units: print status, filament slots, AMS humidity and temperature, HMS errors |
| `solar-panels.yaml` | Solar setup with a Growatt inverter: production, battery charge and discharge, consumption and history |
| `tesla.yaml` | My Tesla (its name is KITT): battery, charging, climate, doors and windows, tyre pressure, location on a map |
| `ups-battery.yaml` | APC SU2200INET UPS: load, battery charge and runtime, temperature, plus an adjustable minimum threshold |
| `vacuum.yaml` | Robot vacuum (Bartolomeo) with map and per-room cleaning |
| `wallbox.yaml` | EV wallbox: start and stop, charging current, status and energy use |

### Custom cards used

Most dashboards rely on cards that don't ship with Home Assistant. You can get them from HACS:

- [Mushroom](https://github.com/piitaya/lovelace-mushroom) (tesla, solar-panels, wallbox, 3d-printer)
- [button-card](https://github.com/custom-cards/button-card) (wallbox, 3d-printer)
- [bar-card](https://github.com/custom-cards/bar-card) (solar-panels, ups-battery, wallbox)
- [config-template-card](https://github.com/iantrich/config-template-card) (3d-printer)
- [tabbed-card](https://github.com/kinghat/tabbed-card) (3d-printer)
- [ha-bambulab](https://github.com/greghesp/ha-bambulab) and its print card (3d-printer)
- [auto-entities](https://github.com/thomasloven/lovelace-auto-entities) and [vertical-stack-in-card](https://github.com/ofekashery/vertical-stack-in-card) (ups-battery)
- [xiaomi-vacuum-map-card](https://github.com/PiotrMachowski/lovelace-xiaomi-vacuum-map-card) and [layout-card](https://github.com/thomasloven/lovelace-layout-card) for the masonry layout (vacuum)

If a card shows up as "Custom element doesn't exist", one of these is usually missing.

### How to use them

1. Install the cards you need from HACS.
2. Create a new dashboard (or a new view) and open the YAML editor from edit mode.
3. Paste the contents of the file you want.
4. Replace the entities with yours. Mine have Italian names because my Home Assistant runs in Italian, so search and replace will take most of the time.
5. Some cards point to images under `/local/` (that's the `www` folder in Home Assistant). Those images aren't in the repository, so add your own or remove the references.

### Notes

The dashboards change whenever I change something at home, so files may get updated, and something might break with a new Home Assistant or card release. If you spot a problem or have an idea, feel free to open an issue.
