# naseeditor
Edytor VST3 dla Novation A-Station — pełna kontrola brzmienia z poziomu DAW. Dwukierunkowa synchronizacja MIDI z hardware, import banków .syx, zapis presetów, odbiór dumpów z syntezatora, biblioteka banków/patchy i panel odwzorowujący sekcje racka (OSC, LFO, filtr, efekty, arpeggiator). / C++.

NaseEditor to wtyczka VST3 (instrument MIDI), która pełni rolę graficznego edytora i mostu między DAW a rackiem Novation A-Station. Zamiast ograniczać się do podstawowych komunikatów CC, daje dostęp do pełnej architektury dźwięku syntezatora w jednym, czytelnym panelu odwzorowującym sekcje hardware.

Projekt powstał z myślą o producentach muzycznych i sound designerach pracujących z A-Station w studiu — szczególnie w Ableton Live, ale wtyczka działa w każdej DAW obsługującej VST3.

Najważniejsze funkcje
Panel sterowania 1:1 z rackiem
Oscylatory — fale, oktawy, PWM, sync, wybór OSC
LFO — wybór, fala, synchronizacja
Mixer — poziomy, źródła, unison
Filtr — cutoff, resonance, envelope, slope
Obwiednie — AMP i MOD (A/D/S/R)
Efekty — reverb, delay, chorus, distortion
Sekcja rozszerzona — pan, arpeggiator, EQ, FM, filter+
Master — volume, portamento, preglide, nawigacja bank/patch

Synchronizacja z hardware
Wysyłanie zmian parametrów na Novation w czasie rzeczywistym
Status SYNC OK / Resync — pełna synchronizacja stanu brzmienia
Automatyczna synchronizacja po wczytaniu projektu DAW
Obsługa natywnego formatu programów Novation (128-bajtowe bloki)

Presety i biblioteka
Nawigacja HW BANK / HW PATCH (hardware)
Osobna biblioteka LIB BANK / LIB PATCH (zaimportowane banki)
Import bank — wczytywanie plików .syx
Load folder — import całego folderu z bankami i presetami
Save preset / Load preset — własne presety (.syx, .astpatch)
Reset library — czyszczenie katalogu zaimportowanych banków

Odbiór dumpów z syntezatora
Receive dump — nasłuch na SysEx wysłany z Novation
Obsługa dumpu pojedynczego presetu i całego banku
Instrukcja w overlay: GLOBAL → Utilities → MIDI Dump (7 = preset, 6 = bank)
Zapis odebranych danych do pliku .syx / .astpatch

Wymagania
DAW
Dowolna z obsługą VST3 (testowane w Ableton Live)
Hardware
Novation A-Station
MIDI
Port MIDI OUT do syntezatora
