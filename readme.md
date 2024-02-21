# Charakterystyka danych
W ramach zespołów (domów znanych z Harry'ego Pottera) poszczególne osoby 
(postacie znane z Harry'ego Pottera) zdobywają punkty.

W strumieniu pojawiają się zdarzenia zgodne ze schematem `ScoreEvent`.

```
create json schema ScoreEvent(house string, character string, score int, ets string, its string);
```

Każde zdarzenie związane z jest z faktem zdobycia określonej 
liczby punktów przez określoną osobę dla określonego domu. 

Dane uzupełnione są o dwie etykiety czasowe. 
* Pierwsza (`ets`) związana jest z momentem zdobycia tych punktów. 
  Etykieta ta może się losowo spóźniać w stosunku do czasu systemowego maksymalnie do 30 sekund.
* Druga (`its`) związana jest z momentem rejestracji zdarzenia zdobycia punktów w systemie.

# Opis atrybutów

Atrybuty w każdym zdarzeniu zgodnym ze schematem `ScoreEvent` mają następujące znaczenie:

* `house`
  * typ: `string`
  * znaczenie: nazwa drużyny
* `character`
  * typ: `string`
  * znaczenie: nazwa postaci, która zdobyła punkt
* `score` 
  * typ: `int`
  * znaczenie: liczba zdobytych punktów
* `ets`
  * typ: `string` 
  * znaczenie: czas zdobycia punktów
* `its`
    * typ: `string`
    * znaczenie: czas rejestracji faktu zdobycia punktów w systemie

