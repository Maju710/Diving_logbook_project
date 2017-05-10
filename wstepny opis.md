# Diving_logbook_project
Diving logbook project for Akademia C# .NET PG

Wykonawca: Jan Majcher

Studiuję oceanografię, a właściwie fizykę morza (specjalność) i nurkuję. Z programowaniem miałem do czynienia właściwie tylko w systemach GIS, gdzie stosuje się Pythona do pisania własnych narzędzi i skryptów pomocniczych w geoprocessingu. Mimo tego, że dostałem się do zaawansowanej, to moja wiedza o c# i ogólnie o IT jest dalej podstawowa i będzie to moja pierwsza próba z programowaniem obiektowym, więc proszę o litość. Tyle tytułem wstępu. 

Mój pomysł na aplikację to tzw. logbook nurkowy - dziennik nurkowań (występujący najczęściej w formie papierowej), służacy do archiwizacji nurkowań różnego rodzaju, wraz ze szczegółami takimi jak:
osiągnięta głębokość (Depth), 
czas nurkowania (DiveTime), 
widoczność (WaterVisibility), 
partner nurkowy (DivingPartner), 
certyfikacja (MyCurrentCertification), 
zabrany ekwipunek (Equipment), 
zawartość tlenu w mieszance oddechowej (OxygenContent), 
zawartość azotu w mieszance oddechowej (NitrogenContent), 
zawartość helu w mieszance oddechowej (HeliumContent)
i tym podobne... 

•	Wszystkie te zmienne będą w nadrzędnej klasie abstrakcyjnej lub interfejsie (Dive), po którym dziedziczyły będą klasy odpowiadające rodzajom nurkowań np. WreckDive, ReefDive, TechnicalDive.  

•	Każdy z rodzajów nurkowań będzie miał swoje dodatkowe, prywatne zmienne i metody jak np. (_{...})OxygenContentInDecoGas, WreckDescription dla WreckDive itp. 

•	Każde nurkowanie będzie miało metodę obliczania ciśnienia parcjalnego tlenu w podanej mieszance oddechowej, użytej w trakcie nurkowania. 

•	W przypadku nurkowania technicznego (TechnicalDive) metoda ta będzie nadpisana. Będzie podawała ciśnienie parcjalne tlenu w gazie dennym i dekompresyjnym (w nurkowaniu technicznym stosuje się kilka gazów). 

Inne funkcjonalności LogBooka:

•	Dodawanie kolejnych rekordów (nurkowań) do pliku XML

•	Edycja już istniejących rekordów (nurkowań)  do pliku XML

•	Klasa statyczna Toolbox zawierająca dodatkowe funkcjonalności: 

 Konwerter metrów do stóp i celsjuszy do fahrenheitów ( w razie nurkowań z tymi co przegrali wojnę z farmerami z Wietnamu ;) )   

•	EquipmentChecklist – użytkownik wpisuje rodzaj nurkowania, program wyświetla podpowiedź co należy na nie zabrać

Chciałbym to stworzyć w formie okienkowej z przyciskami w WPF-ie, ale jeszcze go nie ogarniam. Postaram się. Może dodam też jakiś podstawowy pseudo-sklep z ekwipunkiem nurkowym jak zasugerował mi Michał B. albo biuro podróży z organizacją wypraw. 





