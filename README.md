# zoo-gui

A framework to reflect state of ZooKeeper into Web UI

# Idea

The system state will be put in zookeeper. The UI has a localhost version of zookeeper tree node. Any change in zookeeper tree nodes will be updated to the local tree node via websocket. A service will take care synchronize the server and local tree nodes.

Components in UI will work base on the tree nodes in UI. E.g.:
* A `Start` button show the loading indicator if `/job/start` = true and will hide when `/job/start` = false.
* A progress bar show that it is running 50% when `/job/progressbar/show` = true and `/job/progressbar/value` = 50 
