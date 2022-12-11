# #! hacks

Scripts are executed as `#!interpreter [arg]` and most often as
`#!/usr/bin/env interpreter`. As older versions of env did not support
additional arguments, clever hacks were needed instead. This repo catalogs
single file workarounds.

Modern env users should always favor `-S` / `--split-string=` instead of any of
these hacks. Eg:

```sh
#!/usr/bin/env -S deno --quiet run --allow-read --allow-write --check=typescript
```

## Script Guidelines
- Must be self-contained as a single file executable
- Must support any number of interpreter arguments inline
- Must use `#!/usr/bin/env interpreter`
- Must echo the first argument with zero exit status
- Must exit with nonzero status when no argument
- Must work as any filename but should be named after the target program
- Should be a paradigm (terse, clear, extensible)
- May (or may not) work when the script in its entirety is interpreted
  by interpreter. For example, `python demo/python $RANDOM` and
  `demo/python $RANDOM` are equivalent but only `demo/make $RANDOM`, not
  `make -f demo/make $RANDOM` works

## License (Public Domain)
All code is public domain and may be used without limitation.