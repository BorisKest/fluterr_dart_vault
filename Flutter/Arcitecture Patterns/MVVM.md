Model-View-ViewModel (MVVM) - architectural pattern that separerate View and Model. ViewModel is the mediator between View and Model which carry all user events and return back the result.

Benefits: 
Maintainability: The presentation layer and the logic are loosely coupled, due to this code is easily maintainable and reusable.

Testability: The ViewModel is easier to unit test than code-behind or event-driven code.

Extensibilty: This architecture gives you assurance which enables code to get extensible over the period of time.

Model - represents a single sourece of truth that carries the real-time fetch data or database-related queries.
This layer can contain buisness logic, code validation, ect. This layer interacts whit ViewModel for local data or for real-time. Data are fiven in response to ViewModel.

ViewModel - mediator between View and Model, which accept all the user events and request that to Model for data. Once the Model has data then it returns to ViewModel and then ViewModel notify that data to VIew.

ViewModel can be used by multipel views, which means a single ViewModel can provide Data to more than one View.
![[Pasted image 20220725113525.png]]

VIew - is where the user is intaractiong with Widgets that are shown on the screen. These user events request some actions which navigate to ViewModel, and the rest of VIewModel doew the job.

![[Pasted image 20220725113747.png]]
https://medium.com/flutterworld/flutter-mvvm-architecture-f8bed2521958