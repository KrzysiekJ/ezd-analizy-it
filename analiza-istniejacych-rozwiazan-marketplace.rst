Analiza istniejących rozwiązań marketplace’ów
=============================================

Streszczenie
------------

Cel
~~~

Opracowanie listy istniejących rozwiązań, które można wykorzystać do
stworzenia marketplace’u aplikacje.gov.pl.

Sposób realizacji
~~~~~~~~~~~~~~~~~

-  Zgromadzenie listy wymaganych od marketplace’u funkcji.
-  Zgromadzenie listy istniejących rozwiązań.
-  Sprawdzenie, czy rozwiązania mają funkcje wymagane od marketplace’u
   aplikacje.gov.pl.
-  Zebranie rozwiązań, które spełniają wszystkie wymagania.
-  Zebranie rozwiązań, które mają część funkcji, a funkcje brakujące
   mogą być uzupełnione przez inny system.

Konkluzja
~~~~~~~~~

Systemy, które mają dużą część wymaganych funkcji: pakiet
OpenStack/Murano, YaaS - dostępny jest jako „software as a service” -
oprogramowanie nie jest dostępne.

Systemy, które mają część wymaganych funkcji: Docker Engine, Kubernets.

Kontekst badawczy
-----------------

Założenie polskiej platformy aplikacji dla administracji
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Cel
```

Serwis aplikacje.gov.pl ma zapewnić administracji rządowej (a w dalszej
perspektywie także samorządowej) jedno z najważniejszych narzędzi do
codziennej pracy operacyjnej. Ma on funkcjonować na zasadzie
marketplace’u. Pierwszą aplikacją będzie usługa do elektronicznego
zarządzania dokumentacją (EZD), pozwalająca w sposób nowoczesny
zarządzać dokumentacją w administracji publicznej.

Korzyści dla administracji
``````````````````````````

-  Serwis Aplikacje.gov.pl oprócz aplikacji do zarządzania dokumentacją
   i modułami dodatkowymi uzupełniającymi jej funkcjonalności, będzie
   oferował inne aplikacje wspierające pracę urzędu. Wszystkie aplikacje
   oferowane będą w chmurze publicznej jako SaaS oraz będą posiadały
   zestandaryzowane API, co umożliwi wymianę dokumentów i integrację w
   ramach procesów biznesowych.
-  Wszystkie aplikacje wytworzone w ramach projektu oferowane będą
   administracji rządowej na zasadach niekomercyjnych.
-  Na portalu Aplikacje.gov.pl oferowane będą również aplikacje i moduły
   do tych aplikacji wytworzone przez dowolnych producentów
   oprogramowania. Po zweryfikowaniu ich przez administratora portalu
   (proces certyfikacji) będą mogły być nabywane przez administrację
   publiczną w trybie SaaS.
-  Dzięki otwarciu portalu Aplikacje.gov.pl liczni dostawcy
   oprogramowania będą mogli oferować swoje aplikacje wspierające
   procesy w administracji publicznej oraz moduły wspierające te
   aplikacje w nowy, niedostępny obecnie sposób.
-  Portal Aplikacje.gov.pl oraz pracujące na nim aplikacje zostaną
   uruchomione na specjalnie zaprojektowanej w ramach projektu
   infrastrukturze serwerowej chronionej od strony bezpieczeństwa przez
   zespół i systemy SOC (Security Operation Center). Możliwość
   przeglądania dostępnych aplikacji i modułów będzie publiczna, możliwa
   dla każdego

Warunki użycia
``````````````

Aby aktywnie korzystać z aplikacji dostępnej na Aplikacje.gov.pl,
instytucja będzie musiała w pierwszej kolejności założyć konto. Konto
będzie mogła założyć tylko osoba uprawniona jako reprezentant danej
organizacji. Rejestracja się w chmurze będzie wymagała podania danych
rejestrowych, adresu email i danych reprezentanta. Dzięki połączeniu z
zewnętrznymi bazami rejestrów państwowych, nastąpi weryfikacja danych i
ich autouzupełnienie w formularzu. Po pozytywnej weryfikacji
reprezentanta będzie mógł on wyznaczyć koordynatorów, którzy będą
odpowiedzialni za parametryzację aplikacji i procesów biznesowych
specyficznych dla danej organizacji, takich jak struktura organizacyjna
czy wybór modułów w ramach aplikacji. Finalną wersję parametrów
ostatecznie potwierdza reprezentant.

Analogiczne zagraniczne systemy oferowane dla administracji
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Digital Marketplace (UK), Apps.gov (USA), Estonia
`````````````````````````````````````````````````

Digital Marketplace (Wielka Brytania) oraz Apps.gov (Stany Zjednoczone)
to dwie bazy usług chmurowych, oferowane administracji publicznej (na
brytyjskim Digital Marketplace oferowane są także inne usługi). Są to
katalogi usług, które są hostowane w komercyjnych chmurach
obliczeniowych. Są to te same usługi, które oferowane są przez dostawców
oprogramowania odbiorcom komercyjnym (rynek konsumencki oraz biznesowy).

Zarówno zakup, płatności jak i podpisanie umowy na świadczenie usług
odbywa się poza tymi serwisami. Integracja technologiczna z systemami
administracji nie jest warunkiem koniecznym, aby usługa znalazła się na
Digital Marketplace albo Apps.gov. Konieczne jest natomiast przejście
pewnego procesu certyfikacyjnego – w przypadku brytyjskiego Digital
Marketplace jest to proces swoisty dla usług cyfrowych, w przypadku
Apps.gov to standardowe umowy ramowe, które podpisuje amerykańska
administracja z dostawcami usług (nie tylko IT).

W Estonii - kraju uchodzącym za światowego pioniera rozwiązań z zakresu
e-administracji nie funkcjonuje obecnie podobne rozwiązanie. Kwestia
wprowadzenia podobnych rozwiązań była podnoszona w kraju już od 2012
roku, jednak ze względu na skalę rynku wewnętrznego (populacja Estonii
to 1.3 mln osób, 200 urzędów) sądzono, że efekt skali będzie właściwie
niewidoczny. Większość aplikacji wykorzystywanych w administracji była
więc kupowana bezpośrednio od usługodawców, którzy dodatkowo
rozbudowywali swoje produkty o dodatkowe funkcjonalności. Niektóre z
estońskich urzędów korzystają jednak z usług w chmurze (pierwszym
wdrożeniem tego typu była narodowa strona turystyczna funkcjonująca na
chmurze amazona od 2009 roku). Prawo estońskie nie stawia przeszkód w
korzystaniu z oprogramowania/ chmur, których dane są przesyłane i
przetwarzane poza granicami terytorium estońskiego. Ostatecznie władze
estońskie podjęły decyzję o stworzeniu rządowej chmury. 26 sierpnia 2016
roku firma Ericsson wygrała przetarg, który będzie realizowała w
partnerstwie z innymi firmami i konsorcjum publiczno-prywatnym. W
rozwiązaniu zaplanowane jest m.in wykorzystanie rozwiązań operujących na
blockchainach.

W porównaniu do Digital Marketplace i Apps.gov (szczegóły planowanych
rozwiązań estońskich nie są znane) zaletą proponowanego rozwiązania jest
wzajemna integracja aplikacji, które mogą się znaleźć na
aplikacje.gov.pl. Wadą może być mniejsza liczba dostępnych aplikacji
(przynajmniej początkowo).

Metodologia
~~~~~~~~~~~

Jednym z podstawowych założeń projektu EZD RP B+R, w ramach którego
powstaje platforma Aplikacje.gov.pl jest recykling opracowanych już
rozwiązań programistycznych (software reuse, code reuse) i
wykorzystywanie rozwiązań open source opracowanych przez
deweloperów, inne firmy i instytucje z całego świata. Portal
Aplikacje.gov.pl stworzony będzie na bazie technologii open source i
udostępniany na licencji open source, dzięki czemu będzie mógł być
rozwijany w ramach społeczności informatyków.

Wprowadzenie metodologii recyklingu wiedzy deweloperów i reużywania
narzędzi informatycznych wynika bezpośrednio również z wymagań
narzuconych w ustawie o ponownym wykorzystywaniu informacji sektora
publicznego przygotowanej przez Ministerstwo Cyfryzacji, która
implementuje dyrektywę Parlamentu Europejskiego i Rady 2013/37/UE z dnia
26 czerwca 2013 r. Wprowadzeniu takich rozwiązań przyświeca również
konieczność realizacji zobowiązań Polski wobec Komisji Europejskiej -
maksymalnego wykorzystania produktów, które powstały w ramach
poprzedniej edycji Programu Operacyjnego Innowacyjna Gospodarka oś 7.

Ze względu na przyjęte założenie o recyklingu rozwiązań w pracach nad
opracowaniem technologicznych marketplace w pierwszej kolejności
przeprowadzona została analiza istniejących już na rynku rozwiązań,
które można wykorzystać w stworzeniu marketplace dla polskiej
administracji publicznej.

Wymagane funkcje marketplace’u
------------------------------

Marketplace powinien mieć minimalną liczbę funkcji. Dodatkowe funkcje
będą instalowane przez konkretne aplikacje dostępne wewnątrz
marketplace. Takie założenie wynika z faktu, że systemy o mniejszej
liczbie funkcji są z reguły mniejsze, łatwiejsze do utrzymania i
łatwiejsze do modyfikacji.

Marketplace powinien:

-  przechowywać informacje o podmiotach (instytucjach, instancjach
   systemu)
-  przechowywać informację o wszystkich dostępnych aplikacjach + o ich
   możliwych konfiguracjach + o ich konfiguracji globalnej
-  posiadać interfejs do zarządzania podmiotami
-  posiadać interfejs (shell, WWW, ...?) do zarządzania możliwymi do
   zainstalowania aplikacjami

Marketplace powinien dla każdego podmiotu:

-  przechowywać informację o zainstalowanych aplikacjach + o ich
   lokalnej konfiguracji
-  serwować interfejs WWW do zarządzania zainstalowanymi aplikacjami
-  mając dane miejsce wykonania (VM, JVM, ...?) uruchomić w nim
   zainstalowane aplikacje
-  (?) mając dane miejsce wykonania zmienić uruchomione w nim aplikacje
   (uruchomić lub zakończyć)
-  (?) zrestartować miejsce wykonania - zakończyć wszystkie działające i
   uruchomić wszystkie zainstalowane aplikacje

Marketplace powinien dla każdej działającej albo uruchamianej aplikacji

-  przechowywać informację gdzie się ona znajduje
-  (wynika z powyższego) wskazać gdzie znajdują się aplikacje od których
   jest zależna (wstrzykiwanie zależności)

Zgromadzenie dostępnych narzędzi
--------------------------------

Aby zgromadzić narzędzia, które zostaną poddane analizie, sprawdzono z
jakich narzędzi korzystają istniejące serwisy:

-  Digital Marketplace (UK) - zgodnie ze swoją nazwą: punkt wymiany
   pomiędzy sprzedającymi i kupującymi. Nie posiada funkcji do
   zarządzania instancją.
-  Apps.gov (USA) - podobnie jak wyżej: spis dostawców rozwiązań
   chmurowych.

Szukano też narzędzi poza ww systemami.

Analiza dostępnych narzędzi
---------------------------

+----------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------+
| Nazwa                                                                                              | Czy ma wymagane funkcje?                                                                                                                                                                                            | Licencja kodu                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Konkluzja                                                           |
+====================================================================================================+=====================================================================================================================================================================================================================+==============================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================+=====================================================================+
| `carbon-appmgt <https://github.com/wso2/carbon-appmgt>`__                                          | Nie.                                                                                                                                                                                                                | open source                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Nie nadaje się do użycia bez innych komponentów.                    |
|                                                                                                    |                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
|                                                                                                    | Nie umie uruchamiać aplikacji - podaje się mu URLe do działających aplikacji. Jest bardzo rozbudowanym reverse-proxy.                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
+----------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------+
| `Kong <https://github.com/Mashape/kong>`__                                                         | Nie.                                                                                                                                                                                                                | open source                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Nie nadaje się do użycia bez innych komponentów.                    |
|                                                                                                    |                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
|                                                                                                    | To jest “API gateway” - nie zajmuje się uruchamianiem serwisów.                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
+----------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------+
| `YaaS <https://market.yaas.io/beta>`__                                                             | Tak.                                                                                                                                                                                                                | Kod niedostępny, pytanie czy istnieje w ogóle możliwość uruchomienia YaaS’a (i SAP Hybris, na którym się on opiera) na własnych serwerach. Oferta taka zdaje się nie być dostępna publicznie i wydaje się wątpliwe, aby można było taką możliwość osiągnąć w rozsądnej cenie, biorąc pod uwagę skalę wykorzystania rozwiązań firmy SAP na świecie. Wg strony `https://www.yaas.io/products/saphybris-commerce-as-a-service.html <https://www.yaas.io/products/saphybris-commerce-as-a-service.html>`__ usługi SAP Hybris są oferowane na platformie YaaS „as a service”.     | Brak możliwości stworzenia własnego sklepu.                         |
|                                                                                                    |                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
|                                                                                                    | Platforma, na którą wrzuca się paczki WAR (program dla JVM) - to znaczy, że aplikacje muszą być pisane w językach kompilowanych do kodu maszynowego JVM.                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
+----------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------+
| `OpenStack <https://www.openstack.org/software/>`__ (komponenty wymienione jako “core” + Heat)     | Nie wszystkie.                                                                                                                                                                                                      | open source                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | OpenStack/Murano można wykorzystać.                                 |
|                                                                                                    |                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
|                                                                                                    | System robiący chmurę. Bez Murano nie ma funkcji do zarządzania użytkownikami i ich zainstalowanymi aplikacjami.                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
+----------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+                                                                     |
| `Murano <https://wiki.openstack.org/wiki/Murano/ApplicationCatalog>`__                             | Tak.                                                                                                                                                                                                                | open source                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |                                                                     |
|                                                                                                    |                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
+----------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------+
| `Docker Engine (swarm mode) <https://docs.docker.com/engine/swarm/>`__                             | Nie wszystkie.                                                                                                                                                                                                      | open source                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Nie nadaje się do użycia bez elementu zarządzającego podmiotami.    |
|                                                                                                    |                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
|                                                                                                    | System do uruchamiania aplikacji w kontenerach.                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Można użyć jako „zarządcy per podmiot” - każdy klient ma swojego.   |
|                                                                                                    |                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
|                                                                                                    | Nie umie zarządzać podmiotami, zbiorem zainstalowanych aplikacji per podmiot. Wstrzykiwanie zależności (service discovery) jest realizowane przez DNS. Tylko do rozwiązań bez wspólnej pamięci (np mikroserwisy).   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
+----------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------+
| `Kubernetes <https://kubernetes.io/>`__                                                            | Nie wszystkie.                                                                                                                                                                                                      | open source                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Można użyć jako „zarządcy per podmiot”.                             |
|                                                                                                    |                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
|                                                                                                    | Podobnie jak wyżej - system do uruchamiania aplikacji w kontenerach. Nie zajmuje się przechowywaniem informacji o podmiotach.                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                     |
+----------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------+

Zmapowane ryzyka i sposoby ich przeciwdziałania
-----------------------------------------------

+--------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| Rozwiązanie        | Ryzyko                                                                                                                                                                                                       | Przeciwdziałanie                                                                                                                                 |
+====================+==============================================================================================================================================================================================================+==================================================================================================================================================+
| OpenStack/Murano   | Analiza rozwiązania została opracowana na podstawie opisu produktu i dostępnej dokumentacji. Bez weryfikacji opisanych funkcji - instalacji - nie jest możliwe 100 proc. potwierdzenie opisanych funkcji.    | - przeprowadzenie instalacji (weryfikacja opisanych funkcji)                                                                                     |
|                    |                                                                                                                                                                                                              | - przygotowanie analizy jakości                                                                                                                  |
+--------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| YaaS               | YaaS działa jako Software as a Service                                                                                                                                                                       | Brak - rozwiązanie SaaS oznacza brak możliwości rozbudowywanie aplikacji przez zewnętrzne podmioty, co wyklucza zastosowanie tego rozwiązania.   |
+--------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| Kubernets          | Analiza rozwiązania została opracowana na podstawie opisu produktu i dostępnej dokumentacji. Bez weryfikacji opisanych funkcji - instalacji - nie jest możliwe 100 proc. potwierdzenie opisanych funkcji.    | - przeprowadzenie instalacji (weryfikacja opisanych funkcji)                                                                                     |
|                    |                                                                                                                                                                                                              | - przygotowanie analizy jakości                                                                                                                  |
+--------------------+                                                                                                                                                                                                              |                                                                                                                                                  |
| Docker Engine      |                                                                                                                                                                                                              |                                                                                                                                                  |
+--------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| carbon-appmgt      | Ze względu na to, że rozwiązania te mają mało wymaganych funkcji marketplace, nakład pracy włożonej w ich dobudowanie może być niewspółmierny do korzyści związanych z ich użyciem                           | Należy przeprowadzić weryfikację trudności ich integracji z wybranym systemem                                                                    |
+--------------------+                                                                                                                                                                                                              |                                                                                                                                                  |
| Kong               |                                                                                                                                                                                                              |                                                                                                                                                  |
+--------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
