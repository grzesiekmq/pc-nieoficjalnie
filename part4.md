# Część IV - Encja - obiekt gry


## Rozdział 7  \
Encja, Komponenty  \
i Systemy

**Encja**



<p id="gdcalert45" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image45.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert46">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image45.png "image_tooltip")


Encja to obiekt gry (w silniku Unity nazywa się ona GameObject), który jest kontenerem na komponenty, dzięki niej można ustawić transformację obiektu (pozycja, orientacja, rozmiar). Można też ukryć / pokazać obiekt (właściwość Enabled). Najczęstszy przypadek to ukrywanie jednego ekranu (screen) np. głównego menu, pokazanie innego np. z opcjami lub ustawieniami gry. Nic nie stoi na przeszkodzie, aby encja była pusta i nie zawierała żadnych

komponentów, np. jeżeli chcesz żeby to był punkt. 

Załóźmy, że robisz konfigurator i chcesz mieć hotspoty. Dobrym sposobem na to jest

utworzenie **pustych **encji, które będą reprezentować punkt. 

Albo inny przykład: chcesz mieć przejście kamery z punktu A do punktu B, puste encje dobrze się sprawdzą.

Uwaga: jeżeli tworzysz nową encję, nazwiesz ją kamera, to nie jest to kamera, ponieważ

dołączenie do niej komponentu CameraComponent (czy to z poziomu edytora na

platformie, czy to engine-only) sprawi, że encja jest dopiero wtedy kamerą.

No dobrze, ale co w przypadku jak encja zawiera więcej komponentów niż jeden, czym wtedy jest? :)

Możesz jeszcze zastosować encję np. gdy chcesz mieć skrypt, ale nie w Root.

Przebiega to następująco: tworzysz nową encję, dodajesz do niej komponent script i dorzucasz kod js, nazywasz tą encję adekwatnie do nazwy kodu.

Poniższy rysunek może przekaże co mam na myśli.



<p id="gdcalert46" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image46.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert47">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image46.png "image_tooltip")


<p id="gdcalert47" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image47.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert48">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image47.png "image_tooltip")


Znowu posługuję się przykładem z gry Monopoly. Więc tworzysz encję, która nazywa się UI, dodajesz do niej komponent script, dorzucasz kod np. uiManager.js, trade.js, setup.js.

Na rysunku możesz zauważyć jeszcze, że podobnie postąpiono z elementami potomnymi UI, czyli Main, Main Menu itd., co wskazuje na to ikonka ‘znaczników’ &lt;>.

To jest jeden z takich trików, aby pozwolić na lepszą organizację w hierarchii, przede wszystkim jest to bardziej zrozumiałe niż wpychanie wszystkich skryptów do Root.

Podsumowując encja może zawierać komponenty lub nie, wtedy jest encją pustą.

**Komponenty**

Komponent nadaje encji pewne zachowanie, tak jak już mówiłem, żeby encja była

kamerą musi posiadać komponent kamery. Istnieją jeszcze inne komponenty. 

Ogólnie komponenty to pewien sposób projektowania oprogramowania. Komponenty w tym przypadku są lepsze niż podejście klasowe, dlatego, że z komponentami łatwiej jest zarządzać rzeczami w grze, ponieważ są bardziej modularne i mniejsze niż klasy, to tak w skrócie.

Komponentów szczegółowo nie będę analizował. Poniżej znajduje się lista 18 komponentów.

Komponenty (18):

-	Animation

-	Audio Listener

-	Button

-	Camera

-	Collision

-	Element

-	Layout Child

-	Layout Group

-	Light

-	Model

-	Particle System (system cząsteczek)

-	Rigid Body (bryła sztywna)

-	Screen

-	Script

-	Scrollbar 

-     Scrollview 

-	Sound  

-	Sprite (duszek)

**Animation **



<p id="gdcalert48" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image48.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert49">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image48.png "image_tooltip")


Zacznę od komponentu animacji, określa które zasoby animacji są brane pod uwagę.

  

**Audio Listener**



<p id="gdcalert49" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image49.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert50">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image49.png "image_tooltip")


Lokalizacja nasłuchiwacza audio podawana jest w tym komponencie. Dotyczy ona

dźwięku pozycyjnego w 3D (positional audio). Przykład znajduje się tutaj [https://playcanvas.github.io/#sound/positional.html](https://playcanvas.github.io/#sound/positional.html)

**Button**



<p id="gdcalert50" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image50.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert51">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image50.png "image_tooltip")


Tworzy przycisk UI, 

	**Camera**



<p id="gdcalert51" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image51.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert52">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image51.png "image_tooltip")


Dodaje do encji kamerę, która wyświetla scenę z poziomu encji. Główne właściwości

komponentu to typ projekcji: perspektywa czy ortogonalna, czyli projection (perspective

lub orthographic), pole widzenia (field of view) w stopniach, płaszczyzny przycinania

bliskiej i dalekiej (nearClip, farClip), tzn na jaką odległość kamera widzi z bliska i

daleka. Pozostałe właściwości znajdziesz tutaj [Camera | Learn PlayCanvas](https://developer.playcanvas.com/en/user-manual/packs/components/camera/) 

	**Collision**



<p id="gdcalert52" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image52.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert53">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image52.png "image_tooltip")


Komponent fizyczny Collision jest przydatny w wykrywaniu kolizji. Dostępne typy

kształtu kolizji (collision shape) to: box, sphere (kula), capsule (kapsuła), mesh (siatka),

compound (złożony z innych podstawowych kształtów box, sphere itd.), cone (stożek),

cylinder. Jeżeli encja posiada tylko komponent collision jest wtedy tzw. triggerem, który

dobrze sprawdza się przy wykrywaniu kiedy otworzyć drzwi w grze lub kiedy osiągnąłeś

linię mety. Collision stosowany jest najczęściej z rigidbody o którym później.

Jeszcze jedno odnośnie collision, ponieważ zdarzy się taka sytuacja, że chcesz przesunąć

kształt kolizji, ale problem w tym, że przesuwasz też jednocześnie model 3D. 

Trik polega na tym, żeby stworzyć encję rodzica (parent entity), wrzucić tam komponent collision, a model dać jako encję potomną. W efekcie możesz przesunąć kształt kolizji bez

przesuwania modelu 3D.

	**Element**



<p id="gdcalert53" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image53.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert54">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image53.png "image_tooltip")


Komponent Element jest elementem potomnym dla komponentu Screen.

Buduje się z nim interfejs użytkownika poprzez obrazki lub tekst, dlatego można wybrać typ: Image lub Text.

**	Layout Child**



<p id="gdcalert54" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image54.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert55">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image54.png "image_tooltip")


Layout Child odnosi się do możliwości nadpisania parametrów Layout Group.

**	Layout Group**



<p id="gdcalert55" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image55.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert56">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image55.png "image_tooltip")


W Layout Group można ustawić orientację elementów UI na poziomą lub pionową z właściwością Orientation, która przyjmuje wartości Horizontal lub Vertical.

Ważną właściwością jest Wrap, aktywując tą właściwość otrzymujesz **siatkę **(grid), czyli elementy znajdujące się w wierszach i kolumnach.

	**Light**



<p id="gdcalert56" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image56.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert57">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image56.png "image_tooltip")


Jak już wiesz światło może posiadać typ: kierunkowy, punktowy lub reflektorowy.

W PlayCanvas określa to właściwość Type z możliwymi opcjami: Directional, Point lub

Spot. Światłu możesz nadać kolor i intensywność, z właściwościami Color i Intensity.

	**Model**



<p id="gdcalert57" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image57.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert58">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image57.png "image_tooltip")


Model, z nim możesz wyświetlić prymitywy: box, capsule, cone. cylinder, plane (płaszczyzna, nazywam to podłoga), sphere. Oprócz prymitywów możesz też wyświetlić model 3D (w formacie .glb, .fbx itd.), aby to zrobić musisz ustalić Type jako Asset. Komponent Model posiada właściwość Model tam możesz znaleźć slot do którego możesz przeciągnąć wybrany zasób z modelem 3D. 

**	Particle System (system cząsteczek)**



<p id="gdcalert58" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image58.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert59">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image58.png "image_tooltip")


Z tym komponentem ustawisz system cząsteczek, czy to deszcz czy śnieg.

**	**

**Rigid Body (bryła sztywna)**



<p id="gdcalert59" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image59.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert60">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image59.png "image_tooltip")


Kolejny komponent fizyczny to RigidBody, stosowany jest z komponentem Collision. 

RigidBody nadaje encji właściwości fizyczne takie jak: masa, tłumienie liniowe i kątowe (linear, angular damping), tarcie (friction), odbijalność (restitution).

Dodatkowo RigidBody posiada 3 typy: Static, Dynamic i Kinematic. 

Na Kinematic nie oddziałują żadne siły, Static przydaje się dla podłoża, trasy etc.

Dynamic stosuje się w celach zapewnienia fizyki wraz z siłami.

Mały tip: Nie zapomnij ustawić właściwości odbijalności na 0 przy typie Static, jeżeli nie chcesz aby obiekt się odbijał od podłoża.

	**Screen**



<p id="gdcalert60" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image60.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert61">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image60.png "image_tooltip")


Screen to element rodzic dla komponentu Element. Definiuje obszar wyświetlania elementów.

 

	**Script**



<p id="gdcalert61" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image61.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert62">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image61.png "image_tooltip")


Komponent Script jest podstawowym komponentem najczęściej używanym. Za pomocą niego można doczepić skrypty w js (tzn nie bezpośrednio rysunek poniżej).



<p id="gdcalert62" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image62.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert63">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image62.png "image_tooltip")


Jako przykład możesz wyłączyć komponent Script, jeżeli doczepiłeś skrypt z turn.js i nie chcesz żeby model się obracał. 

Jako inny przykład możesz też włączyć ten komponent, aby uaktywnić CarController.js, gdy chcesz aby samochód startował z linii startu dopiero po odliczaniu 3,2,1. Sposobów innych pewnie znajdzie się więcej.

	**Scrollbar **

   

<p id="gdcalert63" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image63.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert64">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image63.png "image_tooltip")


Scrollbar dotyczy kontrolki przewijania dla poniższego komponentu Scrollview.

**Scrollview **

	

<p id="gdcalert64" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image64.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert65">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image64.png "image_tooltip")


Scrollview określa obszar możliwy do przewijania. 

**Sound ** 

	

<p id="gdcalert65" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image65.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert66">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image65.png "image_tooltip")


Komponent Sound kontroluje dźwięk, odtwarza zasoby audio.

**Sprite (duszek)**



<p id="gdcalert66" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image66.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert67">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image66.png "image_tooltip")


Są dwa rodzaje wewnątrz tego komponentu: duszek prosty lub animowany. Sprite wyświetla zasoby związane ze Sprite.

To są wszystkie możliwe komponenty w PlayCanvas. Nie omówiłem API tych komponentów, więc resztę możesz znaleźć tutaj [https://developer.playcanvas.com/en/api/?filter=component](https://developer.playcanvas.com/en/api/?filter=component)



<p id="gdcalert67" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image67.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert68">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image67.png "image_tooltip")


Jeśli chodzi o to ComponentSystem, przegląd tego znajduje się poniżej, czyli o Systemach.

**Systemy**

Systemy, a dokładniej systemy komponentów inaczej menedźery, a w PlayCanvas **ComponentSystem**s odpowiedzialne są za zarządzanie komponentami. Jako przykład podam globalne ustawienie grawitacji wszystkim komponentom RigidBody, a skorzystam w tym przypadku z RigidBodyComponentSystem, ale dokładniej z gotowego obiektu należącego do app.systems.

**[ComponentSystemRegistry](https://developer.playcanvas.com/en/api/pc.ComponentSystemRegistry.html) systems **

The application's component system registry. The Application constructor adds the following component systems to its component system registry:



*   
animation ([AnimationComponentSystem](https://developer.playcanvas.com/en/api/pc.AnimationComponentSystem.html))


*   
audiolistener ([AudioListenerComponentSystem](https://developer.playcanvas.com/en/api/pc.AudioListenerComponentSystem.html))


*   
button ([ButtonComponentSystem](https://developer.playcanvas.com/en/api/pc.ButtonComponentSystem.html))


*   
camera ([CameraComponentSystem](https://developer.playcanvas.com/en/api/pc.CameraComponentSystem.html))


*   
collision ([CollisionComponentSystem](https://developer.playcanvas.com/en/api/pc.CollisionComponentSystem.html))


*   
element ([ElementComponentSystem](https://developer.playcanvas.com/en/api/pc.ElementComponentSystem.html))


*   
layoutchild ([LayoutChildComponentSystem](https://developer.playcanvas.com/en/api/pc.LayoutChildComponentSystem.html))


*   
layoutgroup ([LayoutGroupComponentSystem](https://developer.playcanvas.com/en/api/pc.LayoutGroupComponentSystem.html))


*   
light ([LightComponentSystem](https://developer.playcanvas.com/en/api/pc.LightComponentSystem.html))


*   
model ([ModelComponentSystem](https://developer.playcanvas.com/en/api/pc.ModelComponentSystem.html))


*   
particlesystem ([ParticleSystemComponentSystem](https://developer.playcanvas.com/en/api/pc.ParticleSystemComponentSystem.html))


*   
rigidbody ([RigidBodyComponentSystem](https://developer.playcanvas.com/en/api/pc.RigidBodyComponentSystem.html))


*   
screen ([ScreenComponentSystem](https://developer.playcanvas.com/en/api/pc.ScreenComponentSystem.html))


*   
script ([ScriptComponentSystem](https://developer.playcanvas.com/en/api/pc.ScriptComponentSystem.html))


*   
scrollbar ([ScrollbarComponentSystem](https://developer.playcanvas.com/en/api/pc.ScrollbarComponentSystem.html))


*   
scrollview ([ScrollViewComponentSystem](https://developer.playcanvas.com/en/api/pc.ScrollViewComponentSystem.html))


*   
sound ([SoundComponentSystem](https://developer.playcanvas.com/en/api/pc.SoundComponentSystem.html))


*   
sprite ([SpriteComponentSystem](https://developer.playcanvas.com/en/api/pc.SpriteComponentSystem.html))

```
// Set global gravity to zero
this.app.systems.rigidbody.gravity.set(0, 0, 0);
```


Jak widzisz w systems są jeszcze inne systemy komponentów (np. animation typu AnimationComponentSystem). Daruję sobie omawianie ich, ponieważ wszystkie działają na podobnej zasadzie, czyli dotyczą ustawień globalnych.

Wracając do przykładu z rigidbody system, dostaję się do niego poprzez `app.systems`, czyli mam `app.systems.rigidbody`. Następnie ustawiam globalną grawitację (a w zasadzie jej brak) z `gravity.set(0,0,0)`, więc razem otrzymuję powyższą linijkę kodu, chyba wiesz jak ją złożyć?

A i systems to rejestr systemów. Pozwolę sobie zakończyć ten rozdział i przejść dalej do praktyki i przykładów.
