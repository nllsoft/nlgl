# nlgl

## nlgl_remove_from_core

Include `nlgl_remove_from_core.h` to undefine all commands and enums that are **not** part of the OpenGL core profile.

Example use :
```C++
#include <GL/glew.h>
#include "nlgl_remove_from_core.h"
...
glBegin(GL_TRIANGLES);
...
glEnd();
```

Results in compilation errors, for example :
```
error C3861: 'glBegin_is_removed': identifier not found
error C3861: 'glEnd_is_removed': identifier not found
```
