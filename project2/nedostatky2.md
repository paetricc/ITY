# Projekt č. 2: Komentář k chybám
Značná část opravování je prováděna automatizovaným skriptem. Ten ale může někdy srazit body za
něco, co je správně (tzv. false alarm) v případě, že je správná konstrukce zapsaná netypickým
způsobem. Na vyrušení false alarmů používám ruční korekce, které se v součtu bodově vynulují s false
alarmy. 


## Překlad
**\# -7:nepřeložitelné pomocí make**\
**\# -8:nepřeložitelné**\
První srážka znamená, že projekt nešel přeložit voláním "make". Druhá srážka znamená, že projekt nešel přeložit ani ručně. Obě dohromady končí na nula bodech.

**\# -2: nefunkční makefile (jednoduchá manuální oprava)**\
**\# -5: nepřeložitelné, manuální úprava zdrojového kódu**\
Tyto dvě srážky nahrazují ty dvě předchozí v případě, že se mi daný problém podařilo rychle opravit. Typický problém v Makefile bylo použití mezer místo tabulátorů pro odsazení, překlad jinak než pomocí "make" (např. make pdf), zapomenuté přepsání z "proj1.tex" na "proj2.tex", smazání vytvořeného PDF na konci překladu atd. Pro určení přeložitelnosti je směrodatný překlad na serveru merlin.


## Časté chyby (více než 30 výskytů) seřazené podle počtu výskytů
**\# -0.2:chybí nezlomitelné mezery (tildy, vlnky) pro spojku 'a'**\
**\# -0.8:chybí nezlomitelné mezery (tildy, vlnky) pro předložky a/nebo spojky**\
Vysvětlení najdete v přednáškách a v běžných chybách z prvního projektu. Srážku za nezlomitelné mezery před 'a' jsem zmírňoval, protože to měli špatně skoro všichni (v projektu byly sloupce širší než 25 znaků). 

**\# -0.5:chybí nezlomitelné mezery (tildy, vlnky) před příkazem \ref, \eqref a nebo \pageref**\
V dokumentu bylo jasně řečeno, že měly být použity nezlomitelné mezery před příkazy pro sázení odkazů. V mnoha případech byly nezlomitelné mezery v úvodu, ale chyběly v odkazu na rovnici (2) v druhé sekci. V těchto případech jsem srážku zmírňoval korekcí.  

**\# -0.2:mezi číslem a jednotkou píšeme zúženou mezeru (např. 0{,}4\,em a 0{,}3\,em)**\
V dokumentu bylo explicitní upozornění na to, že mezera mezi číslem a jednotkou vyžaduje speciální pozornost. Lze nalézt v přednášce.

**\# -0.2:nesprávně vysázená pomlčka (správně: \,--\, ; \,---\, ; \,–\, nebo \,—\,)**\
Viz běžné chyby z prvního projektu.

**\# -0.5:titulní strana - nepoužita explicitní velikost řádku**\
V dokumentu bylo jasně řečeno, že na titulní straně měla být použita explicitní velikost odřádkování. 

**\# 3x-0.2:Odkaz na referenční bod 1-3 sázen 'na tvrdo' nebo nestandardním způsobem (správně: \ref nebo \eqref)**\
**\# -0.5:Odkazy na stránky sázeny 'na tvrdo' nebo nestandardním způsobem (správně: \pageref)**\
Viz běžné chyby z prvního projektu. Navíc bylo jasně zdůrazněno přímo v dokumentu.

**\# -0.1:chybí použití velikosti závorky X**\
V rovnici (2) měli být použity 3 *explicitní* velikosti závorky. Body jsem strhával, když použití velikostí úplně/částečně chybělo (např. jen 2 explicitní velikosti a jedna výchozí). Pokud byly velikosti závorek jen trochu odlišné zadání (tj. ne zřejmě výrazně mimo), snažil jsem se srážky rušit kompenzacemi. 

**\# -0.5:násilné odřádkování pomocí newline, linebreak, break, \\, apod.**\
Viz běžné chyby z prvního projektu. Výjimkou je použití na titulní straně a v konstrukcích array a eqnarray.

**\# -0.1:chybí použití symbolu X**\
Pokud jste použili jiný symbol, který vypadal dostatečně podobně, tak jsem srážku kompenzoval korekcí.

**\# -1:varování - nedefinované reference (pravděpodobně nebylo provedeno více průchodů při překladu)**\
Viz běžné chyby z prvního projektu.

**\# -1:podtečení sazby 'underfull'**\
Viz běžné chyby z prvního projektu.

**\# -1:použity pevné mezery (vspace, hspace, quad, apod.)**\
Viz běžné chyby z prvního projektu. Výjimkou byla první (nečíslovaná, tj. ne rovnice (1)) rovnice v druhé sekci.

**\# -0.5:titulní strana - nepoužit zlatý řez (mezery 0.382 a 0.618)**\
V dokumentu bylo jasně řečeno, že má být použit *přesný* zlatý řez. Většina řešení byla navíc součástí přednášky.

## Ostatní chyby specifické pro druhý projekt
**\# -0.2:chybí použití \binom pro kombinační čísla**\
V dokumentu bylo jasně řečeno, že máte použít příkaz \binom (ne ručně \array, \pmatrix, ...). 

**\# -1:chybí použití \newtheorem (pro Definice a Věty)**\
V dokumentu bylo jasně řečeno, že máte použít příkaz \newtheorem. Ruční sázení a číslování teorémů, vět a definic je nejen pracné, ale vede k nejednotnému stylu, chybám s číslováním a odkazováním.

**\# -1:chybí použití \eqnarray pro skupinu vzorců (Rovnice (1), (2) a (3))**\
Skupiny vzorců se sází pomocí eqnarray nebo align, aby zůstaly vzájemně zarovnány (rovnítka pod sebou). Prostředí align je z balíku amsmath a obvykle vypadá trochu lépe než eqnarray, které je zase použitelné i bez balíků od AMS. Prostředí eqnarray se umí zalomit na konci stránky (což může i nemusí být žádoucí).

**\# -1: špatné použití array**\
**\# -0.2: špatné použití eqnarray**\
V prostředí eqnarray a array je nutné používat znaky '&' pro oddělení sloupců. Není správně zapsat celou matici v jednom sloupci a vkládat ručně mezery. Podobně u eqnarray není vhodné vkládat ručně mezery pro zarovnání rovnítek pod sebe bez použití sloupců pomocí '&'.

**\# -X: vizualni odlisnost titulni strany**\
Body jsem strhával v případě, že byla vizuální odlišnost příliš velká i s přihlédnutím ke zdrojovému kódu. Pokud kód vypadal dobře, ale přesto byla titulní strana vizuálně jiná, tak jsem body nestrhával. Důvodem pro strhnutí bylo třeba zcela jasně výrazně špatná velikost fontu, špatné pořadí řádků textu, nepoužití textsc, relativní velikost mezi řádky (název fakulty větší než školy), špatné zalomení řádků,...

**\# -X: vizuální odlišnost dokumentu**\
**\# -X: individuální srážky, za obsah dokumentu odlišný od zadání**\
Pokud jste měli vše v kódu správně, ale přesto dokument vypadal i výrazně jinak, tak jsem body nestrhával. V této kategorii jsou především "ostatní" individuální chyby, kterých jsem si všiml při  hodnocení. Příkladem bylo špatné zarovnání nuly (vlevo místo na střed) v rovnici s kombinačním číslem, chybějící některý symbol, chybějící části textu/slova,...

## Dále viz běžné chyby z prvního projektu
* přetečení sazby
* sázení poznámek pod čarou
* font a jeho velikost a kódování
* česká lokalizace
* velikost stránky a okrajů
* chybějící a nadbytečné nezlomitelné mezery