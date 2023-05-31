# Projek procesora Z80

## Przygotwanie projektu

---
### Wymagania:

- Zainstalowany program 'Logisim Evolution'<br>
https://github.com/logisim-evolution/logisim-evolution
https://sourceforge.net/projects/logisimevolution/

- Uruchomić plik Z80.circ w programie logisim-evolution

### Obługa układu:

Cały procesor obsługuje się w głownym układzie o nazwie Z80.
Po wyświetleniu głównego układu należy na sztywno wprowadzić kolejne instrukcje do pamięci w postaci heksadecymalnej.

Do sterowania całością zostały przygotwane dwa przyciski (CLOCK/CLK, RESET). Klikając przycisk CLK/CLOCK procesor zacznie zczytywać kolejne instrukcje a następnie wykonywać je. W trakcie testowania układu możliwe jest przechodzenie po różnych częściach procesora w celu podejrzenia aktualnych stanów, wejść, wyjść (Zakładka 'simulation').

Dla przykładu został wgrany nastepujący program:

```
1E C0 43
```

Który ma za zadanie:

```
[1E] 00 011 110 -- Pobrać liczbę 'n' oraz zapisać ją do rejestru 'E'
[C0] 11 000 000 -- Liczba 'n' która zostanie wczytana w ramach poprzedniej instrukcji
[43] 01 000 011 -- Skopiowanie wartości rejestru 'E' do rejestru 'B'
```