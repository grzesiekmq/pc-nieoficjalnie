# Część I - ogólnie

<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")



# <p style="text-align: right">


<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


<img src="images/image3.png" width="" alt="alt_text" title="image_tooltip">
</p>



## Rozdział 1  PlayCanvas, cechy 


### 1.1 PlayCanvas - co to?


        Silnik gier stworzony w WebGL, nie bazuje, nie korzysta z biblioteki 3D threejs,

**został napisany od zera, **też jako platforma w chmurze do tworzenia gier, wizualizacji, konfiguratorów produktów (np. konfigurator samochodu). Można w nim zrobić bardzo zaawansowaną grafikę, dzięki możliwościom silnika. 

Ma on zintegrowany silnik fizyki Ammo. Z PlayCanvas można korzystać jako z platformy z użyciem edytora graficznego i edytora kodu w chmurze lub jako engine-only, czyli mając projekt lokalnie na swoim laptopie i korzystając tylko z silnika w wybranym IDE lub edytorze kodu (VS Code, Atom, Sublime Text), coś jak jest to realizowane w three.js.

Z engine-only jest jedna zaleta możesz korzystać z gita i wrzucać na githuba, w przypadku platformy musisz korzystać z PlayCanvas’owego systemu kontroli wersji i checkpointów, a nie commitów jak to działa w git. 

Nazwa przypomina trochę jakby to miało chodzić o klasyczny canvas, HTML5, czyli 2D, ale jednak jest to bogaty silnik 3D, podobny silnik do PlayCanvas to Babylon.js, też warty spróbowania, a PlayCanvas polecam naprawdę fajny silnik, ale szczerze dopiero od niedawna była wcześniej jedna wada, był limit miejsca na zasoby 100 MB jeżeli korzystałeś z platformy. Teraz limit ten jest 1GB, czyli możesz trzymać zasoby na platformie za darmo jeśli razem nie przekraczają 1 GB, żeby np. mieć 10 GB lub więcej musisz mieć wykupioną miesięczną subskrypcję. 

Społeczność nie jest mała, dokumentacja jest dobrze napisana, tylko jest jedna wada nie ma na ten temat książek ani po angielsku ani po polsku.

W przypadku problemów możesz znaleźć post dotyczący twojego problemu lub możesz zapytać na forum tworząc nowy post. Nie jest tak że nikt nie odpowiada na twoje pytanie, bardzo szybko dostajesz odpowiedź, a nawet możliwe rozwiązanie problemu, co jest bardzo mocną zaletą forum PlayCanvas. Link do forum podaję tu [PlayCanvas Discussion](https://forum.playcanvas.com/) 

 

Z ciekawości przeglądałem kod silnika, jest on naprawdę duży, chociaż nie aż tak ogromny jak to jest w przypadku Unreal Engine.


### 1.2 cechy (features)  



<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image4.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image4.png "image_tooltip")



        PlayCanvas posiada następujące cechy:



1. 
wsparcie WebGL 2


2. 
asynchroniczne streamowanie zasobów


3. 
audio API


4. 
ECS (Entity Component System) - o tym w części Encja


5. 
renderowanie oparte o fizykę (PBR)


6. 
system shader chunk


7. 
skinning GPU


8. 
system cząsteczek GPU


9. 
generowanie mapy świateł w czasie rzeczywistym


10. 
animacja mieszania kształtu


11. 
miękkie cienie i light cookie


12. 
importer zasobów i menedźer


13. 
potok graficzny liniowy i HDR


14. 
 API urządzeń wejścia


15. 
renderer fontu SDF


16. 
silnik fizyki dotyczący rigidbody


17. 
narzędzia dla responsywnych interfejsów


18. 
wsparcie WebVR


19. 
rozwój i testowanie na urządzeniu mobilnym


20. 
filtrowanie zasobów


21. 
edytowanie scen w czasie rzeczywistym


22. 
prefiltering tekstury sześciennej


23. 
profiler


24. 
kompresja tekstur (DXT, PVR i ETC1)


25. 
edytor materiału


26. 
wieloplatformowość


1. 
**wsparcie WebGL 2**
Silnik używa najnowsze WebGL API, ale jest wstecznie kompatybilny z WebGL wersji pierwszej.



2. 
**asynchroniczne streamowanie zasobów**
Asynchroniczne, a więc co za tym idzie szybsze ładowanie się aplikacji, poprzez opóźnienie ładowania mniej ważnych zasobów.



3. 
**audio API**
Pozycyjny dźwięk pozwala na przyczepianie filtrów WebAudio.



4. 
**ECS (Entity Component System) - o tym w części Encja**
Twórz aplikacje szybko z wykorzystaniem ECS.



5. 
**renderowanie oparte o fizykę (PBR)**
Zapewnij realizm w renderingu z użyciem najnowszych technik czasu rzeczywistego w grafice 3D 



6. 
**system shader chunk**
Częściowa i pełna customizacja shaderów: dostosuj parametry, nadpisuj kawałki standardowego shadera lub pisz swój kod GLSL



7. 
**skinning GPU**
Przyspieszana sprzętowo animacji postaci



8. 
**system cząsteczek GPU**
Przyspieszany sprzętowo system cząsteczek 



9. 
**generowanie mapy świateł w czasie rzeczywistym**
Możesz mieć wiele statycznych świateł wysokiej rozdzielczości



10. 
**animacja mieszania kształtu**
 Wsparcie dla animacji mieszania kształtu modeli



11. 
**miękkie cienie i light cookie**
Wybieraj spośród wielu algorytmów cieni.

Light cookies zapewniają fajne efekty tanim kosztem wydajnościowym



12. 
**importer zasobów i menedźer**
Importuj zasoby: modele 3D i animacje (FBX, OBJ, DAE, 3DS), tekstury i tekstury HDR, pliki audio i inne



13. 
**potok graficzny liniowy i HDR**
potok graficzny liniowy i HDR: korekcja gammy, tonemapping, wsparcie dla tekstur sześciennych HDR i mapy świateł



14. 
** API urządzeń wejścia**
Wsparcie klawiatury, myszy, gamepada, ekranów dotykowych



15. 
**renderer fontu SDF**
Konwertuj TTF, OTF na zasoby fontu (podobnie jak w Unity)



16. 
**silnik fizyki rigidbody**
Wbudowany w PlayCanvas system fizyki Ammo, który jest portem Bulleta, pozwala na łatwiejszą implementację fizyki w grze



17. 
**narzędzia dla responsywnych interfejsów**
Komponenty pozwalające na tworzenie responsywnych interfejsów 2D i 3D



18. 
**wsparcie WebVR**
Wsparcie dla najnowszych standardów WebVR



19. 
**rozwój i testowanie na urządzeniu mobilnym**
Szybkie iteracje z użyciem aktualizacji na bieżąco na urządzeniu mobilnym 



20. 
**filtrowanie zasobów**
Przeszukuj i filtruj swoją kolekcję zasobów 



21. 
**edytowanie scen w czasie rzeczywistym**
Zmiany na bieżąco w stylu kolaboracji z Google Docs



22. 
**prefiltering tekstury sześciennej**
Ustaw oświetlenie bazujące na obrazie (IBL) z użyciem tylko jednego kliknięcia przycisku



23. 
**profiler**
Wyświetla wykresy, statystyki związane z wydajnością w czasie rzeczywistym



24. 
**kompresja tekstur (DXT, PVR i ETC1)**
kompresja tekstur jednym kliknięciem



25. 
**edytor materiału**
Szybko dostosowywuj widoczne wizualnie zmiany w parametrach materiałów z wykorzystaniem edytora



26. 
**wieloplatformowość**
Uruchom edytor na każdym urządzeniu: desktop, laptop, tablet, smartfon

Jak widzisz PlayCanvas posiada wiele funkcjonalności.

Przejdę teraz do omówienia zasobów.




##  Rozdział 2   \
zasoby (assets)



<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image5.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image5.png "image_tooltip")



        Zasoby mogą być różnego typu np. model, animacja, obrazki dla tekstur 

(.png,.jpg) i audio.

Poniżej omawiam wszystkie rodzaje zasobów dostępne w PlayCanvas:



*   materiał  
*     	Phonga 
*               fizyczny (physical)



*   
tekstura  


*   model
*   animacja
*   tekstura sześcienna (cubemap)
*   HTML
*   audio
*   CSS
*   shader
*   font
*   duszek (sprite)	
*   prefab (w pc pod nazwą template)
*   moduł Wasm (Wasm module, WebAssembly module)

  


### 2.1 materiał



<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image6.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image6.png "image_tooltip")


Ogólnie materiał definiuje właściwości powierzchni takie jak kolor, połyskliwość itd. Dokładnie czego to dotyczy odsyłam do podręczników z grafiki komputerowej.

W PlayCanvas materiał to jeden z typu zasobów.

Ma 2 podtypy: Phonga i fizyczny.

**  	  **

**Phonga **

**   **Model cieniowania Phonga to przestarzały element, zaleca się korzystania z modelu fizycznego. \
Więcej na temat modelu cieniowania Phonga możesz znaleźć tutaj [Phong Material | Learn PlayCanvas](https://developer.playcanvas.com/en/user-manual/assets/phong-material/)

**fizyczny (physical)**

Materiał fizyczny reprezentuje zaawansowany model cieniowania wysokiej jakości, dlatego jest zalecany w stosowaniu dla uzyskania imponujących efektów.

Szczegółowe info na temat właściwości materiału fizycznego dostępne jest tutaj

[Physical Material | Learn PlayCanvas](https://developer.playcanvas.com/en/user-manual/assets/physical-material/)

 \
Następujące regiony dotyczące tego materiału: **offset i tiling**, **ambient **(związane z ambient occlussion, okluzją otoczenia), **diffuse **(rozproszenie, diffuse to inaczej albedo), **specular **(daje połyskliwość), **emissive **(emituje światło), **opacity** (przezroczystość), **normals **(związane z mapą normalną), **parallax **(związane z mapa wysokościową), **environment** (refleksy), **lightmap **(mapa świateł), 

 


### 2.2 tekstura ** **



<p id="gdcalert7" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image7.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert8">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image7.png "image_tooltip")


Tekstura to obraz, który może zostać przypisany do materiału.

Poniżej wyróżniłem mapy tekstur, które przydaja się przy multiteksturowaniu, aby uzyskać bardziej szczególowy wygląd materiału.

Rodzaje map tekstur: okluzja otoczenia (ambient occlusion, AO map),  tekstura sześcienna (cubemap), środowiskowa (env map), rozproszenia (diffuse map), odbicia (specular map), emissive (emissive map), przezroczystości (opacity map), normalna (normal map), wysokościowa (height map), oświetlenia (light map).

Więcej o teksturach tutaj [Textures | Learn PlayCanvas](https://developer.playcanvas.com/en/user-manual/assets/textures/)

**  **

**   **


### 2.3 model



<p id="gdcalert8" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image8.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert9">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image8.png "image_tooltip")


Modele 3D i animacje są tworzone poza PlayCanvas, eksportowane np. z Blendera, Wings3D, Maya lub 3DS Max i importowane do PlayCanvas. 

Zaleca się korzystać z formatu fbx dla uzyskania najlepszych wyników i tak model zostanie przekonwertowany na glb (tzn fbx pozostanie jako źródłowy format, ale zostanie stworzony glb jako docelowy format i co za tym idzie będą dwa formaty fbx i glb danego modelu).

Więcej o modelach  [Models | Learn PlayCanvas](https://developer.playcanvas.com/en/user-manual/assets/models/)


### 2.4 animacja



<p id="gdcalert9" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image9.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert10">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image9.png "image_tooltip")


Zasób animacja jest używany, aby odtwarzać pojedynczą animację na modelu 3D. \
Formaty pełnych scen zawierają animacje, np. jest to gltf, dae, fbx.

Więcej o animacji [Animation | Learn PlayCanvas](https://developer.playcanvas.com/en/user-manual/assets/animation/)


### 2.5  tekstura sześcienna (cubemap)



<p id="gdcalert10" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image10.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert11">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image10.png "image_tooltip")


Tekstura sześcienna to specjalny typ tekstury składający się z 6 zasobów tekstur.

Stosowana jest jako skybox lub mapa środowiska.

Więcej o cubemap [Cubemaps | Learn PlayCanvas](https://developer.playcanvas.com/en/user-manual/assets/cubemaps/)


### 2.6  HTML



<p id="gdcalert11" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image11.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert12">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image11.png "image_tooltip")


Zasób HTML zawiera kod HTML.

Aby wczytać HTML musisz napisać taki kawałek kodu js:


```
this.element = document.createElement('div');
this.element.classList.add('container'); 
document.body.appendChild(this.element);
this.element.innerHTML = this.html.resource;
```


Teraz opiszę szybko działanie kodu.

Tworzy element div dynamicznie, później dodaje klasę o nazwie container. Następnie podczepia tego diva do &lt;body> i ustawia zawartość twojego htmla jako element potomny dla div’a container. 

To jest jeden ze sposobów.

Oczywiście musisz jeszcze w tym przypadku dodać atrybut z nazwą **html **(jeżeli w kodzie nazwałeś jako this.html, o atrybutach później), napisać kod html, przeciągnąć plik html w edytorze do miejsca gdzie można podczepiać czy to encje czy to różne zasoby, w tym przypadku jest to ui pod komponentem script (tak jak widać to na poniższym rysunku), w ui jest właśnie atrybut typu zasób o nazwie html (natomiast plik HTML nazywa sie ui.html), dopiero wtedy masz zawartość HTML na swojej stronie.



<p id="gdcalert12" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image12.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert13">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image12.png "image_tooltip")


Więcej o HTML

[HTML | Learn PlayCanvas](https://developer.playcanvas.com/en/user-manual/assets/html/)


### 2.7  audio

Zasób audio to plik dźwiękowy.  

[Audio | Learn PlayCanvas](https://developer.playcanvas.com/en/user-manual/assets/audio/)


### 2.8  CSS

Zasób CSS zawiera kod CSS.

Styl CSS podczepia się do strony podobnie jak w przypadku zasobu HTML, czyli dodajesz atrybut o nazwie css, tworzysz kod CSS, przeciągasz plik css w edytorze do miejsca gdzie można podczepiać czy to encje czy to różne zasoby, czyli np. ui pod komponentem script, w ui jest właśnie atrybut typu zasób o nazwie css, dopiero wtedy masz zawartość CSS na swojej stronie, a więc zastosowany wygląd.

Kod do podczepiania CSSa jest trochę inny niż było to przy zasobie HTML.

Tym razem pokażę trochę inny sposób:


```
// get asset from registry by id
const asset = app.assets.get(32);

// create element
const style = pc.createStyle(asset.resource || '');
document.head.appendChild(style);

// when asset resource loads/changes,
// update html of element
asset.on('load', function() {
    style.innerHTML = asset.resource;
});

// make sure assets loads
app.assets.load(asset);
```


Więc tak pobierany jest zasób CSS z rejestru zasobów, tworzony element i wczytywany zasób.

 


### 2.9  shader

Zasób shader zawiera kod GLSL, możesz też przesłać pliki z rozszerzeniem .vert, .frag lub .glsl


```
const vertexShader = this.app.assets.find('my_vertex_shader');
const fragmentShader = this.app.assets.find('my_fragment_shader');
const shaderDefinition = {
    attributes: {
        aPosition: pc.SEMANTIC_POSITION,
        aUv0: pc.SEMANTIC_TEXCOORD0
    },
    vshader: vertexShader.resource,
    fshader: fragmentShader.resource
};

const shader = new pc.Shader(this.app.graphicsDevice, shaderDefinition);
const material = new pc.Material();
material.setShader(shader);
```


Dwie pierwsze linijki dotyczą szukania w rejestrze zasobów shadera wierzchołków i fragmentów.

Dalej zdefiniowany jest shader z atrybutami: pozycja i uv. Do właściwości vshader i fshader doczepiana jest zawartość zasobu shader, najpierw shadera wierzchołków, później fragmentów. Jako przedostatni krok tworzony jest shader i materiał. Wreszcie ustawiany jest shader na materiał. \



### 2.10  font

Zasób fontu zawiera obrazek z wszystkimi znakami fontu, Używa się go do wyświetlenia tekstu.

Więcej o font tutaj [Fonts | Learn PlayCanvas](https://developer.playcanvas.com/en/user-manual/assets/fonts/)


### 2.11  duszek (sprite)	

Sprite to grafika 2D, ze względu na to że książka dotyczy tworzenia gry w 3D, temat 2D zostaje pominięty

Więcej o sprite  [Sprite | Learn PlayCanvas](https://developer.playcanvas.com/en/user-manual/assets/sprites/)


### 2.12  prefab (w pc pod nazwą template)

Prefabrykat, czyli zasób zawierający część encji, pozwalający na tworzenie wielu instancji, dlatego przydatny jest przy konstruowaniu obiektów wyglądających tak samo np. 1000 drzew jednego typu, 10 takich samych przycisków itd. W PlayCanvas nie ma jeszcze wariantów prefabów, czyli np. jest bazowy prefab samochód, a np. chcę mieć różne samochody mające te same cechy, ale inne wartości, np. prędkość maksymalna lub przyspieszenie.

Więcej o prefabach [Template | Learn PlayCanvas](https://developer.playcanvas.com/en/user-manual/assets/templates/)

Pominąłem temat zasobu Wasm. Myślę, że w miarę ok omówiłem możliwe zasoby w PlayCanvas.

Przejdę do części edytor.
