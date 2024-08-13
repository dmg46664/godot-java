# Godot Java

(WIP) Godot bindings for Java.

## Dev information

``` bash
make
javac src/godot_java/*.java
LD_LIBRARY_PATH=/usr/lib/jvm/java-1.11.0-openjdk-amd64/lib/server \
  CLASSPATH="$(readlink -f src/godot_java)" \
  ENTRY_CLASS=DefaultInitHandler \
  HELPER_NODE_CLASS=DefaultNodeOverride \
  godot src/dummy_godot_project/project.godot
```

- `compile_flags.txt` is there so that clangd lsp can find Java headers, it's not used for actual compilation 

- Compile with `mvn package` and find your build in `./target`
