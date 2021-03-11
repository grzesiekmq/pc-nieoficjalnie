# Część II - edytor


## 

<p id="gdcalert13" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image13.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert14">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image13.png "image_tooltip")



## 


##  Rozdział 3 \
 UI


## 

<p id="gdcalert14" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image14.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert15">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image14.png "image_tooltip")


<p id="gdcalert15" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image15.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert16">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image15.png "image_tooltip")



###  3.1 Panel hierarchia


### 

<p id="gdcalert16" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image16.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert17">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image16.png "image_tooltip")



        Panel hierarchii zawiera graf sceny, widok drzewa. Graf ten składa się z korzenia,

domyślnie nazywa się on Root, w tym przypadku na rysunku nazywa się **Main**, może też nazywać się Game.

Main w tym przypadku jest rodzicem takich encji jak:  \
Camera, Board i Room Light, Board Folder, Dice1, Dice2, Tokens, Tile Owned, Houses, PropertyEntities, Walls, Cards, Colours, Furniture, New UI, Money, Property Cards, Property Lights i MainEntity.  \
Jest to fragment gry planszowej Monopoly.

Dodatkowo te encje są rodzicami (wskazuje na to znaczek plusa) innych encji itd. 

Jak widzisz ta struktura jest bardzo złożona, dlatego tak ważne jest grupowanie obiektów, np. jak to zostało przedstawione na rysunku. Grupowanie obiektów to jedna z dobrych praktyk.

Hierarchiczna struktura pozwala na dobrą organizację elementów gry.

Jako mała dygresja: dlatego popatrz jak to jest realizowane na innych przykładach gier stworzonych w PlayCanvas, przejdź do strony PlayCanvas (musisz być zalogowany, zarejestrowany aby widzieć zawartość EXPLORE, gdy już się zalogujesz przejdź do explore, zobaczysz tam różne projekty, kliknij na **Project **przy danym projekcie.

Ja wybrałem SWOOP, jest to gra typu endless runner.



<p id="gdcalert17" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image17.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert18">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image17.png "image_tooltip")


, przejdzie to do dalej overview projektu



<p id="gdcalert18" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image18.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert19">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image18.png "image_tooltip")


 kliknij **EDITOR**,



<p id="gdcalert19" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image19.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert20">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image19.png "image_tooltip")


 kliknij na scenę w tym przypadku Game i już możesz zobaczyć hierarchię.



<p id="gdcalert20" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image20.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert21">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image20.png "image_tooltip")


Pokażę jeszcze parę innych hierarchii

np. hierarchię ze Space Buggy



<p id="gdcalert21" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image21.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert22">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image21.png "image_tooltip")


Ciężko jest uchwycić na obrazku całą, rozwiniętą hierarchię.

Pokażę jeszcze jedną hierarchię z gry **Accelerally **i na tym zakończę o hierarchiach.



<p id="gdcalert22" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image22.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert23">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image22.png "image_tooltip")


Niektóre projekty mają zablokowaną opcję **Project **(np. TANX), można tylko nacisnąć PLAY aby zagrać w grę , rysunek poniżej.



<p id="gdcalert23" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image23.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert24">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image23.png "image_tooltip")



### 


### 3.2 Panel Zasoby



<p id="gdcalert24" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image24.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert25">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image24.png "image_tooltip")


Zasoby jest najlepiej organizować w folderach, np. skrypty w **scripts**, materiały w **materials**, modele w **models**, tekstury w **textures **itp.

Po lewej na rysunku widzisz strukturę folderów: **/** to korzeń (root) w nim znajdują się foldery w tym przypadku: scripts, Chance, Community Chest, CSS, Furniture, HTML, Money, Other, Properties, Tokens, podobnie tak jak to masz zorganizowane w systemie plików na systemie operacyjnym.

Po prawej widać foldery i pliki, foldery wyżej wymienione, 2 pliki: loading.js i redirect.js

Tutaj możesz przesłać swoje zasoby poprzez upload, możesz przefiltrować kategoriami (tu gdzie jest All), wyszukać dany zasób (Search), dodać nowy zasób lub usunąć istniejący, możesz też wejść na PlayCanvas Store.


### 3.3 Panel inspektor



<p id="gdcalert25" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image25.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert26">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image25.png "image_tooltip")


 

Tutaj możesz włączyć / wyłączyć encję (Enabled), nazwać encję (Name)

dodać tagi (Tags), ustawić transformację: pozycję (position), orientację (rotation) i rozmiar (scale).

Co ważne wszystkie te własności są w przestrzeni **lokalnej**, modelu (local space, model space).

Orientację ustawia się przy pomocy tak zwanych kątów Eulera.

Możesz też dodać komponenty (+ add component).

W tym przypadku dodanym komponentem jest komponent script w nim znajduje się kod ui.js.

Encja może mieć wiele doczepionych skryptów js, np. UIHandler, Main, Money, Dice, Movement, Cards, PropertyLight, assets, \
jak to zostało pokazane na rysunku.



<p id="gdcalert26" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image26.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert27">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image26.png "image_tooltip")


To tyle na temat inspektora, zostało jeszcze do mówienia menu i toolbar.

Przejdę do menu.


### 3.4 Panel Menu



<p id="gdcalert27" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image27.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert28">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image27.png "image_tooltip")


 

Menu można pokazać klikając na przycisk z ikoną PlayCanvas.

Menu zawiera listę wszystkich poleceń, które możesz wykonać na scenie.

Tutaj można zrobić następujące rzeczy, dodać encję, edytować, uruchomić grę, dostać się do pomocy, wyświetlić listę dostępnych scen, opublikować grę, wypalić mapę świateł, otworzyć ustawienia, ustawić priorytet wykonywania skryptów.

Ogólnie jest to skrót jeżeli nie możesz znaleźć przycisku lub nie pamiętasz skrótu klawiszowego. 


### 3.5 Panel Toolbar



<p id="gdcalert28" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image28.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert29">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image28.png "image_tooltip")


Panel toolbar, pasek narzędzi zawiera najczęstsze polecenia dostępne w wygodny sposób.

Najbardziej przydatny jest przycisk uruchom (skrót ctrl+enter), który włącza grę w nowej karcie, wczytywana jest scena na której się znajdujesz i po załadowaniu możesz testować, grać.



<p id="gdcalert29" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image29.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert30">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image29.png "image_tooltip")



### 3.6 Viewport


### 

<p id="gdcalert30" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image30.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert31">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image30.png "image_tooltip")


Viewport pokazuje scenę aktualnie wyświetlaną. Możesz poruszać się po scenie z klawiszami WASD i strzałkami góra, dół, lewo, prawo. Trzymając shift przyspieszasz prędkość kamery, możesz w ten sposób przeglądać scenę szybciej, jeżeli np. przestrzeń jest duża, np. tu. 

Jest to model miasta, mod do gry Assetto Corsa, tutaj bardzo przydatny jest sposób szybkiego przeglądania sceny.



<p id="gdcalert31" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image31.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert32">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image31.png "image_tooltip")


Wracając do viewportu możesz ustawić kamerę na perspektywę lub ortograficzną, w przypadku orto są to widoki lewo, prawo, góra, dół, przód, tył (left, right, top, bottom, front, back). Jeszcze możesz zmienić na widok z innej kamery, np. kamery śledzącej (jeżeli taką ustawiłeś w hierarchii). Na tym przykładzie dodatkowe kamery to SplashCamera i Camera. Na marginesie kamery to po prostu macierze.



<p id="gdcalert32" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image32.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert33">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image32.png "image_tooltip")


Teraz przejdę do omówienia części dotyczącej silnika.
