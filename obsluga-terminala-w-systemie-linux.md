Gdy używamy komputerów, telefonów, czasami też konsol do gier czy telewizorów, zazwyczaj mamy do czynienia z interfejsami graficznymi, w których wszystko trzeba wyklikać. Jeśli jednak zejdziemy dostatecznie głęboko w zakamarki systemu operacyjnego, bez względu na to, czy to Windows, Linux, macOS czy BSD, możemy znaleźć interfejs tekstowy, zwany potocznie konsolą lub terminalem.

Chociaż używanie terminala jest powszechnie kojarzone z ciężkimi nerdami i hakierami \(patrz: wszystkie materiały w telewizji o cyberprzestępstwach, w których występuje [pan w kominiarce i/lub bluzie z kapturem, z zielonymi literkami nałożonymi projektorem na twarz](https://stock.adobe.com/pl/search?k=hacker)\), tak naprawdę z pracą w konsoli wiąże się tworzenie stron, zarządzanie serwerami i wiele innych czynności, które po prostu prościej robi się w ten sposób.

# Zdalny dostęp do szkolnego serwera Tanaka

Wiele uniwersytetów posiada specjalny serwer, na którym konta mają wszyscy studenci. Postanowiłem pójść w ich ślad i również zorganizować taki serwer dla uczniów Staszica. Tak powstał Tanaka.

Tanaka w chwili pisania działa na systemie operacyjnym Ubuntu Server 16.04 \(wersja LTS, czyli długo otrzymująca wsparcie techniczne i aktualizacje\) opartym o jądro Linux. Do zdalnego dostępu możemy wykorzystać protokół SSH \(**S**ecure **Sh**ell\).

### Z Linuxa i macOSa

Aby połączyć się z serwerem SSH z systemu Linux \(lub innego, który posiada klienta SSH, np. macOS\) używamy w terminalu komendy  
`ssh nazwauzytkownika@staszic.space`

### Z Windowsa

Aby połączyć się z serwerem SSH z systemu Windows, możemy doinstalować sobie w sprytny sposób konsolowego klienta SSH lub użyć znanego od lat klienta graficznego PuTTY. Możemy pobrać go ze strony [http://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html](http://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) \(link bezpośredni do pobrania: [wersja 32-bit](https://the.earth.li/~sgtatham/putty/latest/w32/putty.exe), [wersja 64-bit](https://the.earth.li/~sgtatham/putty/latest/w64/putty.exe)\).

Po otwarciu programu PuTTY w pole _Host Name \(or IP address\)_ wpisujemy `staszic.space` i klikamy przycisk _Open_ lub wciskamy klawisz <kbd>Enter</kbd>. Zostaniemy zapytani o nazwę użytkownika i hasło.

## Ciekawostki

- Podczas wpisywania hasła, zarówno w programie PuTTY jak i przy użyciu komendy SSH, najprawdopodobniej nie wyświetlą się gwiazdki, kropki ani inne symbole. Jest to po prostu cecha systemów linuxowych i podobnych, hasło jest nadal wpisywane, tylko tego nie widać.
- PuTTY to zestaw narzędzi nie tylko do łączenia z serwerami SSH, ale też do obsługi kluczy kryptograficznych i łączenia przez Telnet.
- Serwer Tanaka początkowo nosił nazwę Miyano \(obie nazwy to imiona postaci z serialu anime _Tanaka-kun wa Itsumo Kedaruge_\). Nazwa została zmieniona po tym, jak serwer spadł z biurka w sali 40, a konkretnie przypadkiem oparłem się o niego ja i się zsunął.
 - Tanaka jest źródłem wielu niezapomnianych cytatów (to ten z ciemnymi włosami po prawej): ![](https://pbs.twimg.com/media/CwRTOWsWYAAKYCb.jpg:large)

# Podstawowe komendy

Po zalogowaniu trafiamy domyślnie do swojego katalogu/folderu domowego, czyli do `/home/mojanazwauzytkownika`. Żeby się o tym upewnić, możemy użyć komendy `pwd` (skrót od _**p**rint **w**orking **d**irectory_ (na obecny folder mówimy folder  roboczy)), która poda nam obecny folder.

Nie musimy się ograniczać do tylko jednego folderu. Możemy utworzyć nowy folder używając komendy `mkdir` (_**m**a**k**e **dir**ectory_), na przykład: aby utworzyć folder `muzyka`, wpisujemy `mkdir muzyka`.

Poprzednio nasz katalog domowy był pusty, więc nie było nam to potrzebne, ale zazwyczaj dobrze jest umieć wypisać wszystkie pliki znajdujące się w określonym folderze. Użyjemy do tego polecenia `ls` (_**l**i**s**t_). Możemy podać nazwę folderu, który chcemy sprawdzić, na przykład `ls muzyka` albo ls `/home`, ale jeżeli nie podamy nic, wypisana zostanie lista plików i katalogów w obecnym katalogu. Możemy również dodawać różne flagi do poleceń, na przykład `ls -l muzyka` wypisze dodatkowe szczegóły zawartości folderu `muzyka`, a `ls -a` wypisze wszystkie, również ukryte pliki z obecnego folderu.

// TODO: write, wall, mesg, rm