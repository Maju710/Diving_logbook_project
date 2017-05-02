# Diving_logbook_project
Diving logbook project for Akademia C# .NET PG

Wykonawca: Jan Majcher

Projekt będzie polegał na stworzeniu dziennika nurkowego (Diving Logbook). Dziennik (najczęściej w formie papierowej) służy nurkom do zapisywania wszystkich odbytych nurkowań, wraz ze szczegółami takimi jak:
osiągnięta głębokość (Depth), czas nurkowania (DiveTime), widoczność (WaterVisibility), partner nurkowy (DivingPartner), certyfikacja (MyCurrentCertification), zabrany ekwipunek (string Equipment), 
zawartość tlenu w mieszance oddechowej (OxygenContent), zawartość azotu w mieszance oddechowej (NitrogenContent), zawartość helu w mieszance oddechowej (HeliumContent). 

•	Wszystkie te zmienne będą w nadrzędnej klasie abstrakcyjnej lub interfejsie (Dive), po którym dziedziczyły będą klasy odpowiadające rodzajom nurkowań np. WreckDive, ReefDive, NitroxDive, CaveDive, TechnicalDive itp.  

•	Każdy z rodzajów nurkowań będzie miał swoje dodatkowe zmienne, wprowadzane przez użytkownika jak np. CaveDepth dla CaveDive, WreckDescription dla WreckDive itp. 

•	Każde nurkowanie będzie miało metodę obliczania ciśnienia parcjalnego tlenu w podanej mieszance oddechowej, użytej w trakcie nurkowania. 

•	W przypadku nurkowania technicznego (TechnicalDive) metoda ta będzie nadpisana. Będzie podawała ciśnienie parcjalne tlenu w gazie dennym i dekompresyjnym (w nurkowaniu technicznym stosuje się kilka gazów). 

Funkcjonalności LogBooka:

•	Dodawanie kolejnych rekordów (nurkowań)  do pliku XML

•	Edycja już istniejących rekordów (nurkowań)  do pliku XML

•	Liczenie sumarycznego czasu dennego z wszystkich nurkowań z pliku XML

•	Konwerter metrów do stóp  

•	EquipmentChecklist – użytkownik wpisuje rodzaj nurkowania, program wyświetla podpowiedź co należy na nie zabrać




