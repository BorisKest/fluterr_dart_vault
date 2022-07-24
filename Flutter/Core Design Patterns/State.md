State - is information that can be read when the Widget is build and might change or modifided over a lifeTime of the app.
To change wiget we need to update the state object, it can be done whit setState() function. 

In Flutter, the state management  categorizes into two conveptual types:

Ephemeral State
This state alsow known as UI state or local state. It is s type of state which is related to the specific widget, state that contains in a single widget. This state we dont need to sheare whit other parts of our application.

AppState
Type of state that we want to share across various parts of our app and want to keep between user sessions. For exemple loging info, notification, shopping cart ect.

List of state solutions: 

Provider
Riverpod
setState
InhertiedWidget and InheritedModel
Redux
Fish-Redux
BLoC/Rx
GetIt
MobX
Flutter Comands
Binder
GetX
States Rebuilder
Triple Pattern