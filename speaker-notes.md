# Angular 2 - Live Coding

## Überblick

* Projekt: Anlegen, Aufbau & Bootstrapping
* Komponenten: Data-Binding & Events
* Services & Dependency Injection
* Kommunikation mit dem Backend
* Routing
* Pipes

## Speaker Notes

* Projekt anlegen
  * ```ng new angular2-live-coding```
  * ```ng serve```
  * [http://localhost:4200](http://localhost:4200)
* index.html & main.ts
  * imports
  * bootstrap-Aufruf
* app.component.ts
  * Klasse
  * Annotation
  * Template
  * Styling
* Komponente anlegen
  * Feature Ordner: ```mkdir trainings```
  * Dateien anlegen
    * ```ng generate component trainings/training-list```
    * ```ng generate component trainings/training-details```
* Data-Binding & Events
  * Demo-Daten in AppComponent (Model & Daten kopieren)
  * Input-Binding der Liste an TrainingListComponent
  * Event-Binding für *click* in TrainingDetailsComponent
  * Output-Bidning *trainingSelected* in AppComponent
  * Input-Binding ausgewähltes Training an TrainingDetailsComponent
  * class-Binding *selected* in TrainingListComponent
* Service & DI
  * Datenbeschaffung in Service auslagern
  * ```ng generate service trainings/training```
  * Demo-Daten in Service verschieben
  * *getAll* Methode mit Observable
  * Provider an *bootstrap* in main.ts
  * Service in AppComponent konsumieren
* Backend Kommunikation
  * Demo-Backend mit Node
  * CORS -> ng serve mit Proxy (*--proxy http://localhost:3000*)
  * *HTTP_PROVIDER* an bootstrap-Aufruf registrieren
  * TrainingService#getAll umstellen
    * http.get mit Mappings (deserialize, dateStringToDate)
* Routing
  * Routen für Listen-Ansicht, Detail-Ansicht und default (*RouterConfig*)
  * Provider registrieren (*provideRouter*)
  * Router-Outlet einbinden
  * Service in TrainingListComponent
  * Routen-Parameter und Service in TrainingDetailsComponent (*ActivatedRoute*)
  * TrainingService#getById
    * http.get mit Mappings (deserialize, dateStringToDate)
  * Links in Liste
  * Link zurück zur Liste
* Pipes
  * nextRun formatiert ausgeben
    * DatePipe in TrainingDetailsComponent
  * takePlaceSoon Pipes
    * ```mkdir utils```
    * ```ng generate pipe utils/take-place-soon```
    * Implementierung kopieren
    * Für class-Binding in TrainingDetailsComponent verwenden 


