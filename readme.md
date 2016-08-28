# #! hacks

Scripts are executed as `#!interpreter [arg]` and most often as
`#!/usr/bin/env interpreter`. Additional arguments cannot be used. This
repo catalogs single file workarounds.

## Script Guidelines
- Must use `#!/bin/sh` when wrapping the interpreter, otherwise use
  `#!/usr/bin/env interpreter`
- Must be self-contained as a single file executable
- Must work as any filename but should be named after interpreter in the
  `demo` directory
- Must echo the first argument passed in
- Must support any number of interpreter arguments inline
- Should be a paradigm (terse, clear, extensible)

## License (Public Domain)
All code is public domain and may be used without limitation.