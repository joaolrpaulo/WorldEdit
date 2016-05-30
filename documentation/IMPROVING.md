# Improving World Edit

### The problem

Minecraft, more specific, the Bukkit Adapter has known limitations related to asynchronous world modification. 
If we try to run block modifications in a separate thread we will get an exception like:

> [Timer-51/WARN]: java.lang.IllegalStateException: Asynchronous block remove!

Derived from this, World Edit core runs every task using the main thread. This decision can cause complications when performing tasks with a massive number of blocks.
As for example, if we try to paste a schematic with 1 million blocks running World Edit in a server with the following specifications:

> Intel Xeon E3 1225v2 3.2 GHz+

> 4GB of RAM allocated to the server

The server will stop responding after a few seconds, possibly causing world chunk errors.

### The solution

After studying the problem, it's possible to understand we can achieve an asynchronous operation and still avoid to use a separate thread.
We can do this by scheduling the number of blocks per a unit of time.

Let's take again our example of 1 million blocks. 
If we define a static constant of **5000 blocks per each second**, we can schedule consecutive tasks and complete our task in about 3.33 minutes.

* Task #1
  * Modify 5000 blocks
  * Run now

* Task #2
  * Modify 5000 blocks
  * Run after 1 second
  
* Task #3
  * Modify 5000 blocks
  * Run after 2 seconds
  
After 200 tasks, we will complete our job. This method will give us the ability to see the progress of our operation and avoid any world/chunk
errors if the server gets shutdown. The job can be saved to the disk and sustained any time.
