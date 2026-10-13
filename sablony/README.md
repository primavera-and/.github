# Název aplikace

> Jednou větou: k čemu aplikace slouží a pro koho.

## Základní údaje

| | |
|---|---|
| **Správce (odpovědná osoba)** | jméno, e-mail |
| **Zástup** | jméno, e-mail |
| **Uživatelé** | kdo aplikaci používá (oddělení, země) |
| **Kde běží** | server Czechia (název / IP), URL aplikace |
| **Technologie** | jazyk, framework, databáze |
| **Data** | s jakými daty pracuje (zákazníci, objednávky, osobní údaje ano/ne) |
| **Napojení** | Abra (Web API), Google, Mapy.cz, … – přes jaký servisní účet |
| **Kde jsou hesla** | položka ve firemním správci hesel (název), **nikdy ne v kódu** |
| **Zálohy** | co se zálohuje, jak často, kam |

## Instalace

```bash
git clone git@github.com:primavera-and/NAZEV-REPA.git
cd NAZEV-REPA
cp .env.example .env   # doplnit hodnoty ze správce hesel
# instalace závislostí, např.:
# npm install   /   pip install -r requirements.txt
```

## Spuštění

```bash
# lokálně pro vývoj
# na serveru (služba / docker compose / pm2 …)
```

## Aktualizace na serveru

```bash
cd /cesta/k/aplikaci
git pull
# migrace databáze, restart služby …
```

## Obnova ze zálohy

1. Kde zálohy leží a jak se k nim dostat.
2. Jak obnovit databázi.
3. Jak obnovit soubory / konfiguraci.
4. Jak ověřit, že aplikace po obnově funguje.

## Proměnné prostředí (.env)

| Proměnná | Popis | Kde vzít hodnotu |
|---|---|---|
| `ABRA_API_URL` | adresa Abra Web API | správce hesel |
| `ABRA_API_USER` | servisní účet | správce hesel |

## Známé problémy a poznámky

- …
