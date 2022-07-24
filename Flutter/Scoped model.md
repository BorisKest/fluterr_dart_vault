Scoped model is a pakege that allow us to easli pass a data Model from a parant Widget down to its descendants. It's also rebuilds all of the children that use the model when the model is updated.

This library provides three main classes:

Model clsass - you will extend this class to create your own Models

ScopedModel widget - if you need to pass a model deep down your Widget hierarchy, you can warp your Model in a ScopedModel Widget. 

ScopedModelDescondant Widget - Use this widget to finde the appropriate ScopedModel in the widget tree.