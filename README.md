<h1>Angular</h1>

#Narzędzia Angular##

Node.js - srodowisko uruchomieniowe javascript poza przeglądarką, pozwala instalowac biblioteki, angular-CLI itp... (node -v; npm -v)
npm
AngularCLI - zbiór polecen do budowania aplikacji Angular
    npm install -g @angular/cli

##Architektura##
<p align="center">
  <img src="src\assets\architektura.PNG" width="350" title="Angular Architecture">
</p>

##Komendy Angular##

ng g new <nazwa> --skip-install - nowy projekt bez pobrania node_modules
ng g component <path>/<component_name>
ng g module
ng g directive, service, pipe

ng install - instalacja modułów node do startu app i aktualizacja wersji
ng serve - wystawienie aplikacji na porcie - domyslny lokalhost:4200

##Angular project Root tree##
e2e - testy
node_modules - uruchomienie aplikacji
src
    app - tutaj laduja moduly, komponenty, dyrektywy 
        (root component -automatycznie stworzony
        posiada pliki styli .css ; .html oraz .ts)
        dodatkowo plik .ts dla calego modułu (definicja całej aplikacji)

    assets - obrazki, ikony, fonty i style globalne 
    environments - ustawienia srodowiska dla bardziej rozbudowanych aplikacji
    favicon.ico - ikona wyswietlana w pasku
    index.html - nie zmieniamy go, zostaje taki sam cały czas
    main.ts - tutaj uruchamiana jest aplikacja, przekazany moduł główny
    pollyfills.ts - wyrobienie wsparcia dla starszych przeglądarek
    styles.css - style globalne dla całej aplikacji
    test.ts - plik testów (oraz wszystkie pliki z nazwą "spec")

tsconfig.app.json - plik konfiguracyjny dla całego projektu
angular.json - plik konfiguracyjny angular CLI
package.json - plik versji dependencji (^ - oznacza pobranie zawsze najnowszej wersji)
tsconfig.json - plik konfiguracyjny projektu
