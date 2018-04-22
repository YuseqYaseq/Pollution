# Pollution

Utw�rz nowy modul o nazwie _pollution_, kt�ry bedzie zbieral i przetwarzal dane ze stacji mierzacych jakosc powietrza. Modul powinien przechowywac:



* informacje o stacjach pomiarowych,

  * wsp�lrzedne geograficzne,

  * nazwy stacji pomiarowych,

* zmierzone wartosci pomiar�w, np stezenia pyl�w PM10, PM2.5 czy wartosci temperatury (wraz z data i godzina pomiaru).



Nie powinno byc mozliwe:



* dodanie dw�ch stacji pomiarowych o tej samej nazwie lub tych samych wsp�lrzednych;

* dodanie dw�ch pomiar�w o tych samych:

  * wsp�lrzednych,

  * dacie i godzinie,

  * typie (PM10, PM2.5, temperatura, �);

* dodanie pomiaru do nieistniejacej stacji.



Zaprojektuj strukture danych dla przechowywania takich informacji (jest przynajmniej kilka dobrych rozwiazan tego problemu).



Zaimplementuj funkcje w module pollution:


* _createMonitor/0_ - tworzy i zwraca nowy monitor zanieczyszczen;

* _addStation/3_ - dodaje do monitora wpis o nowej stacji pomiarowej (nazwa i wsp�lrzedne geograficzne), zwraca zaktualizowany monitor;

* _addValue/5_ - dodaje odczyt ze stacji (wsp�lrzedne geograficzne lub nazwa stacji, data, typ pomiaru, wartosc), zwraca zaktualizowany monitor;

* _removeValue/4_ - usuwa odczyt ze stacji (wsp�lrzedne geograficzne lub nazwa stacji, data, typ pomiaru), zwraca zaktualizowany monitor;

* _getOneValue/4_ - zwraca wartosc pomiaru o zadanym typie, z zadanej daty i stacji;

* _getStationMean/3_ - zwraca srednia wartosc parametru danego typu z zadanej stacji;

* _getDailyMean/3_ - zwraca srednia wartosc parametru danego typu, danego dnia na wszystkich stacjach;



W funkcjach uzywaj nastepujacych typ�w i format�w danych:


* do przechowywania dat uzyj struktur z modulu calendar (zob. calendar:local_time(). ),

* wsp�lrzedne geograficzne to para (krotka) liczb,

* nazwy, typy to ciagi znak�w.



Napisz testy do modulu _pollution_ z wykorzystaniem EUnit.
