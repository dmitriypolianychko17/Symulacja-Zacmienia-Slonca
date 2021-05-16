# Symulacja-Zacmienia-Slonca

Celem projektu jest odzwierciedlenie przyszłych zaćmień Słońca, które przechodzą przez lokalizację zdefiniowaną przez użytkownika. 
Projekt jest stroną internetową, która ładuję i przetwarza dane zaćmień Słońca w zależności od lokalizacji które są wyciągane z usługi hostowanej przez AGOL
z 905 ścieżkami zaćmienia słońca od 1601 do 2200 r. Ścieżki zaćmienia zostały przygotowane przez Michaela Zeilera. Strona umożliwia zapoznanie się z zaćmieniami Słońca,
a także pokazuje informacje o parametrach które mają wplyw na prewidywanie zaćmień. Ze względu na to że bardzo ciężko wyznaczyć każde zaćmienie w każdym punkcie lokalizacji 
(dla tego były napisane całe zlożone algorytmy i programy którym dla tego żeby wszystko obliczyć potrzebna ogromna ilość pamięci)
i informacja dotycząca takich algorytmów nie jest ogólnodostępna.  

1. Część teoretyczna:

  Zaćmienia Słońca nie są wcale rzadkie. Oni występują znacznie częściej niż księżycowe, od dwóch do pięciu razy w roku. Jednak bardzo rzadko można obserwować całkowite zaćmienie z jednego punktu, średnio raz na 300-400 lat. 
Częściowe zaćmienia - kiedy Księżyc zakrywa tylko część tarczy Słońca - każdy może zobaczyć więcej niż raz w życiu. Powtarzane są co 2-3 lata. W przeciwieństwie do zaćmień całkowitych, podczas których ptaki cichną, a na dziennym niebie pojawiają się jasne gwiazdy, zaćmienia częściowe, jeśli faza nie jest zbyt duża, nie mogą być zauważone bez powiadomienia i bez specjalnej optyki, której nie widać. Zastanówmy się, jakie są przyczyny tej ofensywnej niesprawiedliwości?
Faktem jest, że Księżyc jest znacznie mniejszy niż Ziemia i znajduje się bardzo daleko. Średnica jego cienia nie przekracza 270 km. Całkowite zaćmienie obserwuje się tylko w strefie przejścia tego bardzo małego punktu. Wokół znajduje się półcień, której średnica przy maksymalnym rozmiarze zbliża się do 6750 km. A to już ogromna odległość. Inną rzeczą jest to, że im dalej obserwator jest od głównego paska faz, tym mniej Słońce będzie dla niego ukryte. Bliżej krawędzi półcieni zaćmienie będzie zauważane nieco bardziej niż nijak. Czasami księżycowy cień całkowicie omija Ziemię, a półcień częściowo ją uchwyca, wtedy występują tylko częściowe zaćmienia.

![image](https://user-images.githubusercontent.com/61449911/118393614-b5dd1e80-b648-11eb-854e-e6a8ef5e50c4.png)

Jak zachodzą zaćmienia słońca?
Zaćmienie słońca występuje tylko podczas nowiu. Cień księżyca podczas nowiu zwykle pada poza ziemię. Dwa razy w roku Księżyc przecina płaszczyznę ekliptyki (cień Księżyca pada na powierzchnię Ziemi).
Fakty:
- Minimalna prędkość poruszania się księżycowego cienia na powierzchni ziemi to nieco ponad 1 km / s.
- Oszustwo optyczne: rzeczywista średnica Słońca jest prawie 400 razy większa od Księżyca, a Słońce znajduje się około 400 razy dalej od Ziemi, dzięki czemu ich pozorne rozmiary są bardzo zbliżone.
- Pas całkowitej fazy zaćmienia słońca to ślad z cienia księżyca, który może sięgać nawet 270 km.

Rodzaje zaćmień:
- Częściowe: Słońce nie jest całkowicie zaćmione.
- Pierścieniowe: strefa krawędzi Słońca pozostaje niezamknięta.
- Pełne: dysk Słońca zamyka się całkowicie.
- Hybrydowe: w zależności od położenia obserwatora można zobaczyć całkowite lub pierścieniowe zaćmienie.

Zaćmienia Słońca w XXI wieku:

![image](https://user-images.githubusercontent.com/61449911/118393685-018fc800-b649-11eb-98f8-041fa358952a.png)

2. Część praktyczna:

Dla danego projektu były wykorzystywane biblioteki ArcGIS dla JavaScript stworzone przez firmę  ArcGIS - twórcy programów oraz bibliotek przeznaczonych do pracy na mapach i danych GIS (System Informacji Geograficznej). Pakiet umożliwia tworzenie i przetwarzanie istniejących map, analizę danych przestrzennych oraz ich wizualizację i zarządzanie danymi w geobazach. Dla renderowania wektorów które pokazują pasy zaćmień Słońca była wykorzystana technologia ArcGIS API, ale potem jak okazało się ona nie może obslugiwać liniowego wypełnienia gradientowego, dla tego była użyta technologia JavaScript D3.js do wstawiania i stosowania liniowych wypełnień  gradientowych bezpośrednio do osadzonego węzła SVG mapy.  Dla stworzenia samej strony internetowej HTML były wykorzystane biblioteki Bootstrap oraz jQuery Bootstrap.

Po odkryciu projektu widzimy przed sobą mapę światu: 

![image](https://user-images.githubusercontent.com/61449911/118393714-26843b00-b649-11eb-9cdc-9ddc4a9f50d6.png)

Żeby zobaczyć przyszłe zaćmienia Słońca, które przechodzą przez lokalizację zdefiniowaną przez użytkownika mamy nacisnąć na dowolny punkt mapy: 

![image](https://user-images.githubusercontent.com/61449911/118393735-40be1900-b649-11eb-82c8-fe107a6e1a29.png)

Dalej żeby zobaczyć typ zaćmienia i jego szczegóły mamy nacisnąć na zielony pasek: 

![image](https://user-images.githubusercontent.com/61449911/118393746-516e8f00-b649-11eb-9e75-e45268264451.png)

Także przy najechaniu myszką na szczególy zaćmienia możemy przeczytać pojaśnienie szczegółow: 

![image](https://user-images.githubusercontent.com/61449911/118393790-837ff100-b649-11eb-80e6-f2362bfd5c34.png)


Wykorzystane technologie:
- HTML
- JavaScript
- ArcGIS
- JavaScript D3
- Bootstrap
- jQuery
- jQuery Bootstrap
- CSS

Opis uruchomienia projektu:
Do uruchomienia projektu należy rozpakować archiwum do folderu servera (np. XAMPP) i otworzyć go w przeglądarce.
Projekt jest uruchamiany na localhost komputera. 

Żródła:
Strona NASA dotycząca obliczania delty-T i podstawowych info o zaćmieniach Słońca: https://eclipse.gsfc.nasa.gov/solar.html
Strona do teorii, faktów o zaćmieniach: https://kp-tts.ru/kak-mozhno-vychislit-datu-lunnyh-zatmenii-vruchnuyu-predskazaniya.html 
Książka Kazimierza M. Borkowskiego „Astronomiczne obliczenia nie tylko dla geografów”



