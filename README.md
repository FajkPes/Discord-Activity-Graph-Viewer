# Discord Activity Graf Viewer

Jednoduchý lokální prohlížeč počtu zpráv v čase. Nepoužívá server ani externí knihovny.

## Použití

1. Otevři `index.html` v aktuálním Chrome nebo Edge.
2. Klikni na **Načíst složku Zprávy** a vyber složku `Zprávy` z exportu Discordu.
3. Pro zobrazení jmen volitelně načti `Zprávy/index.json` přes **Kanály a lidé** a `Servery/index.json` přes **Servery**; index kanálů doplní jména dalších soukromých konverzací.
4. Přepni graf na dny, týdny nebo roky. Denní graf začíná posledním rokem. Dva úchyty pod grafem přesně vymezují začátek a konec zobrazeného období; ve výchozím stavu je vybraný poslední rok. Vyhlazení je nastavitelné. Roční pohled používá týdenní body pod ročními značkami osy.
5. Aktivitu filtruje jediný seznam nad grafem. Výběr je rozdělený na uživatele a skupiny/servery; přehled konverzací pod grafem je pouze informativní a filtr nemění. Statistiky odpovídají vybranému filtru i období grafu. Pořadí nejaktivnějších konverzací, dnů, hodin a slov zobrazuje prvních 10 výsledků; všechny výsledky lze rozbalit a hledat.

Zpracování probíhá ve stránce prohlížeče. Načtená data se nikam neposílají ani neukládají.

## Počítání

- Každý záznam se započítá jako jedna zpráva, i když nemá text (například obsahuje jen přílohu).
- Počítá se datum a čas ze sloupce `Timestamp` v souborech `messages.json`.
- Při týdenním zobrazení začíná týden pondělím.
- Zprávy se stejným ID se započítají jen jednou.
- Graf doplní období bez zpráv nulou; neplatné záznamy a soubory vypíše jako přeskočené.
- Jeden výběr umožňuje zobrazit všechny zprávy, soukromé konverzace s jednotlivými uživateli, skupinové konverzace nebo aktivitu na serveru. Veřejná verze nemá přednastavená osobní ID; jména načítá z vašeho exportu.
- Frekvence slov počítá jednotlivá slova v textových zprávách; běžná česká slova a odkazy vynechává. Výpočty probíhají pouze v prohlížeči.
- Jestliže Discord označil protistranu jako odstraněný účet, export její původní jméno neobsahuje a konverzace se proto zobrazí s ID.


## Veřejné vydání

Otevřete `index.html` v Chrome nebo Edge. Soukromé zprávy, archivy exportů, indexy uživatelů/serverů a osobní mapování ID nejsou součástí repozitáře ani ZIP. Vlastní export načtěte až lokálně v prohlížeči.
