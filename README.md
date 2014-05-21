#Logbook

Logbook is a compact logging framework for ArmA. It supports static (compile time) and runtime logging with 5 levels.

##Quick start

Download `logbook.h` and `logbook_common.h` files and put them into a directory from where you can reference them.

Open an `sqf` file you want log in and include Logbook with `#include "logbook.h"` at beginning of the file.

Now to use static logging you just have to define the logging level and where to log. For example we want to log at `INFO` level into the RPT file and to the player's chat we add these lines before the `#include "logbook.h"` include:


So we get:

```c++
#define LOGGINT_LEVEL_INFO
#define LOGGING_TO_RPT
#define LOGGING_TO_CHAT
#include "logbook.h"

```

Now if you want to log an error you can write this in the file:

`ERROR("some.script","There was an error!");`

or just log some debug information:

`DEBUG("some.script.more","Debug information here.");`

For more details check the [wiki](https://github.com/kami-/logbook/wiki).
