# Linux

## Arch Linux

Możemy użyć paczki z repozytorium AUR `android-sdk` do zainstalowania generalnej struktury SDK, a następnie paczek:
- `android-platform` (AUR)
- `android-sdk-build-tools` (AUR)
- `android-tools` (nie-AUR)

Przydatna może być też paczka `android-udev` (nie-AUR).

Tak zainstalowane SDK (`ANDROID_HOME`) możemy znaleźć w katalogu `/opt/android-sdk`.

## Byle który Linux

Pobieramy `tools_rWERSJA-linux.zip` z https://developer.android.com/studio/index.html, rozpakowujemy do wybranego folderu, a następnie uruchamiamy z konsoli polecenie `ścieżkatamgdzierozpakowaliśmy/tools/android` i instalujemy co najmniej po jednym _platform tools_, _build tools_ i _SDK platform_.

Tak zainstalowane SDK (`ANDROID_HOME`) możemy znaleźć tam, gdzie je rozpakowaliśmy.