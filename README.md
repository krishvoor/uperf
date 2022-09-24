# Quickstart

Please visit [uperf.org](http://www.uperf.org) for the latest information

# Pre-requisites
As of writing this documented, installed the following on Windows (Server 2019) did the trick.
1. Cygwin
2. autoconf2.7
3. automake1.16
4. gcc-g++, gcc-debuginfo, gcc-core, libgcc1, (11.3.0-1)
5. git
6. glib2.0-networking (2.54.1-1)
7. libssl-devel 1.1.1q-1
8. vim

# Compiling Uperf on Windows
```
git clone https://github.com/krishvoor/uperf
cd uperf
./configure --enable-netstat=no  --enable-sctp=no --enable-ssl=no
make -j4
```

We countered issues while compiling with SCTP enabled, 
it looks for `netinet/sctp.h` header file, which is not available in cygwin/Windows
