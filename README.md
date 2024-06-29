# CMake & Conan Basic Tutorial

## with conan

on macOS:

library:
```bash
conan export-pkg . -f -s build_type=Release -s compiler=apple-clang -s compiler.version=15.0 -s compiler.libcxx=libc++
```

app:
```bash
cmake .. -G Ninja -DCMAKE_BUILD_TYPE=Release
```