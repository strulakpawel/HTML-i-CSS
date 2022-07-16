# ZDFRONpol13

## Model pudełkowy

### Budowa modelu pudełkowego

> margin - *margines zewnętrzny*\
> przykładowa własciwość CSS:\
> margin: 10px;
>>border - *obwódka*
>> przykładowa własciwość CSS:\
>> border: 10px solid black;
>>> padding - *margines wewnętrzny*
>>> przykładowa własciwość CSS:\
>>> padding: 10px;
>>>> content - *miejsce na zawartość*\
>>>> Tutaj wyswietlane sa elementy tresci\
>>>> tj. inne divy, h1, p ...


### wymuszenie/zmiana sposobu obliczania wymiaru elementu przez przeglądarke:

> h1 { box-sizing: content-box; }

Domyslny. Podanie wartosci przy wlasciwosci width spowoduje uzycie tej wartosci jako wymiar TYLKO czesci content modelu pudelkowego.

Jeśli margin wynosi 10 (lewy i prawy), border wynosi 3 (lewy i prawy), padding 5 (lewy i prawy) a szerokosc ustalilismy na 300. To lacznie odległość od lewego kranca lewego marginesu do prawego kranca prawego marginesu wyniesie 336 (szerokosc 300 + padding 2 * 5 + border 2 * 3 + margin 2*10).


> h1 { box-sizing: border-box; }

Podanie wartosci przy wlasciwosci width spowoduje uzycie tej wartosci jako ŁĄCZNY wymiar czesci content, padding i border modelu pudelkowego.
Jeśli margin wynosi 10 (lewy i prawy), border wynosi 3 (lewy i prawy), padding 5 (lewy i prawy) a szerokosc ustawilismy na 300. To lacznie odległość od lewego kranca lewego marginesu do prawego kranca prawego marginesu wyniesie 320 (szerokosc 300 plus prawy i lewy margines czyli 300 + 2*10).


## Właściwość CSS "display"

Przykład użycia:

> h1 {
>    display: block;
> }

> span {
>    display: inline;
>}

### Wartość block

*"zawsze zabieram własną nową linię na swoje potrzeby i przepycham następujace po mnie elementy do nowej linii"*

Block respektuje ustalanie dla niego szerokości.
Ta szerokosc wplywa na obszar "content" modelu pudelkowego - czyli na szerokosc dostępną dla zawartości elementu. Szerokość nie zmienia zachowania polegającego na zajmowaniu całej linii.

### Wartość inline

*"Jesli sąsiedzi mi pozwalaja jestem obok nich. nie możesz nadawać mi rozmiaru. Rozciągam się stosownie do mojej zawartości"*

Element display:block przed elementem z display:inline zawsze wypchnie tego drugiego do nowej linii

### Wartość inline-block

*"jestem jak inline ale możesz nadać mi konkretna szerokosc i bede to respektował"*

## Przykład interakcji elementow  roznymi displayami

> inline\
> block\
> inline

>block\
>zwyklytekst\
>block\
>block

> block\
> inline\
> block

>inline inline\
>block

> block\
> inline-block inline inline-block inline\
> block

*zwroccie uwage na zachowanie zwyklego tekstu. jest ono podobne do inline*

## Niesemantyczne elementy inline i block

### DIV blokowy

### SPAN inline

## Uwaga!!!
Na naszym etapie myslimy o elemencie blokowym jako rozciagajacym sie na cala szerokosc ekranu.

To uproszczenie. Tak naprawdę element blokowy rozciąga sie na cała szerokość elemenu w ktorym sie znalazł.

> body
>> div style="width: 50%;"
>>> div id="nasz" style="width: 50%;"

W powyzszym ukladzie div o id="nasz" będzie miał  25% szerokości ekranu.

nie powinnismy zagnieżdżać elementów blokowych w elementach inline ani inline-block.

Pamiętamy również że dowolny element możey zmienic z blokowego w inline poprzez własciwosc CSS display

