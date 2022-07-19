# ZADANIE 1

Utwórz następujący ciąg elementów:

>       <div style="width: 500px;">
>           <span>tekst0</span>
>           <div>
>                <span>tekst1a</span>
>                <span>tekst1b</span>
>           </div>
>           <div>
>               tekst2
>           </div>
>            <div>
>               <span>tekst3</span>
>               <span>tekst4</span>
>           </div>
>            <div style="display: inline;">
>               tekst5
>           </div>
>           <div style="display: inline;">
>               tekst6
>           </div>
>       </div>

Uruchom dev toolsy i inpektuj kolejne elementy. Upewnij się że jesteś w stanie wytłumaczyć: 
1. dlaczego divy znajdujące się wewnątrz głównego ( nadrzędnego diva) nie są szerokie na całą szerokość ekranu
2. dlaczego span z tekst0(el. liniowy) jest nad napisem tekst1a tekst1b mimo ze obydwa są w span (el linowy)
3. Dlaczego tekst6 jest obok tekst5 mimo że znajdują się w div (el blokowym) ?
4. wykorzystując wiedzę o el. liniowym i modelu pudełkowym zwiększ odległość miedzy tekst3 a tekst4
5. zmień pionową odległość między "tekst1a tekst1b" a "tekst2"



# ZADANIE 2

Na podstawie informacji o właściwości display i zachowaniu przy wartościach: inline, block, inline-block spróbuj utworzyć odpowiednik układu tabeli:

>       |-----------------|
>       |                 |
>       |-----------------|
>       |            |    |
>       |            |    |
>       |-----------------|
>       |      |     |    |
>       |-----------------|

Używaj tylko jednego typu elementu np: DIV i zmieniaj jego display stosownie do potrzeb.
Tabela ma mieć szerokość 500px.

Podpowiedzi:
- użyj jednego nadrzędnego elementu jako przechowującego całą zawartość tabeli (komorki z danymi wykonaj jako zagniezdzone elementy)
- dla ustalania szerokości wybranych części użyj właściwośći width
- pamiętaj o modelu pudełkowym i uniwersalnym selektorze *
- jest możliwe że będziesz musiał/a zaadresować konkretną komórkę chcąc przypisać jej konkretną właściwość (np. width). W tym celu uzyj selektora element#wartoscatrybutuid np. dla:


        > <div id="komorka2">
        > wartosc w srodku
        > </div>

    selektor nadający jej właściwość to:

        > div#komorka2 {
        >   width: 200px;
        > }

- wykorzystaj rozciąganie się elementu display: block do utworzenia pierwszej komórki

# ZADANIE 3

Nawiązuje do zadania 2. Spróbuj wykonać stronę która wyświetli różnokolorowe (uzyj własnosci np. background-color: red) elementy w taki sposób aby znajdowały się obok siebie na tyle na ile pozwala szerokość ekranu. Gdy szerokość się zmniejsza elementy przechodzą do nowej linii. Wykorzystaj ementy HTML tego samego typu np DIV.
Utwórz selektor na ten element w którym zwiększysz odstępy między każdym z elementów. Wypróbuj odstępu przy pomocy margin, padding a nawet border (pomocna będzie własność box-sizing) - obserwuj zachowanie elementów przy każdej zmianie.