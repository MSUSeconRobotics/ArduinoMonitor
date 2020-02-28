# ArduinoMonitor
This is a set of two libraries to view Arduino data. They rely on JsonSerialStream to output data through USB.

### Things to note
* Dependent on JsonSerialStream as a sibling library
```
  | JsonSerialStream
    + JsonSerialStream.h
  | ArduinoMonitor
    + Logger.h
    + SensorMonitor.h
```

### To include:

<details>
<summary> Into a git repository </summary>

1) Create a `src` folder in your sketch's directory.
2) In terminal, navigate to the `src` directory.
3) Run the command `git submodule add https://github.com/MSUSeconRobotics/ArduinoMonitor.git`
4) In your sketch, add `#include "src/ArduinoMonitor/Logger.h"` and add `#include "src/ArduinoMonitor/SensorMonitor.h"`

This results in a structure that looks like this:
+ ExampleSketch
  + ExampleSketch.ino
  + src
    + JsonSerialStream
      + JsonSerialStream.h
      + JsonSerialStream.cpp

Please note that to clone your git repo now, you **must** either:
* Run `git clone --recurse-submodules <RepoURL>`

    or

1) Run `git clone <RepoURL>`
2) Run `git submodule init`
3) Run `git submodule update`

_Details can be found here: https://git-scm.com/book/en/v2/Git-Tools-Submodules_

</details>

<details>
<summary> Outside a git repository </summary>

The recommended way of including this library into your sketch is to:
1) Creating a `src` folder in your sketch's directory
2) Cloning this repository into that `src` folder. 
3) In your sketch, add `#include "src/ArduinoMonitor/Logger.h"` and add `#include "src/ArduinoMonitor/SensorMonitor.h"`

This results in a structure that looks like this:
+ ExampleSketch
  + ExampleSketch.ino
  + src
    + JsonSerialStream
      + JsonSerialStream.h
      + JsonSerialStream.cpp

You may also clone this repository into your Arduino libaries directory. Or you can extract the `.h` and `.cpp` and put them into your sketch directory.
These are not advised as they can get cluttered, are hard to update, or may result in "works on my machine" as a result of different installed libraires.
</details>