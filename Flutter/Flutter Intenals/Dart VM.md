Dart VM is a collection of components for executing Dart code natively. Notably it includes the following: 
Runtime System 
	Object Model
	Garbage Collecion
	Snapshots 

Core libraries native methods 
Development Experience components accessible via service protocol *Debugging* *profiling* *Hot-reload*

Just-in-time and ahed-of-time compilation pipelines 
Interpreter 
ARM simulators

Dart VM is a virtual machine in a sense that it provides an execution environment for a high - level programming language, however it does not imply that Dart is always interpreted or JIT - compiled, when executing on Dart VM.

How does Dart VM run your code?

Dart VM has multiple ways to execute the code, the example:

from source or Kernel binary using JIT; 
from snapshot: 
	from AOT snapshot
	from AppJIT snapshot

However the main difference between these lies in when and how VM convrts Dart source code to executable code. The runtime environment that facilitates the execution remains the same.