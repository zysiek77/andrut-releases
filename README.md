# Andrut – wydania

Andrut to demo aplikacji na Androida (telefon i tablet), w której razem z AI budujesz „światy” –
małe aplikacje tworzone i zmieniane na bieżąco w czacie lub głosem.

**Najnowsza wersja: 0.1.67** – [pobierz andrut.apk](https://github.com/zysiek77/andrut-releases/raw/main/andrut.apk)

## Pierwsza instalacja
1. Otwórz link do `andrut.apk` na telefonie lub tablecie i pobierz plik.
2. Otwórz pobrany plik. Android zapyta o zgodę na instalację z tego źródła (przeglądarki / menedżera plików) – zezwól.
3. Zainstaluj i uruchom. Do rozmowy z AI potrzebny jest klucz API (Claude, OpenAI, Gemini, Grok, OpenRouter lub Groq) albo – bez klucza – darmowe modele LLM7. Klucz wpisujesz w ustawieniach środowiska.

## Aktualizacje
Aplikacja sama sprawdza [`version.json`](version.json) przy starcie (i przyciskiem w ustawieniach),
pobiera nową wersję, sprawdza sumę SHA-256 i otwiera okno instalacji. Za pierwszym razem Android poprosi
o zgodę „Instaluj nieznane aplikacje” dla Andruta. Każda wersja jest podpisana tym samym kluczem,
więc instaluje się jako aktualizacja – bez utraty danych.

## Historia zmian
## 0.1.67 – 2026-11-09

Przycinaj starą historię dla AI (przełącznik w ustawieniach projektu, domyślnie wyłączony): w długich sesjach mniej tokenów – stare treści plików, długie wyniki testów, stare konteksty i zrzuty nie są wysyłane ponownie. Instrukcja modelu krótsza: wskazówki ze skilli mobile-ui-patterns, canvas-2d-game i threejs-3d włączasz przełącznikami w oknie Instrukcja modelu (nowe projekty – wyłączone, istniejące – bez zmian). „Wyślij do AI” w konsoli pisze w języku projektu, a w czacie zostaje rozwijany komentarz systemowy; wszystkie komentarze systemowe pokazują po rozwinięciu, co wysłano do AI.

## 0.1.63 – 2026-11-08

Model AI projektu: w ustawieniach projektu i na dole okna nowego projektu wybierasz „Domyślny środowiska” albo „Inny model” – dostawcę z rozwijanej listy (z kluczem w środowisku oraz LLM7 bez tokena) i model z listy. Nowy projekt od razu wita się wybranym modelem.

## 0.1.59 – 2026-11-08

Nowi dostawcy: Groq (groq.com – to nie Grok) i LLM7 (llm7.io – darmowe modele bez tokena, np. gpt-oss:20b). Lista modeli z ikonkami (🖼 obrazy, 🧠 myślenie, 📄 PDF, 🎤 audio, 🎬 wideo, 🆓 darmowy, 🔑 wymaga tokena), kontekstem i ceną; filtry „darmowe / z obrazami / z myśleniem” i sortowanie; z OpenRoutera, LLM7 i Groq tylko modele czatu z narzędziami. Claude przez OpenRouter korzysta teraz z cache promptu (dużo taniej przy długich czatach); czas cache 1 godz. (domyślnie) lub 5 min w ustawieniach. Koszt w ℹ️ dla wszystkich dostawców – z OpenRoutera rzeczywisty. Jasne komunikaty: model bez narzędzi, płatny model LLM7 bez tokena, limit darmowego planu Groq, czas do odnowienia limitu.

## 0.1.53 – 2026-11-08

Pliki dla AI: w czacie 📎 „Plik” (PDF, DOCX, XLSX, PPTX, ODT, TXT…) – telefon zamienia go na tekst albo obrazy. Załączniki w skillach (dodawanie, podgląd, usuwanie); AI czyta je i może kopiować do świata. „Dodaj plik z telefonu” w plikach świata. Automatyczna naprawa błędów JS – teraz przełącznik w ustawieniach projektu, domyślnie wyłączony.

## 0.1.52 – 2026-11-08

AI może testować joysticki i gesty: interact_world umie przeciągać palcem (od elementu albo między punktami, z przytrzymaniem) i dwa palce naraz; pokazuje stan gry przed i po, ostrzega, gdy sterowanie nic nie zmieniło.

## 0.1.51 – 2026-11-08

Gry z ekranem startowym: check_world wypisuje przyciski, ostrzega o zasłoniętych i o nakładce „Start” nad grą; interact_world nie klika zasłoniętego przycisku, tylko zgłasza błąd; AI ma uruchamiać scenę od razu, a Start tylko włącza rozgrywkę. Skill three.js zaktualizowany.

## 0.1.50 – 2026-11-08

Gdy AI pracuje, a Ty wyjdziesz z projektu (pliki, konsola, lista, ustawienia), świat działa dalej w tle – sprawdzanie świata przez AI nie przerywa się. AI dostaje prawdziwą przyczynę, gdy podglądu nie ma. Pomiar sceny 3D łapie pierwszą klatkę z treścią.

## 0.1.49 – 2026-11-08

Skille: w Ustawieniach aplikacji nowy ekran Skille – instrukcje dla AI do konkretnych zadań (format Anthropic): tworzenie, edycja, włącz/wyłącz, import i eksport ZIP. W projekcie: ⋮ → Skille w projekcie. AI widzi listę i wczytuje skill, gdy zadanie pasuje. Na start 5 skilli: three.js 3D, gry 2D, wzorce UI, dane i wykresy, dźwięk i wibracje.

## 0.1.48 – 2026-11-08

AGENTS.md: gdy praca już trwa (są pliki albo plan), a pliku brak – AI dostaje polecenie, by utworzyć go od razu; w trybie etapami plan jest też zapisywany w AGENTS.md. Koniec fałszywego błędu favicon.ico w konsoli i kontroli świata.

## 0.1.47 – 2026-11-08

3D: kontrola świata mierzy jasność i kontrast sceny (wykrywa prawie niewidoczną scenę), w instrukcji wskazówki do three.js (światła r155+, kontrast, kamera), nowa opcja projektu „Zrzuty ekranu bez pytania”.

## 0.1.46 – 2026-11-08

Obrazy: jednorazowe odrzucenie obrazu przez dostawcę (np. „media could not be screened”) nie wyłącza już obrazów dla modelu na stałe; modele, które według OpenRoutera przyjmują obrazy, zawsze je dostają; w ustawieniach projektu przycisk „Przywróć obrazy”.

## 0.1.45 – 2026-11-08

Usuwanie plików świata (wybór: pliki strony, AGENTS.md, dane; z cofaniem). AI robi okna, komunikaty i listy wyboru jako elementy strony zamiast systemowych okienek (gotowe klasy w motywie, kontrola w check_world). Kolejność projektów: przytrzymaj i przeciągnij kartę, do tego sortowanie.

## 0.1.44 – 2026-11-08

Edycja plików przez AI: gdy fragment różni się tylko odstępami, zmiana się wykonuje; gdy nie pasuje, model dostaje numer linii i fragment pliku do skopiowania; powtórzone identyczne nieudane wywołanie jest wprost oznaczane.

## 0.1.43 – 2026-11-08

AGENTS.md: AI tworzy go dopiero po pierwszych konkretnych ustaleniach z Tobą (cel, pomysły, plan – także na etapie projektowania), a nie z samej nazwy projektu przy powitaniu.

## 0.1.42 – 2026-11-08

Język rozmowy z AI: przy tworzeniu projektu i w ustawieniach projektu wybierasz polski albo angielski. W wybranym języku AI dostaje instrukcję, kontekst, opisy i wyniki narzędzi oraz komunikaty aplikacji, odpowiada i pisze AGENTS.md. Pomaga modelom, które słabo znają polski. Aplikacja zostaje po polsku.

## 0.1.41 – 2026-11-08

Przycisk „Kontynuuj” pod komunikatem błędu, gdy praca AI przerwie się przez zerwany internet lub błąd dostawcy – wznawia od miejsca przerwania. W dzienniku zapis powrotu do wcześniejszej wiadomości (ile usunięto, czy cofnięto świat, czy AI pracowało).

## 0.1.40 – 2026-11-07

Naprawa równoległej pracy AI: „Zatrzymaj” i „zacznij od tej wiadomości” czekają, aż poprzednia praca naprawdę się skończy – nie ruszają dwie AI naraz. Po wykorzystaniu limitu 25 kroków AI pisze podsumowanie (co zrobiło, co zostało), a pod nim jest przycisk „Kontynuuj”. Wpisy w dzienniku: start i koniec każdej pracy AI z powodem.

## 0.1.39 – 2026-11-07

Menu projektu: „Instrukcja modelu” – podgląd i edycja instrukcji systemowej osobno dla projektu. „Czat: streszczenia i statystyki” – liczby wiadomości, narzędzi i tokenów, lista streszczeń oraz „Usuń cały czat” (świat i dane zostają).

## 0.1.38 – 2026-11-07

Przycisk „Aktualizuj” najpierw sprawdza, czy nie ma jeszcze nowszej wersji, i pobiera najnowszą (wcześniej baner mógł wskazywać starszą wersję, której pliku już nie było).

## 0.1.37 – 2026-11-07

Praca etapami: AI planuje tylko zadania do wykonania – przy pytaniach, rozmowie i drobnych poprawkach odpowiada bez planu.

## 0.1.35 – 2026-11-07

Nowa opcja projektu „Praca etapami”: AI pokazuje plan do akceptacji, realizuje go punkt po punkcie, oznacza gotowe tylko po sprawdzeniu (z opisem testu), jest ponaglane przy niedokończonym planie i kończy raportem.

## 0.1.34 – 2026-11-07

W czacie widać, jakie pliki model czyta (oraz konsolę, ogląd świata i dane świata) – z wynikiem do rozwinięcia.

## 0.1.33 – 2026-11-07

Zrzuty świata 3D nie są już czarne (dla Ciebie i dla AI). Przy przerwanej transmisji Andrut nie wykonuje żadnego narzędzia z urwanej odpowiedzi. Dziennik zapisuje, czym kończy się każda odpowiedź modelu.

## 0.1.32 – 2026-11-06

Konsola po przeładowaniu świata pokazuje tylko nowe wpisy (starsze pod „Pokaż wcześniejsze”), także dla AI. W czacie widać kod i wynik run_js oraz parametry i wyniki pozostałych narzędzi sprawdzających.

## 0.1.31 – 2026-11-06

Gdy model wklei wywołanie narzędzia jako tekst (<invoke …>), Andrut je odczytuje i wykonuje (w czacie dopisek „odczytano z tekstu”); urwane nie są wykonywane, a model dostaje wyjaśnienie.

## 0.1.30 – 2026-11-06

Gdy dostawca przerwie odpowiedź w trakcie zapisu pliku, AI dostaje prawdziwą przyczynę i radę (mniejsze części), a w czacie widać ❌ z nazwą pliku i tym, co przekazano modelowi. Aktualizacje nie trafiają już na stary plik z cache GitHuba.

## 0.1.29 – 2026-11-06

Dziennik: gdy model wyśle zepsute dane narzędzia, zapisuje się powód zakończenia odpowiedzi i surowe kawałki strumienia – do diagnozy nieudanych zapisów plików.

## 0.1.28 – 2026-11-06

Dziennik zapisuje każde wywołanie narzędzia przez AI (plik, wynik, a przy błędzie surowe dane), żeby dało się sprawdzić, czemu zapisy nie wychodzą.

## 0.1.27 – 2026-11-06

AI dostało narzędzia do sprawdzania własnej pracy: check_world (przeładowanie i raport błędów), run_js (stan świata), interact_world (klika, dotyka, naciska klawisze i patrzy na efekt) i check_syntax (składnia JS z numerami linii). AI ma ich używać, zanim napisze, że działa.

## 0.1.26 – 2026-11-06

Nowa opcja projektu „Sprawdzaj świat po zmianach AI” (domyślnie wyłączona): po zmianach aplikacja sama sprawdza konsolę i czy świat coś wyświetla, a problemy odsyła AI do poprawki (maks. 2 razy). Czat przewija się za AI tylko przy dole; po przewinięciu w górę zostaje na miejscu, przycisk ↓ wraca na dół.

## 0.1.25 – 2026-11-06

Naprawa błędu HTTP 400 z Cohere (OpenRouter, np. north-mini-code): argumenty wcześniejszych wywołań narzędzi w historii są teraz zawsze poprawnym obiektem JSON – czat, w którym inny model zapisał zepsute argumenty, znów działa. Obsługa argumentów narzędzi przysłanych jako obiekt.

## 0.1.24 – 2026-11-06

Naprawiony czarny ekran w światach: podgląd ma pełny rozmiar, więc 100vh/100dvh działa (wcześniej wynosiło 0 px). Dziennik zapisuje wczytanie świata i rozmiar okna, a po awarii silnika podglądu świat uruchamia się ponownie sam.

## 0.1.22 – 2026-11-05

Przywracanie projektu z pliku ZIP (menu ⋮): wybierasz, co przywrócić – pliki świata, dane świata, rozmowę, ustawienia; ostrzeżenie, gdy plik jest z innego projektu (można go też zaimportować jako nowy); automatyczna kopia i „Cofnij przywrócenie”. Automatyczne streszczenie rozmowy domyślnie przy 150 tys. tokenów, z możliwością zmiany w ustawieniach środowiska i projektu (także wyłączenia); w ℹ️ widać kontekst / próg.

## 0.1.21 – 2026-11-05

Poprawka: przy przełączaniu Świat/Czat nie znika wpisany tekst, a czat zostaje w tym samym miejscu (bez przewijania). Niewysłany szkic jest zapamiętywany osobno dla każdego projektu, także po zamknięciu aplikacji.

## 0.1.20 – 2026-11-05

Internet przez aplikację: AI samo wyszukuje (DuckDuckGo) i czyta strony oraz dane z API przez telefon – działa z każdym dostawcą (drugi przełącznik w ustawieniach projektu; dotychczasowy to teraz „Dostęp do internetu przez dostawcę”). Tryb Jasny/Ciemny/Auto w każdym projekcie (domyślnie jak w aplikacji). Ustawienia projektu pokazują globalny model, poziom myślenia i długość odpowiedzi ze środowiska.

## 0.1.19 – 2026-11-05

Okienka i menu są kryjące i czytelne we wszystkich motywach. Osobne „Pliki” i „Konsola błędów” (z liczbą nowych błędów), a AI samo czyta konsolę. Zrzuty ekranu działają z modelami, które przyjmują tylko jeden obraz (np. Nemotron VL). Działania projektu w menu ⋮ zamiast w informacjach.

## 0.1.18 – 2026-11-05

Tekst czytelny we wszystkich motywach (także ciemnych). Podgląd plików z kolorowaniem składni, Markdown jako podgląd, zawijanie i A−/A+. Lista modeli nie zawiesza się – okienko postępu i czytelny błąd. Import projektu z „+” i przez „Udostępnij → Andrut”.

## 0.1.17 – 2026-11-05

Zrzuty ekranu i podgląd świata dla AI działają też w poziomie, po pełnym ekranie i w trybie z wysuwanym czatem. Nowe: „Zrzut świata” w menu 📎, duplikowanie projektów (gałęzie z innym motywem), AGENTS.md – dokumentacja projektu prowadzona przez AI.

## 0.1.16 – 2026-11-05

Nowe: „Pliki i konsola” – lista plików świata, podgląd treści, ostrzeżenia o brakujących plikach i konsola błędów z „Wyślij do AI”. Maks. długość odpowiedzi do ustawienia; koniec błędu 402 w OpenRouterze przy zwykłych rozmowach. Błędy w czacie da się skopiować.

## 0.1.15 – 2026-11-05

Skrót na ekranie głównym: potwierdzenie albo okienko z przyciskiem do uprawnień. Przyciski ◀ ⛶ ⟳ w górnym pasku (na telefonie w menu ⋮). „Cofnij zmiany” pod ostatnią odpowiedzią AI, z potwierdzeniem. Gry i prezentacje mieszczą się w oknie. Aktualizacje sprawdzane też po powrocie do aplikacji.

## 0.1.14 – 2026-11-05

Poprawka: aplikacja nie wysypuje się już przy otwieraniu projektu, który ma świat.

## 0.1.13 – 2026-11-05

Przycisk ◀ i gest wstecz w świecie, ↩️ cofnij zmiany AI, ⛶ pełny ekran i skrót świata na ekranie głównym. Zdjęcia w czacie (📎), rozmowa bez rąk (🎧), streszczanie długich rozmów (taniej), szybsze poprawki plików. Świat może używać aparatu, lokalizacji, czujnika ruchu i przypomnień. Eksport/import projektu, dziennik błędów do wysłania.

## 0.1.12 – 2026-11-05

Odpowiedź AI na żywo (streaming) – koniec z „błędem sieci” przy długim myśleniu, automatyczne ponowienie i praca w tle z powiadomieniem. Zaznaczanie tekstu w dymkach, ikonki ✏️/📋, edycja zawsze dostępna. Opcjonalny dostęp AI do internetu ze źródłami. Auto-naprawa: 3 próby.

## 0.1.10 – 2026-11-05

Formatowanie odpowiedzi AI, kopiowanie (przytrzymaj dymek lub 📋), edycja własnej wiadomości, poziom myślenia i streszczenie 💭, wyszukiwanie modeli, styl odpowiedzi (domyślnie zwięzły), Piper nie ucina początku, poprawka Aurory na tablecie.

## 0.1.8 – 2026-11-05

Piper nie ucina już początku i końca wypowiedzi. 7 nowoczesnych motywów graficznych (projekt + aplikacja) z trybem Auto/Jasny/Ciemny. Aktualizacje prosto z aplikacji.

## 0.1.6 – 2026-11-04

Głosy systemowe i neuronowe Piper (offline), głos per projekt; przełącznik czat/podgląd w pasku; AI widzi stan świata (dane, dziennik, tekst ekranu); zrzut ekranu świata za zgodą; karty pytań z opcjami; informacje o tokenach i plikach.

## 0.1.4 – 2026-11-04

Odpowiedź głosem tylko po pytaniu głosowym; ikona 🔊 pod odpowiedziami.

## 0.1.3 – 2026-11-04

Układ dla tabletów i poziomej orientacji.

## 0.1 – 2026-11-04

Pierwsza wersja: środowiska, projekty, wielu dostawców AI, czat i rozmowa głosowa, świat HTML/JS w podglądzie.

