# Planowanie ruchu


## Najkrótsza ścieżka między dwoma punktami

### Definicja

Na płaszczyźnie dany jest obszar D (ograniczony lub nie) z dziurami
(będącymi zbiorami otwartymi) mający w sumie n krawędzi oraz dwa
wybrane punkty s i t.
Znajdź najkrótszą ścieżkę łączącą s i t (o ile istnieje).

### Algorytmy szukania najkrótszej ścieżki między dwoma punktami

| Algorytm | Złożoność | 
| --------- | --------- |
| Algorytm Dijkstry (Hershberger, Suri) | O(nlogn) pamięć i czas |
| Zamiatanie + metoda trapezów | O(nlogn) czas, O(n) pamięć |
| Problem decyzyjny | O(nlogn) czas, O(n) pamięć |

## Ruchy robota wielokątnego w 2D

Punkt odniesienia -- środek robota.

Przestrzeń, w której porusza się robot
nazywamy ***przestrzenią rzeczywistą***.
Przestrzeń parametrów robota nazywamy
***przestrzenią konfiguracji***.

W przestrzeni tej robot przyjmuje postać jednopunktową
odpowiadającą jego punktowi odniesienia.

## Suma Minkowskiego

Rozpatrzmy wielokąty A i B jako zbiory
wektorów o współrzędnych odpowiada-
jących współrzędnym punktów
należących do tych wielokątów. Sumą
Minkowskiego wielokątów A i B jest:
A + B := {x + y : x należy do A i y należy do B}.

Powiększone przeszkody określane są przez sumę Minkowskiego D-R.

Załóżmy, że robot R ma stałą liczbę wierzchołków, a obszar D ma n wierz-
chołków.

| Rozmiar R | R | D | Rozmiar sumy | Złożoność czasowa konstrukcji | Szukanie ścieżki |
|-----------| --------- | --------- | --------| ---------- |
| O(1) | wypukły | wypukły | O(n) | O(n) | O(nlogn) |
| O(1) | wypukły | niewypukły | O(n) | O(nlogn) | O(nlogn) |
| O(1) | niewypukły | niewypukły | O(n^2) | O(n^2 logn) | O(nlogn) |
| O(m) | wypukły | wypukły | O(n + m) | - | O((n+m)log(n +m)) |
| O(m) | wypukły | niewypukły | O(nm) | - | O(nmlog(nm)) |
| O(m) | niewypukły | wypukły | O(nm) | - | O(nmlog(nm)) |
| O(m) | niewypukły | niewypukły | O((nm)^2) | - | O((nm)^2 log(nm)) |

## Ruch z możliwością obrotów

Problem planowania ruchu, w którym robot ma d stopni swobody można
rozwiązać w czasie O(n^d log n).

## Stabbing w 3D

### Definicje

Stabbing -- dla danego zbioru wypukłych wielościanów w R 3 o łącznym rozmiarze
n znajdź (o ile istnieje) prostą przeszywającą wszystkie z nich.


### Jak?

Jeśli prosta przeszywająca istnieje, to istnieje prosta przeszywająca
przechodząca przez co najmniej dwie krawędzie wielościanów.
Rozszerzając to rozumowanie możemy stwierdzić, że cztery
niewspółpłaszczyznowe proste wyznaczają prostą przecinającą je wszystkie.
Złożoność ***O(n^5)***.

Znalezienie prostej przecinającej cztery krawędzie kosztuje O(n^4) a sprawdzenie,
czy przecina wszystkie wielościany O(n). Może być O(n^2) par krawędzi
współpłaszczyznowych, których zbadanie wymaga czasu O(n log n).

Problem stabbingu w 3D można rozwiązać w czasie ***O(n 4 alfa(n) log n)***.
O(n^2 ) x (O(n log n) (rozwiązanie stabbingu planarnego) +
O(n) (rzutowanie skośne) + O(n^2 alfa(n) log n) (znalezienie części wspólnej z
wykorzystaniem ciągów Davenporta- Schinzla) ) = O(n^4 alfa(n) log n).


