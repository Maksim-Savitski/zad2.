




# Lekcja 1 – Markdown lekki język znaczników

## Spis treści

Lekcja 1 – Markdown lekki język znaczników.................................................................................... 1
Wstęp............................................................................................................................................... 1
Podstawy składni............................................................................................................................. 3

Definiowanie nagłówkówDefiniowanie list.................................................................................................................................................................................................................................... (^34)
Wyróżnianie tekstu...................................................................................................................... 4
Tabele.......................................................................................................................................... 5
Odnośniki do zasobów................................................................................................................ 5
ObrazkiKod źródłowy dla różnych języków programowania......................................................................................................................................................................................................... (^55)
Tworzenie spisu treści na podstawie nagłówków....................................................................... 6
Edytory dedykowane....................................................................................................................... 7
Pandoc – system do konwersji dokumentów Markdown do innych formatów............................... 8
Lekcja 2 – Git – system kontroli wersji................................................................................................ 9
Git - podstawowe cechy................................................................................................................... 9
Idea pracy:........................................................................................................................................ 9
Git – tworzenie pustego archiwum lokalnego............................................................................... 11
Zadania do wykonania na punkty....................................................................................................... 21
Zadanie 1 – 2pkt............................................................................................................................ 21
Zadanie 2 – 4pktZadanie 3 - 4pkt......................................................................................................................................................................................................................................................... (^2121)

## Wstęp

Obecnie powszechnie wykorzystuje się języki ze znacznikami do opisania dodatkowych informacji
umieszczanych w plikach tekstowych. Z pośród najbardziej popularnych można wspomnieć o:

1. **html** – służącym do opisu struktury informacji zawartych na stronach internetowych,
2. **Tex** (Latex) – poznany na zajęciach język do „profesjonalnego” składania tekstów,
3. **XML** ( _Extensible Markup Language)_ - uniwersalnym języku znaczników przeznaczonym
    do reprezentowania różnych danych w ustrukturalizowany sposób.


Przykład kodu html i jego interpretacja w przeglądarce:
<!DOCTYPE < **html** > **html** >
<< **headmeta** > charset="utf-8" />
<<title/ **head** >Przykład<> /title>
<< **bodyp** > Jakiś paragraf tekstu<> / **p** >
<<// **bodyhtml** >>

Przykład kodu _Latex_ i wygenerowanego pliku w formacie _pdf_
\\documentclassusepackage{lipsum[]{letter} }
\\usepackagesetmainlanguage{polyglossia{polish}}
\\ **beginbegin** {{ **documentletter** }{ **Szanowny Panie XY** } }
\\addressopening{{}Adres do korespondencji}
\\lipsumsignature[ 2 ]{Nadawca}
\\closing **end** { **letter** {Pozdrawiam} }
\ **end** { **document** }

Przykład kodu XML – fragment dokumentu SVG (Scalar Vector Graphics)
<!DOCTYPE < **html** > **html** >
<<svg **body** height> ="100" width="100">
<circle cx</svg> ="50" cy="50" r="40" stroke="black" stroke-width="3" fill="red" />
<<// **htmlbody** >>

W tym przypadku mamy np. znacznik np. < _circle_ > opisujący parametry koła i który może być
właściwie zinterpretowany przez dedykowaną aplikację (np. przeglądarki www).
Jako ciekawostkę można podać fakt, że również pakiet MS Office wykorzystuje format XML do
przechowywania informacji o dodatkowych parametrach formatowania danych. Na przykład pliki z
rozszerzeniem _docx_ , to nic innego jak spakowane algorytmem zip katalogi z plikami xml.


$Archive: unzip -l **testtest** .docx.docx

Length --------- ---------- **Date** (^) ----- **Time** ---- Name
573731 2020-10-112020-10-11 1818 :: 2020 _rels docProps **/** .rels **/** core.xml
508531 2020-10-112020-10-11 1818 :: 2020 docProps word **/** _rels **/** app.xml **/** document.xml.rels
14212429 2020-10-112020-10-11 1818 :: 2020 word word **//** document.xmlstyles.xml
853241 2020-10-112020-10-11 1818 :: 2020 word word **//** fontTable.xmlsettings.xml
1374 2020-10-11 18 : 20 **[** Content_Types **]** .xml
Wszystkie te języki znaczników cechują się rozbudowaną i złożoną składnią i dlatego do ich edycji
wymagają najczęściej dedykowanych narzędzi w postaci specjalizowanych edytorów. By
wyeliminować powyższą niedogodność powstał **Markdown** - uproszczony język znaczników
służący do formatowania dokumentów tekstowych (bez konieczności używania specjalizowanych
narzędzi). Dokumenty w tym formacie można bardzo łatwo konwertować do wielu innych
formatów: np. html, pdf, ps (postscript), epub, xml i wiele innych. Format ten jest powszechnie
używany do tworzenia plików README.md (w projektach open source) i powszechnie
obsługiwany przez serwery git’a. Język ten został stworzony w 2004 r. a jego twórcami byli John
Gruber i Aaron Swartz. W kolejnych latach podjęto prace w celu stworzenia standardu rozwiązania
i tak w 2016 r. opublikowano dokument RFC 7764 który zawiera opis kilku odmian tegoż języka:

- CommonMark,
- GitHub Flavored Markdown (GFM),
- Markdown Extra.

## Podstawy składni

Podany link: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet zawiera opis
podstawowych elementów składni w języku angielskim. Poniżej zostanie przedstawiony ich krótki
opis w języku polskim.

### Definiowanie nagłówków

W tym celu używamy znaków kratki: #
Lewe okno zawiera kod źródłowy – prawe -podgląd przetworzonego tekstu


### Definiowanie list

Listy numerowane definiujemy wstawiając numery kolejnych pozycji zakończone kropką.
Listy nienumerowane definiujemy znakami: ***,+,-**


### Wyróżnianie tekstu

### Tabele

Centrowanie zawartości kolumn realizowane jest poprzez odpowiednie użycie znaku dwukropka **:**

### Odnośniki do zasobów

[odnośnik do zasobów](www.gazeta.pl)
[odnośnik do pliku](LICENSE.md)
[odnośnik do kolejnego zasobu][1]
[1]: [http://google,com](http://google,com)

### Obrazki

![alt text](https://server.com/images/icon48.png "Logo 1") – obrazek z zasobów
internetowych
![](logo.png) – obraz z lokalnych zasobów


### Kod źródłowy dla różnych języków programowania

### Tworzenie spisu treści na podstawie nagłówków


## Edytory dedykowane

Pracę nad dokumentami w formacie Markdown( rozszerzenie md) można wykonywać w
dowolnym edytorze tekstowym. Aczkolwiek istnieje wiele dedykowanych narzędzi:

1. Edytor Typora - https://typora.io/
2. Visual Studio Code z wtyczką „markdown preview”


## Pandoc – system do konwersji dokumentów Markdown do

## innych formatów

Jest oprogramowanie typu _open source_ służące do konwertowania dokumentów pomiędzy
różnymi formatami.
Pod poniższym linkiem można obejrzeć przykłady użycia:
https://pandoc.org/demos.html
Oprogramowanie to można pobrać z spod adresu: https://pandoc.org/installing.html
Jeżeli chcemy konwertować do formatu _latex_ i _pdf_ trzeba doinstalować oprogramowanie
składu _Latex_ (np. Na MS Windows najlepiej sprawdzi się Miktex - https://miktex.org/)
Gdyby podczas konwersji do formatu _pdf_ pojawił się komunikat o niemożliwości
znalezienia programu _pdflatex_ rozwiązaniem jest wskazanie w zmiennej środowiskowej
**PATH** miejsca jego położenia


Pod adresem ( _https://gitlab.com/mniewins66/templatemn.git_ ) znajduje się przykładowy plik
Markdown z którego można wygenerować prezentację w formacie _pdf_ wykorzystując
klasę latexa _beamer_.
W tym celu należy wydać polecenie z poziomu terminala:
$pandoc templateMN.md -t beamer -o prezentacja.pdf