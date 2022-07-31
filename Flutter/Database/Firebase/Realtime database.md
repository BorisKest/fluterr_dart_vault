Set up firebase real time database

Plugins: 

firebase_core
firebase_database

Initialize the RTDB packege
-
import 'package:firebase_database/firebase_database.dart';
to use Database instance :
FirebaseDatabase database = FirebaseDatabase.instance;

Structure Database

Data structured in a JSON tree

Avoid nesting data
In fierbase realtime database allows nesting data up to 32 levels deep. However when you fetch data at a location in database, you also retrieve all of its child nodes. In addition, when you grant someone read or write access at a node in db, you also grant them access to all data under that node.