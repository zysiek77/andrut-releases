# Andrut – wydania

Andrut to demo aplikacji na Androida (telefon i tablet), w której razem z AI budujesz „światy” –
małe aplikacje tworzone i zmieniane na bieżąco w czacie lub głosem.

**Najnowsza wersja: 0.1.20** – [pobierz andrut.apk](https://github.com/zysiek77/andrut-releases/raw/main/andrut.apk)

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

