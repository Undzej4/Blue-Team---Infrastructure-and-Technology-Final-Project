# Blue-Team---Infrastructure-and-Technology-Final-Project
Infrastructure and Technology

International Infrastructure and Technology – Final Project


Celem projektu było przeanalizowanie działania infrastruktury IT oraz identyfikacja potencjalnych zagrożeń związanych z usługami sieciowymi, logami systemowymi i podejrzaną aktywnością. W ramach zadań skoncentrowano się na diagnostyce usług, pracy z narzędziami administracyjnymi Windows oraz analizie logów przy użyciu Splunka.

Projekt odzwierciedla realne procesy wykorzystywane na stanowiskach SOC Analyst, Blue Team oraz w działach IT Infrastructure / Network Operations.

Task 1 – Połączenie z serwerem pocztowym

W pierwszym etapie projektu wykonano próbę połączenia z serwerem pocztowym działającym na porcie 110 (POP3).

Podczas testu:

-zidentyfikowano brak narzędzia Telnet w systemie Windows 10,

-co uniemożliwiało wykonanie podstawowej diagnostyki usługi.

Problem został rozwiązany poprzez instalację narzędzia przy użyciu DISM:

dism /online /Enable-Feature /FeatureName:TelnetClient


Po aktywacji narzędzia wykonano ponowne testy komunikacji oraz potwierdzono poprawność działania serwera.

Ten etap odzwierciedla realne scenariusze diagnozowania usług sieciowych w środowiskach korporacyjnych.

Task 2 – Search for Suspicious Activity

Druga część projektu obejmowała analizę podejrzanej aktywności w systemie oraz identyfikację anomalii wskazujących na potencjalne zagrożenia.

Zakres pracy obejmował:

-przegląd logów systemowych,

-analizę zdarzeń związanych z nieudanymi logowaniami,

-analizę ruchu sieciowego,

-identyfikację nietypowej aktywności.

Do wyszukania potencjalnie szkodliwych operacji wykorzystano Splunka.
Użyto między innymi zapytania:

index=* "download"


Zapytanie to umożliwiło identyfikację zdarzeń związanych z pobieraniem plików — mogących wskazywać na:

-pobranie złośliwego oprogramowania,

-nieautoryzowane transfery,

-aktywność użytkowników naruszającą zasady bezpieczeństwa.

Wynik analizy:

-zidentyfikowano zdarzenia związane z downloadami do dalszej weryfikacji,

-na podstawie danych z logów określono potencjalne ryzyka bezpieczeństwa,

-przygotowano rekomendacje dotyczące reakcji oraz dalszego monitorowania.

Efekt końcowy projektu

Projekt pozwolił na praktyczne przećwiczenie:

-diagnozowania usług sieciowych w Windows,

-obsługi narzędzi administracyjnych (DISM, Telnet),

-analizy logów i wyszukiwania zdarzeń w Splunku,

-rozpoznawania podejrzanych wzorców zachowań,

-podstawowych technik wykrywania incydentów.
