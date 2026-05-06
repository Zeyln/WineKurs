# WineKurs
Instruksjoner for installering av Wine på macOS.
### Hva du må ha på forhånd:
- <a href="https://brew.sh" target="_blank">Homebrew</a>
> naviger til "Install Homebrew", kopier kommandoen, lim inn i terminal.
> <br>
> **_Advarsel_**, bruk av terminal shells annet enn Bash kan gjøre at enkelte
> <br>
> kommandoer ikke virker. Om du er usikker, kjør ```bash``` før noe annet.
# Steg 1, klargjøring
Verifiser at homebrew er installert og oppdatert:
```bash
brew --version
```
# Steg 2, Installer wine:
```bash
brew install --cask wine-stable
# Fungerer ikke? si ifra.
```
når det er ferdig installert, test med:
```bash
winecfg
```
Du vil mest sannsynlig bli møtt med "Apple could not verify "Wine Stable" is not free of malware [...]" <br>
-> Trykk "**Done**"<br>
**IKKE** trykk "Move to trash"

### Fiks: Åpne macOS Settings –> Privacy & Security –> Scroll ned til Security –> Trykk "Open Anyways" –> Vidu åpnes, Trykk "Open Anyways" –> Skriv Passord.
Kjør ```winecfg``` igjen. <br>
Burde fungere, hvis ikke, si ifra.

# Bruk og Applikasjoner
Velg en windows applikasjon som dere vil bruke med Wine.<br>
Jeg har kurert en liste med applikasjoner som fungerer fint, men
gjerne finn noe annet, om dere så ønsker.<br>
Unngå applikasjoner med mye backend, som login, webservere, eller kernel nivå funksjoner som anticheats.
#### Applikasjoner (klikk for å laste ned):
- <a href="https://github.com/notepad-plus-plus/notepad-plus-plus/releases/download/v8.9.4/npp.8.9.4.Installer.x64.exe" target="_blank">Notepad++</a> Fungerer perfekt
- <a href="https://github.com/ip7z/7zip/releases/download/26.01/7z2601-x64.exe" target="_blank">7-Zip</a> Fungerer perfekt
- <a href="https://github.com/paintdotnet/release/releases/download/v5.1.12/paint.net.5.1.12.install.anycpu.web.zip" target="_blank">Paint.net</a> ustabil, **Krever:**
```bash
brew install winetricks
```
Pakk ut filer om det trengs før du går videre... <br>
Vær oppmerksom på hvor du har lastet ned / pakket ut filen.

#### Kjør applikasjonen:
Åpne terminal, skriv:
```bash

wine Downloads/7z2601-x64.exe
# dette er et eksempel, bytt ut filnavn og path,
# MÅ være en .exe fil, om det er .zip må du pakke den ut først
```
Om alt går som planlagt, vil applikasjonen starte, og du kan bruke den slik du vil.

Og om ting begynner å brenne:
```
wineserver -k
```
