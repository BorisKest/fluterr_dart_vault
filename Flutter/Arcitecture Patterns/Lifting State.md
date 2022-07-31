Lifting State up and Callbacks.

In flutter we have a concept of lifting the state up, which implies, we take that state of widgets and lift it up as far as the parent widget that enclose all those widgets.

For exemple: 
we have a button, if we press it the text will change. To do that in button on tap we call function whit setState and some parametr that will be chengd. In Text we use this parametr to show, and when state chenge Text will be updated. 