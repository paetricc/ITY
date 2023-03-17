# Projekt č. 1: Běžné chyby
Zde najdete přehled a vysvětlení nejčastějších chyb v prvním projektu.

* **-2: nepřeložitelné, manuální úprava makefile**
* **-2: nepřeložitelné, manuální úprava zdrojového kódu**
##
* **-1:přetečení sazby overfull**
* **-1:podtečení sazby underfull**

V některých případech se může jednat o vážný prohřešek: v případě většího přetečení nebo podtečení vypadá výsledek velmi neprofesionálně.
Nápomocné je použití parametru 'draft' při psaní (a následné 'final' při hotovém vysázení) jako parametr documentclass.
##

* **-2:vizuální neshoda dokumentu**

Velmi výrazný nesoulad mezi vzorem a vygenerovaným PDF. \
Malé variace ve vzhledu výsledného dokumentu mohou být způsobeny trochu jiným použitím správných značek.\
Tyto rozdíly oproti vzorovému dokumentu obvykle nevedly ke ztrátě bodů.\
Je rozhodně chybou snažit se sazbu násilně upravovat například pomocí \hspace.\
Někdy to však může být nezbytnost.\
Nicméně, nic z tvrdé sazby nebylo v dokumentu použito.\
Další odlišnosti mohou způsobovat různá prostředí pro tisk vícesloupcové sazby (twocolumn coby parametr třídy article, twocolumn jako samostatný balík, multicol - zde už je rozdíl podstatně větší).
##

* **-0.1:špatná úprava**

Drobný nesoulad mezi vzorem a vygenerovaným PDF.\
Častou příčinou je použití špatného formátování některých slov nebo úseku textu (např. nepoužití tučného řezu nebo špatná velikost písma).
##

* **-1:formát strany**
* **-1:nesprávné rozměry strany**
* **-1:chybějící balíček geometry**
Není nastaven parametr a4paper nebo při transformaci ps2pdf používáte letter a ne a4.\
Není použit balík geometry a rozměry textu jsou nastaveny ručně nebo vůbec.\
Standardní nastavení okrajů nepočítá s listem velikosti A4, takže se plýtvá místem.\
Ruční nastavení bez balíku geometry je sice možné, ale rozhodně to není tak přehledné.\
##

* **-0.5:použitý nesprávný font**

Použity jiné fonty, než předepisuje zadání.\
Použití jiné rodiny fontů vede k typograficky zcela odlišnému výsledku.
##

* **-0.5:chybí česká lokalizace (babel)**
* **-0.5:použito manuální dělení slov**

V dokumentu není použit balík babel s parametrem czech. \
Bez toho nebude fungovat české dělení slov, správné odsazování prvních řádků v odstavcích a další věci, kterými se česká sazba liší od anglické. \
Ruční dělení slov stylem "důle- žitých" způsobí problémy v okamžiku, kdy do textu něco připíšete.\
Pokud babel náhodou nemá nějaké slovo ve slovníku, lze použít příkaz \hyphenation nebo příkaz \- přímo v neposlušném slově: "důle\-žitých".\
Podobně nešťastné je vkládání krátkých mezer (\,) v místech, kde chcete zalomení zabránit.
##

* **-0.5:nesprávné kódování fontu (fontenc)**

Nepoužíváte balík fontenc se správným parametrem (IL2 nebo T1, dle zadáni).\
Balík umožní používat lokalizované fonty, u nichž bývají lépe spočítány znaky s diakritikou.\
Správné použití tohoto balíku umožňuje například české fulltextové vyhledávání ve výsledném PDF dokumentu.\
Bez jeho použití (nebo když není vybraný font k dispozici v lokalizované verzi) se znaky s diakritikou vysází na první pohled správně, ale v PDF dokumentu je pak např. písmeno č vysázeno jako cˇ.
##

* **-0:newcommand**

Chybně zapsaný parametr \newcommand.\
Prvním parametrem příkazu \newcommand je název nového příkazu.\
Tento název musí být ve složených závorkách, jinak s tím jsou v některých distribucích LaTeXu potíže.\
Hvězdička \newcommand* se píše, když příkaz nemůže obsahovat \par.
##

* **-0.5:chybí maketitle**

Nadpis článku je vysázen 'na tvrdo' namísto použití \maketitle.\
Vhodnější je v tomto případě použití makra \maketitle, které pracuje s předpřipravenými mezerami.\
Makro \maketitle bylo zmíněno ve 2. přednášce z ITY.
##

* **-1:chybí nezlomitelné mezery (tildy, vlnky)**
* **-0.5:nadbytečné nezlomitelné mezery tam, kde nepatří**

Chybějící nebo špatně užité znaky ~.\
Nepoužitím programu 'vlna' se vystavujete nebezpečí, že váš text se může vysázet chybně (např. po změně textu dokumentu).\
Jedná se o hrubou chybu.\
Pokud jsou vlnky i za vícepísmennými předložkami a spojkami, zvyšuje se pravděpodobnost, že si LaTeX nebude vědět rady se zalomením řádku a začne sázet "za roh" odstavce, do prostoru okraje stránky.
##

* **-0:diakritika nesázena přímo ale pomocí \v, \' apod.**

Pokud háčky a čárky sázíte takto: h'{a}\v{c}ky a \v{c}'{a}rky, pak je zdrojový text nečitelný a nedá se s ním příliš pracovat.\
Navíc bývá takto vysázená diakritika odlišná od diakritiky v českých fontech při použití balíku czech (anglický latex neumí najít optickou osu písmenek, místo toho používá osu geometrickou, takže háčky jsou pak mírně posunuty).\
Pokud tento způsob sazby způsobuje příliš chytrý editor, snažte se tuto vlastnost vypnout.
##

* **-0.5:Chybí sazba nadpisů pomocí \section**
Číslování sekcí svěřte LaTeXu, ruční zadávání 'na tvrdo' není vhodné.\
Degradujete tak LaTeX na úroveň poznámkového bloku.\
Udržování dokumentu při změnách do jeho struktury je pak výrazně náročnější.
##

* **-0.5:použity pevné mezery (vspace, hspace, quad, apod.)**
* **-0.5:manuální nastavení mezer mezi řádky**

Použití násilných mezer (\quad, \hspace, \vspace a pod.), pevných vertikálních mezer \\[velikost], '\kern velikost' a nebo změny mezer stylu pomoci \baselinestretch.\
Místo nich se používají relativní nebo pružné mezery (\ , \,, \stretch, \vfill apod.).\
Tvrdá sazba se rozpadne při změně textu nebo rozměrů strany.\
Často použity místo prostředí 'quotation' nebo '\maketitle', ovšem občas na ně bylo možné narazit i v textu.
##

* **-0:dělení odstavců je lepší dělat pomocí nových řádků než příkazem \par (z hlediska čitelnosti kódu)**
* **-0:manuální odsazení odstavce pomocí \indent by nemělo být potřeba**

Tyto příkazy se používají při tvorbě maker a nových tříd.\
Používání příkazů \par, \indent a \noindent je v běžných dokumentech naprosto zbytečné, a v některých případech to dokonce může rozhodit formátování dokumentu.\
Stejného (lepšího) efektu dosáhnete, když mezi odstavci necháte prázdný řádek.\
Odsazování odstavců je lepší nechat na LaTeXu.
##

* **-0:manuální nastavení odsazení odstavce pomocí \parindent by nemělo být potřeba**
Velikost odsazení prvního řádku odstavce je dáno použitým stylem, nepoužívá se ruční nastavení pomocí \parindent=velikost.\
Zásahy do tohoto nastavení dělejte, jen když víte, proč to děláte.\
Standardní styly jsou navrženy typografickými odborníky a obvykle není důvod je nějak měnit.
##

* **-0.5:násilné odřádkování pomocí newline, linebreak, break, \\, apod.**
Násilně vynucené odřádkování i na konci odstavce (\\, \linebreak nebo \newline) má obvykle za následek, že se konec věty přilepí k pravému okraji.\
V běžném textu je to typografická chyba.\
Uvnitř \title a \author to chyba není.
##

* **-0:nepoužití verb pro sazbu příkazů**
Doporučuji používat \verb pro sázení LaTeX příkazů, (např. místo {\tt \textbackslash textit\{text\}}).
##

* **-0:zvýraznění neděláno pomocí \emph (např. u 'nezlomitelnou mezerou')**
Dávejte přednost značce \emph před značkou \textit.\
Značky \emph lze smysluplně vnořovat do sebe.
##

* **-0.5:ručně dělané odrážky namísto standardního prostředí itemize**

Ručně sázené odrážky v seznamu, například pomocí \bullet.\
Ruční sázení odrážek je zbytečné a nepraktické, seznam (prostředí itemize) si odrážky vysází správné sám.
##

* **-0.1:nesprávně vysázené anglické uvozovky (správně např. \`\`text'')**
* **-0:složitě sázené anglické uvozovky (správně např. \`\`text'')**
* **-0:složitě sázené české uvozovky (správně např. \uv{text})"**

Nevhodně nebo chybně sázené uvozovky.\
Lepší je použít správnou kombinaci znaků, které vytvoří správné uvozovky (např. \`\`anglicke uvozovky''), nebo znaky z unicode.\
Ruční používání příkazů jako \textquotedblleft a \textquotedblright nebo \textquotedbl (s příslušným kódováním T1) je zase příliš pracné.\
Tyto příkazy obvykle slouží pro vytváření maker.
##

* **-0.1:nesprávně vysázené české uvozovky**

Používejte \uv nebo si je předdefinujte např. pomocí \newcommand{\uvcs}[1]{\quotedblbase #1\textquotedblleft}.
##

* **-0.2:nesprávně vysázená pomlčka (správně: \,--\, ; \,---\, ; \,–\, nebo \,—\,)**
* **-0.2:pomlčka místo spojovníku**

Spojovníky - jsou vysázeny jako pomlčky --.\
A opačně, pomlčky jsou sázeny naivním způsobem jako -, namísto -- nebo ---.\
Kolem dlouhé pomlčky ve větě se mají sázet zúžené mezery (správně \,--\, nebo \,---\,).\
Jednoduchá pomlčka použitá uprostřed věty je typografickou chybou.
##

* **-0.5:Odkazy na sekce sázeny 'na tvrdo' nebo nestandardním způsobem (správně: \label a \ref)**
* **-0.25:Referenční body v textu sázeny 'na tvrdo' nebo nestandardním způsobem (správně: \label)**
* **-0.25:Odkazy na referenční body sázeny 'na tvrdo' nebo nestandardním způsobem (správně: \ref)**

Reference na sekce, kapitoly, tabulky nebo třeba obrázky v dokumentu se dělají pomocí příkazů \label a \ref.\
LaTeX zajistí konzistenci odkazů a jejich číslování i při změnách dokumentu.\
Takto vytvořené odkazy navíc lze mít "klikací", kdy při kliknutí dojde k přesměrování čtenáře na odkazovaný element v dokumentu.\
Použití konstrukcí jako např. '\hyperlink{section.2}{2}' nebo '\hyperref[sec:2]{2}' není vhodné, protože musíte sami zajistit konzistenci odkazů při úpravách dokumentu (degradujete tak LaTeX na poznámkový blok).\
Další problém s těmito konstrukcemi je detekce nefunkčních odkazů; odkazy se vysázejí zdánlivě v pořádku, ale nefungují.
##

* **-0.2:nedefinované reference (pravděpodobně nebylo provedeno více průchodů při překladu)**

Varování v souboru s informacemi o překladu.\
Pravděpodobně jste použili správné příkazy pro sázení odkazů, ale zapomněli jste upravit překlad tak, aby odkazy skutečně fungovaly.\
V případě použití odkazů je potřeba vícekrát (většinou stačí dvakrát) provést překlad pomocí příkazu 'latex'.
##

* **-0.2:odkaz na web nedělán pomocí url nebo href**
* **-0.2:mailová adresa nedělána pomocí href nebo url**

Externí odkazy na web nebo email by měly být dělány pomocí \url z balíku url nebo \href z balíku hyperref (možnost nastavení barev). \
Odpadá nutnost kopírování adresy do prohlížeče nebo emailového klienta.
##

* **-0.2:LaTeX by měl být sázen příkazem \Latex**

Pro sazbu názvu LaTeX se používá příkaz \LaTeX.
##

* **-0.1:manuálně vysázeny tři tečky (správně: \dots)**

Výpustku (tři tečky) je vhodné sázet pomocí předpřipraveného příkazu \dots, který zajistí správnou a konzistentní šířku mezer.
##

* **-0.5:nevhodně sázené poznámky pod čarou (správně: \footnote)**

Chybně vysázený příkaz \footnote.\
Používejte raději \footnote než \footnotemark a \footnotetext.\
Tato dvě makra jsou určena spíše pro tvorbu složitějších maker.\
V delším dokumentu se vám mohou takto sázené poznámky pod čarou snadno zpřeházet.\
Úplně scestné je sázet odkazy na poznámky pod čarou pomocí matematického módu jako $^1$.
##

* **-0.5:nepoužito prostředí quotation pro sazbu citace ve 2. sekci**

Použití různých způsobů odsazení odstavce "Čím více druhů..." namísto použití prostředí quotation. \
Obvykle je tato chyba spojena s ručním pozicováním pomocí \hskip, \quad, \qquad, nebo použitím quote + \indent.\
Nápovědu k použití prostředí quotation jste měli explicitně uvedenou ve 2. přednášce z ITY. 
