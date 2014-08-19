Logbook is a compact logging framework for ArmA. It supports static (compile time) and runtime logging with 5 log levels.

##Quick start

Download `logbook.h` and `logbook_common.h` files and put them into a directory from where you can include them.

Open an `sqf` file you want log in and include Logbook with `#include "logbook.h"` at beginning of the file. The file needs to be preprocessed and compiled for Logbook to work.

Here's an example:

```c++
#define LOGGING_LEVEL_INFO
#define LOGGING_TO_RPT
#define LOGGING_TO_CHAT
#include "logbook.h"
```

Here we are using static logging, meaning that the preprocessor will either remove or keep the log statements in the code based on the log level. We defined `INFO` level, so all of the `DEBUG` and `TRACE` log statements will be removed, and all of the `ERROR`, `WARN` and `INFO` log statements will be left in the code. Next we define, that we want to log into the RPT file and to the player chat.

Now if you want to log an error you can write this in the file:

`ERROR("some.script","There was an error!");`

or just log some debug information:

`DEBUG("some.script.more","Debug information here.");`

For more details check the [wiki](https://github.com/kami-/logbook/wiki).
