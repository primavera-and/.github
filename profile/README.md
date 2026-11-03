# Primavera Andorrana – interní aplikace

Tady jsou všechny interní aplikace firmy. Většinu z nich píšou manažeři s pomocí Clauda („vibe coding“). Chceme to podporovat. Claude ale umí napsat aplikaci, která funguje, a přitom pouští data ven. Proto platí pár pravidel.

**Kód patří firmě, ne autorovi.**

## Best practices pro vibe kodéry (stačí přečíst tohle)

1. **Než začnete, zavolejte IT.** Pět minut: co to bude dělat a s jakými daty. IT založí repozitář ze šablony a určí úroveň aplikace.
2. **Pracujte v repozitáři ze šablony.** Je v něm `CLAUDE.md` s pravidly a Claude podle nich sám dělá bezpečnostní kontroly. Nemažte ho a neříkejte Claudovi, ať ho ignoruje.
3. **Když Claude hlásí 🔴 nebo „zavolejte IT“, poslechněte ho.** Neobcházejte ho jiným zadáním.
4. **Hesla nikdy do chatu ani do kódu.** Patří do firemního správce hesel a do souboru `.env`. Když heslo někam omylem uteče, hned volejte IT. Heslo se musí změnit.
5. **Nejdřív plán, potom kód.** U přihlašování, osobních údajů, mazání dat a Abry nechte Clauda nejdřív popsat, co udělá.
6. **Když to funguje, uložte to.** Řekněte Claudovi „commitni to“. Vždycky se pak dá vrátit k poslednímu funkčnímu stavu.
7. **Malé kroky.** Jedna změna, vyzkoušet, uložit. Ne „předělej celou aplikaci“.
8. **Zkoušejte na testovacích datech.** Nikdy ne na ostré Abře nebo na skutečných zákaznících.
9. **Před spuštěním pro ostatní řekněte Claudovi „hotovo, zkontroluj to“.** Udělá celkovou kontrolu a zapíše ji do README. U oranžových a červených aplikací ji pak projde IT.
10. **Aplikace pro víc lidí běží jen na firemních serverech.** Ne na vašem počítači, ne na Vercelu ani na podobných službách.

## Úrovně aplikací

| Úroveň | Typicky | Co je potřeba |
|---|---|---|
| 🟢 **Zelená** | Jen čte data, používá ji autor nebo malý tým, žádné osobní údaje zákazníků. | Repozitář ze šablony, README, zápis v registru. |
| 🟠 **Oranžová** | Zapisuje data, pracuje s osobními údaji, nebo ji používá víc lidí či oddělení. | Navíc kontrola IT před nasazením, testovací kopie, zálohy, přihlašování. |
| 🔴 **Červená** | Dostupná z internetu pro lidi mimo firmu, zapisuje do Abry, posílá e-maily zákazníkům, platby. | Navíc schválení návrhu IT **před začátkem**, bezpečnostní kontrola a zátěžový test. |

## Pravidla organizace

- Každá aplikace je v organizaci `primavera-and`, ne na osobním účtu.
- Každá aplikace je zapsaná v registru aplikací a má **správce a zástup**.
- Napojení na Abru, Google a další služby jen přes servisní účet od IT. Výchozí oprávnění je jen pro čtení. Účtů do Abry je omezený počet, proto je přiděluje jen IT a aplikace je mohou sdílet.
- Nové domény, externí služby a předplatné jen přes IT, a to i ty „zkušební“.
- Aplikaci, kterou už nikdo nepoužívá, IT vypne a repozitář archivuje.

## Kdy hned volat IT

- Heslo nebo token se dostal do chatu, do kódu nebo na GitHub.
- Aplikace smazala nebo přepsala data.
- Někdo cizí má přístup, kam nemá.
- Aplikace nefunguje a závisí na ní práce ostatních.

Kontakt: IT oddělení
