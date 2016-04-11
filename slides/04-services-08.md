### Servicios
#### Factory IV

html
```html
<ul ng-controller="ListCtrl">
    <li ng-repeat="task in tasks track by $index">
    {{task}}
    <span class="glyphicon glyphicon-remove" ng-click="removeTask(task)"></span>
    </li>
</ul>
```
controller()
```javascript
$scope.removeTask = function(task) {
    taskList.removeTask(task);
}
```
factory()
```javascript
removeTask: function(task) {
    var index = tasks.indexOf(task);

    if (index > -1) {
        tasks.splice(index, 1);
    }
}
```
