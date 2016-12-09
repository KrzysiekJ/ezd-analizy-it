Format danych EZD
=================

Wstęp
-----

Niniejszy dokument proponuje standard przechowywania w systemie EZD mających znaczenie prawne danych dotyczących dokumentów i spraw, który pozwoli na:

1. Zachowanie dowodliwości powstania dokumentów w konkretnym czasie.
2. Zawarcie informacji dowodzących autentyczności wytworzonych dokumentów.
3. Ustandaryzowanie procesu migracji w/w danych między różnymi systemami EZD.
4. Wydzielanie kompletów danych wybranych spraw w sposób zachowujący ich dowodliwość.

Wykonanie
---------

Elementy metryki sprawy uznajemy za obiekty istotne prawnie (i tym samym podpisywane). Każdy element metryki zawiera następujące pola:

* URI elementu poprzedniego.
* URI wykonawcy czynnośći.
* Specyfikacja czynności (polimorficzna).
* Powiązania (lista URI).

`Konkretny format elementów metryki`_ jest wyspecyfikowany w oddzielnym pliku. Format serializacji jest do ustalenia; póki co struktury danych zostały zapisane z użyciem `Protocol Buffers`_.

Pytania i odpowiedzi
~~~~~~~~~~~~~~~~~~~~

W jaki sposób zostanie przedstawione zwrócenie sprawy do dekretującego?
  Poprzez zwrotną dekretację na dekretującego.

W jaki sposób zostanie przedstawiona prośba o wkład do dokumentu?
  Poprzez nadanie uprawnień wraz z odpowiednim komentarzem.

W jaki sposób zostanie przedstawione odebranie uprawnień?
  Poprzez zmianę uprawnień z rodzaju ``ODCZYT`` lub ``ZAPIS`` na ``NIC``.

W jaki sposób zostanie przedstawione przedłożenie pisma do akceptacji?
  Poprzez dekretację z oznaczeniem pism przedłożonych do akceptacji jako „do edycji”.

W jaki sposób zostanie przedstawiona akceptacja proponowanej wersji pisma?
  Poprzez podmianę dokumentu na ten sam, z ustawioną zmienną „zaakceptowany” (ten sposób pozwala też na wprowadzenie zmian przez akceptującego).

W jaki sposób zostanie przedstawiona notatka w sprawie?
  Jako dokument w jednym z formatów tekstowych.

W jaki sposób zostanie przedstawiona akceptacja dla sposobu załatwienia sprawy?
  Jako akceptacja notatki opisującej sposób załatwienia sprawy.

W jaki sposób zostanie przedstawiony dokument z podpisem kwalifikowanym?
  Tak samo, jak każdy inny plik; klient EZD może we własnym zakresie przetworzyć plik i wyświetlić informacje o podpisie.

W jaki sposób zostanie przedstawione przyjęcie dokumentu przez kancelarię?
  Poprzez utworzenie działania dodającego dokument, niezawierającego URI elementu poprzedniego.

W jaki sposób zostanie przedstawione przekazanie dokumentu przez kancelarię do właściwej komórki?
  Poprzez dekretację „sprawy” utworzonej przy przyjęciu dokumentu przez kancelarię do właściwej komórki.

W jaki sposób zostanie przedstawione przekazanie przez kancelarię jednego dokumentu do dwóch komórek merytorycznych?
  Poprzez utworzenie działania dodającego dokument, a następnie utworzenie dwóch dekretacji na właściwe komórki.

W jaki sposób zostanie przedstawione utworzenie sprawy?
  Poprzez wykonanie działania nadającego znak sprawy.

W jaki sposób zostanie przedstawione dołączenie zadekretowanego dokumentu do akt istniejącej sprawy?
  Poprzez włączenie historii dokumentu (ostatniego działania wykonanego na dokumencie) do akt sprawy.

Pytania
~~~~~~~

#. Czy urzędnik powinien za pomocą oddzielnej czynności potwierdzać przyjęcie dekretacji do wiadomości? Bez tego nie będzie wiarygodnego dowodu, że urzędnik faktycznie otrzymał sprawę, która została mu zlecona. Być może jest to regulowane przez istniejące przepisy bądź też pozostawione do decyzji w ramach autonomii poszczególnych urzędów. Tak czy siak, pytanie jest bardziej proceduralne i wydaje się nie naruszać struktury danych formatu EZD.

Uwagi
-----

Daty zawarte w dokumentach nie mają (nie powinny mieć) większego znaczenia prawnego — znaczenie mają obiektywne daty wynikające z KSI bądź z innej usługi oznaczającej dokumenty czasem.

Nie da się efektywnie (w sposób dowodliwy) kontrolować dostępu do danych, w związku z czym rdzeń systemu nie zawiera informacji o tym, kto kiedy jaki dokument otrzymał. Można takie informacje przechowywać niezależnie, w celach poglądowych lub jeśli taka potrzeba wynika z obowiązujących przepisów. Można też w ramach systemu wytwarzać pokwitowania dostępu do dokumentów (być może jako wydzielona czynność w aktach sprawy).

Można wyobrazić sobie pracę w systemie EZD nad sprawami pobranymi już na komputer urzędnika w trybie offline, podobnie jak można pracować z Gitem w trybie offline. Można też rozważać częściową synchronizację prac z pominięciem centralnego serwera, w przypadku awarii tegoż.

.. _ciągliwość transakcji: https://en.bitcoin.it/wiki/Transaction_Malleability
.. _CAdES: https://tools.ietf.org/html/rfc5126
.. _XAdES: https://www.w3.org/TR/XAdES/
.. _Konkretny format elementów metryki: ezd.proto
.. _Protocol Buffers: https://developers.google.com/protocol-buffers/docs/proto3
