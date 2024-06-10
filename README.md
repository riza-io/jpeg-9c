# wasi-sdk

Copy over config.* from WASI SDK to the repository

```sh
export WASI_SDK_PATH="/Users/kyle/riza/x-wasi-libs/wasi-sdk-22.0"
export CFLAGS="-D__EMSCRIPTEN__=1 -DNPY_NO_SIGNAL -fno-exceptions"
export AR="${WASI_SDK_PATH}/bin/ar"
export CC="${WASI_SDK_PATH}/bin/clang --sysroot=${WASI_SDK_PATH}/share/wasi-sysroot"
export LD="${WASI_SDK_PATH}/bin/wasm-ld"
export RANLIB="${WASI_SDK_PATH}/bin/ranlib"
```

```
./configure --host wasm32-wasi --prefix=/Users/kyle/riza/x-wasi-libs/local
```

## wasi-wheels

```sh
export WASI_SDK_PATH="/Users/kyle/riza/wasi-wheels/build/wasi-sdk"
export CFLAGS="-D__EMSCRIPTEN__=1 -DNPY_NO_SIGNAL -fno-exceptions -fPIC"
export AR="${WASI_SDK_PATH}/bin/ar"
export CC="${WASI_SDK_PATH}/bin/clang --sysroot=${WASI_SDK_PATH}/share/wasi-sysroot"
export LD="${WASI_SDK_PATH}/bin/wasm-ld"
export RANLIB="${WASI_SDK_PATH}/bin/ranlib"
```

```
export LDSHARED=${CC}
```

```
./configure --host wasm32-wasi --prefix=/Users/kyle/riza/wasi-wheels/build/local
```


