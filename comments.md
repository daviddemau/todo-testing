ETAPE 1 PROJET OPENCLASSROOMS:

1.Regardez comment il est structuré et essayez de comprendre comment il fonctionne.
Il y a deux bugs dans le code et c'est votre mission de les trouver ! Voici quelques indices:

a) Le premier est une faute de frappe.

=> constroller.js ligne 95. (faute de frappe 'adddItem');

b) Le deuxième introduit un conflit éventuel entre deux IDs identiques.

=> store.js ligne 116. Vérifier que le newID est different de tous les ID de todos avant de mettre à jour updateData.

c)Il y a également des améliorations à faire, même s'il ne s'agit pas de bugs proprement dit. Essayez de trouver où vous pouvez optimiser des boucles et vérifiez s'il y a des fonctions qui affichent des informations dans la console de déboggage  qui ne sont pas nécessaires.

=> controller.js ligne 170 : est-il interessant de faire une loop pour loger que les éléments avec id... ont été supprimés?

=> store.js ligne 130: ne pas répéter deux boucles pour supprimer une tâche par rapport à son id.

=> template.js ligne 65 : variable 'l' inutile.

Mode de fonctionnement du projet to-do list:
MVC pattern: (Model-View-Controller)
- Model (Data Layer)- This is where the data is stored for your app. Whenever a model changes, it will notify its observers that a change has occurred using an Event Dispatcher. IN THE PROJECT: the Model will hold the list of tasks and be responsible for any actions taken upon each task object.

- View (Presentation Layer)- This part of your App has access to the DOM and is responsible for setting up Event Handlers such as: click, onmouseover, onmouseout, etc.  IN THE PROJECT: whenever a user enters in a new task through the input field, the view will use an Event Dispatcher to notify the controller, then the controller will update the model.

- The controller is the glue between the model and the view. The controller processes and responds to events set off by either the model or view. IN THE PROJECT: when the user clicks the add task button, the click is forwarded to the controller, and the controller modifies the model by adding the task to it.

- Event Dispatcher - The Event Dispatcher is an object that allows you to attach an unlimited number of functions/methods to it. When you finally call the notify method on that Event object, every method you attached to that Event will be ran.



view: tout le rendu visuel.
modèle: les données. communiquer avec la BDD si elle existe. (sinon localStorage ou autre)
controller: point d'entrée. le chef d'orchestre.
