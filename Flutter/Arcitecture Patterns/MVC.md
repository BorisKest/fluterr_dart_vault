Model-View-Controller(MVC) - architectural pattern that separates an application into 3 main logical components: model, view, controller. Each of them is build to handle specific developmeny aspects of an application.

MVC+S - separate also the service layer.

Model - data classes that we create when we need (user.dart, product.dart, plants.dart)

View - All the UI part is in here. All Widgets, pages of Flutter Application. Can contain "view controller" but that is still considered part of the view app tier.

Controller - State managmant logic goes in here. Providers, blocs, or any other state managmant logic can be placed into this folder

+

Services - fetch data from the outside world and return it to the app.
Whatever data that comes into tour app must have to be from here. It may be connecting with REST API or any DB connection.

![[Pasted image 20220725103231.png]]
https://itnext.io/mvc-s-design-pattern-in-flutter-6eba15169413