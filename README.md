# Andrut – wydania

Andrut to demo aplikacji na Androida (telefon i tablet), w której razem z AI budujesz „światy” –
małe aplikacje tworzone i zmieniane na bieżąco w czacie lub głosem.

**Najnowsza wersja: 0.1.31** – [pobierz andrut.apk](https://github.com/zysiek77/andrut-releases/raw/main/andrut.apk)

## Pierwsza instalacja
1. Otwórz link do `andrut.apk` na telefonie lub tablecie i pobierz plik.
2. Otwórz pobrany plik. Android zapyta o zgodę na instalację z tego źródła (przeglądarki / menedżera plików) – zezwól.
3. Zainstaluj i uruchom. Do rozmowy z AI potrzebny jest klucz API (Claude, OpenAI, Gemini, Grok lub OpenRouter) – wpisujesz go w ustawieniach środowiska.

## Aktualizacje
Aplikacja sama sprawdza [`version.json`](version.json) przy starcie (i przyciskiem w ustawieniach),
pobiera nową wersję, sprawdza sumę SHA-256 i otwiera okno instalacji. Za pierwszym razem Android poprosi
o zgodę „Instaluj nieznane aplikacje” dla Andruta. Każda wersja jest podpisana tym samym kluczem,
więc instaluje się jako aktualizacja – bez utraty danych.

## Historia zmian
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

