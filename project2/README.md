# Zadání projektu č. 2
Instrukce jsou velmi podobné jako v prvním projektu. Vaším úkolem je opět vytvořit v LaTeXu dokument, který bude co nejvíce odpovídat vzorovému PDF dokumentu.

* Na titulní straně uveďte své **jméno a login**.
* Chybějící nebo nefunkční [**Makefile**](http://www.fit.vutbr.cz/~martinek/clang/make.html.cs) povede ke ztrátě až 7 bodů.
* Po odevzdání si zkuste své řešení stáhnout z IS a zkontrolujte, že je opravdu **přeložitelné na merlinovi**. Nepřeložitelný projekt pravděpodobně povede na 0 bodů.
* Pozorně čtěte text v zadaném PDF. Obsahuje **instrukce a nápovědy**.
* **Používejte vhodné příkazy a konstrukce** pro sázení seznamů, odkazů, rovnic, titulní strany, definic, nadpisů atd. Za ruční sázení "na tvrdo" budu strhávat body.
* Stejně jako u prvního projektu se nesnažte za každou cenu dosáhnout naprosto totožného vzhledu jako u vzorového dokumentu. Je lepší použít správné konstrukce LaTeXu s mírně odlišným vzhledem (nemusí vést ke ztrátě bodů), než používat triky vedoucí k "dokonalé" kopii vzoru (určitě vede ke ztrátě bodů). Například **budu strhávat body za umělé horizontální a vertikální mezery** s výjimkou titulní strany a použití \quad v první rovnici v sekci 2.

* Z AmS balíků byly použity příkazy \newtheorem a \binom, plus další příkazy pro sázení speciálních symbolů. Dále byly až na pár výjimek použity příkazy uvedené na přednáškách (sázení rovnic, matematických výrazů, indexů, mocnin, matic atd.).
  * Body se budou strhávat i **za stejné chyby jako v prvním projektu**. Snažte se je tedy neopakovat.

## Textová verze dokumentu
Máte k dispozici soubor vzor_text.txt. Najdete v něm text vzorového dokumentu, ze kterého byly odstraněny všechny LaTeXové příkazy, konstrukce a matematické zápisy. Ušetří vám psaní a překlepy, ale přesto si svůj výsledný text samy pečlivě zkontrolujte.


## Základní informace o parametrech dokumentu
* rozměry stránky: A4
* sazba na dva sloupce: parametr 'twocolumn' dokumentové třídy 'article'
* font: times 11pt
* rozměry textové oblasti: 18,2 x 25,2 cm
* mezera vlevo: 1,4 cm
* mezera nahoře: 2,3 cm
* kódování fontu: IL2
* kódování zdrojového textu (volitelné): utf8

## Informace k překladu dokumentu
Vzorový dokument byl vysázen LaTeXem těmito nástroji:
* latex
* dvips -t a4
* ps2pdf

## Odevzdání
Odevzdávejte 2 soubory:
* proj2.tex – zdrojový soubor  
* Makefile – pro překlad příkazem "make"

Své odevzdané řešení můžete v systému ponechat ve stavu návrh pro potřeby dodatečných úprav v rámci lhůty pro vypracování projektu – I projekty ve stavu návrh budou chápány jako korektně odevzdané.