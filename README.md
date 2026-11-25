# EVE Gate Travel

Narzędzie dla EVE Online, które samo przeskakuje przez kolejne bramy (stargate) ustawionej trasy aż do celu.
Uruchamiasz jeden klient gry, ustawiasz trasę (*Set Destination*), startujesz `EveGateTravel.exe` – i tyle.

## [Pobierz najnowsze wydanie](https://github.com/pa0l0s/eve-gate-travel-releases/releases/latest)

Rozpakuj ZIP. `EveGateTravel.exe`, `EveGateTravel.asdat` i `gate-travel.ini` muszą leżeć w tym samym folderze.
EXE wymaga uprawnień administratora.

## Jak używać

1. Zaloguj **jedną** postać (makro bierze pierwsze okno `EVE - *`).
2. Ustaw cel: najlepiej stację (np. *Personal Assets*, **Alt+T** → prawy klik → *Set Destination*), trasa *Safer*.
3. Overview widoczny i posortowany po *Distance* rosnąco; panel informacyjny z sekcją *Route* po lewej u góry.
4. Uruchom `EveGateTravel.exe`. Stop: **Num2**, pauza: **Num3**, albo plik `STOP` obok exe.

Na końcu pojawi się okno z liczbą skoków i powodem zakończenia; szczegóły w `gate-travel.log`.

## Ustawienia (`gate-travel.ini`)

| Ustawienie | Działanie |
|---|---|
| `MODE=auto` (domyślnie) | cel na stacji → dokuje; cel w systemie → kończy na końcu trasy |
| `MODE=station` | cel zawsze na stacji – najszybciej, dokuje na końcu |
| `MODE=system` | cel to system |
| `CLOAK=auto` (domyślnie) | lot z cloakiem (cloak + MWD trick), gdy statek ma cloak pod **F1** i MWD pod **Alt+F1** |
| `CLOAK=on` / `CLOAK=off` | wymusza włączenie / wyłączenie |

## Co robi automatycznie

- zaznacza bramę trasy w overview i skacze aż do celu, na końcu dokuje na stacji docelowej,
- akceptuje ostrzeżenia *EDENCOM Forces* i *Triglavian Forces*; każde inne ostrzeżenie (low/null sec) zostawia i kończy,
- odmawia trasy przez systemy low/null sec (0.4 i niżej) – ustaw trasę *Safer*,
- przy półprzezroczystych oknach ustawia *Settings › User Interface › Transparency* na *Off*,
- z cloakiem: *Align to* → cloak → MWD (jeden cykl) → zdjęcie cloaka tuż przed końcem cyklu → *Jump*.

## Ograniczenia

- jeden klient EVE naraz,
- domyślny układ interfejsu (panel informacyjny po lewej u góry).

Używasz na własną odpowiedzialność – automatyzacja gry może naruszać zasady EVE Online (EULA).
