```bash
$ sudo apt install -y libboost-dev
$ sudo apt install -y libgnutls28-dev openssl libtiff-dev pybind11-dev
$ sudo apt install -y qt6-base-dev
$ sudo apt install -y meson cmake libevent-dev
$ sudo apt install -y python3-yaml python3-ply
$ sudo apt install -y libglib2.0-dev libgstreamer-plugins-base1.0-dev

$ meson setup build --buildtype=release -Dpipelines=rpi/vc4,rpi/pisp -Dipas=rpi/vc4,rpi/pisp -Dv4l2=true -Dgstreamer=disabled -Dtest=true -Dlc-compliance=disabled -Dcam=enabled -Dqcam=enabled -Ddocumentation=disabled -Dpycamera=disabled
```

```bash
The Meson build system
Version: 1.5.1
Source dir: /home/vanperdung/workspace/libcamera
Build dir: /home/vanperdung/workspace/libcamera/build
Build type: native build
DEPRECATION: Option 'v4l2' value 'true' is replaced by 'enabled'
Project name: libcamera
Project version: 0.5.1
C compiler for the host machine: cc (gcc 12.2.0 "cc (Debian 12.2.0-14+deb12u1) 12.2.0")
C linker for the host machine: cc ld.bfd 2.40
C++ compiler for the host machine: c++ (gcc 12.2.0 "c++ (Debian 12.2.0-14+deb12u1) 12.2.0")
C++ linker for the host machine: c++ ld.bfd 2.40
Host machine cpu family: aarch64
Host machine cpu: aarch64
Header "fcntl.h" has symbol "F_ADD_SEALS" : YES
Header "unistd.h" has symbol "issetugid" : NO
Header "locale.h" has symbol "locale_t" : YES
Header "sys/mman.h" has symbol "memfd_create" : YES
Header "stdlib.h" has symbol "secure_getenv" : YES
Compiler for C supports arguments -Wno-c99-designator: NO
Found pkg-config: YES (/usr/bin/pkg-config) 1.8.1
Found CMake: /usr/bin/cmake (3.25.1)
Run-time dependency lttng-ust found: NO (tried pkgconfig and cmake)
Message: Enabling vimc pipeline handler for tests
Message: Enabling virtual pipeline handler for tests
Program ./parser.py found: YES (/home/vanperdung/workspace/libcamera/utils/codegen/ipc/./parser.py)
Program ./generate.py found: YES (/home/vanperdung/workspace/libcamera/utils/codegen/ipc/./generate.py)
Program ./extract-docs.py found: YES (/home/vanperdung/workspace/libcamera/utils/codegen/ipc/./extract-docs.py)
Configuring version.h using configuration
Program openssl found: YES (/usr/bin/openssl)
Run-time dependency libyuv found: NO (tried pkgconfig and cmake)
Has header "libyuv.h" : NO

Executing subproject libyuv method cmake

libyuv| Found CMake: /usr/bin/cmake (3.25.1)

| Configuring the build directory with CMake version 3.25.1
| Running CMake with: -G Ninja -DCMAKE_INSTALL_PREFIX=/usr/local -DCMAKE_POSITION_INDEPENDENT_CODE=ON -DCMAKE_BUILD_TYPE=Release
|   - build directory:          /home/vanperdung/workspace/libcamera/build/subprojects/libyuv/__CMake_build
|   - source directory:         /home/vanperdung/workspace/libcamera/subprojects/libyuv
|   - toolchain file:           /home/vanperdung/workspace/libcamera/build/subprojects/libyuv/__CMake_build/CMakeMesonToolchainFile.cmake
|   - preload file:             /usr/lib/python3/dist-packages/mesonbuild/cmake/data/preload.cmake
|   - trace args:               --trace-expand --trace-format=json-v1 --no-warn-unused-cli --trace-redirect=cmake_trace.txt
|   - disabled policy warnings: [CMP0025, CMP0047, CMP0056, CMP0060, CMP0065, CMP0066, CMP0067, CMP0082, CMP0089, CMP0102]

| Running with expanded trace output on.
| Not searching for unused variables given on the command line.
| Trace will be written to cmake_trace.txt
| -- The C compiler identification is GNU 12.2.0
| -- The CXX compiler identification is GNU 12.2.0
| -- Detecting C compiler ABI info
| -- Detecting C compiler ABI info - done
| -- Check for working C compiler: /usr/bin/cc - skipped
| -- Detecting C compile features
| -- Detecting C compile features - done
| -- Detecting CXX compiler ABI info
| -- Detecting CXX compiler ABI info - done
| -- Check for working CXX compiler: /usr/bin/c++ - skipped
| -- Detecting CXX compile features
| -- Detecting CXX compile features - done
| CMake Deprecation Warning at CMakeLists.txt:6 (CMAKE_MINIMUM_REQUIRED):
| Compatibility with CMake < 2.8.12 will be removed from a future version of
| CMake.

| Update the VERSION argument <min> value or use a ...<max> suffix to tell
| CMake that the project does not need compatibility with older versions.


| -- Found JPEG: /usr/lib/aarch64-linux-gnu/libjpeg.so (found version "62")
| CMake Warning (dev) at CMakeLists.txt:45 (if):
| Policy CMP0064 is not set: Support new TEST if() operator.  Run "cmake
| --help-policy CMP0064" for policy details.  Use the cmake_policy command to
| set the policy and suppress this warning.

| TEST will be interpreted as an operator when the policy is set to NEW.
| Since the policy is not set the OLD behavior will be used.
| This warning is for project developers.  Use -Wno-dev to suppress it.

| Building ver.: 0.0.1770
| Packaging for: amd-64
| -- Configuring done
| -- Generating done
| -- Build files have been written to: /home/vanperdung/workspace/libcamera/build/subprojects/libyuv/__CMake_build

libyuv| CMake configuration: SUCCEEDED
libyuv| CMake project YUV  has 3 build targets.
libyuv| Generated Meson AST: /home/vanperdung/workspace/libcamera/build/subprojects/libyuv/meson.build
libyuv| DEPRECATION: Option 'v4l2' value 'true' is replaced by 'enabled'
libyuv| Project name: YUV
libyuv| Project version: undefined
libyuv| C++ compiler for the host machine: c++ (gcc 12.2.0 "c++ (Debian 12.2.0-14+deb12u1) 12.2.0")
libyuv| C++ linker for the host machine: c++ ld.bfd 2.40
libyuv| Build targets in project: 23
libyuv| Subproject libyuv finished.

Library atomic found: YES
Run-time dependency threads found: YES
Run-time dependency libdw found: YES 0.188
Run-time dependency libunwind found: YES 1.6.2
Header "execinfo.h" has symbol "backtrace" : YES
Library rt found: YES
Run-time dependency libpisp found: NO (tried pkgconfig and cmake)
Looking for a fallback subproject for the dependency libpisp

Executing subproject libpisp

libpisp| DEPRECATION: Option 'v4l2' value 'true' is replaced by 'enabled'
libpisp| Project name: libpisp
libpisp| Project version: 1.2.0
libpisp| C compiler for the host machine: cc (gcc 12.2.0 "cc (Debian 12.2.0-14+deb12u1) 12.2.0")
libpisp| C linker for the host machine: cc ld.bfd 2.40
libpisp| C++ compiler for the host machine: c++ (gcc 12.2.0 "c++ (Debian 12.2.0-14+deb12u1) 12.2.0")
libpisp| C++ linker for the host machine: c++ ld.bfd 2.40
libpisp| Configuring pisp_build_config.h using configuration
libpisp| Run-time dependency nlohmann_json found: NO (tried pkgconfig and cmake)
libpisp| Looking for a fallback subproject for the dependency nlohmann_json

Executing subproject libpisp:nlohmann_json

nlohmann_json| DEPRECATION: Option 'v4l2' value 'true' is replaced by 'enabled'
nlohmann_json| Project name: nlohmann_json
nlohmann_json| Project version: 3.11.2
nlohmann_json| C++ compiler for the host machine: c++ (gcc 12.2.0 "c++ (Debian 12.2.0-14+deb12u1) 12.2.0")
nlohmann_json| C++ linker for the host machine: c++ ld.bfd 2.40
nlohmann_json| Build targets in project: 32
nlohmann_json| Subproject nlohmann_json finished.

libpisp| Dependency nlohmann_json from subproject subprojects/nlohmann_json-3.11.2 found: YES 3.11.2
libpisp| Dependency threads found: YES unknown (cached)
libpisp| Library dl found: YES
libpisp| Run-time dependency Boost (found: log, log_setup, thread | missing: system) found: NO (tried system)
libpisp| Build targets in project: 34
libpisp| Subproject libpisp finished.

Dependency libpisp from subproject subprojects/libpisp found: YES 1.2.0
Run-time dependency libjpeg found: YES 2.1.5
Checking for function "dlopen" : YES
Run-time dependency libudev found: YES 252
Run-time dependency yaml-0.1 found: NO (tried pkgconfig and cmake)
Looking for a fallback subproject for the dependency yaml-0.1

Executing subproject libyaml

libyaml| DEPRECATION: Option 'v4l2' value 'true' is replaced by 'enabled'
libyaml| Project name: yaml-0.1
libyaml| Project version: 0.2.5
libyaml| C compiler for the host machine: cc (gcc 12.2.0 "cc (Debian 12.2.0-14+deb12u1) 12.2.0")
libyaml| C linker for the host machine: cc ld.bfd 2.40
libyaml| Configuring config.h using configuration
libyaml| Build targets in project: 39
libyaml| Subproject libyaml finished.

Dependency yaml-0.1 from subproject subprojects/yaml-0.2.5 found: YES 0.2.5
Run-time dependency gnutls found: YES 3.7.9
Dependency libexif skipped: feature android disabled
Dependency libjpeg skipped: feature android disabled
Message: Enabling vimc IPA to support tests
Run-time dependency libevent_pthreads found: YES 2.1.12-stable
Run-time dependency libtiff-4 found: YES 4.5.0
Dependency gtest skipped: feature lc-compliance disabled
Run-time dependency libdrm found: YES 2.4.123
Dependency libjpeg found: YES 2.1.5 (cached)
sdl2-config found: NO
Run-time dependency sdl2 found: NO (tried pkgconfig, config-tool and cmake)
Run-time dependency qt6 (modules: Core, Gui, OpenGL, OpenGLWidgets, Widgets) found: YES 6.4.2 (pkg-config)
Detecting Qt6 tools
Run-time dependency qt6 (modules: Core) found: YES 6.4.2 (pkg-config)
Program /usr/lib/qt6/bin/moc found: NO
Program /usr/lib/qt6/libexec/moc found: YES 6.4.2 6.4.2 (/usr/lib/qt6/libexec/moc)
Program /usr/lib/qt6/bin/uic found: NO
Program /usr/lib/qt6/libexec/uic found: YES 6.4.2 6.4.2 (/usr/lib/qt6/libexec/uic)
Program /usr/lib/qt6/bin/rcc found: NO
Program /usr/lib/qt6/libexec/rcc found: YES 6.4.2 6.4.2 (/usr/lib/qt6/libexec/rcc)
Program /usr/lib/qt6/bin/lrelease found: NO
Program /usr/lib/qt6/libexec/lrelease found: NO
Program lrelease6 found: NO
Program lrelease-qt6 found: NO
Program lrelease found: NO
Dependency glib-2.0 skipped: feature gstreamer disabled
Dependency gstreamer-video-1.0 skipped: feature gstreamer disabled
Dependency gstreamer-allocators-1.0 skipped: feature gstreamer disabled
Dependency python3 skipped: feature pycamera disabled
Dependency pybind11 skipped: feature pycamera disabled
Configuring libcamerify using configuration
Program doxygen skipped: feature documentation disabled
Program dot skipped: feature documentation disabled
Program sphinx-build-3 sphinx-build skipped: feature documentation disabled
Configuring config.h using configuration
Program python3 (jinja2, yaml, jinja2, ply) found: YES (/usr/bin/python3) modules: jinja2, yaml, jinja2, ply
Build targets in project: 144

libcamera 0.5.1

  Versions
    Sources                  : 0.5.1+100-e53bdf1f

  Paths
    LIBCAMERA_DATA_DIR       : "/usr/local/share/libcamera"
    LIBCAMERA_SYSCONF_DIR    : "/usr/local/etc/libcamera"
    IPA_PROXY_DIR            : "/usr/local/libexec/libcamera"
    IPA_CONFIG_DIR           : "/usr/local/etc/libcamera/ipa:/usr/local/share/libcamera/ipa"
    IPA_MODULE_DIR           : "/usr/local/lib/aarch64-linux-gnu/libcamera/ipa"

  Configuration
    SoftISP support          : false
    IPA modules signed with  : gnutls
    Enabled pipelines        : rpi/vc4
                               rpi/pisp
                               vimc
                               virtual
    Enabled IPA modules      : rpi/vc4
                               rpi/pisp
                               vimc
    Controls files           : control_ids_core.yaml
                               control_ids_debug.yaml
                               control_ids_draft.yaml
                               control_ids_rpi.yaml
    Properties files         : property_ids_draft.yaml
                               property_ids_core.yaml
    Hotplug support          : YES
    Tracing support          : NO
    Android support          : NO
    GStreamer support        : NO
    Python bindings          : NO
    V4L2 emulation support   : YES
    cam application          : YES
    qcam application         : YES
    lc-compliance application: NO
    Unit tests               : YES

  Subprojects
    libpisp                  : YES 1 warnings
    libyaml                  : YES
    libyuv                   : YES
    nlohmann_json            : YES (from libpisp)

  User defined options
    buildtype                : release
    cam                      : enabled
    documentation            : disabled
    gstreamer                : disabled
    ipas                     : rpi/vc4,rpi/pisp
    lc-compliance            : disabled
    pipelines                : rpi/vc4,rpi/pisp
    pycamera                 : disabled
    qcam                     : enabled
    test                     : true
    v4l2                     : true

Found ninja-1.11.1 at /usr/bin/ninja
```

```
$ ninja -C build install
```

