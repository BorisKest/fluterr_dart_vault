Asynchronus programming in dart is  characterized by the Future nad Stream classes.

Stream is a siquens of asincronus data. 
We use them when we need to resive many events from server.

Future represents a computation that dosen't complete immediately. Where a normal function returns the result, an asynchronous function returnd a Future, which will eventually contain the result. The future will tell you when the result is ready.

Reciving stream events 
Streams can be created in many ways, which is a topic for another aricle, but they can all be used in the dame way: the asynchronous for loop(commonly just called await for) iterates over the events of a stream like the for loop iterates over an iterable.

How to create a Stream

If you wnat to create a stream where you can put a value, you start with a StreamController.

StreamController<double> controller = StreamController<double>();

This will construct a contriller that you can then use to manipulate the stream the controller manages. The controllers stream can be accessed through the stream property 

Stream stream = controller.stream;

How to use a stream

The next thing to do is to be able to get the values from a stream. This is commonly referred to as subscribting or listning to a stream. When you subscribe to a stream you will only get the values that are  emitted(put onto the stream) after the subscriprion. You subscribe to the stream by calling the listen function and supplying it with a Function to call back to when there's a new value available, commonly referred to as a callback function, or just a callback.

Stream.listen((value) {
print('$value');
});
