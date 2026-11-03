# Název aplikace

> Jednou větou: k čemu aplikace slouží a pro koho.

## Základní údaje

| | |
|---|---|
| **Úroveň aplikace** | 🟢 zelená / 🟠 oranžová / 🔴 červená (určuje IT) |
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

## Zátěž Abry

Vyplnit, pokud aplikace čte z Abry (viz `CLAUDE.md`, část 4A). Nové napojení nebo vyšší zátěž předem probrat s IT.

| | |
|---|---|
| **Servisní účet** | název účtu (heslo jen ve správci hesel) |
| **User-Agent** | `název-repozitáře/verze` |
| **Agendy a intervaly přes den** | např. `issuedinvoices` každých 15 min (:02, :17, :32, :47) |
| **Dotazů za hodinu přes den** | odhad, limit je 150 |
| **Noční dávky** | co, kdy, kolik dotazů |
| **Zápis do Abry** | ne / ano – písemný souhlas IT ze dne … |

## Kontrola bezpečnosti

Doplňuje Claude při kontrole před nasazením (`CLAUDE.md`, část 2c).

- datum, výsledek, seznam stránek a endpointů s přihlášením a rolí, audit závislostí, co zbývá opravit

## Pojistky pro Clauda

Složka `.claude/` obsahuje háčky, které Claudovi zablokují nebezpečné akce: zápis hesel do souborů, čtení `.env`, `git push --force` na `main`, mazání mimo projekt, `DROP`/`TRUNCATE` a zápis do Abry. Nemažte je. Funkčnost ověří `bash .claude/hooks/test-ochrana.sh`; testy se spouštějí i automaticky na GitHubu spolu s hledáním hesel (gitleaks).

## Známé problémy a poznámky

- …
