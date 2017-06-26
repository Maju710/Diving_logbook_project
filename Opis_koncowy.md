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
Wewnątrz pliku XML tworzone są nodes - główny  Diving_logbook, podrzędny Dive oraz jego podrzędny Property. Kod wyposażono w test Try/Catch.<br>

<b>Load directory:</b><br>
To jest najważniejsze okno aplikacji. Właściwie na początku chciałem, żeby było jedyne, ale pomysł nieco ewoluował, bo się wkręciłem. <br>
Zestaw Textboxes i TextBlocks z różnymi właściwościami nurkowania, które chcemy dodać. Kod wyposażony w testy Int.TryParse. <br>
Dodatkowo użyłem Checkboxes to tworzenia listy ekwipunku zabranego na nurkowanie - tworzony jest z nich string. <br>
Wykorzystałem również jeden combobox pod Dive Type. <br>
Po uzupełnieniu wszystkich właściwości, całość jest zapisywana do wcześniej utworzonego pliku XML wskazanego ścieżką. <br>
Właściwości trafiają pod node "Property" pliku XML. Całe nurkowanie trafie pod node "Dive". <br>
Zgodnie z pierwotnym założeniem aplikacji (ze wstępnego opisu), tworzony jest też obiekt nurkowania. <br>
Utworzyłem kilka klas różnych typów nurkowań, dziedziczących po klasie abstrakcyjnej Dive. <br>
Rozpisanie klas nie ma jednak póki co praktycznego zastosowania - może wykorzystam je w dalszym rozwoju aplikacji. <br>
Chciałem też udowodnić, że mniej więcej wiem na czym polega pisanie, dziedziczenie klas i tworzenie ich instancji .<br>

<b>Logbook:</b><br>
Wyświetla się OpenFileDialog do znalezienia pliku XML logbooka z nurkowaniami. Jeśli zostanie wybrany, w otwierającym się oknie<br>
zawierającym Textblock, pojawi się odpowiednio wyedytowana zawartość pliku XML. Wyposażyłem okienko w poziome i pionowe Scrollbary<br> (za pomocą Scrollviewer), żeby było czytelnie. Jeśli użytkownik nie wybierze pliku XML to pojawi się MessageBox z informacją, że nie<br>
wybrano pliku. <br>
<b>Calculator:</b><br>
Calculator to okno prostego kalkulatora do konwertowania metrów do stóp, celsjuszy do fahrenheitów i na odwrót.<br>
Ponadto policzyć można ciśnienie parcjalne tlenu w mieszance oddechowej (Calculate PO2), a także dostać radę, czy przy danym ciśnieniu parcjalnym można nurkować. Wykorzystałem tu delegaty, żeby było bardziej czytelnie w kodzie. Deleguję metody klasy<br>
toolbox, która również będzie jeszcze przeze mnie rozwijana w przyszłości. Delegowane metody zostały również wyposażone w testy <br> try/catch.







