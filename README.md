Sugeruje wykorzystanie MobaXTerm (jeśli robimy setup przez windowsa) - MobaXTerm umie otworzyć okienka w trybie graficznym (normalnie korzystamy z konsoli, ale gdy odpalimy VSCode to otworzy nam się normalne graficzne okienko).

# Tutorial VSCode Taurus
* Logujesz się do taurusa
* CD do folderu, w którym chcesz zainstalować Visual Studio Code
* Wywołaj komendę: `wget https://az764295.vo.msecnd.net/stable/f46c4c469d6e6d8c46f268d1553c5dc4b475840f/code-stable-1536736541.tar.gz`
* Wypakuj archiwum: `tar -xf nazwa_archiwum.tar.gz`
* Wejdź do folderu, który został utworzony
* Odpal komendę: `mkdir data`
* Gratulację zainstalowałeś VSCode! :) Aby odpalić na razie musisz być w folderze w którym jest zainstalowany i wywołać komendę `./code`

# Konfiguracja VSCode:
* Gdy VSCode jest już odpalony wchodzimy w File -> Preferences -> Settings
* Szukamy trzech kropeczek w prawym górnym rogu (pod polem "Search settings")
* Klikamy w nie i wybieramy opcję "Open settings.json"
* Po ostatnim ustawieniu wpisujemy "," i klikamy enter i wklejamy poniższy tekst:
```
// Controls if quick suggestions should show up while typing
"editor.quickSuggestions": false,

// Controls if suggestions should be accepted with "Enter" - in addition to "Tab". Helps to avoid ambiguity between inserting new lines and accepting suggestions.
"editor.acceptSuggestionOnEnter": false,

// Controls the delay in ms after which quick suggestions will show up.
"editor.quickSuggestionsDelay": 10,

// Enable word based suggestions
"editor.wordBasedSuggestions": false,

// Controls if the editor should automatically close brackets after opening them
"editor.autoClosingBrackets": false,

// Controls if suggestions should automatically show up when typing trigger characters
"editor.suggestOnTriggerCharacters": false
```

* W tym momencie wyłączyliśmy IntelliSense. Również możemy wykonać tą podpowiedź ze stackoverflow: https://stackoverflow.com/questions/30269449/how-do-i-set-up-visual-studio-code-to-compile-c-code/40570882#40570882 - dzięki niej będziemy mogli odpalać kod za pomocą prawego kliku w pliku i wybraniu opcji "Run Code".

# Dodanie VSCode do PATH'a.
* Aby odpalać VSCode w dowolnym miejscu z konsoli za pomocą komendy `code` należy go dodać do patha. Przejdź do swojego katalogu domowego.
* Edytuj plik .bashrc - jak skorzystam z nano, więc odpalam komendę `nano .bashrc`.
* Przechodzimy na sam dół pliku (w nano można korzystać z klawisza PAGE DOWN).
* Dopisujemy na sam dół: `export PATH=$HOME/DROGA_DO_VSCODE/:$PATH` - Ja mam zainstalowany VSCode w następującej lokalizacji: `~/VSCode/VSCode-linux-x64/` - dlatego wpisuje `export PATH=$HOME/VSCode/VSCode-linux-x64/:$PATH`.
* Zapisujemy plik (dla nano - CTRL+X -> y -> ENTER).
* Wywołujemy komendę `source .bashrc`.
* Sprawdzamy za pomocą komendy `code` czy wszystko śmiga - powinno być OK :)
