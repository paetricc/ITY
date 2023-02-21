# Zadání projektu č. 1
Vaším úkolem je vytvořit v LaTeXu dokument, který bude co nejvíce odpovídat vzorovému PDF dokumentu.

* **Nesnažte se za každou cenu dosáhnout naprosto totožného vzhledu jako u vzorového dokumentu.** Při hodnocení projektu je kladen důraz především na použití správných konstrukcí LaTeXu a ne na maximální vizuální podobu dokumentů. Je lepší použít správné konstrukce LaTeXu s mírně odlišným vzhledem, než používat triky vedoucí k "dokonalé" kopii vzoru (např. vkládání umělých horizontálních nebo vertikálních mezer), které ve výsledku spíše povedou ke ztrátě bodů.
* I samotný dokument, který máte vysázet, obsahuje užitečné informace ke správnému vypracování projektu. Text dokumentu si proto pozorně přečtěte!
Příkazy použité při vysázení dokumentu byly, až na pár výjimek, uvedeny na přednáškách z ITY. Některé dříve neuvedené příkazy, které ale budete potřebovat pro korektní vysázení dokumentu, jsou zmíněny v textu dokumentu. Při vysázení dokumentu však bylo použito i několik dříve neuvedených příkazů, které by však nemělo být příliš náročné dohledat (i to patří k praktickému používání LaTeXu).
* Pozor si dejte zejména na použití správných příkazů k vysázení výčtů, sekcí a poznámek pod čarou. Dále si dejte pozor na správné vysázení adres webových stránek, e-mailu a odkazů na sekce (v poslední sekci dokumentu). Na všechny adresy a odkazy v dokumentu lze myší kliknout a při kliknutí Vás přesměrují na relevantní část dokumentu nebo externí zdroj. Při přejetí kurzorem myši přes odkazy rovněž dojde k jejich zvýraznění.
* U odkazů na sekce si dejte pozor na správný překlad projektu; v případě nesprávného překladu může dojít k tomu, že místo odkazů se v dokumentu objeví pouze symboly "??".
Nezapomeňte ve svém dokumentu uvést své jméno a e-mailovou adresu.

## Textová verze dokumentu
Při přepisu textu dokumentu je možné použít jeho textovou verzi, která neobsahuje formátování. **Věnujte však pozornost následujícím informacím.**

* Pomlčky a spojovníky jsou v textové verzi dokumentu reprezentovány pouze znakem -. Ve vysázeném dokumentu musí být správná šířka pomlček, spojovníků a mezer podle kontextu.
* V textové verzi jsou použity tyto "dvojité uvozovky". Ve vysázeném dokumentu musí být uvozovky podle vzorového PDF (když nepoužijete UTF-8, řešte české uvozovky pomocí předdefinovaného příkazu).
* Adresy (e-mail, http) a odkazy na číslované sekce (Sekce 2 a 3) nebo poznámky pod čarou jsou v textové verzi vysázeny tzv. "na tvrdo". Ve výsledném PDF však musí být vysázeny speciálními LaTeX příkazy k tomu určenými.

## Základní informace o parametrech dokumentu
Použití správných parametrů sázeného dokumentu je klíčové pro dosažení vizuálně podobného řešení.

* rozměry stránky: A4
* rozměry textové oblasti: 18x24,7 cm
* mezera vlevo: 1,6 cm
* mezera nahoře: 1,5 cm
* font: standardní 10 pt
* kódování zdrojového textu (volitelné): utf8
* kódování fontu: T1
* sazba na dva sloupce: parametr 'twocolumn' dokumentové třídy 'article'


## formace k překladu dokumentu
Vzorový dokument byl vysázen LaTeXem těmito nástroji:

* latex
* dvips -t a4
* ps2pdf

## Odevzdání
Odevzdávejte pouze zdrojový soubor s příponou .tex a soubor Makefile.