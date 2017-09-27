# Protobuf example on BU remote server

This tutorial comes from [protocol buffers](https://developers.google.com/protocol-buffers/)

## Must-know of runnning protobuf on BU remote server

Protobuf is installed on my userspace. Similar to Apache Thrift, you need to specify enviornment variables at compile and run time.

- Protobuf binary
```bash
export PATH=/home/phao3/protobuf/bin/bin:$PATH
```

- Protobuf Package configuration file location
``` bash
export PKG_CONFIG_PATH=/home/phao3/protobuf/bin/lib/pkgconfig
```

### cpp

You need to set LD\_LIBRARY\_PATH for runtime dynamic link.
```bash
export LD_LIBRARY_PATH=/home/phao3/protobuf/bin/lib
```

### java
You need to set CLASSPATH for runtime class discovery
```bash
export CLASSPATH=/home/phao3/protobuf/protobuf-3.4.0/java/core/target/protobuf.jar
```

### python
You need to set sys.path within the code
```python
import sys
sys.path.append('/home/phao3/protobuf/protobuf-3.4.0/python')
```
