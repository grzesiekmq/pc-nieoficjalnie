# Część III - silnik


# 

<p id="gdcalert33" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image33.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert34">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image33.png "image_tooltip")



## 


##  Rozdział 4 \
 skrypty  



<p id="gdcalert34" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image34.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert35">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image34.png "image_tooltip")



### 3.1 inicjalizacja i aktualizowanie

** 	 initialize()  **

Metoda `initialize `odnosi się do inicjalizacji, która wykonywana jest tylko raz dla

encji do której został dodany skrypt po załadowaniu się aplikacji. Korzystasz z tej

metody, gdy chcesz zdefiniować zmienne i stałe dotyczące konkretnej instancji skryptu,

czyli np. **<code>this.speed</code></strong>, gdzie <strong><code>this </code></strong>odnosi się do skryptu, nie do <code>window</code>, a speed to

nazwa zmiennej dostępna w `initialize `i `update`, w ten sposób możesz przekazać

zmienną<code> <strong>this</strong>.speed</code> z initialize do update.

** 	 update(dt)  **

Aktualizacja może być realizowana poprzez zastosowanie animacji czasowej

(time-based) lub klatkowej (frame-based). Jeżeli nie korzystasz z dt, czyli różnicy czasu

(delta time) stosujesz animację klatkową. Skutkiem jest brak płynności w animacji.

Natomiast gdy dorzucisz **dt** otrzymujesz wtedy płynną animację na podstawie czasu, a

nie klatek na sekundę (fps). Dlatego najczęściej mnoży się parametr przez dt, np. **<code>this.speed * dt</code></strong>.


### 3.2 atrybuty aka `attributes.add()`  

Dzięki atrybutom otrzymujesz możliwość szybszych iteracji, tzn jesteś w stanie

eksperymentować z parametrami, tworząc i testować grę szybciej, np jeżeli jesteś

designerem, a nie programistą, możesz dostosowywać parametry bezpośrednio z poziomu

edytora zamiast w kodzie. Koncepcja podobna do Unity.

Nawet nie potrzebujesz korzystać z dat.GUI.

Nie ma sensu stosować atrybutów jeżeli pracujesz engine-only, dlatego że nie masz

wtedy dostępu do edytora.

Dostępne atrybuty:



*   encji
*   zasobu



*   
koloru


*   
krzywej


*   
wyliczenia


*   
JSON
** encji**

Jednym ze sposobów nawet lepszym niż korzystanie z find (find ogólnie jest wolną operacją, może dlatego że korzysta z rekurencyjnego wyszukiwania w głąb, DFS) jest odwoływanie się do encji poza skryptem za pomocą atrybutu encji. Podajesz nazwę atrybutu encji, jej typ. 

Na poniższym przykładzie odwołuję się do car, po to aby w ui mieć informację na temat prędkości samochodu. Załóżmy, że encja car posiada skrypt CarController, wtedy mogę się dostać do CarController przy pomocy tego atrybutu encji car. 


```
Ui.attributes.add('car', {type: 'entity'});
```


** **

A tutaj można zauważyć efekt dodania powyższej linii i sparsowania kodu (musisz nacisnąć jeszcze Parse).



<p id="gdcalert35" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image35.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert36">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image35.png "image_tooltip")


Zauważ, że car i Car różnią się między sobą tym że pierwsze dotyczy nazwy **atrybutu **encji, a drugie nazwy encji w hierarchii, więc zachowaj czujność!

Albo jak chcesz znajdź inny sposób, np. nazwij obydwa inaczej, to już zostawiam Tobie jako, może nie wyzwanie, ale mikrozadanie.

Można też skorzystać z innego sposobu i nic nie przyczepiać, sposobem tym są zdarzenia o których później. 

** zasobu**

**       **Atrybut zasobu pozwala na odwołanie się do zasobu znajdującego się w projekcie,

Można podać tylko typ jako zasób, czyli` type: 'asset'` lub ograniczyć tylko do wybranego typu zasobu: tekstura, model, materiał itd.

Celem takiego zabiegu jest minimalizacja ewentualnej pomyłki, jeśli nie możesz podczepić zasobu każdego typu, tylko wybranego, jesteś w stanie upewnić się, że możesz przeciągnąć do slotu np. tylko tekstury, a nie model czy materiał, aby to zrobić musisz dodać jeszcze właściwość assetType i typ konkretnego zasobu:


```
MyScript.attributes.add('texture', { type: 'asset', assetType: 'texture' });
```


**      **

**                 **

**                 **

**koloru**

Atrybut koloru pokazuje color pickera, Możesz jako typ podac ‘rgb’ lub ‘rgba’.


```
MyScript.attributes.add('color', { type: 'rgba' });
```


**krzywej**

Atrybut krzywej określa wartość, która zmienia się w czasie


```
MyScript.attributes.add('wave', { type: 'curve' }); // one curve
```


**wyliczenia**

Dzięki atrybutowi wyliczenia możesz wybrać jedną wartość spośród kilku opcji.

Właściwość enum jest tablicą obiektów, czyli opcji.


```
Car.attributes.add('value', {
    type: 'number',
    enum: [
        { 'valueOne': 1 },
        { 'valueTwo': 2 },
        { 'valueThree': 3 }
    ]
});
```


W edytorze działa to jak dropdown, czy HTML’owy `&lt;select>`



<p id="gdcalert36" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image36.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert37">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image36.png "image_tooltip")


**JSON**

Atrybut JSON jest nowym atrybutem, pozwala na zagnieżdżanie atrybutów, czyli nadaje się do złożonych struktur związanych z grą, Przykład poniżej dotyczy konfiguracji gry.

Kluczowa jest tu właściwość schema, która jest tablicą obiektów i zawiera definicje atrybutów, ale jest to już dość specyficzny przypadek.


```
MyScript.attributes.add('gameConfig', {
    type: 'json',
    schema: [{
        name: 'numEnemies',
        type: 'number',
        default: 10
    }, {
        name: 'enemyModels',
        type: 'asset',
        assetType: 'model',
        array: true
    }, {
        name: 'godMode',
        type: 'boolean',
        default: false
    }]
});
```


To są wszystkie możliwe atrybuty skryptu. Przejdę teraz do koncepcji zdarzeń.


### 3.3 Komunikacja - zdarzenia

Komunikacja może występować jako przesyłanie parametrów od skryptu do skryptu, czyli np. pomiędzy dwoma encjami lub dotyczyć aspektu globalnego, tzn związanego ze zdarzeniami aplikacji. 

Taki sposób posiada jedną zaletę, nie trzeba dzięki temu sprawdzać co klatkę z instrukcjami warunkowymi if.

zdarzenia skryptA-skryptB

Tak jak wspomniałem wcześniej zamiast korzystać z atrybutów encji i przeciągać encję do slotu można to zrealizować przy pomocy zdarzeń skryptowych. Jeśli chodzi o zdarzenia typu skryptA do skryptB, jest to bezpośrednia metoda, a co za tym idzie szybsza niż w przypadku zdarzeń aplikacji.

W zdarzeniach skryptowych stosuje się specjalne metody fire(), on() i off().

fire() wyzwala zdarzenie, on() wykorzystywane jest w celu nasłuchiwania, a off() wyłącza nasłuchiwanie.


```
class Player extends pc.ScriptType{
...
    update(dt) {
       const x = 1;
       const y = 1;
       this.fire('move', x, y);
    }
}
```


W metodzie update() wywoływane jest zdarzenie z fire() i podawana jest nazwa zdarzenia w tym przypadku ‘move’ z przekazywanymi od Player do Display parametrami x, y.


```
class Display extends pc.ScriptType{

    initialize() {
        // method to call when player moves
        const onPlayerMove = function(x, y) {
            console.log(x, y);
        };

        // listen for the player move event
        this.playerEntity.script.player.on('move', onPlayerMove);

        // remove player move event listeners when script destroyed
        this.playerEntity.script.player.on('destroy', function() {
        this.playerEntity.script.player.app.off('move', onPlayerMove);
        });
    }
} 
// set up an entity reference for the player entity
Display.attributes.add('playerEntity', { type: 'entity' });
```


Klasa Display otrzymuje parametry x i y, dokładniej chodzi o metodę wywołania zwrotnego (callback) nazwaną tutaj onPlayerMove(). Jeżeli gracz poruszy się, zostanie wyświetlona w konsoli wartość x i y, `console.log(x, y);`

Aby dostać się do skryptu player, musisz odpowiednio odnieść się do encji gracza (this.playerEntity), dostać się do komponentu script, aż w końcu do skryptu player.

W on() przekazujesz nazwę zdarzenia ‘move’ z poprzedniej klasy (tzn zależy co piszesz najpierw czy zaczynasz od części zawierającej fire() czy on() ).

Wyłączasz ‘move’ z metodą off().

W taki oto sposób już wiesz jak działa komunikacja pomiędzy dwoma skryptami, tutaj było to Display i Player.

zdarzenia aplikacji

Aplikacja stanowi centralny magazyn w kontekście zdarzeń, nie musisz odwoływać się do encji. 


```
...
update(dt) {
    const x = 1;
    const y = 1;
    this.app.fire('player:move', x, y);
} 
```


Na tym przykładzie zauważ sposób pisania nazwy zdarzenia.

Widzisz, że nazwa zdarzenia składa się z player i move oddzielonym dwukropkiem.

Więc taki sposób zapewnia na uniknięcie konfliktu nazw, np jeżeli masz więcej ‘move’, to dobrym rozwiązaniem jest zastosowanie pewnej przestrzeni nazw, czyli np. tak jak powyżej.

fire() wyzwala zdarzenie ‘player:move’ z parametrami x i y.


```
initialize() {
    // method to call when player moves
    const onPlayerMove = function(x, y) {
        console.log(x, y);
    };

    // listen for the player:move event
    this.app.on('player:move', onPlayerMove);

    // remove player:move event listeners when script destroyed
    this.on('destroy', function() {
        this.app.off('player:move', onPlayerMove);
    });

}
```


on() jest nasłuchiwaczem zdarzenia ‘player:move’, kluczowe jest tu **<code>this.app.on()</code></strong> i <strong><code>this.app.off()</code></strong>, dotyczą one zdarzeń aplikacji.

Wynik działania jest ten sam, zostanie wypisana w konsoli wartość x i y.

Z on() i off() mogłeś się już spotkać przy event-driven programming, fire() jest specyficzną metodą w PlayCanvas, a przynajmniej jej nazwa.

Przejdę teraz do grafiki, czyli mocnej strony tego silnika.


## 


## Rozdział 5  \
Grafika

PlayCanvas ma zaawansowany silnik renderowania (rendering engine).

Korzysta pod spodem z WebGL API do rysowania prymitywów (linii, punktów,

krzywych itd.). 

W tym rozdziale przedstawię elementy grafiki takie jak: kamera, oświetlenie,

renderowanie oparte na fizyce (szczególną uwagę poświęcę materiałom PBR), system

cząsteczek i postprocessing.

Nie skupiam uwagi na renderingu statycznej siatki i siatki typu skinned (static and

skinned mesh rendering).

 


### 5.1 Kamera

W WebGL nie ma czegoś takiego jak kamera, jest to po prostu macierz. 

Ale dzięki silnikowi gier, mamy dostęp do zaimplementowanej kamery. 

Kamera jest obiektem, który odpowiedzialny jest za wyświetlanie obrazu sceny na

ekranie. 

Posiada różne właściwości: pole widzenia, płaszczyzny przycinania bliskiej i dalekiej

(near, far clip) itd., ale jest to temat o CameraComponent, który znajduje się w dalszej

części dotyczącej komponentów. 

W PlayCanvas są w 2 typy projekcji kamer: perspektywa i ortogonalna.

Perspektywa polega na tym, że obiekty dalej położone są mniejsze, a bliżej położone

większe, dlatego sprawia to wrażenie, że obraz jest w 3D.

Perspektywę miałeś okazję widzieć, gdy pokazywałem mod z modelem miasta.

Kamera ortogonalna dobrze sprawdza się w grach typu 2D lub 2.5D, zwane też pseudo3D

(izometryczne) rysunek poniżej.



<p id="gdcalert37" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image37.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert38">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image37.png "image_tooltip")
  


### 5.2 Oświetlenie

Pod maską świateł kryją się shadery (programy cieniowania), czyli symulacja oświetlenia

przebiega w taki sposób, że obliczany jest kolor każdego piksela na podstawie

właściwości materiału powierzchni i źródeł światła. Innymi słowy na podstawie

przyjętego modelu cieniowania, który jest pewnym modelem matematycznym.

Oświetlenie może być dynamiczne lub ukryte w mapie świateł.

Jeśli chodzi o światła to mamy do wyboru takie typy źródeł jak: kierunkowe, punktowe i

typu spot.

Kierunkowe są kojarzone z padaniem promieni słonecznych, czyli posiadają tylko kierunek.



<p id="gdcalert38" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image38.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert39">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image38.png "image_tooltip")


Punktowe emitują światło z jednego punktu we wszystkie strony, czyli symulują żarówkę.



<p id="gdcalert39" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image39.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert40">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image39.png "image_tooltip")


Spot, inaczej reflektorowe, emitują światło w podobny sposób jak punktowe. Różnią się tym, że światło jest ograniczone do kształtu stożka, dlatego dają taki efekt, więc przydają się przy symulacji latarki lub reflektorów samochodu.



<p id="gdcalert40" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image40.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert41">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image40.png "image_tooltip")



### 
    


### 
    5.3 PBR

Tu poruszę bardziej zaawansowany temat dotyczący renderowania opartego na fizyce

(physically based rendering), który jest bardzo popularny w grach. Skupię się na

materiałach PBR, ponieważ ogólnie o PBR można napisać książkę, a nawet jedna taka

jest i to **bardzo dobra**, link do niej podaję tutaj

[Physically Based Rendering: From Theory to Implementation](http://www.pbr-book.org/)

Generalnie na PBR składa się: rozproszenie, odbicie, zachowanie energii, metaliczność,

Fresnel term i mikropowierzchnie.

Koncepcje te są pokazane poniżej.   

**rozproszenie (diffuse)**

Rozproszenie dotyczy sposobu interakcji pomiędzy symulowanym światłem i

materiałem. Jak sama nazwa wskazuje światło ulega rozproszeniu na wszystkie strony.

**odbicie (specular)**

Światło odbijane od powierzchni daje efekt blasku.

**zachowanie energii (energy conservation)**

Suma rozproszonego i odbitego światła nie może być większa niż wartość całkowitego światła padającego na materiał. Oznacza to, że jeżeli powierzchnia jest wysoce odblaskowa efektem będzie niskie rozproszenie koloru.

**metaliczność (metalness)**

Nadaje wygląd materiałowi jakby był wykonany z metalu. 

**Fresnel **

Efekt Fresnela, kąt pod którym patrzysz na powierzchnię ma wpływ na to w jakim stopniu powierzchnia pokazuje refleksy.

**mikropowierzchnie**

Mikropowierzchnie są związane z połyskliwością, działają na podobnej zasadzie co mapy normalne ale na skali mikro, stąd mikropowierzchnie. Definiują czy powierzchnia ma być szorstka czy gładka.

 

Powyższe koncepcje dotyczą ogólnie PBR. Teraz przedstawię jak to jest w przypadku materiałów fizycznych.

Więc tak w PlayCanvas możesz korzystać z 2 metod tzw. workflow: Metalness i Specular.



<p id="gdcalert41" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image41.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert42">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image41.png "image_tooltip")


Gdy zaznaczysz opcję Use Metalness, korzystasz… z Metalness, czyli metaliczności.

W przeciwnym razie gdy odznaczysz tą opcję korzystasz wtedy ze Specular.

Obydwie metody dają te same rezultaty. Tak naprawdę jest to zależne od twoich preferencji.

Metalness powiązane jest z wartością od 0 do 1 (0 - brak metaliczności, 1 - metal) lub mapą metalness, która zdecyduje jakie obszary materiału mają być metaliczne.

Specular powiązane jest z wartością specular lub mapą specular, która określa kolor i intensywność odbitego światła.

Jeśli chodzi o materiały PBR, podstawowym składnikiem jest kolor rozproszenia inaczej albedo. Jest to po prostu kolor materiału wyrażony wartością RGB (red, green, blue).

Można też skorzystać z mapy rozproszenia, aby np. przypisać materiałowi teksturę zamiast koloru.

Załóżmy, że np. robisz grę podobną do Gran Turismo, inspirując się licencjami chcesz mieć medale lub puchary w kolorze złota, srebra i brązu.



<p id="gdcalert42" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image42.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert43">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image42.png "image_tooltip")


 Rozwiązaniem na to jest poszukanie wartości koloru w Internecie:


<table>
  <tr>
   <td>Gold
   </td>
   <td>(1.000, 0.766, 0.336) or [255, 195, 86]
   </td>
  </tr>
  <tr>
   <td>Silver
   </td>
   <td>(0.972, 0.960, 0.915) or [248, 245, 233]
   </td>
  </tr>
  <tr>
   <td>Copper
   </td>
   <td>(0.955, 0.637, 0.538) or [244, 162, 137]
   </td>
  </tr>
</table>


Jak widzisz na tabelce, pierwszy kolor to złoty, podana jest znormalizowana wartość koloru od 0 do 1 oraz od 0 do 255.

Drugi kolor to srebrny, a trzeci kolor to może nie brąz, ale dość podobny.

I tak oto masz puchary w tych kolorach.

Bylo o metalness i specular, ale nie było jeszcze o glossiness.

Parametr glossiness używany jest w metalness i specular, co może zauważyłeś na rysunku odnośnie workflow.

Glossiness określa jak gładka jest powierzchnia materiału, czyli stopień połyskliwości, który mieści się w granicach 0-100. Możesz też skorzystać z mapy glossiness.



<p id="gdcalert43" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image43.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert44">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image43.png "image_tooltip")


Na powyższym rysunku przypomina to trochę bombkę na choince, tak to można sobie skojarzyć.

To tyle na temat terminów metalness, specular i glossiness.


### 
     


## Rozdział 6  \
API omówienie



<p id="gdcalert44" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image44.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert45">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image44.png "image_tooltip")


Poddane tutaj zostaną analizie takie klasy jak: Application, GraphNode, Entity.

Są jeszcze klasy dotyczące danego komponentu, nazwę to zbiorczo **x**Component (np.

`AnimationComponent`), gdzie **x** to jeden z podanych komponentów: 

`Animation, Audio Listener, Button, Camera, Collision, Element, Layout Child, Layout Group, Light, Model, Particle System, Rigid Body, Screen, Script, Scrollbar, Scrollview, Sound, Sprite`.

Są też systemy tych komponentów, czyli **x**ComponentSystem, gdzie **x** to jeden z powyższych komponentów (np. `AnimationComponentSystem`).

Razem, taka struktura (Entity + Component + ComponentSystem) tworzy coś co się nazywa ECS (Entity Component System). O komponentach i systemach komponentów później.

I tak o to przejrzałem większość API PlayCanvas, reszta klas znajduje się w Dodatku A, a najbardziej aktualną listę klas znajdziesz tutaj [PlayCanvas API Reference](https://developer.playcanvas.com/en/api/) .

Przejdę teraz do klasy Application. 


### 6.1 Application

Szczególną uwagę należy poświęcić podstawowemu obiektowi app typu Application. Jest on bardzo specyficzny, ponieważ sam zawiera obiekty typu: 

`AssetRegistry, Scene, Keyboard, Mouse, Touch, Gamepad`.

Jeszcze jedno, **pc **to jest przestrzeń nazw (skrót od PlayCanvas).


    **pc.app**

assets -  rejestr zasobów (`AssetRegistry`)

scene - scena (`Scene`)

root - korzeń (`Entity`)

graphicsDevice - urządzenie graficzne (`GraphicsDevice`)

**input**:

keyboard - klawiatura `Keyboard `

mouse - mysz `Mouse`

touch - urządzenie mobilne `Touch`

gamepad  `Gamepad`

Pozostałe obiekty, właściwości, metody dostępne tu [Application | PlayCanvas API Reference](https://developer.playcanvas.com/en/api/pc.Application.html)


### 6.2 GraphNode i Entity

**6.2.1 GraphNode **

Dzięki klasie GraphNode można manipulować encjami: dodawać encje potomne, 

pobierać / ustawiać orientację z kątami Eulera lub kwaternionami, pobierać / ustawiać pozycję w przestrzeni świata lub lokalnej, pobierać / ustawiać skalę tylko w przestrzeni lokalnej, ale też umożliwić aby encja patrzyła w dany punkt (lookAt()). Jest jeszcze parę innych metod nie omówionych w tej klasie.


### **6.2.2 Entity**

Klasa Entity rozszerza / dziedziczy po GraphNode, więc zawiera odziedziczone metody takie jak: 

addChild(), get/set[Local]Position/Rotation(), getLocalScale(), lookAt(), get/set[Local]EulerAngles(), translate[Local](), rotate[Local]().

**addChild(node) **

Dodaje element potomny, na tym przykładzie jest to encja


```
const e = new pc.Entity(app);
this.entity.addChild(e);
```


Najpierw tworzony jest obiekt encji, a później dodawany ten element potomny do elementu rodzica (**<code>this.entity</code></strong>)

Najczęstszy sposób by ustawić kamerę śledzącą, wtedy postać / pojazd to element rodzic, a kamera jest elementem potomnym. Jest to też sposób dynamicznego grupowania obiektów, np. encja nadrzędna miasto, encja potomna budynek. 

Pozycję, orientację i skalę można ustawić z trzema liczbami x, y, z lub jednym wektorem `Vec3`

**getEulerAngles() **

pobiera kąty Eulera w przestrzeni świata (world space)


```
const angles = this.entity.getEulerAngles(); // [0,0,0]
angles[1] = 180; // rotate the entity around Y by 180 degrees
this.entity.setEulerAngles(angles);
```


Tak jak powyżej po to pobiera aby później obrócić encję wokół osi Y o 180 stopni

**getLocalEulerAngles() **

pobiera kąty Eulera w przestrzeni lokalnej


```
const angles = this.entity.getLocalEulerAngles();
angles[1] = 180;
this.entity.setLocalEulerAngles(angles);
```


Pobiera aby później obrócić encję wokół **własnej **osi Y o 180 stopni

**getLocalPosition() **

pobiera lokalną pozycję


```
const position = this.entity.getLocalPosition();
position[0] += 1; // move the entity 1 unit along x.
this.entity.setLocalPosition(position);
```


Pobiera aby później przesunąć encję o jedną jednostkę wzdłuż x.

**getLocalRotation() **

pobiera lokalną orientację


```
const rotation = this.entity.getLocalRotation();
```


**getLocalScale() **

pobiera lokalną skalę


```
const scale = this.entity.getLocalScale();
scale.x = 100;
this.entity.setLocalScale(scale);
```


Pobiera aby później ustawić rozmiar x na 100 jednostek

**getPosition() **

pobiera pozycję w przestrzeni świata


```
const position = this.entity.getPosition();
position.x = 10;
this.entity.setPosition(position);
```


Pobiera aby później ustawić pozycję x na 10 jednostek

**getRotation() **

pobiera orientację w przestrzeni świata


```
const rotation = this.entity.getRotation();
```


**lookAt(x, [y], [z], [ux], [uy], [uz]) **

umożliwia aby encja patrzyła na inną encję, czyli w dany punkt


```
// Look at another entity, using the (default) positive y-axis for up
const position = otherEntity.getPosition();
this.entity.lookAt(position);
```



```
// Look at the world space origin, using the (default) positive y-axis for up
this.entity.lookAt(0, 0, 0);
```


Można też ustawić aby encja patrzyła na punkt 0, 0, 0

**rotate(x, [y], [z]) **

Obraca encję w przestrzeni świata


```
// Rotate via 3 numbers
this.entity.rotate(0, 90, 0);
// Rotate via vector
const r = new pc.Vec3(0, 90, 0);
this.entity.rotate(r);
```


**rotateLocal(x, [y], [z]) **

Obraca encję w przestrzeni lokalnej


```
// Rotate via 3 numbers
this.entity.rotateLocal(0, 90, 0);
// Rotate via vector
const r = new pc.Vec3(0, 90, 0);
this.entity.rotateLocal(r);
```


**setEulerAngles(x, [y], [z]) **

ustawia kąty Eulera w przestrzeni świata (world space)


```
// Set rotation of 90 degrees around world-space y-axis via 3 numbers
this.entity.setEulerAngles(0, 90, 0);
// Set rotation of 90 degrees around world-space y-axis via a vector
const angles = new pc.Vec3(0, 90, 0);
this.entity.setEulerAngles(angles);
```


**setLocalEulerAngles(x, [y], [z]) **

ustawia kąty Eulera w przestrzeni lokalnej


```
// Set rotation of 90 degrees around y-axis via 3 numbers
this.entity.setLocalEulerAngles(0, 90, 0);
// Set rotation of 90 degrees around y-axis via a vector
const angles = new pc.Vec3(0, 90, 0);
this.entity.setLocalEulerAngles(angles);
```


**setLocalPosition(x, [y], [z]) **

ustawia lokalną pozycję


```
// Set via 3 numbers
this.entity.setLocalPosition(0, 10, 0);
// Set via vector
const pos = new pc.Vec3(0, 10, 0);
this.entity.setLocalPosition(pos);
```


**setLocalRotation(x, [y], [z], [w]) **

ustawia lokalną orientację


```
// Set via 4 numbers
this.entity.setLocalRotation(0, 0, 0, 1);
// Set via quaternion
const q = pc.Quat();
this.entity.setLocalRotation(q);
```


**setLocalScale(x, [y], [z]) **

ustawia lokalną skalę / rozmiar


```
// Set via 3 numbers
this.entity.setLocalScale(10, 10, 10);
// Set via vector
const scale = new pc.Vec3(10, 10, 10);
this.entity.setLocalScale(scale);
```


**setPosition(x, [y], [z]) **

ustawia pozycję w przestrzeni świata


```
// Set via 3 numbers
this.entity.setPosition(0, 10, 0);
// Set via vector
const position = new pc.Vec3(0, 10, 0);
this.entity.setPosition(position);
```


**setRotation(x, [y], [z], [w]) **

ustawia orientację w kwaternionach w przestrzeni świata 


```
// Set via 4 numbers
this.entity.setRotation(0, 0, 0, 1);
// Set via quaternion
const q = pc.Quat();
this.entity.setRotation(q);
```


**translate(x, [y], [z]) **

Przesuwa encję o x jednostek w przestrzeni świata


```
// Translate via 3 numbers
this.entity.translate(10, 0, 0);
// Translate via vector
const t = new pc.Vec3(10, 0, 0);
this.entity.translate(t);
```


Tutaj przesuwa o 10 jednostek w przestrzeni świata

**translateLocal(x, [y], [z]) **

Przesuwa encję o x jednostek w przestrzeni lokalnej


```
// Translate via 3 numbers
this.entity.translateLocal(10, 0, 0);
// Translate via vector
const t = new pc.Vec3(10, 0, 0);
this.entity.translateLocal(t);
```


Tutaj przesuwa o 10 jednostek w przestrzeni lokalnej
