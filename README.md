<h1>Angular</h1>

#Narzędzia Angular##

<ul>
<li>Node.js - srodowisko uruchomieniowe javascript poza przeglądarką, pozwala instalowac biblioteki, angular-CLI itp... (czesc node to -> npm)
  
>node -v; npm -v
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

>ng new "nazwa" --skip-install - nowy projekt bez pobrania node_modules

>ng g component <path>/<component_name>

>ng g module

>ng g directive, service, pipe

>npm install - instalacja modułów node do startu app i aktualizacja wersji

>ng serve - wystawienie aplikacji na porcie - domyslny lokalhost:4200

##Angular project Root tree##
<ul>
<li>e2e -testy</li>
<li>node_modules -uruchomienie aplikacji</li>
<li>src</li>
<ul>
<li>app - tutaj lądują moduly, komponenty, dyrektywy (root component -automatycznie stworzony posiada pliki styli .css ; .html oraz .ts) dodatkowo plik .ts dla calego modułu (definicja całej aplikacji)</li>
<li>models - katalog z modelami obiektów Angular (export interface nazwa_klasy)

>export interface person {
>id: number;
>name: string;}
</li>
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
  
##Biblioteki Angular##
<ul>
<li>Pomocne biblioteki - <a href="https://material.angular.io/">Angular Material</a></li>
</ul>

##Mechanizmy Angular##
<ul>
<li>Dyrektywy
<ul>
<li>*ngFor (iteracja na widoku po jakiejś np. liście)

```text
<tr *ngFor="let person of persons" class="row">
<td> {{ person.name }}</td>
```
</li>
<li>*ngIf (warunkowe ukrywanie drzewa DOM - html)

```text
<table *ngIf="people.lenght > 0; else noPersonInfo">
<ng-template #noPersonInfo>
<div class="xyz-zyx">
<p>No People</p>
</div>
</ng-template>
```
</li>
<li>[ngClass] (dodawanie warunkowe klass css)

```text
<td [ngClass]="{'row-avaiable': person.isAvaiable}">{{person.name}}</td>
row-avaiable - css class
```
</li>
</ul>

</li>

<li>Eksporty i importy modułów, komponentów! - Angular nie tworzy połączeń automatycznie, należy: 
<ul>
<li>zawsze zaimportować nowo tworzony moduł do modułu głownego</li>
<li>weksportować child komponent w nowo tworzonym module - aby był widoczny dla modułu głównego</li>
</ul>

</li>
</ul>

##Inne komendy##
<ul>
<li>Dodanie Bootstrapa do aplikacji Angular. Po pobraniu nalezy przejść do pliku angular.json i podpiąć bootstrap przy parametrze "styles": -> kolejność styli według priorytetu
 ["../node_modules/bootstrap/dist/css/bootstrap.min.css"], ...

>npm install bootstrap@"version" --save-dev (flaga służy dodaniu biblioteki bootstrap do pliku package.json )

```text
Przykładowe wykorzystanie bootstrap:
<div class="container">
  <div class="row">
    <div class="col-sm-12">
        <thead>
          <tr>
            <th>name</th>
          </tr>
        </thead>
        <tbody>
          <tr *ngFor="let person of persons" class="row">
            <td> {{ person.name }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
  <div class="row">
    <div class="col-sm-12">
      <button (click)="showSomething()" class="btn btn-primary btn-sm float-right">
        SHOW SOMETHING
      </button>
    </div>
  </div>
```
</li>
<li>next</li>
</ul>
