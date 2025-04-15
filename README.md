# TSwR_projekt 2025

Projekt zakłada stworzenie funkcji imitującej działanie Lidar’u umieszczonego na formule f1:10. Funkcja ta na podstawie mapy oraz położenia i orientacji będzie odczytywać odległości formuły od krawędzi toru. Zwróci wartości dla kolejnych wiązek wysyłanych pod kątem z zakresu -90 do 90 stopni. Na tej podstawie sieć neuronowa zostanie nauczona aby pojazd mógł się lokalizować wykorzystując bieżące pomiary, bez konieczności wcześniejszego wgrywania mapy toru oraz znajomości dokładnego położenia. Działanie programu zostanie przetestowane pod kątem skuteczności poruszania się pojazdu w torze oraz czasu potrzebnego na obliczenie pozycji i orientacji w zależności od ilości wiązek lidara oraz rozdzielczości mapy.



Całe środowisko z symulacją ForzaETH jest tutaj:
https://github.com/ForzaETH/race_stack

Filtr cząsteczkowy / biblioteka rangelibc
https://github.com/ForzaETH/particle_filter



* Zadanie to zrobienie funkcji, która na podstawie biblioteki rangelibc, pozycji i orientacji auta oraz mapy zwróci macierz wiazek lidara.

* pomiar czasu przeliczania różnej liczby wiązek lidara (różna liczba wiązek) na odległości

* funkcja do trenowania autka w symualcji:
	- na wejściu: położenie auta z symulacji x,y, kąt obrotu/orientacja phi, mapa M --- f(x,y,phi,M)
	- na wyjściu macierz jednowymiarowa numpy zawierająca odległości oczytane z lidara co cały kąt (my go wybieramy)

* mapy w formacie zdjęcia importowane jako "occupancy grid". Później dostaniemy zbiór map do trenowaina
