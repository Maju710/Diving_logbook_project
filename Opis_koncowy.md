# Diving_logbook_project
Diving logbook project for Akademia C# .NET PG

Tytułem wstępu, do sprawdzającego:
Nie mam wykształcenia powiązanego bezpośrednio z IT. Przypominam - mimo, że dostałem się do grupy zaawansowanej, na początku akademii c# szczytem moich umiejętności było wyprintowanie tabliczki mnożenia w Pythonie, ewentualnie jakieś proste skrypty pomocniczne do geoprocessingu. Także, żeby napisać co napisałem, musiałem naprawdę dużo czasu sam przesiedzieć (no dobra, z drobną pomocą YT, MSDN i Stack Overflow).<br><br> 

Pomysł: <b>Logbook nurkowy - dziennik nurkowań</b><br>
Użyta technologia: <b>WPF</b><br><br>

Aplikacja składa się z kilku okienek.<br>
Okienka projektowałem manualnie, tylko pisząc kod, a nie nanosząc kontrolki myszką - drag&drop. <br>
Czytałem, że w takim wypadku jest większa kontrola nad wyglądem i zgadzam się z tym.<br>
Okienka projektowałem na StackPanels - które ustawiają wierszowo (z góry na dół) kolejne elementy.<br><br>

Poniżej opis kolejnych okienek wraz z funkcjonalnościami i click eventami zawartymi w kodzie:<br>

<b>Main window:</b> <br>
cztery buttony:<br>
+ Create Log  - otwiera okno Save Directory.xaml, które umożliwia utworzenie nowego logbooka nurkowego w formacie XML<br>
+ New dive - otwiera manager dodawania nowego nurkowania do pliku XML (Load Directory.xaml)<br>
+ View log - Otwiera OpenFileDialog do wybrania ścieżki istniejącego logbooka, a następnie wyświetla logbook w kolejnym okiengu (logbook.xaml)<br>
+ Calculator - otwiera okno prostego kalkulatora nurkowego (calculator.xaml)<br>
+ grafika mojego koła naukowego na UG(ENG_LOGO.png)<br><br>

<b>Save directory:</b><br> 
Textblock, textbox do wpisania ścieżki zapisu oraz button, połączony z eventem tworzącym plik XML logbooka. <br>
Wykorzystanie technologii System.Xml. W kodzie tworzona jest  instancja klasy XmlTextWriter - obiekt xWriter w kodowaniu UTF8. <br>
Wewnątrz pliku XML tworzone są nodes - główny  Diving_logbook, podrzędny Dive z Property. Kod wyposażono w test Try/Catch.<br><br>

<b>Load directory:</b><br>
To jest najważniejsze okno aplikacji. Właściwie na początku chciałem, żeby było jedyne, ale pomysł nieco ewoluował, bo się wkręciłem. <br>


