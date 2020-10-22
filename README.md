# jaz_first

## Objectives

symulator SKM:

- Gradle, Docker, Git
- dwie aplikacje: symulator i klient
- wszystkie stacje od GDYNIA GLOWNA do GDANSK GLOWNY (powinno ich byc ok 15)
- dystans miedzy stacjami uznajemy za jednakowy
- bedzie naraz jezdzilo X pociagow, kazdy pociag ma miec Y przedzialow, kazdy przedzial - pomiesci Z osob
- X,Y,Z ladujemy z pliku konfiguracyjnego
- gdy pociag dojezdza do stacji, pojawia sie na niej losowa (2-8) ilosc osob, ktore chca sie dostac na losowy przystanek na dalszej czesci tej linii.
  Wysiadaja z pociagu gdy dotra na miejsce
- gdy pociag dojezdza na koniec linii, robi postoj na 2 tury, po czym rusza w przeciwnym kierunku
- symulator powinien miec:
  - endpoint na przesuniecie symulacji do przodu - pociagi sie przesuwaja o jedno pole, np:
        POST symulator:9000/doprzodu
  - wystawic endpointy dla klienta
- klient ma miec mozliwosc odpytania symulatora o:
  - ilosc pociagow np:
	GET api:8080/pociagi - i otrzymac w odpowiedzi JSONa z danymi pociagow: w tym przypadku tylko numer identyfikacyjny
  - stan pociagu np:
        GET api:8080/pociagi/1234 - otrzymac w odpowiedzi JSONa z danymi pociagu o id 1234: numer id, procentowe zapelnienie przedzialow, ilosc osob

Dodatkowo:
- kazdy czlowiek ma miec losowe imie i nazwisko, klient powinien moc dopytac symulator o informacje o przedziale i w odpowiedzi otrzymac informacje o pasazerach