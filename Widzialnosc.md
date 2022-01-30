# Widzialność

## Problem galerii

Decyzyjny problem galerii w 2D jest NP-zupełny,
można go zredukować do 3-CNF-SAT.

### Galeria dla krawędzi

Czasem interesuje nas tylko przypadek, gdy strzeżone są jedynie krawędzie
wielokąta.

## Lemat na ograniczenie górne

Liczba strażników w galerii o n wierzchołkach jest nie mniejsza od 1 i nie
większa niż n.

## Lepsze ograniczenie górne

Do pilnowania galerii potrzeba i wystarcza n//3 strażników.
Potrzeba dokładnie tyle dla "grzebienia".

## Ochrona wypukłych podzbiorów zbiorów punktów

Niech k >= 3 będzie liczbą całkowitą. Przez G_k (n)
oznaczmy najmniejszą liczbę s taką, że każdy zbiór
n punktów na płaszczyźnie P ma zbiór k-wypukłych
strażników rozmiaru s.
Lemat.
G_n (n) <= G_(n-1) (n) <= .... <= G_3 (n).

### Twierdzenie.

Jeśli punkty ze zbioru P tworzą wielokąt wypukły,
to G_3 (n) = n-2.

Dla dowolnego k >= 3 nie może być
mniej strażników niż (n-2)//(k-2) (bo możemy po-
dzielić wielokąt na rozłączne podwielokąty).


## Iluminacje

Każdy trójkąt można oświetlić trzema lampami o kącie oświetlenia PI/6,
umieszczonymi w jego wierzchołkach.

## Graf widzialności

Graf widzialności może mieć rozmiar kwadratowy, więc algorytm znajdujący ten
graf wymaga w pesymistycznym przypadku czasu ***O(n^2)***, n to liczba odcinków.


## Grafy łukowe

* Znajdywanie minimalnego pokrycia klikami
* Problem Odyseusza
* Uproszczony problem rozgłaszania