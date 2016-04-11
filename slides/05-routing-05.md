### Enrutamiento
#### Configurar los estados

- Los estados hay que declararlos en el **método config**.

```javascript
myApp.config(function($stateProvider, $urlRouterProvider) {
  // Si no coincide ninguna URL, cargar el estado state1
  $urlRouterProvider.otherwise("/state1");
  // Declarar estados
  $stateProvider
    .state('state1', {
      url: "/state1",
      templateUrl: "partials/state1.html",
      controller: state1Controller
    })
    .state('state2', {
      url: "/state2",
      templateUrl: "partials/state2.html",
      controller: state2Controller
    })
});

.controller('state1Controller', function() {...})

.controller('state2Controller', function() {...})
```
