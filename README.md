<h1>Angular</h1>

#Narzędzia Angular##

<ul>
<li>Node.js - srodowisko uruchomieniowe javascript poza przeglądarką, pozwala instalowac biblioteki, angular-CLI itp... 

>node -v; npm -v
</li>
<li>
npm
</li>
<li>
AngularCLI - zbiór polecen do budowania aplikacji Angular
</li>

>npm install -g @angular/cli
</ul>

##Architektura##
<br>
<img src="https://github.com/P3droCi7/angular_cheat_sheet/blob/d32f64205bbe27e53c2976a01fa7862e6c83bc3f/architektura.PNG" width="50%" height="50%">

##Komendy Angular##

>ng g new <nazwa> --skip-install - nowy projekt bez pobrania node_modules

>ng g component <path>/<component_name>

>ng g module

>ng g directive, service, pipe

>ng install - instalacja modułów node do startu app i aktualizacja wersji

>ng serve - wystawienie aplikacji na porcie - domyslny lokalhost:4200

##Angular project Root tree##
<ul>
<li>e2e -testy</li>
<li>node_modules -uruchomienie aplikacji</li>
<li>src</li>
<ul>
<li>app - tutaj lądują moduly, komponenty, dyrektywy (root component -automatycznie stworzony posiada pliki styli .css ; .html oraz .ts) dodatkowo plik .ts dla calego modułu (definicja całej aplikacji)</li>
<li>assets - obrazki, ikony, fonty i style globalne </li>
<li>environments - ustawienia srodowiska dla bardziej rozbudowanych aplikacji</li>
<li>favicon.ico - ikona wyswietlana w pasku</li>
<li>index.html - nie zmieniamy go, zostaje taki sam cały czas</li>
<li>  main.ts - tutaj uruchamiana jest aplikacja, przekazany moduł główny</li>
<li>    pollyfills.ts - wyrobienie wsparcia dla starszych przeglądarek</li>
<li>styles.css - style globalne dla całej aplikacji</li>
<li>test.ts - plik testów (oraz wszystkie pliki z nazwą "spec")</li>
</ul>
<li>tsconfig.app.json - plik konfiguracyjny dla całego projektu</li>
<li>angular.json - plik konfiguracyjny angular CLI</li>
<li>package.json - plik versji dependencji (^ - oznacza pobranie zawsze najnowszej wersji)</li>
<li>tsconfig.json - plik konfiguracyjny projektu</li>
</ul>
