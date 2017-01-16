Architektura platformy aplikacje.gov.pl
=======================================

Niniejszy dokument przedstawia architekturę platformy aplikacje.gov.pl (w skład której wejdzie m.in. aplikacja EZD) od strony oprogramowania.

Kluczowym elementem platformy aplikacyjnej będzie moduł obsługujący tożsamość użytkowników. Oprócz przechowywania kont użytkowników będzie on pozwalał na uwierzytelnianie ich za pomocą wymienialnych metod (np. hasło, podpis elektroniczny, cyfrowy dowód osobisty — eDowód). Moduł ten będzie również odpowiadał za wytwarzanie danych pozwalających na uwierzytelnienie w zewnętrznym API systemu (ciastka sesyjne lub alternatywne rozwiązania jak JSON Web Tokens).

Na bazie modułu użytkowników będą tworzone aplikacje odpowiedzialne za grupy powiązanych ze sobą funkcjonalności. Aplikacje będą podzielone na moduły, korzystające po części ze wspólnego API programistycznego. Jednym z najważniejszych elementów interfejsu administracyjnego instancji aplikacje.gov.pl będzie więc komponent zarządzający dodawaniem nowych aplikacji oraz zależnościami pomiędzy nimi. Dodanie nowej aplikacji powinno być możliwe nawet dla użytkownika, który nie posiada zdolności programistycznych. Aplikacje będą we własnym zakresie kształtować polityki uprawnień określające dostęp do obiektów, którymi zarządzają.

Wybrane obiekty w ramach poszczególnych aplikacji (uznawane za istotne z punktu widzenia prawnego) będą mogły być podpisywane (w postaci zserializowanej) z wykorzystaniem bądź to osobistego podpisu elektronicznego urzędnika (jeśli aplikacja kliencka udostępni taką możliwość), bądź pieczęci elektronicznej serwera. Do opakowania podpisów oraz znaczników czasu posłużą ustandaryzowane formaty kontenerów (CAdES/XAdES). Poświadczanie utworzenia tych obiektów będzie dokonywane z wykorzystaniem Keyless Signature Infrastructure — dzięki tej technologii będzie można udowodnić, że pismo powstało w danym momencie, a nie np. zostało antydatowane przez administratora.

Wybrane pola z wybranych modeli będą indeksowane w systemie do wyszukiwania pełnotekstowego, takim jak ElasticSearch (dokładny wybór technologii nie został jeszcze dokonany). Indeksowanie i aktualizacja indeksu będzie odbywała się automatycznie. Aplikacje pisane w ramach platformy będą miały dostęp do modułu wyszukującego aby móc udostępniać funkcje takie jak wyszukiwarka.

Komunikacja z zewnętrznymi serwisami (ePUAP, Envelo itp.) będzie następować za pomocą wydzielonych usług, do których dostęp będzie zapewniany przez interfejsy programistyczne.

Akcje i zdarzenia w systemie będą wysyłane do systemu logów, indeksowane i przesyłane do dziennika zdarzeń analizowanego przez specjalistów od bezpieczeństwa. Po anonimizacji będą one też uwzględniane w systemie statystyk, przeglądanym m.in. przez specjalistów od UX.

Komunikacja serwera z aplikacją kliencką (webową, smartfonową, desktopową itp.) będzie odbywać się poprzez REST API. REST API będzie też używane do udostępniania wybranych danych stanowiących informację publiczną oraz potencjalnie do komunikacji z innymi instancjami systemów EZD.

Architektura aplikacji będzie pozwalać na automatyzację instalacji instancji na maszynie wirtualnej za pomocą technologii takich jak Ansible (dokładny wybór technologii nie został jeszcze wykonany).

Wstępny diagram architektury aplikacji przedstawia poniższy rysunek.

.. image:: images/architektura-aplikacje.gov.pl.png
